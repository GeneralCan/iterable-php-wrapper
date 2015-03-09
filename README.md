# Iterable PHP Wrapper

[![Build Status](https://travis-ci.org/cdlewis/iterable-php-wrapper.svg?branch=master)](https://travis-ci.org/cdlewis/iterable-php-wrapper)
[![Coverage Status](https://coveralls.io/repos/cdlewis/iterable-php-wrapper/badge.svg?branch=master)](https://coveralls.io/r/cdlewis/iterable-php-wrapper?branch=master)

## Getting Started

Clone the repository
```
git clone https://github.com/cdlewis/iterable-php-wrapper.git
```

Include the wrapper
```php
require_once( 'iterable-php-wrapper/iterable.php' );
```

Instantiate the class with your API key
```php
$iterable = new Iterable( 'YOUR API KEY' );
```

## Examples

### Lists

Show all lists:
```php
$iterable->lists();
```

Subscribe users to a list:
```
$iterable->list_subscribe( $list_id, array(
	array( 'email' => john@example.com ),
	array( 'email' => harry@example.com )
);
```

Unsubscribe users from a list:
```php
$iterable->list_unsubscribe( $list_id, array(
	array( 'email' => john@example.com ),
	array( 'email' => harry@example.com )
) );
```

### Users

Get a user by email:
```php
$iterable->user( 'john@example.com' );
```

Change a user's email:
```php
$iterable->user_update_email( 'old@example.com', 'new@example.com' );
```

Delete a user:
```php
$iterable->delete( 'john@example.com' );
```

### Campaigns

Get all campaigns:
```php
$iterable->campaigns();
```

### Export

Export as JSON
```php
$iterable->export_json( 'user', 'All' );
```

Export as CSV
```php
$iterable->export_csv( 'user', 'All' );
```
