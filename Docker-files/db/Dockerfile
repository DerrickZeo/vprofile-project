FROM mysql:8.0.33
LABEL "project"="vprofile"
LABEL "Author"="Derrick"

ENV MySQL_ROOT_PASSWORD="vprodbpass"
ENV MySQL_DATABASE="accounts"

ADD db_backup.sql docker-entrypoint-initdb/db_backup.sql
