# Setting up and working with Git and Github

# Connecting local repos with Github
In order to connect repos on Git with corresponding repos on Github, make sure the repos 
have the same name...not sure if this is a requirement, but it makes life a lot easier

To initialize version control in a Git repository
`git init [folder_name]`

### Copy the files .bash_profile, git-completion.bash and .gitconfig into the Git home directory and 
modify the .gitconfig file to adjust the directory info for Notepad++ 

The shortcut (alias) for notepad++ is set to notep, so if you want to open a file in
notepad++ type:
`notep readme.txt`

### To set a new home directory, type:
`setx HOME "C:\Users\Daniel\"`

### To add an alias (eg change directory to project directory) change .bash_profile and set:
`alias projects="cd C:/Users/Daniel/Dropbox/projects"`

o create a new repository on the command line and to have it connected to the 
respective repo on Github
`echo "# Git" >> README.md`

```
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/danielbraas/Git.git
git push -u origin master
```

To push an existing repository from the command line to the corresponding repo on
Github
```
git remote add origin https://github.com/danielbraas/Git.git
git push -u origin master
```

To check what URL is used for a remote
`git remote -v`

To change a set remote URL for a repo 
`git remote set-url origin https://github.com/danielbraas/Git.git`

To stage files
`git add . [or specify what file should be staged]`

To commit
`git commit -m "Message"`

To push files from Git to Github
`git push`

# R configuration

### Setup R libraries

- make sure .Rprofile file exists in home directory otherwise create file with `file.edit('~/.Rprofile')`
- add .libPaths('C:/R_lib') # R_lib is the library target folder
- have config file saved (e.g. as `config.json`) with information about file structure etc. If not present
this file can be created with `file.edit('~/config.json')`
- the file can easily be populated from a list using the jsonlite package
