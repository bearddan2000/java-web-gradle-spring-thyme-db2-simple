# FROM gradle:jdk11

FROM alpine:edge

WORKDIR /app

COPY bin .

ENV WAIT_VERSION 2.7.2

RUN apk update \
    && apk add gradle

ADD https://github.com/ufoscout/docker-compose-wait/releases/download/$WAIT_VERSION/wait /wait

RUN chmod +x /wait

ENTRYPOINT ["gradle"]

CMD ["bootRun"]