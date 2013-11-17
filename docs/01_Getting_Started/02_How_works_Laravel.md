Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable, creative experience to be truly fulfilling. Laravel attempts to take the pain out of development by easing common tasks used in the majority of web projects, such as authentication, routing, sessions, and caching.

Laravel aims to make the development process a pleasing one for the developer without sacrificing application functionality. Happy developers make the best code. To this end, we've attempted to combine the very best of what we have seen in other web frameworks, including frameworks implemented in other languages, such as Ruby on Rails, ASP.NET MVC, and Sinatra.

Laravel is accessible, yet powerful, providing powerful tools needed for large, robust applications. A superb inversion of control container, expressive migration system, and tightly integrated unit testing support give you the tools you need to build any application with which you are tasked.

## Documentation

You can access to the full documentation [there](http://laravel.com/docs)


## Laravel presentation
The folder /app is where all the fun happens, so let's have a look of mains folder of the /app directory.

* /config
* /controllers
* /lang
* /migrations
* /models
* /views
* /routes.php [file]
* /filters.php [file]

## config

The config folder contains a number of config files for changing various aspects of the framework. No config needs to be set at install for the framework to work 'out of the box'. Most of the config files return key-value PHP arrays of options, sometimes key-closure pairs that allow a great deal of freedom to modify the inner working of some of Laravel's core classes.

## controllers

Laravel provides two methods for routing, using controllers and using routes. This folder contains the Controller classes that are used to provide basic logic, interact with data models, and load view files for your application. Controllers were added to the framework at a later date to provide familiar ground for users migrating from other frameworks. Although they were added as an afterthought, due to Laravel's powerful routing system, they allow you to perform any action which can be performed using routes to closures.

## lang

In this directory, PHP files containing arrays of strings exist to enable easy localization of applications built using Laravel.

## migrations

The migrations folder contains PHP classes which allow Laravel to update the Schema of your current database, or populate it with values while keeping all versions of the application in sync. Migration files must not be created manually, as their file name contains a timestamp. Instead use the Artisan CLI interface command php artisan migrate:make <migration_name> to create a new Migration.

## models

Models are classes that represent your project's data. Normally this would mean integrating with a form of database, or other data source. Laravel provides three methods for interacting with common database platforms, including a query builder named 'Fluent', which allows you to create SQL queries by chaining PHP methods, using Eloquent ORM to represent your tables as PHP Objects, or the plain old raw SQL queries that you're used to. Fluent and Eloquent both use a similar syntax, making their adoption a smooth transition.

The models directory has been auto-loaded automatically from start.php.

## storage

The storage directory is used as temporary file store for various Laravel services such as sessions, cache, compiled view templates. This directory must be writable by the web server. This directory is maintained by Laravel and you need not tinker with it.

## views

The views directory contains your HTML template files to be used by controllers or routes, although please use a .php extension for files in this folder. You can alternatively use a .blade.php extension to enable parsing with the Blade templating library.

## routes.php [file]

The routes file contains the methods which enable routes to be mapped to their appropriate outcome with Laravel. This topic will be explained more thoroughly in upcoming chapters. This file also contains declarations for several events including error pages, and can be used to define view composers or route filters.

## filters.php [file]

This file contains various application & route filter methods that alter the outcome of your application. Laravel has some pre-defined filters for access control and XSS protection