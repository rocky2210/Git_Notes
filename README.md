# Git Commands 🦫
This repository contains basic git commands 

<h1 style="color:blue;">1. Git Basics Commands</h1>

## 1.1 Git Help
#### Take help from the Git help section for different commands and other errors.
    git help

<hr><hr>

## 1.2 Git Config
####  To set the basic configurations on Git like your name and email.
    git config

####  Sets configuration values for your user name on git.
    git config --global user.name "rocky"

####  Sets configuration values for your user email on git.
    git config --global user.email "goldmine@gmail.com"

#### To see different colors on the command line for different outputs.
    git config --global color.ui true

####  To create a local git repository for us in our store folder. This will help to manage the git commands for that particular repository.
    git init

####  To see what’s changed since the last commit. It shows all the files that have been added and modified and are ready to be committed and files that are untracked.
    git status
<hr><hr>

## 1.3 Adding and Committing Files
####  To add a file Readme.txt to the staging area to track its changes.
    git add Readme.txt

####  To commit our changes (taking a snapshot) and provide a message to remember for future reference.
    git commit -m "Created a Readme.txt"

####  To check the history of commits for our reference.
    git log

#### To add a specific list of files to the staging area.
    git add

#### To add all files of the current directory to the staging area.
    git add --all

#### To add all text files of the current directory to the staging area.
    git add *.txt

#### To add all text files of a particular directory (docs) to the staging area.
    git add docs/*.txt

#### To add all files in a particular directory (docs) to the staging area.
    git add docs/

#### To add text files of the entire project to the staging area.
    git add "*.txt"

#### To figure out what changes you made since the last commit.
    git diff

<hr><hr>

## 1.4 Undoing Changes
#### To undo the staging of the file that was added in the staging area.
    git reset HEAD license

#### To blow away all changes since the last commit of the file.
    git checkout --license

#### To add any of our tracked files to the staging area and commit them by providing a message to remember.
    git commit -a -m "Readme.md"

#### To undo the last commit and bring the file to the staging area.
    git reset --soft HEAD^

#### To undo the last commit and remove the file from the staging area as well (In case we went horribly wrong).
    git reset --hard HEAD^

#### To undo the last 2 commits and all changes.
    git reset --hard HEAD^^

<hr><hr>

## 1.5 Working with Remotes
#### These commands make a bookmark which signifies that this particular remote refers to this URL. This remote will be used to pull any content from the directory and push our local content to the global server.
    git remote add origin https://github.com/something.git

#### To add new remotes to our local repository for a particular git address.
    git remote add <address>

#### To remove a remote from our local repository.
    git remove rm

#### To push all the contents of our local repository that belong to the master branch to the server (Global repository).
    git push -u origin master

#### To clone or make a local copy of the global repository in your system (git clone command downloads the repository and creates a remote named origin which can be checked by the command – git remote -v).
    git clone https://github.com/something.git

<hr><hr>

## 1.6 Branching
#### To create a new branch named Testing.
    git branch Testing

#### To see all the branches present and current branches that we are working on.
    git branch

#### To switch to branch Testing from the master branch.
    git checkout Testing

#### To merge the Testing branch with the master branch.
    git merge Testing

#### To delete the Testing branch.
    git branch -d Testing

#### To create a new branch admin and set it as the current branch.
    git checkout -b admin

#### To look at all the remote branches.
    git branch -r

#### To forcefully delete a branch without making commits.
    git branch -D Testing

<hr><hr>

## 1.7 Tags
#### To see the list of available tags.
    git tag

#### To set the current tag to v0.0.1.
    git checkout v0.0.1

#### To create a new tag.
    git tag -a v0.0.3 -m "version 0.0.3"

#### To push the tags to the remote repository.
    git push --tags

<hr><hr>

## 1.8 Fetching and Stashing
#### To fetch down any changes from the global repository to the current repository.
    git fetch

#### To move staged files to the stash area which is present in the staging area.
    git stash

#### To get back the files that are present in the stash area.
    git stash pop

#### To clear the stash folder.
    git stash clear

<hr><hr>

## 1.9 Rebasing
#### Three tasks are performed by git rebase
##### 1. Move all changes to master which are not in origin/master to a temporary area.
##### 2. Run all origin master commits.
##### 3. Run all commits in the temporary area on top of our master one at a time, so it avoids merge commits.
    git rebase

<hr><hr>

## 1.10 Miscellaneous
#### Used to show the current version of Git.
    git --version

<hr><hr>

# 2. Advanced Git Commands

## 2.1 Cherry-Pick
#### To apply the changes from a specific commit.
    git cherry-pick <commit_hash>

## 2.2 Reflog
#### To see the history of all references in the repository.
    git reflog

## 2.3 Blame
#### To show what revision and author last modified each line of a file.
    git blame <file>

## 2.4 Archive
#### To create an archive of files from a named tree.
    git archive --format=tar <commit_hash> | tar -x -C /path/to/extract

## 2.5 Submodule
#### To add a submodule to the repository.
    git submodule add <repository_url> <path>

#### To initialize, fetch, and checkout the submodule.
    git submodule update --init --recursive

## 2.6 Clean
#### To remove untracked files from the working directory.
    git clean -f

## 2.7 Shortlog
#### To summarize the commit history.
    git shortlog

## 2.8 Show
#### To show various types of objects.
    git show <object>

## 2.9 Tag
#### To sign a tag with GPG.
    git tag -s <tag_name> -m "message"

## 2.10 Worktree
#### To manage multiple working trees.
    git worktree add <path> <branch>

#### To prune working trees.
    git worktree prune

# 3. Additional Commands

## 3.1 Revert
#### To create a new commit that undoes the changes from a previous commit.
    git revert <commit_hash>

## 3.2 Log with Graph
#### To view the commit history as a graph.
    git log --graph --oneline --all

## 3.3 Branch Rename
#### To rename a branch.
    git branch -m <old_name> <new_name>

## 3.4 Pull
#### To fetch and merge changes from the remote repository to the current branch.
    git pull

## 3.5 Rebase Interactive
#### To interactively rebase the current branch.
    git rebase -i <base_commit>

## 3.6 Squash Commits
#### To combine multiple commits into one.
    git rebase -i HEAD~<number_of_commits>

## 3.7 Tag Listing
#### To list all tags in the repository.
    git tag -l

## 3.8 Show Branch
#### To show branches and their commits.
    git show-branch

## 3.9 Apply Patch
#### To apply a patch file to the repository.
    git apply <patch_file>

## 3.10 Amend Commit
#### To modify the last commit.
    git commit --amend

# 4. Conclusion 😁
#### This cheat sheet covers basic, advanced, and additional Git commands to help manage your Git repositories efficiently.
