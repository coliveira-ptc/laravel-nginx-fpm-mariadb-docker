FROM php:7.4-fpm
RUN apt-get update && apt-get install -y

RUN sed -i s/9000/9002/g /usr/local/etc/php-fpm.d/zz-docker.conf

RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install bcmath

RUN apt-get update && apt-get install -y zlib1g-dev libzip-dev \
    && docker-php-ext-install zip

