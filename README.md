# Laravel Mongodb Cache
A MongoDB cache driver for Laravel

Installation
------------

Make sure you have [jenssegers\mongodb](https://github.com/jenssegers/Laravel-MongoDB) installed before you continue.

Install using composer:

    composer require emresari89/laravel-mongo-cache

Add the session service provider in `app/config/app.php`:

    'Emresar\Mongodb\Cache\MongoCacheServiceProvider',
    
Add mongodb cache store in `app/config/cache.php`

    'stores' => [
        /...

        'mongodb' => [
            'driver' => 'mongodb',
            'table' => 'cache',
            'connection' => null,
        ],
    ],
    
Update your .env file and change the `CACHE_DRIVER` to mongodb

    CACHE_DRIVER=mongodb
