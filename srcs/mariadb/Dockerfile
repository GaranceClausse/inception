FROM debian:buster

RUN apt-get update && apt-get install -y mariadb-server;

COPY ./mariadb-entrypoint.sh /usr/local/bin/

ENTRYPOINT ["mariadb-entrypoint.sh"]

EXPOSE 3306

STOPSIGNAL SIGQUIT

CMD ["mysqld_safe"]