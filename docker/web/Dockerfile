FROM php:7.4-apache

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN apt-get update && apt-get install -y \
    zlib1g-dev \
    libzip-dev \
    unzip
RUN docker-php-ext-install zip

RUN docker-php-ext-install \
	pdo_mysql \
	&& a2enmod \
	rewrite