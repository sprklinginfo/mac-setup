
# Development tools installed for php/laravel development

- [PHP/Laravel Tools](#phplaravel-tools)
- [Node.js/nvm](#nodejs)
- [VS Code IDE extentions](#vs-code-ide-extentions)

## PHP/Laravel Tools

### PHP
```sh
brew install php
```
the above command install the latest PHP, to install a specific version of PHP other than the latest version you need to use the @ notation. For example : `brew install php@7.4`.
If you already have a version of PHP installed and need to switch to another version, you need to first unlink the version you’re running and link the new version. For example:
```sh
brew unlink php@8.1
brew link php@7.4
```


### composer
```sh
brew install composer
```
Add the following line to `.bash_profile` file:
```sh
export PATH="$HOME/.composer/vendor/bin:$PATH"
```

### Laravel Valet
```sh
composer global require laravel/valet
```
then config and install Valet and DnsMasq
```sh
valet install
```

### DBngin
download and install [DBngin](https://dbngin.com/)

### PHP Monitor for Valet
[phpmon](https://github.com/nicoverbruggen/phpmon) is a lightweight macOS utility app that runs on your Mac and displays the active PHP version in your status bar. It's tightly integrated with Laravel Valet.
```sh
brew tap nicoverbruggen/homebrew-cask
brew install --cask phpmon
```

### Valet Launchpad
[Valet Launchpad](https://github.com/gbuckingham89/valet-launchpad): A web based UI for browsing the projects being served by Laravel Valet, show all the projects being served by Laravel Valet, give you quick access to all the URLs it's served via (linked or parked) and will highlight if there is a match / mismatch with your current PHP version. 


### Mailhog
```sh
brew install mailhog
brew services start mailhog
```
After that we can access mailhog web interface here:
[mailhog web](http://127.0.0.1:8025/)

To stop the service:
```sh
brew services stop mailhog
```

May need to add this line in `php.ini` file:
```sh
sendmail_path = /usr/local/bin/MailHog sendmail
```

## Node.js
have to use [nvm](https://github.com/nvm-sh/nvm) to manage multiple versions as laravel 7 has 'opensslErrorStack' error if using node 17+.

first, uninstall existing node
```sh
brew uninstall --ignore-dependencies node
brew uninstall --force node
```
Install NVM using Homebrew
```sh
brew install nvm
nvm install --lts ### As of Jan, 18m 2023, the version is v18.13
nvm install 16.19
nvm use 16 ### node --version will output v16.19.0
nvm ls ### list all installed versions
nvm alias default 16.19 ### set default version of node
```

**For Apple M1, versions under Node 14 are not supported. so we need to install them via Rosetta**
How to open the terminal in Rosetta2 mode: 
 - Go to Application -> Right click on terminal app -> Get Info -> Select "Open using Rosetta" -> Restart Terminal
In Terminal, write -> arch -x86_64 zsh or arch -x86_64 zsh
then run `nvm install 14`

**Notes on July 5, 2023, use PNPM for node package management**

download and install [Pnpm](https://pnpm.io/)

## VS Code IDE extentions

Launch VS code, click the extentions icon.

- Community Material Theme by Equinusocio
  - install it and select a color theme
- Laravel Artisan by Ryan Naddy
  - Run Laravel Artisan commands within Visual Studio Code
- Laravel Blade Snippets by Winnie Lin
  - Laravel blade snippets and syntax highlight support
- Laravel Blade Spacer by Austen Cameron
  - Automatically add spaces in Laravel Blade template tags
- Laravel Extra Intellisense by amir
  - better intellisense for laravel projects.
- PHP Intelephense by Ben Mewburn
  - PHP code intelligence for Visual Studio Code
- Laravel goto view by codingyu
  - Quick jump to view
- Laravel Goto by Adrian
- Laravel Snippets by Winnie Lin
  -  Laravel snippets for Visual Studio Code (Support Laravel 5 and above)
- PHP DocBlocker by Neil Brayfield
  - A simple, dependency free PHP specific DocBlocking package
- PHPDoc Comment by Rex Shi
  - Add phpdoc @param and @return tag for selected function signatures.
Install
- PHP Namespace Resolver by Mehedi Hassan
- DotENV by mikestead
  - Support for dotenv file syntax
- Dotenv Official +Vault  by Dotenv
- Paste JSON as Code by quicktype
  - Copy JSON, paste as Go, TypeScript, C#, C++ and more.
- Tailwind CSS IntelliSense by Tailwind Labs
  - Intelligent Tailwind CSS tooling for VS Code
- Material Icon Theme by Philipp Kief
- Thunder Client by Ranga Vadhineni
  - Lightweight Rest API Client for VS Code
- Svg Preview by Simon Siefke











