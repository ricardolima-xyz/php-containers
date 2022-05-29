# Docker Image
FROM php:8.1-apache

# Updating sources
RUN apt-get -y update

# Enabling Apache RewriteEngine
RUN a2enmod rewrite

# Installing PHP Modules
RUN docker-php-ext-install calendar mysqli pdo pdo_mysql 

# Installing intl module
RUN apt-get install -y libicu-dev \
&& docker-php-ext-configure intl \
&& docker-php-ext-install intl

# Installing postgresql support
# Install Postgre PDO
RUN apt-get install -y libpq-dev \
    && docker-php-ext-configure pgsql -with-pgsql=/usr/local/pgsql \
    && docker-php-ext-install pdo_pgsql pgsql

#RUN docker-php-ext-install pgsql

# Setting Timezone
#RUN sed -i 's/;date.timezone =/date.timezone = Europe\/Berlin/g' /usr/local/etc/php/php.ini-production
#RUN sed -i 's/;date.timezone =/date.timezone = Europe\/Berlin/g' /usr/local/etc/php/php.ini-development
#RUN echo 'date.timezone = Europe/Berlin' > /usr/local/etc/php/conf.d/timezone.ini
