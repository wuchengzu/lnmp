FROM php:7.2.14-fpm

ENV EXT_DIR=/usr/src/ext

COPY ./ext $EXT_DIR

RUN docker-php-source extract \
&& docker-php-ext-install \
pdo_mysql \
bcmath \ 
&& pecl update-channels \
&& pecl install \
$EXT_DIR/redis-4.2.0.tgz \
$EXT_DIR/xdebug-2.6.0.tgz 


