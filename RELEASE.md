* Install [nodejs](https://nodejs.org/en/download/package-manager/) 
* Install yarn
```
curl -sL https://dl.yarnpkg.com/debian/pubkey.gpg | gpg --dearmor | sudo tee /usr/share/keyrings/yarnkey.gpg >/dev/null
echo "deb [signed-by=/usr/share/keyrings/yarnkey.gpg] https://dl.yarnpkg.com/debian stable main" | sudo tee /etc/apt/sources.list.d/yarn.list
sudo apt-get update && sudo apt-get install yarn
```
* Install vsce
```
npm install --global vsce
vsce -h # check
```
* Install typescript
```
npm install --global typescript
tsc -h
```
* Install eslint
```
npm install --global eslint
eslint -h
```
* Go into the folder of this repo, e.g. `cd vscode-find-in-current-file`
* Edit `version` in package.json, e.g. increase minor version by 1.
* Build extension release package with `vsce package`
* Install the extension locally with `code --install-extension find-in-current-file-x.y.z.vsix` and validate the extension is working as expected.
* [Optional] Release the version in github with tags `git commit && git tag vx.y.z && git push && git push --tags`
* Release the extension to vscode marketplace with `vsce publish --yarn`. You will be prompted for the marketplace token. Or you can publish directly with `vsce publish --yarn -p <token>`.

Alternatively you can publish the extension via the marketplace web portal.
* Login https://marketplace.visualstudio.com/vscode
* Click 'Publish extensions' 
* Click 'New extension'/'vs code' and upload the `find-in-current-file-x.y.z.vsix` file built by vsce.
* It takes a few minutes to approve.
* Then search the extension in the marketplace by the full name with double quote, e.g. "find in current file", to confirm.
