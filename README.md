# Find in Current File

A fork of great work https://github.com/shibayu36/vscode-search-in-current-file.

This is a Visual Studio Code extension that makes it easily to find all in current active editor.  It is inspired by the emacs extension helm-occur.

![Demo](images/demo.gif)

## Commands

### Find in Current File

Search only in current file displayed in the active editor.  Automatically, the currently selected text is filled into the search query, and the current file is filled into "files to include" in the Search Panel.

## Default Keyboard Shortcut

```json
{
  "key": "ctrl+alt+c",
  "mac": "cmd+alt+c",
  "command": "find-in-current-file.searchInCurrentFile",
  "when": "editorFocus || editorIsOpen"
}
```

## Build, Test and Publish

Check [RELEASE.md](RELEASE.md)

## Contribution

Issues and PRs are welcomed.
