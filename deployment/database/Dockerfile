FROM postgres:alpine
# TODO: The Postgres image limits permissions for the initializtion scripts.
#       Therefore, if you need to fetch any external resources,
#       install packages or run other system commands,
#       you must do so here at build time.
RUN apk update && apk --no-cache add curl
WORKDIR /docker-entrypoint-initdb.d
RUN curl -L -o instance.tsv https://www.dropbox.com/s/pa717g92x8pij49/instance.tsv?dl=1
