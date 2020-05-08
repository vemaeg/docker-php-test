FROM php:7.2-cli

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y libzip-dev zlib1g-dev git libssl-dev zip \
    && docker-php-ext-install pdo pdo_mysql opcache zip \
    && apt-get clean
