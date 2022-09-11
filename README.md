# Laravel Migrations Generator Laravel 5/6/7/8 +
[![Latest Stable Version](https://poser.pugx.org/oscarafdev/migrations-generator/v/stable)](https://packagist.org/packages/oscarafdev/migrations-generator)
[![Monthly Downloads](https://poser.pugx.org/oscarafdev/migrations-generator/d/monthly)](//packagist.org/packages/oscarafdev/migrations-generator)
[![License](https://poser.pugx.org/oscarafdev/migrations-generator/license)](https://packagist.org/packages/oscarafdev/migrations-generator)

Generate Laravel Migrations from an existing database, including indexes and foreign keys!

# 100,000 downloads


I have been with very little time, doing what I can so that this library is useful for everyone who needs it. As of today we have more than 100,000 downloads, thank you very much everyone!

Help me with a coffe: https://cafecito.app/oscarafdev (1 USD)



## Laravel 6/7/8/9 installation

The recommended way to install this is through composer:

```bash
composer require oscarafdev/migrations-generator --dev
```

In Laravel 5.5+ the service providers will automatically get registered. 

## Usage

To generate migrations from a database, you need to have your database setup in Laravel's Config.

Run `php artisan migrate:generate` to create migrations for all the tables, or you can specify the tables you wish to generate using `php artisan migrate:generate table1,table2,table3,table4,table5`. You can also ignore tables with `--ignore="table3,table4,table5"`

Laravel Migrations Generator will first generate all the tables, columns and indexes, and afterwards setup all the foreign key constraints. So make sure you include all the tables listed in the foreign keys so that they are present when the foreign keys are created.

You can also specify the connection name if you are not using your default connection with `--connection="connection_name"`

Run `php artisan help migrate:generate` for a list of options.

Check out Chung Tran's blog post for a quick step by step introduction: [Generate Migrations from an existing database in Laravel 4](http://codingtip.blogspot.com/2014/04/laravel-4-generate-migration-existed-dabase-laravel-4.html)

## Changelog

Changelog for Laravel Migrations Generator

### Jan 2021: v2.0.24
* Support for Laravel 8
* Fixed a issue where double single quotes were generated

### Ago 2020: v2.0.23
* Added support for precisions in timestamp.
* Fixed an issue with the text type.
* Fixed other reported bugs

### May 2020: v2.0.19
* Support for Laravel 7

## Thank You

Thanks to Jeffrey Way for his amazing Laravel-4-Generators package. This package depends greatly on his work.

## Contributors

Bernhard Breytenbach ([@BBreyten](https://twitter.com/BBreyten))

Oscar Fernandez ([@oscarafdev](https://www.linkedin.com/in/oscarafdev/))

ofernandez@sofrecom.com.ar

## License

The Laravel Migrations Generator is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
