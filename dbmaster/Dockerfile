FROM postgres:13-alpine

RUN apk add --no-cache pwgen

USER postgres

# mountable storage
VOLUME /var/lib/postgresql/data

ENTRYPOINT ["entrypoint-wrapper.sh"]
CMD ["postgres"]

ADD docker-entrypoint-initdb.d /docker-entrypoint-initdb.d
COPY entrypoint-wrapper.sh /usr/local/bin/
