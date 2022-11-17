FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server;

EXPOSE 80

COPY ./conf/50-server.cnf /etc/mysql/mariadb.conf.d/

RUN service mysql start && mysql < /var/www/initial_db.sql && rm -f /var/www/initial_db.sql;

CMD ["mysqld"]