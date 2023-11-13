FROM postgres:latest
ENV POSTGRES_PASSWORD=1tdata
ENV POSTGRES_USER=1tdata
ENV POSTGRES_DB=1tdata
COPY init_scripts/init.sql /docker-entrypoint-initdb.d/init.sql
