# Notes and helps:

### Install node.js
See http://nodejs.org for various methods to install.
  1. You can install using package manager https://nodejs.org/en/download/package-manager/#debian-and-ubuntu-based-linux-distributions
  1. You can use nvm for multiple node versions https://github.com/creationix/nvm#install-script
    
### Prepare environment before creating a new node.js application
1. Install express globally ```npm install -g express```
1. Install express application generator globally ```npm install -g express-generator```
1. Install bower globally ```npm install -g bower```

### Create a new node.js express application
###### In the following steps **replace** `<work directory>` and `<application name>` with the actual names
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
