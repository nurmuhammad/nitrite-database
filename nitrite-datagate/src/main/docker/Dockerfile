FROM openjdk:8-jdk-alpine
VOLUME /tmp
VOLUME /logs
COPY ./nitrite-datagate.jar /
COPY ./datagate.properties /
COPY ./datagate.sh /

ENV JAVA_OPTS "$JAVA_OPTS -Drun.mode=docker -Djava.security.egd=file:/dev/./urandom"
# log settings
ENV DATAGATE_LOG_FILE "/logs/datagate.log"

ENV DATAGATE_SYNC_LOG_CLEANUP_DELAY "30"  #days

## Configure below environment variables
#ENV DATAGATE_HOST ""
#ENV DATAGATE_HTTP_PORT ""
#ENV DATAGATE_HTTPS_PORT ""
#ENV DATAGATE_MONITOR_PORT ""
#ENV DATAGATE_KEY_STORE ""
#ENV DATAGATE_KEY_PASSWORD ""

## mongo connection details
#ENV DATAGATE_MONGO_HOST ""
#ENV DATAGATE_MONGO_PORT ""
#ENV DATAGATE_MONGO_USER ""
#ENV DATAGATE_MONGO_PASSWORD ""
#ENV DATAGATE_MONGO_DATABASE ""

#ENTRYPOINT [ "./datagate.sh" ]