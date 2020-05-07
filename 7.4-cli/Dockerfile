FROM php:7.4-cli

COPY --from=composer-file /usr/bin/composer /usr/bin/composer

RUN apt-get update \
    && apt-get install -y libzip-dev zlib1g-dev git libssl-dev zip \
    && docker-php-ext-install pdo pdo_mysql opcache \
    && apt-get clean
