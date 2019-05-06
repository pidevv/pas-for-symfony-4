FROM php:7.2-fpm

# Install APCu
RUN pecl install apcu
RUN echo "extension=apcu.so" > /usr/local/etc/php/conf.d/apcu.ini

RUN apt-get update

RUN docker-php-ext-install bcmath mbstring

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN docker-php-ext-install pdo_mysql

RUN docker-php-ext-install pdo

RUN docker-php-ext-install opcache

RUN apt-get install -y libpq-dev

# Install git
RUN apt-get install -y git

# Install xdebug
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug

