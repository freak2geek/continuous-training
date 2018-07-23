# Virtual Studio Code

This document gather an opinionanted setup for [VSCode](https://en.wikipedia.org/wiki/Visual_Studio_Code). The purpose is to have a list of resources useful to improve productivity for the projects.

- [Virtual Studio Code](#virtual-studio-code)
    - [Installation](#installation)
    - [Plugins](#plugins)
        - [Editor enhancements](#editor-enhancements)
            - [Better Comments](#better-comments)
            - [Better Whitespace](#better-whitespace)
            - [Bookmarks](#bookmarks)
            - [Color Highlight](#color-highlight)
            - [Duplicate action](#duplicate-action)
            - [Import Cost](#import-cost)
            - [Indent Rainbow](#indent-rainbow)
            - [Material Icon Theme](#material-icon-theme)
            - [Open in Browser](#open-in-browser)
            - [Path Intellisense](#path-intellisense)
            - [Rainbow Brackets](#rainbow-brackets)
            - [Settings Sync](#settings-sync)
            - [Workbench](#workbench)
        - [Code Style and Snippets](#code-style-and-snippets)
            - [Console Wrapper](#console-wrapper)
            - [Document This](#document-this)
            - [HTML Snippets](#html-snippets)
            - [Markdown All in One](#markdown-all-in-one)
        - [Linters, Formatting and Syntax Highlighting](#linters-formatting-and-syntax-highlighting)
            - [DotENV](#dotenv)
            - [ESLint](#eslint)
            - [Gremlins](#gremlins)
            - [Markdownlint](#markdownlint)
            - [Prettier](#prettier)
            - [Trailing Spaces](#trailing-spaces)
        - [Git Integration](#git-integration)
            - [Git Blame](#git-blame)
            - [Git History](#git-history)
            - [gitflow](#gitflow)
            - [GitHub](#github)
            - [gitignore](#gitignore)
            - [GitLens](#gitlens)
            - [Git Commitizen](#git-commitizen)
        - [Tecnology integration](#tecnology-integration)
            - [Meteor](#meteor)
            - [NPM](#npm)
            - [NPM Intellisense](#npm-intellisense)
            - [Version Lens](#version-lens)
            - [Yarn](#yarn)
        - [Themes](#themes)
            - [One Dark Pro](#one-dark-pro)
    - [Tips & Tricks](#tips--tricks)
    - [References](#references)

## Installation

The recommended version is to get the [VSCode Insiders Edition](https://code.visualstudio.com/insiders/) as:

\+ Get you updated with new features and performance improvements

\- Get you with an unstable version that could introduce issues

## Plugins

### Editor enhancements

#### Better Comments

- Improve the code commenting colors by highlighning the alerts, informational, TODO, and more.

Check out: [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments)

#### Better Whitespace

- Improve the whitespace and tab awareness by rendering them on selection.

Check out: [Better Whitespace](https://marketplace.visualstudio.com/items?itemName=chmln.better-whitespace)

#### Bookmarks

- Manage bookmarks on the code being able to visit them using quick actions.

Check out: [Bookmarks](https://marketplace.visualstudio.com/items?itemName=alefragnani.Bookmarks)

#### Color Highlight

- Highlight the colors used on your files.

Check out: [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)

#### Duplicate action

- Ability to duplicate files and directories.

Check out: [Duplicate action](https://marketplace.visualstudio.com/items?itemName=mrmlnc.vscode-duplicate)

#### Import Cost

- Display the size of each imported module.

Check out: [Import Cost](https://marketplace.visualstudio.com/items?itemName=wix.vscode-import-cost)

#### Indent Rainbow

- Colorize the indentation in front of your text alternating four different colors on each step.

Check out: [Indent Rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow)

#### Material Icon Theme

- Replace file and folder icons to use Material Design ones.

- Support fully customization enabling you to tweak the icon associations, opacity and more.

Check out: [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)

#### Open in Browser

- Support a command to open current html files in any browser you configure.

Check out: [Open in Browser](https://marketplace.visualstudio.com/items?itemName=techer.open-in-browser)

#### Path Intellisense

- Autocomplate import paths from the file system.

- Support custom mapping, which is useful to enable intellistense for custom aliasses or resolutions.

Check out: [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)

#### Rainbow Brackets

- Add colors to any kind of brackets used on the code. This is useful to understand the different scopes created, and where these start and end.

Check out: [Rainbow Brackets](https://marketplace.visualstudio.com/items?itemName=2gua.rainbow-brackets)

#### Settings Sync

// TODO: Write the purpose and why is useful on support vscode setting sharing.

Check out: [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

#### Workbench

- Keep a list of favorite files and navigate between them with a quick action (`Alt + Q`).

Check out: [Workbench](https://marketplace.visualstudio.com/items?itemName=andrew-lis.workbench)

### Code Style and Snippets

#### Console Wrapper

Check out: [Console Wrapper](https://marketplace.visualstudio.com/items?itemName=fabiodam.vscode-console-wrapper)

#### Document This

Check out: [Document This](https://marketplace.visualstudio.com/items?itemName=joelday.docthis)

#### HTML Snippets

Check out: [HTML Snippets](https://marketplace.visualstudio.com/items?itemName=abusaidm.html-snippets)

#### Markdown All in One

Check out: [Markdown All in One](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)

### Linters, Formatting and Syntax Highlighting

#### DotENV

Check out: [DotENV](https://marketplace.visualstudio.com/items?itemName=mikestead.dotenv)

#### ESLint

Check out: [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

#### Gremlins

Check out: [Gremlins](https://marketplace.visualstudio.com/items?itemName=nhoizey.gremlins)

#### Markdownlint

Check out: [Markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

#### Prettier

Check out: [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)

#### Trailing Spaces

Check out: [Trailing Spaces](https://marketplace.visualstudio.com/items?itemName=shardulm94.trailing-spaces)

### Git Integration

#### Git Blame

Check out: [Git Blame](https://marketplace.visualstudio.com/items?itemName=waderyan.gitblame)

#### Git History

Check out: [Git History](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)

#### gitflow

Check out: [gitflow](https://marketplace.visualstudio.com/items?itemName=vector-of-bool.gitflow)

#### GitHub

Check out: [GitHub](https://marketplace.visualstudio.com/items?itemName=KnisterPeter.vscode-github)

#### gitignore

Check out: [gitignore](https://marketplace.visualstudio.com/items?itemName=codezombiech.gitignore)

#### GitLens

Check out: [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)

#### Git Commitizen

Check out: [Git Commitizen](https://marketplace.visualstudio.com/items?itemName=KnisterPeter.vscode-commitizen)

### Tecnology integration

#### Meteor

Check out: [Meteor](https://marketplace.visualstudio.com/items?itemName=vuhrmeister.vscode-meteor)

#### NPM

Check out: [NPM](https://marketplace.visualstudio.com/items?itemName=eg2.vscode-npm-script)

#### NPM Intellisense

Check out: [NPM Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)

#### Version Lens

Check out: [Version Lens](https://marketplace.visualstudio.com/items?itemName=pflannery.vscode-versionlens)

#### Yarn

Check out: [Yarn](https://marketplace.visualstudio.com/items?itemName=gamunu.vscode-yarn)

### Themes

#### One Dark Pro

Check out: [One Dark Pro](https://marketplace.visualstudio.com/items?itemName=zhuangtongfa.Material-theme)

## Tips & Tricks

## References

- Read: [VSCode Wikipedia](https://en.wikipedia.org/wiki/Visual_Studio_Code)

- Check out: [VScode site](https://code.visualstudio.com/)

- Print: [VSCode shortcuts for macOS](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
