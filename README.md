# Configuration Mangament System's week3's exercises
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
![git log](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitlog.png)
This shows the different commits with the accompanying hashcode for each commit made

### gitdiff hash1 hash2
This command shows the difference between 2 files/commits as can be seen on the image below. Also it's enough to only write the first 4 characters of the hashcode of a particular log, git will still udnerstand which one is which.
![git diff](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitdiff.png)
### gitblame filename 
Shows the individual contributors of each specific line on the file
![git blame](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitblame.png)
### git reset --hard
Reset's/clears the staging area of added files to the latest revision that is committed as can be seen on example.
![git reset](https://github.com/mjHarakka/configurationmanagementsystems_week3/blob/master/images/gitreset.png)
