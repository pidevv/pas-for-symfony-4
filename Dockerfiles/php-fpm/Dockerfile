FROM php:7.2-fpm

# Install APCu
RUN pecl install apcu
RUN echo "extension=apcu.so" > /usr/local/etc/php/conf.d/apcu.ini

RUN apt-get update

RUN docker-php-ext-install bcmath mbstring

# Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

#  Install php extension and git
RUN docker-php-ext-install pdo_mysql \
    && docker-php-ext-install pdo \
    && docker-php-ext-install opcache \
    && apt-get install -y libpq-dev \
    && apt-get install -y git \
    && pecl install xdebug \
    && docker-php-ext-enable xdebug

