#FROM php:8.0.0RC3-fpm-alpine
FROM php:8.1.0alpha3-fpm-alpine
#FROM php
RUN apk --update --no-cache add git
RUN docker-php-ext-install pdo_mysql
COPY --from=composer /usr/bin/composer /usr/bin/composer
WORKDIR /var/www
CMD composer install ;  php-fpm
EXPOSE 9000
