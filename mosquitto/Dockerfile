ARG MOSQUITTO_VERSION
FROM eclipse-mosquitto:${MOSQUITTO_VERSION}

COPY mosquitto.conf /mosquitto/config/mosquitto.conf
COPY docker-entrypoint.sh /

ENV TZ America/Guayaquil

ENTRYPOINT ["sh", "./docker-entrypoint.sh"]

CMD ["/usr/sbin/mosquitto", "-c", "/mosquitto/config/mosquitto.conf"]