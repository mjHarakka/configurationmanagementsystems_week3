# Configuration Mangament Systems week3's exercises
## First Steps - Creating new Repository and pushing the changes from local machine to remote repository in github

This weeks exercises were mostly about Git version control and Github, these exercises are made with markdown

1. Create the repository on my github profile
1. mkdir cms_week3 on my home folder on my local machine
1. Run the command: "git init" within the new folder
1. Create a new file with some text with the command "echo "Hello git" > README.md", this README.md file is a markdown file that is pushed on to github eventually
1. Run the command "git add README.md"
1. Run the command "git commit -m "first commit"" to commit the staged change, aka. the readme file in this case
1. Run the command "git remote add origin https://github.com/mjHarakka/configurationmanagementsystems_week3.git " to add the github repository as the origin for this local repository.
1. Run the command "git push -u origin master" to push the change to the origina (github repository)

https://guides.github.com/features/mastering-markdown/

## Examples of different git commands

### gitlog
This shows the different commits with the accompanying hashcode for each commit made
![git log](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitlog.png)
### gitdiff hash1 hash2
This command shows the difference between 2 files/commits as can be seen on the image below. Also it's enough to only write the first 4 characters of the hashcode of a particular log, git will still udnerstand which one is which.
![git diff](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitdiff.png)
### gitblame filename 
Shows the individual contributors of each specific line on the file
![git blame](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitblame.png)
### git reset --hard
Reset's/clears the staging area of added files to the latest revision that is committed as can be seen on example.
![git reset](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitreset.png)

## Creating new salt-module

For this one I decided to create a new salt state that installs vim for example on a new server installation and also adds a vimrc file on the ~/.vimrc path that has non-default vim configuration.

I added the file "vim.sls" to the /srv/sal -folder with the following code:

vim:
  pkg:
    - installed

After testing it and seeing that the installation had gone through, I also added the following for configuring the VIM.
The configuration file is just a default one I found on github. Nothing special, you can for example specify different VIM themes on the configuration file. This is the one I used: https://gist.githubusercontent.com/simonista/8703722/raw/d08f2b4dc10452b97d3ca15386e9eed457a53c61/.vimrc

/.vimrc:
  file.managed:
    - source: salt://vimrc

Next I ran the command "sudo salt '*' state.apply vim" one more time and this is the result:

![vim salt](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/vim.png)

So atleast there was no bugs in applying the state, but after inspection I found out that the configuration file ~/.vimrc did not exist. I really scratched my head on this one, I just could not figure out why was there not a proper configuration file on my home folder.

