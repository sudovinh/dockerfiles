FROM mysql:5.6

ENV MYSQL_DATABASE=databasename \
    MYSQL_USER=dbuser \
    MYSQL_PASSWORD=userpassword \
    MYSQL_ROOT_PASSWORD=12345

ADD yourdatabase.sql /docker-entrypoint-initdb.d/yourdatabase.sql
