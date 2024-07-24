ARG KC_VERSION

FROM quay.io/keycloak/keycloak:${KC_VERSION} as builder

ENV KC_HEALTH_ENABLED=true
ENV KC_METRICS_ENABLED=true
ENV KC_DB=postgres

WORKDIR /opt/keycloak
RUN /opt/keycloak/bin/kc.sh build

FROM quay.io/keycloak/keycloak:${KC_VERSION}
COPY --from=builder /opt/keycloak/ /opt/keycloak/

COPY certs/eurofish* /opt/truststore/
ENV KC_HTTPS_CERTIFICATE_FILE /opt/truststore/eurofish_com_ec.pem
ENV KC_HTTPS_CERTIFICATE_KEY_FILE /opt/truststore/eurofish.key
ENV KC_HOSTNAME_STRICT false

ENV TZ America/Guayaquil

ENTRYPOINT ["/opt/keycloak/bin/kc.sh"]
