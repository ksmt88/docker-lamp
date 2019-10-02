FROM php:7.3-fpm-alpine

RUN apk update && apk add \
    libmemcached-dev \
    libmcrypt-dev \
    libxml2-dev \
    libgsasl-dev \
    && docker-php-ext-install mysqli mbstring pdo pdo_mysql tokenizer xml

RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/bin --filename=composer
