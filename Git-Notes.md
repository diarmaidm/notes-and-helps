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

#### General Notes
* https://git-scm.com
* https://git-scm.com/documentation

List global config ` git config --global -l`

Set email `git config --global user.email "diarmaidm@users.noreply.github.com"`

Stop warning message `git config --global push.default simple`

Set color git messages `git config --global color.ui auto`

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
