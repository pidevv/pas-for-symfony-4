FROM php:7.2-fpm

RUN apt-get update

RUN docker-php-ext-install bcmath mbstring

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN docker-php-ext-install pdo_mysql

RUN docker-php-ext-install pdo

RUN docker-php-ext-install opcache

RUN apt-get install -y libpq-dev

