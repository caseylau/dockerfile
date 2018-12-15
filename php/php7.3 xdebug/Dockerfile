FROM php:7.3-fpm

# Install xdebug
RUN pecl install xdebug && docker-php-ext-enable xdebug
WORKDIR /var/www