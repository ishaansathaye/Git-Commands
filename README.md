# Git and Git Commands

## Commands to Create Repo in Remote and Local from scratch
### Going back one directory
```zsh
cd ..
```
### Back to User Directory
```zsh
~ 
```
### Creating a Local repository
```zsh
cd Github
git init ExampleName
```
### Create a new public Github Repository
```zsh
#Or create repo with or without readme on Github
curl -u ishaansathaye https://api.github.com/user/repos -d '{"name":"NEW_REPO_NAME","private":false}'
#Enter token
```
### Add remote connection to local
```zsh
git remote add origin #clone link
```
### Pushing to cloud onto Github (upstream)
```zsh
git push --set-upstream origin master #consider using ssh instead of https
git push #after above command
```
### Creating Files (Readme file)
```zsh
touch README.md
```
### Status of Repo and **Differences in Code**
```zsh
git status
git diff #differences in code
```
### Staging and Committing
```zsh
git add . #stages all files or git add -A
git add "filename"
git status
git commit -m "message"

git reset FILE_NAME #remove files from staging area (git reset alone applies to all files)
```
---
## Branching
### Creating a Branch
```zsh
git branch #shows all the branches
git branch <BRANCH_NAME> #creates branch
git checkout <BRANCH_NAME> #switches to branch
```
## Pushing Branch to Remote
```zsh
git push -u origin <BRANCH_NAME> #associate remote and local branches (after, use git push and pull)
git branch -a #see all branches
```
## Merging a Branch
```zsh
git checkout master
git pull origin master #always pull down from master
git branch --merged #what branches have been merged so far
giet merge <BRANCH_NAME> 
git push origin master
```
## Deleting a Branch
```zsh
git branch --merged #just check if everything successfully merged
git branch -d <BRANCH_NAME> #deletes branch
git branch -a #still have branch on remote
git push origin --delete <BRANCH_NAME> #deletes remote branch
```
---
## Useful Commands
### Cloning a Remote Repo
```zsh
git clone <url> <where to clone> # . means current directory
```
### Timestamp, Log, Removing Git from Repo
```zsh
git log #gives history of changes to repository
ls -la #lists all files in repo with timestamp
rm -rf .git #removes git directory (used for removing directories)
```
### Ignore Files
```zsh
touch .gitignore 
*.pyc #putting star before extension ignores all file names swith extension
```
### Renaming Local and Remote Repository
```zsh
git mv #renames a file or directory in a repo
git remote set-url origin NEW_URL #change remote name first and then retrieve url
```
### View Info on Remote Repo
```zsh
git remote -v #information about remote branch
git branch -a #views all the branches 
```
### Practice for Pulling and Pushing
```zsh
git pull origin master
git push origin master
```