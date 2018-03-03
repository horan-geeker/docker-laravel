######
# See: https://hub.docker.com/_/php/
######
FROM php:7.1-fpm
WORKDIR /var/www
######
# You can install php extensions using docker-php-ext-install
######

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
    && docker-php-ext-install -j$(nproc) iconv mcrypt pdo pdo_mysql gd \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
