# LazyPDO
Lazy loadable PDO

## Description
You can use LazyPDO in place of PDO, when you need lazy-load. No database connection will be made until first call to one of PDO's methods.

## Installation

With composer:

```
composer install senasi/lazy-pdo
```

## Usage

```
$dsn = 'mysql:hostname=localhost;dbname=test';
$user = 'test';
$password = 'test';

$pdo = new LazyPDO\LazyPDO($dns, $user, $password); // doesn't connect yet

$pdo->query('SELECT * FROM `table` WHERE 1'); // connection is made before executing query
```
