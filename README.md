# Automate Git

> Two bash scripts to automate creating a new project folder with git initalized and to automate commiting in the Linux bash terminal.

## CreateGitProject

Creates a new git project by creating a new directory where your git projects are located. It then asks you for the directory link from Github.

## AutomateCommit

Automates making git commits from any location.

## Installation

You can create a directory in called `~/bin` or you can place these files in your `/usr/local/bin` if you want all users to have access to these commands. Place these two files in that directory and cd into that directory in the terminal. Run the following commands.

```
chmod +x CreateGitProject
chmod +x AutomateCommit
```

This will make them executable from the bash terminal. Run `updatedb` to update the command database.

Now you can use these commands calling there names

```
CreateGitProject
AutomateCommit
```
