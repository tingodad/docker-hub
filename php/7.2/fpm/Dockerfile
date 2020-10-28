FROM php:7.2-fpm

RUN apt-get update && apt-get install -y \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng-dev \
    postgresql-server-dev-11 \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install -j$(nproc) iconv \
    && docker-php-ext-install -j$(nproc) gd \
    && docker-php-ext-install zip pgsql pdo pdo_mysql pdo_pgsql sockets opcache \
    && rm -r /var/lib/apt/lists/* \
    && pecl install mcrypt-1.0.1 \
    && pecl install -o -f redis \
    && rm -rf /tmp/pear \
    && docker-php-ext-enable mcrypt redis

RUN pecl install mongodb \
&& echo "extension=mongodb.so" > /usr/local/etc/php/conf.d/ext-mongodb.ini