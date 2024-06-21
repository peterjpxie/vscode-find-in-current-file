# Find in Current File

This is a Visual Studio Code extension that makes it easily to find all in current active editor.  It is inspired by the emacs extension helm-occur.

![Demo](images/demo.gif)

## Commands

### Find in Current File

Search only in current file displayed in the active editor.  Automatically, the currently selected text is filled into the search query, and the current file is filled into "files to include" in the Search Panel.

## Useful Keyboard Shortcuts Example

```json
// Shortcut for this extension
{
  "key": "ctrl+alt+c",
  "command": "find-in-current-file.searchInCurrentFile",
  "when": "editorFocus || editorIsOpen"
}
```

## How to Publish to VS Code Marketplace

Check [RELEASE.md](RELEASE.md)

## How to Run Tests

Install dependencies as per [RELEASE.md](RELEASE.md).

Open a terminal from a desktop environment as it is a VS code UI test, and run the tests as follows:

```
cd vscode-find-in-current-file
npm install -g yarn
yarn install
cd src
yarn pretest
yarn test
```

## Contribution

Mac users are much welcomed to test and raise PR.

## Credit

Forked from great work https://github.com/shibayu36/vscode-search-in-current-file
