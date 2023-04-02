FROM php:8.2-apache

RUN apt-get update
RUN apt-get install -y libpq-dev
RUN docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql
RUN docker-php-ext-install mysqli pgsql pdo pdo_mysql pdo_pgsql  &&\
    pecl install xdebug && docker-php-ext-enable xdebug

