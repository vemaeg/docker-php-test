FROM php:7.3.32-cli

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y libzip-dev zlib1g-dev git libssl-dev zip libxml2-dev \
    && docker-php-ext-install pdo pdo_mysql opcache zip soap \
    && pecl install mongodb \
    && docker-php-ext-enable mongodb \
    && apt-get clean
