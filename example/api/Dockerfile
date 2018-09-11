FROM php:7-fpm-alpine

# Install app dependencies
RUN apk update && apk add openssl zip unzip git
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer
RUN docker-php-ext-install pdo mbstring pdo_mysql

WORKDIR /var/www

COPY . /var/www
RUN composer install