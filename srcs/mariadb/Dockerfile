FROM debian:buster

WORKDIR /srcs

RUN apt-get update && apt-get install -y mariadb-server;

EXPOSE 3306

HEALTHCHECK --start-period=5m \
  CMD mariadb -e 'SELECT @@datadir;' || exit 1

CMD ["mysqld"]