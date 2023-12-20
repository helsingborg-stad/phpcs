# PHP_CodeSniffer rules for Helsingborg Stad

## Installation

Run the following from the root of your project:

```bash
composer config allow-plugins.dealerdirect/phpcodesniffer-composer-installer true
composer require --dev helsingborg-stad/phpcs
```

## Available rulesets

### Hbg-WordPress
Specific ruleset for WordPress themes and plugins.

#### Example Usage
```xml
<?xml version="1.0"?>
<ruleset name="Some Wordpress Plugin">
    <file>./source/php</file>
    <file>./tests</file>
    <rule ref="Hbg-WordPress"></rule>
</ruleset>
```

## Available composer binaries
Included are 2 binaries for running phpcs and phpcbf on changed files only. The changes in the current branch are compared to supplied branch, and are meant to be used in a CI environment.

### Examples

```bash
vendor/bin/phpcs-changed origin/main
```
This example runs phpcs on all changed files in the current branch compared to origin/main.

```bash
vendor/bin/phpcbf-changed origin/main
```
This example runs phpcbf on all changed files in the current branch compared to origin/main.