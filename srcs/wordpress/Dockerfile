FROM debian:buster

RUN apt-get update && apt-get -y install php7.3 php-fpm

EXPOSE 90

CMD ["/usr/sbin/php-fpm7.3"]