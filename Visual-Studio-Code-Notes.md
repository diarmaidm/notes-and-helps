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
