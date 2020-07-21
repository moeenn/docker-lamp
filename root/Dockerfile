FROM php:7.4-cli
RUN apt-get update && apt-get upgrade -y && apt-get install apt-utils -y 
RUN docker-php-ext-install mysqli pdo pdo_mysql
EXPOSE 80
