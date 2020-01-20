FROM php:7.2-fpm

RUN apt-get update && apt-get install -y libpq-dev mariadb-client libpng-dev libfreetype6-dev libjpeg62-turbo-dev \
    && docker-php-ext-configure gd \
        --with-freetype-dir=/usr/lib/x86_64-linux-gnu/ \
        --with-jpeg-dir=/usr/lib/x86_64-linux-gnu/ \
    && docker-php-ext-install pdo_mysql bcmath gd

ADD ./default.ini /usr/local/etc/php/conf.d/default.ini

WORKDIR /var/www
