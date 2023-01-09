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
#Or create directory and then initalize git
mkdir ExampleName
git init
#add file or change code
```

### Create a new public GitHub Repository

```zsh
#Or create repo with or without readme on Github
curl -u ishaansathaye https://api.github.com/user/repos -d '{"name":"NEW_REPO_NAME","private":false}'
#Enter token
```

### Add remote connection to local

```zsh
git add .
git commit -m "first commit"
git branch -M main
git remote add origin #clone link
```

### Pushing to cloud onto Github (upstream)

```zsh
git push -u origin main
git push #after above command
git push --set-upstream origin master #consider using ssh instead of https
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
#neds to be empty directory to specify directory
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
*.pyc #putting star before extension ignores all file names with extension
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

---

## Contributing

### Forking

```zsh
#fork from remote
git clone <url> <where to clone>
#make a new branch for oneself if in team
#make changes
#push it back to your repo
```

### Submitting a Pull Request

- Once changes made:
  - Compare and Pull Request button shows up on remote
  - click Create pull request

### Reviewing and Approving a Pull Request

- **Finding Pull Request**
  - click Pull requests on repo in remote
  - click pull request that has to be reviewed
  - click on files changed
- **Reviewing Pull Request**
  - add a comment on line of code (blue plus button on side)
  - click and drag to select block and then click blue plus button
  - can also suggest changes to lines
- **Starting a Review**
  - if finished, click on start a review
- **Options to Submit Review**
  - select comment to leave general feedback, but no actual approval
  - select approve to submit feedback and approve merging the changes
  - select request changes to submit feedback before pull request is merged
