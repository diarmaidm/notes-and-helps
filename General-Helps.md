# Notes and helps:

### Install node.js
See http://nodejs.org for various methods to install.

* Binary Directly from nodejs.org - follow instructions under **Binary Directly from nodejs.org** http://stackabuse.com/how-to-install-node-js-on-ubuntu/
```
wget http://nodejs.org/dist/v4.4.2/node-v4.4.2-linux-x64.tar.gz
sudo tar -C /usr/local --strip-components 1 -xzf node-v4.4.2-linux-x64.tar.gz
```
* You can install using package manager https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions

* You can use nvm for multiple node versions https://github.com/creationix/nvm#install-script

### Prepare environment before creating a new node.js application
1. Install express globally ```npm install -g express```
1. Install express application generator globally ```npm install -g express-generator```
1. Install bower globally ```npm install -g bower```

### Create a new node.js express application
#### In the following steps **replace** `<work directory>` and `<application name>` with the actual names
1. Navigate to the work directory ```cd <work directory>```
1. Create the new application ```express <application name>```
1. ssRun the 2 commands from end of previous step
  * ```cd <application name> && npm install```
  * ```DEBUG=<application name>:* npm start```
  * In chrome navigate to http://localhost:3000/ to verify its working
  * Close tab in Chrome and Ctrl+C to stop the local server
1. Add libraries for testing as dev dependancies ```npm install --save-dev supertest mocha chai```

[This Stack Overflow question has answers with lots of helps](http://stackoverflow.com/questions/2353818/how-do-i-get-started-with-node-js)

### [Sublime Text](https://www.sublimetext.com/)
A sample user preferences/setting to override defaults:
```
{
  // The number of spaces a tab is considered equal to
  "tab_size": 2,
  // Set to true to insert spaces when tab is pressed
  "translate_tabs_to_spaces": true,
  // Set to true to removing trailing white space on save
  "trim_trailing_white_space_on_save": true,
  // Makes tabs with modified files more visible
  "highlight_modified_tabs": true,
  // Show folders in the side bar in bold
  "bold_folder_labels": true,
  // Preview file contents when clicking on a file in the side bar. Double clicking or editing the preview will open the file and assign it a tab.
  // set this to false if want to turn off...
  "preview_on_click": true
}
```
Add Jade highlighting [Package Control can be used](https://github.com/davidrios/jade-tmbundle#using-package-control-in-sublime-text-23)

### [Markdown guide](https://guides.github.com/features/mastering-markdown/) :sparkles: :camel: :boom:

### Markdown editing and preview using Sublime Text
Guide - http://www.ryanthaut.com/guides/sublime-text-3-markdown-and-live-reload/

Follow instructions to install Package Control https://packagecontrol.io/installation#st3
Install using Package Control https://packagecontrol.io/packages/Markdown%20Preview

In Sublime Shift+Ctrl+P -> Package Control: Install Package -> LiveReload
To enable LiveReload on Sublime start:
  On Sublime Menu -> `Preferences -> Package Settings -> LiveReload -> Settings - User` add the following:
```
{
  "enabled_plugins": [
    "SimpleReloadPlugin",
    "SimpleRefresh"
  ]
}
```

#### Add shortcut key in Sublime to preview markdown (`Alt+M`).
Add keybinding. On Sublime Menu -> Preferences -> Key Bindings - User
```
[
  { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} }
]
```

### IntelliJ IDEA
Preferences (or Settings)->Editor->General->Appearance

### Git helps
List global config ` git config --global -l`
Set email `git config --global user.email "diarmaidm@users.noreply.github.com"`
Stop warning message `git config --global push.default simple`
Set color git messages `git config --global color.ui auto`

### General npm and node helps

Trends
1. http://www.npmtrends.com/mocha-vs-chai-vs-jasmine
1. http://www.npmtrends.com/react-vs-angular
1. http://www.npmtrends.com/gulp-vs-grunt


### Visual Studio Code (on Linux)
1. Download from https://code.visualstudio.com/
1. Follow instructions to install/setup https://code.visualstudio.com/Docs/editor/setup
If you get the follwoing message when starting from the command line
```
bash: cannot set terminal process group (-1): Inappropriate ioctl for device
bash: no job control in this shell
```
remove the symbolic link (if you created 1) and add the following to .bashrc as per http://askubuntu.com/questions/636621/vscode-error-when-launched-from-terminal
```
function __code {
   if [ "$@x" != 'x' ]; then
      (~/path/to/Code "$@" &) &> /dev/null
   else
      (~/path/to/Code &) &> /dev/null
   fi
}
alias code='__code'
```

#### Editor Preferences

File -> Preferences -> User Settings (opens settings.json).
  These are some of the useful settings. You can copy from `Default Settings`
```
    "editor.tabSize": 2,
    "files.trimTrailingWhitespace": true,
    "files.autoSave": "onFocusChange"
```

#### Extensions

https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint

