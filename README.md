#Common classes and interfaces for PHP

[![Latest Stable Version](https://poser.pugx.org/phpextra/unknown/v/stable.svg)](https://packagist.org/packages/phpextra/unknown)
[![Total Downloads](https://poser.pugx.org/phpextra/unknown/downloads.svg)](https://packagist.org/packages/phpextra/unknown)
[![License](https://poser.pugx.org/phpextra/unknown/license.svg)](https://packagist.org/packages/phpextra/unknown)
[![Build Status](http://img.shields.io/travis/phpextra/unknown.svg)](https://travis-ci.org/phpextra/unknown)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/phpextra/unknown/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/phpextra/unknown/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/phpextra/unknown/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/phpextra/unknown/?branch=master)
[![GitTip](http://img.shields.io/gittip/jkobus.svg)](https://www.gittip.com/jkobus)

##Usage

###UnknownType (PHPExtra\Type\UnknownType)

It should not happen but sometimes does - you have a method with many different response types, but want to handle it like a pro:

```php
$messedUpResponse = $api->getMeSomeChickens(); // returns "Chicken" **or** "Collection" **of** "Chickens" **or** "no" as an error response :-)

$result = new UnknownType($messedUpResponse);

if($result->isCollection()){
    $result->getAsCollection()->sort($sorter);
    ...
}elseif($result->isException){
    throw $result->getAsException();
    ...
}
```

UnknownType can be extended and customized :-)

## Installation (Composer)

```json
{
    "require": {
        "phpextra/unknown":"~1.0"
    }
}
```

##Changelog

    No releases yet

##Contributing

All code contributions must go through a pull request.
Fork the project, create a feature branch, and send me a pull request.
To ensure a consistent code base, you should make sure the code follows
the [coding standards](http://symfony.com/doc/2.0/contributing/code/standards.html).
If you would like to help take a look at the **list of issues**.

##Requirements

    See composer.json for a full list of dependencies.

##Authors

    Jacek Kobus - <kobus.jacek@gmail.com>

## License information

    See the file LICENSE.txt for copying permission.on.