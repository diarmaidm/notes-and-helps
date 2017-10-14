[Back to README](README.md)
### Git

#### New repo from a local new application
From https://help.github.com/articles/adding-a-remote/

Initialise local as a git repository `git init`

`git remote add origin https://github.com/<username>/<repo-name>.git`

verify `git remote -v`

when you `git push` you will get an error something like:
```
fatal: The current branch master has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin master
```

Execute the provided command `git push --set-upstream origin master`

It will give an error. Create new remote repository (empty)

Push the code to github.

<hr>

#### Git config
* https://git-scm.com
* https://git-scm.com/documentation

List global config ` git config --global -l`

Set email `git config --global user.email "diarmaidm@users.noreply.github.com"`

Stop warning message `git config --global push.default simple`

Set color git messages `git config --global color.ui auto`

set alias `git config --global alias.st status`

unset alias `git config --global --unset alias.st`

Cache credentials https://help.github.com/articles/caching-your-github-password-in-git/

```
git config --global credential.helper cache
# Set git to use the credential memory cache
git config --global credential.helper 'cache --timeout=7200'
# Set the cache to timeout after 2 hours (setting is in seconds)
```

<hr>

#### Fork and track a repo
https://help.github.com/articles/fork-a-repo/

<hr>

#### Configuring a remote for a fork
https://help.github.com/articles/configuring-a-remote-for-a-fork/ **Summary:**

```
git remote -v
    origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    origin  https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
```

```
git remote add upstream https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git
```

```
git remote -v
    origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
    origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
    upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
    upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```

<hr>

#### Syncing a fork:

https://help.github.com/articles/syncing-a-fork/

#### undoing changes

https://www.atlassian.com/git/tutorials/undoing-changes/git-clean

#### From github for developers training
Some commands used:
```
git --version
ls
mkdir scratch
cd scratch/
git --version
git clone https://github.com/githubteacher/developers-july-PM.git
git --version
git config
git config list
git confif ls -al
git config ls -al
git config --list
git config --global core.autocrlf input
git config --list
git config --global push.default simple
git config --list
cd developers-july-PM/
git branch
git branch --all
git checkout <BRANCH_NAME>
git branch
code <FILE_NAME>.md
git st
git status
git add <FILE_NAME>.md
git status
git commit
git status
git add <FILE_NAME>.md
git status
git commit
git status
git log
git push
git log
git status
code .
git checkout master
git branch --all
git branch --all | wc
git pull --prune
git branch --all | wc
git pull --prune
git branch --all | wc
git branch -d <BRANCH_NAME>
git branch --merged
git log
git log --oneline
git log --oneline --graph
git log --oneline --graph --decorate
git log --oneline --graph --decorate -- all
git config --global alias.lol "log --oneline --decorate --all"
git lol
git config --global alias.lol "log --oneline --decorate --graph --all"
git lol
git config --global alias.st "status"
git st
```

Create a task list use:
- [ ] TASKNAME

