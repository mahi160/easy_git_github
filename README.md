# easy_git_github
An easy cheat sheet on git and github for beginners

## What is git and github?
- Git is a version control system. What does that mean? It means i creates a history tree with all the changes done in the lifetime of the codebase. How it is done is amazing, the creater of Linux, Linus Torvalds wrote this software in just a month! There are other version control system too. But git is way more popular and industry standard.
- Github is a platform (or a company) which uses git to save all the code repositories in a cloud platform so it becomes easier to colaborate between team members. there are some other platforms like Gitlab, Bitbucket, Gitea etc.

## Github
- Create a github account. It's pretty easy. You just need a valid email. Pro tip: use github phone app for two factor authenticate.
- To create a repo, when you are in github, click add new, and you can add a repo.
- *Private Repo*: This repo is private and only people given access can, well access them!
- *Public Repo*: Anyone in the internet can see them, clone them, copy them, fork them. But only colabs can edit the code.

## Preparing Local Machine
### Install Git (main guide)[ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIIm7I2DDT8T2weZ4Lv56StCVSAsP6Z0pjLgkhhuVpdco mahi@workstation]
- *Linux*: Use default package manager to install git. Many distros come with git preinstalled
`git -v` to check if installed or not.
- *Windows*: Install gitbash from (git)[https://git-scm.com/downloads]

### Adding SSH key (guide)[https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent]
- To generate ssh key, type `ssh-keygen -t ed25519 -C "your_email@example.com"` in the terminal and press enter. it will prompt for location (default is good) and passphrase (if you don't want, press enter)
- To copy the key, enter the follwing code
```sh
# for windows
clip < ~/.ssh/id_ed25519.pub
#for linux
cat ~/.ssh/id_ed25519.pub
```