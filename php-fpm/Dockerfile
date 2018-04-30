######
# See: https://hub.docker.com/_/php/
######
FROM php:7.2-fpm
WORKDIR /var/www
######
# You can install php extensions using docker-php-ext-install
######

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    && docker-php-ext-install -j$(nproc) gd pdo pdo_mysql bcmath \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/
