[Back to README](README.md)
### General linux and bash helps.
<hr>
#### Change terminal prompt.
Edit `.bashrc`

change prompt `PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\[\033[00m\]\[\033[01;34m\][\w]\[\033[34m\] \$ \[\033[00m\]'`

**Git aware prompt** https://gist.github.com/bjornkri/4025270
```
. ~/git-prompt.sh
export GIT_PS1_SHOWDIRTYSTATE=1
```

`PS1='${debian_chroot:+($debian_chroot)}\[\033[01;32m\]\[\033[01;34m\]\w\[\033[0;32m\]$(__git_ps1 " (%s)")\[\033[00m\]\$ '`

to make terminal prompt git aware https://github.com/jimeh/git-aware-prompt

having to press key twice to get backtick `xmodmap -e 'keycode 49 = grave asciitilde'` from http://ubuntuforums.org/showthread.php?t=1332160

<hr>
#### Change file manager in Ubuntu (to Nemo - Only use for Ubuntu):
http://www.webupd8.org/2013/10/install-nemo-with-unity-patches-and.html
(I got link from http://artfulrobot.uk/blog/whats-best-file-manager-ubuntu-gnome-1404-trusty)

Copied from link above - check link as things will change:
```
sudo add-apt-repository ppa:webupd8team/nemo
sudo apt-get update
sudo apt-get install nemo nemo-fileroller
```

To prevent Nautilus from handling the desktop icons (and use Nemo instead), use the command below:
```
gsettings set org.gnome.desktop.background show-desktop-icons false
```
Set Nemo as the default file manager (replacing Nautilus) by running the following command
```
xdg-mime default nemo.desktop inode/directory application/x-gnome-saved-search
```

<hr>
#### Format USB
* http://www.wikihow.com/Format-a-USB-Flash-Drive-in-Ubuntu
* http://askubuntu.com/questions/198065/how-to-format-a-usb-drive

<hr>
#### Make terminal do partial match previous commands on up and down arrow.
http://askubuntu.com/questions/59846/bash-history-search-partial-up-arrow

Update (or create) `~/.inputrc` with:
```
## arrow up
"\e[A":history-search-backward
## arrow down
"\e[B":history-search-forward
```

<hr>
### Errors, gotchas etc...
Investigate:
```
Failed to fetch http://dl.google.com/linux/chrome/deb/dists/stable/Release  Unable to find expected entry 'main/binary-i386/Packages' in Release file (Wrong sources.list entry or malformed file)
```

<hr>
#### Screen capture.
**Capture** part of a screen `scrot -s` - file is saved in home directory.

Lubuntu keyboard map https://help.ubuntu.com/community/Lubuntu/Keyboard

<hr>
SEARCHING in man pages (press "`h`" when viewing man page for complete help)
```
  /pattern          *  Search forward for (N-th) matching line.
  ?pattern          *  Search backward for (N-th) matching line.
  n                 *  Repeat previous search (for N-th occurrence).
  N                 *  Repeat previous search in reverse direction.
  ESC-n             *  Repeat previous search, spanning files.
  ESC-N             *  Repeat previous search, reverse dir. & spanning files.
  ESC-u                Undo (toggle) search highlighting.
  &pattern          *  Display only matching lines
```
#### Disk and storage
```
sudo lshw -C disk -class storage
sudo lshw -businfo
```
##### Check USB (in this case is /dev/sdc1)
```
sudo dosfsck -w -r -l -a -v -t /dev/sdc1
```
