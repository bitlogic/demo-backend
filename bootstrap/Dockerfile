FROM alpine:edge

ARG COMPOSE_VER=1.9.0

RUN apk add -U python \
            py-setuptools \
            py2-pip \
    && pip install docker-compose==${COMPOSE_VER} \
    && apk del py-pip \
    && rm -rf /var/cache/apk/*

WORKDIR /demo
ENTRYPOINT ["docker-compose"]
CMD ["up", "-d"]

ADD docker-compose*  /demo/

