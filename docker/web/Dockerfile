FROM php:7.4-apache

COPY --from=composer /usr/bin/composer /usr/bin/composer

RUN docker-php-ext-install \
	pdo_mysql \
	&& a2enmod \
	rewrite