# ClamAV Validator For Laravel 5

[![Build Status](https://scrutinizer-ci.com/g/sunspikes/clamav-validator/badges/build.png?b=master)](https://scrutinizer-ci.com/g/sunspikes/clamav-validator) [![Code Quality](https://scrutinizer-ci.com/g/sunspikes/clamav-validator/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/sunspikes/clamav-validator)

Custom Laravel 5.0 anti-virus validator for file uploads.

* [Installation](#installation)
* [Usage](#usage)
* [Change Log](#changelog)
* [Author](#author)

<a name="installation"></a>
## Installation

Install the package through [Composer](http://getcomposer.org).

In your `composer.json` file:

```json
{
    "repositories":
        [
			{
                "type": "vcs",
                "url": "https://github.com/lenrsmith/clamav-validator"
            }
        ],
	"require": {
		"laravel/framework": "5.0.*",
		"lenrsmith/clamav-validator": "dev-master"
	}
}
```

**Note:** the minimum version of Laravel that's supported is 5.0. 

Run `composer install` or `composer update` to install the package.

Add the following to your `providers` array in `app/config/app.php`:

```php
'providers' => array(
	// ...

	'Lenrsmith\ClamavValidator\ClamavValidatorServiceProvider',
),
```


<a name="usage"></a>
## Usage

Use it like any `Validator` rule:

```php
$rules = array(
	'my_file_field' => 'clamav',
);
```


<a name="changelog"></a>
## Change Log
2015.07.28 - Updated to support Laravel 5.0 by Leonard Smith (https://github.com/lenrsmith/clamav-validator)

2014.12.05 - Initial version, using extension php-clamav

2014.12.05 - Removed the dependency php-clamav, Now using [Quahog](https://github.com/jonjomckay/quahog)

<a name="author"></a>
## Author

Krishnaprasad MG [@sunspikes]

_Contact me at [sunspikes at gmail dot com]_
