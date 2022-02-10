Scheduling task manager for laravel-admin
============================

[![StyleCI](https://styleci.io/repos/99676857/shield?branch=master)](https://styleci.io/repos/99676857)
[![Packagist](https://img.shields.io/packagist/l/laravel-admin-ext/scheduling.svg?maxAge=2592000)](https://packagist.org/packages/laravel-admin-ext/scheduling)
[![Total Downloads](https://img.shields.io/packagist/dt/laravel-admin-ext/scheduling.svg?style=flat-square)](https://packagist.org/packages/laravel-admin-ext/scheduling)
[![Pull request welcome](https://img.shields.io/badge/pr-welcome-green.svg?style=flat-square)]()

A web interface for manage task scheduling in laravel.

[Documentation](http://open-admin.org/docs/en/extension-scheduling)

## Screenshot

![extention-schedualing](https://user-images.githubusercontent.com/86517067/153514589-e6204239-d227-483a-bf4d-c5da2720f038.png)

## Installation

```
$ composer require open-admin-ext/scheduling

$ php artisan admin:import scheduling
```

Open `http://your-host/admin/scheduling`.

Try to add a scheduling task in `app/Console/Kernel.php` like this:

```php
class Kernel extends ConsoleKernel
{
    protected function schedule(Schedule $schedule)
    {
        $schedule->command('inspire')->everyTenMinutes();

        $schedule->command('route:list')->dailyAt('02:00');
    }
}

```

And you can find these tasks in scheduling panel.

Debugging
------------
If console shows errors like: `sh: : command not found`
Try adding this your .env file: `PHP_BINARY=/path/to/your/php/binaray/`

License
------------
Licensed under [The MIT License (MIT)](LICENSE).
