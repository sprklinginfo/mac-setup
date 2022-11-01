
# Development tools installed for php/laravel development

- [PHP/Laravel Tools](#phplaravel-tools)
- [VS Code IDE extentions](#development-tools-installed-for-phplaravel-development)

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











