[![Gitpod - Code Now](https://img.shields.io/badge/Gitpod-code%20now-blue.svg?longCache=true)](https://gitpod.io#https://github.com/theia-ide/theia-xml-extension)
[![Build Status](https://travis-ci.org/theia-ide/theia-xml-extension.svg?branch=master)](https://travis-ci.org/theia-ide/theia-xml-extension)

# Theia XML Extension

Adds XML support to Theia IDE (https://theia-ide.org).
To be installed as an extension.

## Developing and Trying out

The easiest way to get your hands on this extension is to start this repo using Gitpod.io:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io#https://github.com/theia-ide/theia-xml-extension)

For local installation:
 - clone
 - `yarn`
 - `cd browser-app`
 - `yarn start ..`

## Running the Electron example

    yarn rebuild:electron
    cd electron-app
    yarn start

## Publishing

Create a npm user and login to the npm registry, [more on npm publishing](https://docs.npmjs.com/getting-started/publishing-npm-packages).

    npm login

Publish packages with lerna to update versions properly across local packages, [more on publishing with lerna](https://github.com/lerna/lerna#publish).

    npx lerna publish

## Additional info

The jar in `xml/lsp4xml/` is produced by the [lsp4xml](https://github.com/angelozerr/lsp4xml) maven build. Unfortunately there is no easy way to consume it during the build [see angelozerr/lsp4xml#229](https://github.com/angelozerr/lsp4xml/issues/229)

To get a new lsp4xml version one need to download and extract the latest version of [vscode-xml vsix file](http://download.jboss.org/jbosstools/vscode-xml/staging/?C=M;O=D). The jar can than be found in `extension/server/` folder.
