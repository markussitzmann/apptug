FROM debian:stretch
LABEL maintainer="markussitzmann@gmail.com "

RUN apt-get update && apt-get -y --no-install-recommends install \
    ca-certificates \
    curl wget gosu sudo \
    gnupg \
    unzip tar bzip2 \
    git \
    postgresql-client
    
COPY docker-entrypoint.sh /
COPY ./appdock /opt/appdock

ENTRYPOINT ["/docker-entrypoint.sh"]