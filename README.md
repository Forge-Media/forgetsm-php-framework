Introduction
============
[![Build Status](https://scrutinizer-ci.com/g/Forge-Media/forgetsm-php-framework/badges/build.png?b=master)](https://scrutinizer-ci.com/g/Forge-Media/forgetsm-php-framework/build-status/master)
[![Latest Stable Version](https://poser.pugx.org/forge-media/forgetsm-php-framework/v/stable)](https://packagist.org/packages/forge-media/forgetsm-php-framework)
[![License](https://poser.pugx.org/forge-media/forgetsm-php-framework/license)](https://packagist.org/packages/forge-media/forgetsm-php-framework)


Clone of [TS3 ADMIN PHP Framework 0.8.0.0](http://ts3admin.info/index.php) providing the library as composer project.


Usage
=====

Install via composer:

    "require": {
        "forge-media/forgetsm-php-framework": "dev-master"
    },

Skip the required_once part of official documentation and replace it with use API\TeamSpeak3 statement.

Examples:

```php
$ts3_ip = '127.0.0.1';
$ts3_queryport = 10011;
$ts3_port = 9987;

require("../vendor/autoload.php");

#build a new ts3admin object
$tsAdmin = new ts3admin($ts3_ip, $ts3_queryport);

if($tsAdmin->getElement('success', $tsAdmin->connect())) {
	#select teamspeakserver
	$tsAdmin->selectServer($ts3_port);

	}
}else{
	echo 'Connection could not be established.';
}

```

For more information visit the [official documentation](http://ts3admin.info/manual/classts3admin.html).
