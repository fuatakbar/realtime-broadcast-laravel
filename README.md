<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>

## About Laravel

Laravel is a web application framework with expressive, elegant syntax. We believe development must be an enjoyable and creative experience to be truly fulfilling. Laravel takes the pain out of development by easing common tasks used in many web projects, such as:

- [Simple, fast routing engine](https://laravel.com/docs/routing).
- [Powerful dependency injection container](https://laravel.com/docs/container).
- Multiple back-ends for [session](https://laravel.com/docs/session) and [cache](https://laravel.com/docs/cache) storage.
- Expressive, intuitive [database ORM](https://laravel.com/docs/eloquent).
- Database agnostic [schema migrations](https://laravel.com/docs/migrations).
- [Robust background job processing](https://laravel.com/docs/queues).
- [Real-time event broadcasting](https://laravel.com/docs/broadcasting).

Laravel is accessible, powerful, and provides tools required for large, robust applications.

## How to use

- Set .env file, adjust it with your database setting
- Change broadcast driver setting in .env file like :
  
> BROADCAST_DRIVER=redis

- Change redist client to predis in config/database.php

> 'redis' => [
>
>   'client' => env('REDIS_CLIENT', 'predis'),
> 
>   'options' => [
>       'cluster' => env('REDIS_CLUSTER', 'redis'),
>       'prefix' => env('REDIS_PREFIX', ''),
>   ],

- Add laravel echo server package with npm

> $ npm install -g laravel-echo-server

- create laravel echo server config.

> $ laravel-echo-server init

- install laravel echo

> $ npm install && npm install laravel-echo

- install socket io client and create laravel-echo-setup

> $ npm install socket.io-client
>
    >> import Echo from 'laravel-echo';
    >>
    >> window.Echo = new Echo({
    >> broadcaster: 'socket.io',
    >> host: window.location.hostname + ":" + window.laravel_echo_port
    >> });

- add laravel-echo-setup.js to mix (webpack)
  
> mix.js('resources/assets/js/laravel-echo-setup.js', 'public/js');
> $ npm run dev




