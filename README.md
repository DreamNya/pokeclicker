![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/DreamNya/pokeclicker/node.js.yml?label=%E9%83%A8%E7%BD%B2%E7%8A%B6%E6%80%81)
![GitHub package.json version](https://img.shields.io/github/package-json/v/DreamNya/pokeclicker?label=%E6%B8%B8%E6%88%8F%E7%89%88%E6%9C%AC)  
官方测试版游戏地址：https://dreamnya.github.io/pokeclicker/  
仅编译+汉化+制作Banner，未做其余任何改动，更新进度保持和源版本相同（使用了Action全自动更新，若自动部署失败可以在群里联系我）    
   
官方源代码仓库：https://github.com/pokeclicker/pokeclicker  


汉化文件使用了锅巴汉化
汉化发布页：https://gityx.com/g8hh/hanhuazhong/238.html  
  
QQ交流群：595329229  

个人Pokeclicker油猴脚本发布页：https://bbs.tampermonkey.net.cn/forum.php?mod=viewthread&tid=3842

[![GitHub package.json version (branch)](https://img.shields.io/github/package-json/v/pokeclicker/pokeclicker/develop?label=dev%20version)](https://github.com/pokeclicker/pokeclicker/tree/develop)<br/>
[![GitHub package.json version (branch)](https://img.shields.io/github/package-json/v/pokeclicker/pokeclicker/master?label=live%20version)](https://www.pokeclicker.com/)<br/>
[![Build Status](https://img.shields.io/travis/com/pokeclicker/pokeclicker?logo=travis)](https://travis-ci.com/pokeclicker/pokeclicker)<br/>
[![Discord](https://img.shields.io/discord/450412847017754644?color=7289DA&label=Discord&logo=discord)](https://discord.gg/a6DFe4p)

# PokéClicker
A game about catching Pokémon, defeating gym leaders, and watching numbers get bigger.

You can try out the current state at https://www.pokeclicker.com/

You can reach out on discord to discuss your ideas and how to implement them: https://discord.gg/a6DFe4p

> [!NOTE]
> PokéClicker is still in development!

# Developer instructions

## Guidelines
- Make sure the build script is a success. We won't test Pull Requests that fail the building script.
- We won't accept balance Pull Requests, unless it's from a developer or Code Contributor (Discord roles).
- Pull Requests adding new translatable content should link to a Pull Request in the [translation repo](https://github.com/pokeclicker/pokeclicker-translations) adding your new strings. See the Developer instructions on that repo for more info.
- Split Pull Requests into smaller Pull Requests when possible. It will make it easier for us to review, and easier for you if something's needs to be changed or is rejected.

## Editor/IDE setup

We have an [EditorConfig](https://editorconfig.org/) and linting configured, to help everyone write similar code. You will find our recommended plugins for VSCode below, however you should be able to find a plugin for other IDEs as well.

* [EditorConfig](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)
* [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
* [Stylelint](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)

## Building from Source

First make sure you have git and npm available as command-line utilities (so you should install Git and NodeJS if you don't have them already).

Open a command line interface in the directory that contains this README file, and use the following command to install PokéClicker's other dependencies locally:
```cmd
npm run clean
```

Then finally, run the following command in the command line interface to start a browser running PokéClicker.
```cmd
npm start
```

> [!TIP]
> Changes to the sourcecode will automatically cause the browser to refresh. <br/>
> This means you don't need to compile TypeScript yourself. Gulp will do this for you :thumbsup:


## Use Google cloud shell _(alternative)_
[![Google Cloud Shell](https://gstatic.com/cloudssh/images/open-btn.png)](https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/pokeclicker/pokeclicker&git_branch=develop&page=editor&open_in_editor=README.md)
```cmd
npm clean-install
npm start
```
Click the [Web Preview](https://cloud.google.com/shell/docs/using-web-preview) Button and select port `3001` from the displayed menu.<br/>
Cloud Shell opens the preview URL on its proxy service in a new browser window.

## Deploying a new version to Github Pages
> [!IMPORTANT]
> Before deploying, check that the game compiles and starts up without errors.

Then run the following:
```cmd
npm run website
```
This will populate the `/docs` folder.

After this command completes you can now publish this to your GitHub pages branch using:
```cmd
npm run publish
```
Which by default will push to the `master` branch
