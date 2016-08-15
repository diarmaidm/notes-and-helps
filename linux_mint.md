
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
