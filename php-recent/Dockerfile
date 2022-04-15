# Docker Image
FROM php:8-apache

# Enabling Apache RewriteEngine
RUN a2enmod rewrite

# Installing PHP Modules
RUN docker-php-ext-install calendar mysqli pdo pdo_mysql

# Setting Timezone
#RUN sed -i 's/;date.timezone =/date.timezone = Europe\/Berlin/g' /usr/local/etc/php/php.ini-production
#RUN sed -i 's/;date.timezone =/date.timezone = Europe\/Berlin/g' /usr/local/etc/php/php.ini-development
#RUN echo 'date.timezone = Europe/Berlin' > /usr/local/etc/php/conf.d/timezone.ini

