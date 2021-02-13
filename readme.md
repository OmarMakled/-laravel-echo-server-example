## Laravel-echo-server

Before installation laravel valet and redis shoud be up and running.

## Server Side

```
 git clone git@github.com:OmarMakled/laravel-echo-server-example.git
 cd laravel-echo-server-example
 composer install
 cp .env.example .env
```

Update `.env` file

```
APP_URL=laravel-echo-server-example.test
BROADCAST_DRIVER=redis
QUEUE_CONNECTION=redis
MIX_APP_URL="${APP_URL}"
```

```
php artisan key:generate
php artisan optimize
```

## Client side

```
npm i
./node_modules/.bin/laravel-echo-server init
./node_modules/.bin/laravel-echo-server start
npm run watch
```

## Emit an event

```
php artisan queue:work
php artisan tinker
event(new \App\Events\UserEvent());
```

Enjoy !
