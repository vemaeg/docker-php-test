FROM php:8.2.13-cli

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y libzip-dev zlib1g-dev git libssl-dev zip libxml2-dev \
    && docker-php-ext-install pdo pdo_mysql opcache zip soap sockets \
    && pecl install mongodb xdebug \
    && docker-php-ext-enable mongodb xdebug \
    && apt-get clean
