# Carrier Elephant
Simple and light library that facilitates the management of dynamic class loading through a list of previously defined namespaces.


### How to use the library
```php
//... step 1: load the main class of the library into memory
include __DIR__ . "/lib/carrier/src/Main.php";

//... step 2: define namespaces and their respective location paths
Carrier::active(array( 
	'Ksike'=> '/home/me/libs/ksike/lib/',
	'Cordova'=> '/home/me/libs/cordova/',
	'Scure'=> '/var/www/scure/' 
));

//... step 3: use the desired libraries
use Ksike\secretary\src\server\Main as Secretary;
print_r(Secretary::this());
```