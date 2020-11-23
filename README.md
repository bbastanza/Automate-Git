# Automate Git

> Two bash scripts to automate creating a new project folder with git initalized and to automate commiting in the Linux bash terminal.

## createGit

Creates a new git project by creating a new directory where your git projects are located. It then asks you for the directory link from Github.

## automate

Automates making git commits from any location.

## Installation

You can create a directory in called `~/bin` or you can place these files in your `/usr/local/bin` if you want all users to have access to these commands. Place these two files in that directory and cd into that directory in the terminal. Run the following commands.

```
chmod +x createGit
chmod +x automate
```

This will make them executable from the bash terminal. Run `updatedb` to update the command database.

Now you can use these commands calling there names

```
createGit
automate	
```

You must edit the file to add the path to the directory that contains your git projects. This is exactly what mine looks like

```
#!/bin/bash

ls /home/stanzu10/Dev/git
read -p "Which git directory: " FOLDER
cd /home/stanzu10/Dev/git/$FOLDER
git branch
read -p "Which branch: " BRANCH
cd /home/stanzu10/Dev/git/$FOLDER
git add .
git status
read -p "Enter commit name: " COMMIT
read -p "Description? (press enter or add description): " DESCRIPTION

git commit -m "commit $COMMIT" -m "$DESCRIPTION"  
git push origin -u $BRANCH
git status

exit
```

<a href="https://www.brianbastanza.me/" target="_blank" rel="noopener">Personal Website</a>
