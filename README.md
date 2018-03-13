Clone from Caffeinated Modules
===================

# Jasahub Modules
[![Latest Version](https://img.shields.io/github/release/faisalrizal/modules.svg?style=flat-square)](https://github.com/faisalrizal/modules/releases)
[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](LICENSE)
[![Total Downloads](https://img.shields.io/packagist/dt/faisalrizal/modules.svg?style=flat-square)](https://packagist.org/packages/faisalrizal/modules)

Jasahub Modules is a simple package to allow the means to separate your Lumen 5.6 application out into modules. Each module is completely self-contained allowing the ability to simply drop a module in for use.

The package follows the FIG standards PSR-1, PSR-2, and PSR-4 to ensure a high level of interoperability between shared PHP code.

## Documentation
You will find user friendly and updated documentation in the wiki here: [Caffeinated Modules Wiki](https://github.com/caffeinated/modules/wiki)

## Quick Installation
Begin by installing the package through Composer.

```
composer require faisalrizal/modules
```

Once this operation is complete, simply add both the service provider and facade classes to your project's `bootstrap/app.php` file:

## For Laravel

#### Service Provider

Add the following service provider in `config/app.php`.

```php
'providers' => array(
  'Jasahub\Modules\ModulesServiceProvider',
),
```
Next, add the following aliases to `aliases` array in the same file.

```php
'aliases' => array(
  'Module' => 'Jasahub\Modules\Facades\Module',
),
```
Next publish the package's configuration file by run :

```php
php artisan vendor:publish
```

## For Lumen

#### Service Provider

```php
$app->register(Jasahub\Modules\ModulesServiceProvider::class);
```

#### Facade

```php

$app->withFacades(true, [Jasahub\Modules\Facades\Module::class => 'Module']);
```

And that's it! With your coffee in reach, start building out some awesome modules!

#### Add Module 
```php
$app->register(App\Modules\[ModuleName]\Providers\ModuleServiceProvider::class);
```
