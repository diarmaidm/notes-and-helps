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
