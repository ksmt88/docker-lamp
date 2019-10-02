LAMP - docker
====

A LAMP environment built using docker-compose.

## Dependencies
- [Docker](https://www.docker.com/)

## Example(For Laravel)
Add application.
```bash
git submodule add https://github.com/laravel/laravel.git app
```
Run docker-compose.
```bash
git submodule add https://github.com/laravel/laravel.git app
docker-compose up -d
```
Laravel set up.
```bash
docker-compose exec php-fpm sh -c "cd /var/www/html;composer install"
docker-compose exec php-fpm sh -c "cd /var/www/html;cp .env.example .env"
docker-compose exec php-fpm sh -c "cd /var/www/html;php artisan key:generate"
```
Check [https://localhost](https://localhost)
