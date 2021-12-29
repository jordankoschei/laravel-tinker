Just tinkering around in Laravel.

# Working locally

- Instructions for [Laravel Sail](https://laravel.com/docs/8.x/sail)

## Starting the local server

1. Start the Docker app
2. `j example-app`
3. `./vendor/bin/sail up`

## Working with MySQL

Use **Sequel Ace**, not Sequel Pro. Use the values found in `.env`:

- Host: `localhost`
- Username: `sail`
- Password: `password`
- Port: `3306`

## Running migrations and other `php artisan` commands

Artisan commands must be run from within the virtual machine, as explained in [this Stack Overflow answer](https://stackoverflow.com/a/62095275).

1. `docker ps`
2. Copy the Docker ID.
3. `docker exec -it <containerId> /bin/bash`
4. `php artisan migrate` or whatever