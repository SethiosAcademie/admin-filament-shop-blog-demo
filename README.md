# admin-filament-shop-blog-demo
this is a admin full panel demo, for a complete blog and shop for any ecommerce. it's provide by Filament, Laravel and some spatie packages.

A demo application to illustrate how Filament Admin works.

![Filament Demo](https://github.com/filamentphp/demo/assets/171715/899161a9-3c85-4dc9-9599-13928d3a4412)

## Installation

Clone the repo locally:

```sh
https://github.com/SethiosAcademie/admin-filament-shop-blog-demo.git SethiosFilament-demo && cd SethiosFilament-demo
```

Install PHP dependencies:

```sh
composer install
```

Setup configuration:

```sh
cp .env.example .env
```

Generate application key:

```sh
php artisan key:generate
```

Create an SQLite database. You can also use another database (MySQL, Postgres), simply update your configuration accordingly.

```sh
touch database/database.sqlite
```
For Mysql, Go and change some Variable in env file:
```sh

DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=your_data_base_name
DB_USERNAME=your_user_name
DB_PASSWORD=your_password
```

Run database migrations:

```sh
php artisan migrate
```

Run database seeder:

```sh
php artisan db:seed
```

> **Note**  
> If you get an "Invalid datetime format (1292)" error, this is probably related to the timezone setting of your database.  
> Please see https://dba.stackexchange.com/questions/234270/incorrect-datetime-value-mysql


Create a symlink to the storage:

```sh
php artisan storage:link
```

Run the dev server (the output will give the address):

```sh
php artisan serve
```

You're ready to go! Visit the url in your browser, and login with:

-   **Username:** admin@filamentphp.com
-   **Password:** password

## Features to explore

### Relations

#### BelongsTo
- ProductResource
- OrderResource
- PostResource

#### BelongsToMany
- CategoryResource\RelationManagers\ProductsRelationManager

#### HasMany
- OrderResource\RelationManagers\PaymentsRelationManager

#### HasManyThrough
- CustomerResource\RelationManagers\PaymentsRelationManager

#### MorphOne
- OrderResource -> Address

#### MorphMany
- ProductResource\RelationManagers\CommentsRelationManager
- PostResource\RelationManagers\CommentsRelationManager

#### MorphToMany
- BrandResource\RelationManagers\AddressRelationManager
- CustomerResource\RelationManagers\AddressRelationManager

