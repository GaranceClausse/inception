FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server mariadb-client;

HEALTHCHECK --start-period=5m \
  CMD mariadb -e 'SELECT @@datadir;' || exit 1

EXPOSE 3306

COPY tools/configure.sh /tmp/configure.sh

RUN chmod 777 /tmp/configure.sh

COPY ./tools/server.cnf /etc/mysql/mariadb.conf.d/server.cnf

RUN bash ./tmp/configure.sh

CMD exec mysqld_safe