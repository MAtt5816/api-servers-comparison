FROM mysql:9.0
COPY db.sql /docker-entrypoint-initdb.d/

# set charset
RUN echo "[mysqld]\ncharacter-set-server=utf8mb4\ncollation-server=utf8mb4_unicode_ci" > /etc/mysql/conf.d/charset.cnf

EXPOSE 3306
