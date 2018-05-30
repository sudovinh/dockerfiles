### MySQL Server docker

# Throwaway MySQL Docker Server
- Change settings in the docker file as needed
   - FROM mysql:5.6 ( depending on version of the sql database, please use the same version similar to your database.)
   - ENV MYSQL_DATABASE=database name \
       MYSQL_USER=database user \
       MYSQL_PASSWORD=database user pw\
       MYSQL_ROOT_PASSWORD=12345
   - ADD yourdatabase.sql(in the same folder with this dockerfile) /docker-entrypoint-initdb.d/yourdatabase.sql


# Build and Run
- `docker build -t mysqlserver` .
- `docker run -d --name mysqlserver --rm mysqlserver`

# MySQL server docker info
- mysql server port 3306 open
- Find the ip address of your sqlserver docker
  - `docker inspect mysqlserver`
     - "IPAddress": "172.17.0.2", something similar to this
- mysqlserver host: 172.17.0.2:3306
