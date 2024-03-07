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

## How to Git!
- *Inialize a folder*: Go into the folder, open terminal there, run `git init`.
- *Addin your identity*: Use the below code to add. This is important because you can't commit code without it.
```sh
git config --global user.name "your name or username"
git config --global user.email "your@email.com"
# if you want user to be project vise, omit the --global, run the commands in git project.
```
- *Branch*: Every git repo has atleast one branch. generally it is called the _main_ branch. But what is branch? The main branch generally holds the base code, ie. stable code. Now if you want to add some feature, or develope on something, it is dangerous to work directly on main because many things can fail. So you create a _sandboxed_ entity ie branch where you can take the code from the main one, and develope on that. It won't affect the main branch at all. Unless of course you merge.
```sh
# create a branch
git checkout -b branch_name

# switch to another branch
git checkout branch_name
```
- *Merge*: Merging means, merging the changes in a branch to other branch. Be cautious in this, because there can be _merge conflict_. Oh is it? It's a bad thing! it means same file has been in different branch at the same time. Fixing merge conflict is hell on earth!
```sh
# to merge branchA to main
git checkout main
git merge branchA
```