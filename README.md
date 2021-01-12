## PDOx
```
 _____  _____   ____       
 |  __ \|  __ \ / __ \      
 | |__) | |  | | |  | |_  __
 |  ___/| |  | | |  | \ \/ /
 | |    | |__| | |__| |>  <
 |_|    |_____/ \____//_/\_\
```
Fast, efficient and useful Query Builder and PDO Class for #PHP

[![Total Downloads](https://poser.pugx.org/izniburak/pdox/d/total.svg)](https://packagist.org/packages/izniburak/pdox)
[![Latest Stable Version](https://poser.pugx.org/izniburak/pdox/v/stable.svg)](https://packagist.org/packages/izniburak/pdox)
[![Latest Unstable Version](https://poser.pugx.org/izniburak/pdox/v/unstable.svg)](https://packagist.org/packages/izniburak/pdox)
[![License](https://poser.pugx.org/izniburak/pdox/license.svg)](https://packagist.org/packages/izniburak/pdox)

## Install

composer.json file:
```json
{
    "require": {
        "izniburak/pdox": "^1"
    }
}
```
after run the install command.
```
$ composer install
```

OR run the following command directly.

```
$ composer require izniburak/pdox
```

## Example Usage
```php
require 'vendor/autoload.php';

$config = [
	'host'		=> 'localhost',
	'driver'	=> 'mysql',
	'database'	=> 'test',
	'username'	=> 'root',
	'password'	=> '',
	'charset'	=> 'utf8',
	'collation'	=> 'utf8_general_ci',
	'prefix'	 => ''
];

$db = new \Buki\Pdox($config);

$records = $db->table('users')
		->select('id, name, surname, age')
		->where('age', '>', 18)
		->orderBy('id', 'desc')
		->limit(20)
		->getAll();

var_dump($records);
```

## Docs
Documentation page: https://github.com/tanvir-siddique/pdox/blob/master/DOCS.md
