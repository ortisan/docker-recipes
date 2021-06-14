FROM adoptopenjdk/openjdk11:jdk-11.0.10_9-alpine

RUN apk add --no-cache --update supervisor curl busybox-extras && \
    mkdir -p /var/log/supervisor && \
    mkdir -p /etc/supervisor/conf.d

WORKDIR '/app'
COPY apps/hello-app.jar ./hello-app.jar
COPY apps/world-app.jar ./world-app.jar

COPY wrapper_script.sh ./wrapper_script.sh

EXPOSE 8080
EXPOSE 8081


HEALTHCHECK CMD curl --fail http://localhost:8080/actuator/health && http://localhost:8081/actuator/health || exit 1

CMD ["sh", "./wrapper_script.sh"]