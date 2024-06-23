* Install [nodejs](https://nodejs.org/en/download/package-manager/), and `nvm` is recommended.
* Install yarn
```
npm install -g yarn
```
* Install vsce
```
npm install -g vsce
vsce -h # check
```
* Install typescript
```
npm install -g typescript
tsc -h
```
* Install eslint
```
npm install --global eslint
eslint -h
```
* Install local dependencies
```
yarn install
```
* Go into the folder of this repo, e.g. `cd vscode-find-in-current-file`
* Edit `version` in package.json, e.g. increase minor version by 1.
* Edit CHANGELOG.md
* Build extension release package with `vsce package`
* Install the extension locally with `code --install-extension find-in-current-file-x.y.z.vsix --force` and validate the extension is working as expected.
* [Optional] Release the version in github with tags `git commit && git tag vx.y.z && git push && git push --tags`
* Release the extension to vscode marketplace with `vsce publish --yarn`. You will be prompted for the marketplace token. Or you can publish directly with `vsce publish --yarn -p <token>`.

Alternatively you can publish the extension via the marketplace web portal.
* Login https://marketplace.visualstudio.com/vscode
* Click 'Publish extensions' 
* Click 'New extension'/'vs code' and upload the `find-in-current-file-x.y.z.vsix` file built by vsce.
* It takes a few minutes to approve.
* Then search the extension in the marketplace by the full name with double quote, e.g. "find in current file", to confirm.
