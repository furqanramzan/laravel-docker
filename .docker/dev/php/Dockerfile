FROM php:8.1.4-fpm-alpine

WORKDIR /var/www

RUN docker-php-ext-install pdo_mysql mysqli

# copy config file which was transfered to container from php.ini into the exact location after installing php extensions
COPY php.ini /usr/local/etc/php/php.ini

# install composer for later use
COPY --from=composer:2 /usr/bin/composer /usr/bin/composer

# open port 9000
EXPOSE 9000