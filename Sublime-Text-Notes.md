[Back to README](README.md)
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

