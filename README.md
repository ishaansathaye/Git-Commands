# Git and Git Commands

## Creating Repo in Remote and Local from scratch
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
### Status of Repo
```zsh
git status
```
### Staging and Committing
```zsh
git add . #stages all files
git add "filename"
git status
git commit -m "message"
```
## Renaming Local and Remote Repository
```zsh
git mv #renames a file or directory in a repo

#change remote name first and then retrieve url
git remote set-url origin NEW_URL
```

