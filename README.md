# PHP Min coverage test

[![PHP version](https://badge.fury.io/ph/lencse%2Fmin-coverage.svg)](https://badge.fury.io/ph/lencse%2Fmin-coverage)
[![Build Status](https://travis-ci.org/lencse/php-min-coverage.svg?branch=master)](https://travis-ci.org/lencse/min-coverage)

## Install

Via Composer

````bash
composer require --dev lencse/min-coverage
````

## Usage

### Checking code coverage

````bash
# Create a Clover XML output of your project with PHPUnit
phpunit --coverage-clover build/logs/clover.xml
# Check code coverage
vendor/bin/min-coverage --min-coverage 95 --clover-file build/logs/clover.xml
````

#### Integrating into composer.json

````json
{
    "scripts": {
        "test-all": [
            "phpunit --coverage-clover build/logs/clover.xml",
            "vendor/bin/min-coverage --min-coverage 95 --clover-file build/logs/clover.xml"
        ]
    }
}
````

````bash
composer test-all
````

## Testing

``` bash
composer test
```


## License

The MIT License (MIT)
