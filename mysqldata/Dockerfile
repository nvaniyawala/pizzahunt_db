# Derived from official mysql image (our base image)
FROM mysql/mysql-server:latest
# Add a database
ENV MYSQL_DATABASE order_delivery_sys
ENV MYSQL_ROOT_PASSWORD root
# Add the content of the sql-scripts/ directory to your image
# All scripts in docker-entrypoint-initdb.d/ are automatically
# executed during container startup
COPY order_delivery_sys.sql /docker-entrypoint-initdb.d/
ADD grant.sql /docker-entrypoint-initdb.d