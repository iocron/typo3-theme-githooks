# Typo3 Theme Githooks

Custom Typo3 Theme Githooks for easier Developments within Teams.

## How to install

1. Go to your Typo3 ext folder:

  ```bash
  cd typo3conf/ext/<yourThemeFolder>
  ```

2. Clone the Typo3 Theme Githooks Project to your Theme:

  ```bash
  git clone https://github.com/iocron/typo3-theme-githooks.git .githooks
  ```

3. Set the new hooks Path:

  ```bash
  git config core.hooksPath .githooks
  ```

4. Try it out:

  * 4.1 Try pulling / merging something and the .githooks should get triggered
  * 4.2 Or try/execute the post-merge script directly: `bash .githooks/post-merge`

*(Note: If any problems occur, then please check the logs in .githooks/logs)*

## Features

Current available Githooks:

  - post-merge:
    - Executes a filesync of new fileadmin files in the theme everytime a pull, merge, etc. is going on (usually it syncs from <theme>/Initialisation/Files/ to <Typo3Root>/fileadmin/<theme>/)
    - Installs https://github.com/iocron/typo3-gulp-scss and it's dependencies (then you can list some gulp commands with `gulp --tasks`)

## Feature Requests

- Empty typo3Root/typo3temp/* (except index.html)
- Auto Install of Typo3 Deployer

## Todos

 - More Hooks for different jobs (e.g. scss?!)
 - Auto-Update/Self-Update (Pull) on post-merge of .githooks?!
 - Need some feedback :)
