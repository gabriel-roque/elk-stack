ARG ELK_VERSION

FROM docker.elastic.co/apm/apm-server:${ELK_VERSION}

WORKDIR /usr/share/apm-server/

COPY config/apm-server.yml /usr/share/apm-server/apm-server.yml

USER root

RUN chmod go-w /usr/share/apm-server/apm-server.yml

USER apm-server