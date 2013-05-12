# FuelPHP Package for Gdata

This package depend on google-api-php-client.  
https://code.google.com/p/google-api-php-client/

***

## Install
### Setup to fuel/packages/gdata
* Use composer https://packagist.org/packages/mp-php/fuel-packages-gdata
* git submodule
* Download zip

If you use git submodule or download zip, you must install vendors

	$ cd fuel/packages/gdata
	$ php composer.phar install

## Usage
### 1: Configuration
1. Copy packages/gdata/config/gdata.php to under app/config directory.  
2. Edit gdata.php that copied.

### 2: Enable Gdata package.
##### In app/config/config.php

	'always_load' => array('packages' => array(
		'gdata',
		...

or

##### In your code

	Package::load('gdata');

### 3: Forge Gdata

	$gdata = Gdata::forge(
		$service_name,
		$instance_name = 'default',
		$config = array()
	);

##### You can access $gdata->client and $gdata->service.
