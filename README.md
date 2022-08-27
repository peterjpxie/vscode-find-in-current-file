# Find in Current File

This is a Visual Studio Code extension that makes it easily to find all in current active editor.  It is inspired by the emacs extension helm-occur.

![Demo](images/demo.gif)

## Commands
### Find in Current File
Search only in current file displayed in the active editor.  Automatically, the currently selected text is filled into the search query, and the current file is filled into "files to include" in the Search Panel.

## Useful Keyboard Shortcuts Example
```json
// Shortcut ctrl+alt+f for this extension
{
  "key": "ctrl+alt+f",
  "command": "find-in-current-file.searchInCurrentFile",
  "when": "editorFocus || editorIsOpen"
}
```

## How to Pubish to VS Code Marketplace
Check [RELEASE.md](RELEASE.md)

## Contribution
Mac users are much welcomed to test and raise PR.

## Credit
Forked from great work https://github.com/shibayu36/vscode-search-in-current-file
