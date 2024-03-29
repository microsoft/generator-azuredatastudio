# Welcome to your Azure Data Studio Extension

## What's in the folder
* This folder contains all of the files necessary for your notebook extension.
* `package.json` - this is the manifest file in which you declare your extension and command.
The sample plugin registers a command and defines its title and command name. With this information
Azure Data Studio can show the command in the command palette. It doesn’t yet need to load the plugin.
* `src/notebook.ts` - this is the main file where you will provide the implementation of your command.
The file exports one function, `activate`, which is called the very first time your extension is
activated (in this case by executing the command). Inside the `activate` function we call `registerCommand`, which uses the `azdata.nb.showNotebookDocument` command to open your notebooks.

## Share your notebooks instantly
* Ensure that you have the [vsce](https://www.npmjs.com/package/vsce) module installed, which is an extenion manager.
* Update your extension's README to your liking.
* Run `vsce package` in your extension's base directory.
* Upload the generated VSIX file in Azure Data Studio.
* Run your command from the command palette by pressing (`Ctrl+Shift+P` or `Cmd+Shift+P` on Mac) and typing `Launch Notebooks`.

## Make changes
* You can repackage the extension after changing code in `src/notebook.ts`.
* You can reload (`Ctrl+R` or `Cmd+R` on Mac) the Azure Data Studio window after re-installing a new VSIX file.

## Explore the API
* You can open the full set of our API when you open the file:
  * SQL specific APIs: `node_modules/@types/azdata/azdata.d.ts`.
  * Other APIs: `node_modules/@types/vscode/vscode.d.ts`.