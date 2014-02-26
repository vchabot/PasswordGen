# PasswordGen

PasswordGen is a PHP library generating passwords for you. For every new account to create, you can use this library to get a new and strong password, according to different settings.

PasswordGen requires PHP >= 5.3.3.

## Basic Usage

Instanciate the `PasswordGen\Generator` class, set up the settings (min length, symbols allowed...), and then call the `generate()` method.

```php
<?php
// instanciate the generator class
$passwordGen = new \PasswordGen\Generator();

// set up settings
$passwordGen->setMinLength(10);
$passwordGen->setAllowedSymbols(array('$', ':', '+', '='));
$passwordGen->setCase('both'); // choose between both/upper/lower
// ...

// generate
echo $passwordGen->generate();
// A$3e3:Slofo083
```

## License

PasswordGen is released under the MIT Licence. See the bundled LICENSE file for details.
