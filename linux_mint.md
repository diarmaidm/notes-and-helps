
#### Using built in Software Manager
* Install `Chromium Web Browser`
* Install `Sublime Text`

#### Install git
`apt-get install git` from https://git-scm.com/download/linux


#### Add git global config
From https://gist.github.com/jesperronn/3047625#file-git-global-config-sh
* `git config --global alias.lol "log --oneline --graph --decorate"'
* `git config --global --add alias.loa 'log --pretty=format:"%C(red)%cr%C(blue) %h %C(reset)%an %Cgreen%d%x09%Cblue%s %C(yellow)(%ad)" --abbrev-commit --decorate=short --date=local''
* `git config --global user.email "diarmaidm@users.noreply.github.com"'
* `git config --global push.default simple'
* `git config --global color.ui auto'
* `git config --global user.name "diarmaidm"'

#### Change the terminal prompt.
Change the prompt that it doesnt show username@machine
```
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\u@\h\[\033[00m\] \[\033[01;34m\]\w \$\[\033[00m\]'
```
to
```
PS1='${debian_chroot:+($debian_chroot)}\[\033[01;34m\]\w \$\[\033[00m\] '` in `subl $HOME .bashrc
```

#### Downloaded and install [atom](https://atom.io/).
See [Atom_notes.md](atom_notes.md)

#### Install nodejs
Follow instructions [Node.js_notes.md](nodejs_notes.md)

At time of writing I used instructions from [Installing Node.js via package manager](https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions) and verified versions:
```
curl -sL https://deb.nodesource.com/setup_6.x | sudo -E bash -
sudo apt-get install -y nodejs
npm -v  ## Returned 3.10.3
node -v ## Returned v6.4.0

```

#### Install traceroute
`sudo apt install traceroute`

#### Partial command line match previous commands.
https://github.com/diarmaidm/Notes-and-Helps/blob/master/linux_notes.md#make-terminal-do-partial-match-previous-commands-on-up-and-down-arrow
