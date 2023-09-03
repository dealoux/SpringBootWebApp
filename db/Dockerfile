#STAGE 1 - runtime
FROM postgres as runtime_init
ENV POSTGRES_PASSWORD=postgres
#ADD db/scripts/schema.sql db/scripts/data.sql /docker-entrypoint.initdb./

##STAGE 2 - initialize the database during the build
#FROM runtime_init AS buildtime_init_builder
#RUN echo "exit 0" > /docker-entrypoint-initdb.d/100-exit_before_boot.sh
#WORKDIR /var/lib/postgresql/data/
#RUN docker-entrypoint.sh postgres
#
## STAGE 3 - Copy the initialized db to a new image to reduce size.
#FROM postgres AS buildtime_init
#WORKDIR /var/lib/postgresql/data/
#COPY --chown=postgres:postgres --from=buildtime_init_builder . .
#EXPOSE 5432