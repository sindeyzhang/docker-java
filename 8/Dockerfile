FROM openjdk:8-jdk-alpine

ENV TZ=Asia/Shanghai
RUN set -eux; \
    apk add --no-cache --update tzdata; \
    ln -snf /usr/share/zoneinfo/$TZ /etc/localtime; \
    echo $TZ > /etc/timezone

RUN set -eux; \
    addgroup --gid 1000 java-app; \
    adduser -S -u 1000 -g appuser -h /home/java-app/ -s /bin/sh -D appuser;
