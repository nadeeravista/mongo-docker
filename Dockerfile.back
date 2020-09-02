FROM php:7.2-fpm-alpine

RUN docker-php-ext-install pdo pdo_mysql

RUN apk add --update --no-cache --virtual .docker-php-mongodb-dependancies \
      $PHPIZE_DEPS \
       # Dependancies for MongoDB \
      heimdal-dev && \
      pecl install mongodb && \
      docker-php-ext-enable mongodb && \
      apk del .docker-php-mongodb-dependancies && \
      php -m; \