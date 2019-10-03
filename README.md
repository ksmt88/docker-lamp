LAMP - docker
====

A LAMP environment built using docker-compose.

## Dependencies
- [Docker](https://www.docker.com/)

## Example(For Laravel)
### Set up database.
Copy .env
```bash
cp .env.example .env
```
Set environment variable
```bash
MYSQL_ROOT_PASSWORD=
MYSQL_USER=
MYSQL_PASSWORD=
MYSQL_DATABASE=
```
### Add application.
```bash
git submodule add https://github.com/laravel/laravel.git app
```
### Run docker-compose.
```bash
docker-compose up -d
```
### Set up Laravel.
```bash
docker-compose exec php-fpm sh -c "cd /var/www/html;composer install"
docker-compose exec php-fpm sh -c "cd /var/www/html;cp .env.example .env"
docker-compose exec php-fpm sh -c "cd /var/www/html;php artisan key:generate"
```
When using database, Edit .env and run the following command
```bash
docker-compose exec php-fpm sh -c "cd /var/www/html;php artisan migrate"
```
Check [https://localhost](https://localhost)
