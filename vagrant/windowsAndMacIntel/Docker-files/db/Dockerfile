FROM mysql:8.0.33
LABEL "project"="vprofile"
LABEL "Author"="Derrick"

ENV MYSQL_ROOT_PASSWORD=vprodbpass
ENV MYSQL_DATABASE=accounts

ADD db_backup.sql /docker-entrypoint-initdb/
