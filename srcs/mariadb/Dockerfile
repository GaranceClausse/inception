FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server;

RUN chmod a+rx /usr/sbin

EXPOSE 3306


CMD ["mysqld"]