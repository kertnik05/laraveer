# Laraveer

> Prerequisites: `Docker` installed on  your machine

### Docker Development Set-Up


1. Build images, volume and network by running the following:
    ```
    docker-compose up -d --build
    ```

2. Install laravel by running the following:

    ```
    docker-compose exec app composer create-project laravel/laravel .
    ```

3. Set your database credentials.

    **Database**:
    ```
    DB_HOST=mysql
    DB_PORT=3306
    DB_DATABASE=app
    DB_USERNAME=app
    DB_PASSWORD=secret
    ```

4. Voila! All should be working right now.
   > [http://localhost](http://localhost)

----

Footnotes:

* Note that this takes a longer time to be accessible, specially when the container is freshly built. You can check the container logs to see its progress.

### Docker-compose cheat sheet
1. Laravel artisan commands `docker-compose exec app php artisan {command}`
2. Laravel migrate command `docker-compose exec app php artisan migrate`
3. Stopping services `docker-compose stop`
4. Starting services `docker-compose start`
5. Bash `docker-compose exec app bash`