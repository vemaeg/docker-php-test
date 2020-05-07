FROM php:7.4-cli

COPY --from=composer:latest /usr/local/composer /usr/local/composer

RUN apt-get update \
    && apt-get install -y libzip-dev zlib1g-dev git libssl-dev zip \
    && docker-php-ext-install pdo pdo_mysql opcache \
    && apt-get clean
