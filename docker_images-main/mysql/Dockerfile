FROM mysql:latest

MAINTAINER baeldung.com

RUN chown -R mysql:root /var/lib/mysql

ARG MYSQL_DATABASE
ARG MYSQL_USER
ARG MYSQL_PASSWORD
ARG MYSQL_ROOT_PASSWORD

ENV MYSQL_DATABASE=studentapp.crcos8q68fwd.eu-north-1.rds.amazonaws.com
ENV MYSQL_USER=admin
ENV MYSQL_PASSWORD=12345678
ENV MYSQL_ROOT_PASSWORD=root

COPY student.sql /etc/mysql/student.sql

RUN sed -i 's/MYSQL_DATABASE/'$MYSQL_DATABASE'/g' /etc/mysql/student.sql
RUN cp /etc/mysql/student.sql /docker-entrypoint-initdb.d

EXPOSE 3306

CMD /bin/bash


