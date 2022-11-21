FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server;

HEALTHCHECK --start-period=5m \
  CMD mariadb -e 'SELECT @@datadir;' || exit 1

RUN chmod 777 /usr/sbin/mariadb

COPY tools/configure.sh /tmp/configure.sh

ENTRYPOINT ["sh", "/tmp/configure.sh"]