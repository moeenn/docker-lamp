FROM php:7.4-apache
RUN apt-get update
RUN apt-get install -y apt-utils
RUN apt-get upgrade -y
RUN docker-php-ext-install pdo pdo_mysql mysqli
RUN apt-get autoremove -y
RUN a2enmod rewrite
EXPOSE 80
