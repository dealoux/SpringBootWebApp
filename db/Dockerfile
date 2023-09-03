FROM postgres

ENV POSTGRES_PASSWORD=postgres
ENV POSTGRES_USER=postgres

WORKDIR /docker-entrypoint.initdb.d
ADD db/schema.sql .
ADD db/data.sql .

EXPOSE 5432