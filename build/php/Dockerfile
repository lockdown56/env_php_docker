FROM php:7.3.4-fpm
  RUN apt-get update && apt-get install -y \
         libzip-dev \
         libfreetype6-dev \
         libjpeg62-turbo-dev \
         libpng-dev \
         # php5-mysql \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd pdo pdo_mysql zip \
    && cp "$PHP_INI_DIR/php.ini-production" "$PHP_INI_DIR/php.ini"
