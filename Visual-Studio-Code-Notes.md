[Back to README](README.md)
#### Visual Studio Code (on Linux)
1. Download from https://code.visualstudio.com/
1. Follow instructions to install/setup https://code.visualstudio.com/Docs/editor/setup

**NOTE: The following does not appear to be necessary with 1.1.0 (Installed May 2016)**
> If you get the follwoing message when starting from the command line
> ```
> bash: cannot set terminal process group (-1): Inappropriate ioctl for device
> bash: no job control in this shell
> ```
> remove the symbolic link (if you created 1) and add the following to .bashrc as per http://askubuntu.com/questions/636621/vscode-error-when-launched-from-terminal
> ```
> function __code {
>    if [ "$@x" != 'x' ]; then
>       (~/path/to/Code "$@" &) &> /dev/null
>    else
>       (~/path/to/Code &) &> /dev/null
>    fi
> }
> alias code='__code'
> ```

#### Editor Preferences

File -> Preferences -> User Settings (opens settings.json).
  These are some of the useful settings. (You can use `Default Settings` for reference).
```
{
  "editor.tabSize": 2,
  "editor.fontSize": 12,
  "files.trimTrailingWhitespace": true,
  "files.autoSave": "onFocusChange",
  "explorer.workingFiles.maxVisible": 5,
  "explorer.workingFiles.dynamicHeight": false
}
```

#### Useful keyboard shortcuts
View full list in the editor - File -> Preferences -> Keyboard Shortcuts
<br>https://code.visualstudio.com/docs/customization/keybindings **(Some do not work on ubuntu due to default keybindings)**
* "ctrl+shift+k" - Delete Line.
* "ctrl+shift+\" - Move to matching bracket
* "ctrl+shift+i" - Format the code
* "ctrl+1" - Focus on 1st editor
* "ctrl+2" - Focus on 2nd editor
* "Alt+up" or "Alt+down" - Move current line up or down

#### Extensions
https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint

