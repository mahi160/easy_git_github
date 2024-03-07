# easy_git_github
An easy cheat sheet on git and github for beginners

## What is git and github?
- Git is a version control system. What does that mean? It means i creates a history tree with all the changes done in the lifetime of the codebase. How it is done is amazing, the creater of Linux, Linus Torvalds wrote this software in just a month! There are other version control system too. But git is way more popular and industry standard.
- Github is a platform (or a company) which uses git to save all the code repositories in a cloud platform so it becomes easier to colaborate between team members. there are some other platforms like Gitlab, Bitbucket, Gitea etc.

## Tips Github
- Create a github account. It's pretty easy. You just need a valid email. Pro tip: use github phone app for two factor authenticate.
- To create a repo, when you are in github, click add new, and you can add a repo.
- *Private Repo*: This repo is private and only people given access can, well access them!
- *Public Repo*: Anyone in the internet can see them, clone them, copy them, fork them. But only colabs can edit the code.
- Then it will take you to a page where you have different options. If you have not local repo, ie no code in your machine, use the first chunk of codes. (4 lines)
- If you alread have a git repo in your machine, use the second chunk of codes (3 lines)

## Preparing Local Machine
### Install Git 
- *Linux*: Use default package manager to install git. Many distros come with git preinstalled
`git -v` to check if installed or not.
- *Windows*: Install gitbash from [git](https://git-scm.com/downloads)

### Adding SSH key
- To generate ssh key, type `ssh-keygen -t ed25519 -C "your_email@example.com"` in the terminal and press enter. it will prompt for location (default is good) and passphrase (if you don't want, press enter)
- To copy the key, enter the follwing code. This will copy the ssh key to clipboard. **DO NOT SHARE WITH ANYONE**
```sh
# for windows
clip < ~/.ssh/id_ed25519.pub

#for linux
cat ~/.ssh/id_ed25519.pub
```
### Add to github
- Click on the profile icon
- Go to settings
- On the sidebar, click on _ssh & pgp keys_
- Click on add ssh key
- Paste the ssh key in large box. You can add name, but it is not necessary.

### Testing the key
- Run `ssh -T git@github.com` in the termial. If it's connected, you will get `Hi Username` type message.

Now you are all set!
