FROM postgres:16.3-alpine3.20
ENV LANG en_EN.utf8
ENV POSTGRES_USER_FILE /run/secrets/postgres_user
ENV POSTGRES_PASSWORD_FILE /run/secrets/postgres_password
ENV POSTGRES_DB_FILE /run/secrets/postgres_db
ENV POSTGRES_INITDB_ARGS_FILE /run/secrets/postgres_initdb_args
ENV PGDATA=/var/lib/postgresql/data/pgdata

COPY init-user-db.sh /docker-entrypoint-initdb.d/init-user-db.sh

EXPOSE 5432
