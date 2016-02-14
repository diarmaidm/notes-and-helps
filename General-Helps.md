# Notes and helps:

### Prepare environment before creating a new node.js application
1. Install node.js if it is not already installed. ```node -v``` will check the version.
  * Use nvm for multiple versions https://github.com/creationix/nvm#install-script
1. Install express globally ```npm install -g express```
1. Install express application generator globally ```npm install -g express-generator```
1. Install bower globally ```npm install -g bower```

### Create a new node.js express application
###### In the following steps **replace** `<work directory>` and `<application name>` with the actual names
1. Navigate to the work directory ```cd <work directory>```
1. Create the new application ```express <application name>```
1. run the 2 commands from end of previous step 
  * ```cd <application name> && npm install```
  * ```DEBUG=<application name>:* npm start```

### [Sublime Text](https://www.sublimetext.com/)

### [Markdown guide](https://guides.github.com/features/mastering-markdown/) :sparkles: :camel: :boom:

### Markdown editing and preview using Sublime Text
Follow instructions to install Package Control https://packagecontrol.io/installation#st3 
Install using Package Control https://packagecontrol.io/packages/Markdown%20Preview

In Sublime Shift+Ctrl+P -> Package Control: Install Package -> LiveReload

Guide - http://www.ryanthaut.com/guides/sublime-text-3-markdown-and-live-reload/ 

#### Add shortcut key in Sublime to preview markdown (`Alt+M`).
Add keybinding. On Sublime Menu -> Preferences -> Key Bindings - User
```
[
  { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser", "parser":"markdown"} }
]
```
