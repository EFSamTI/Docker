ARG GF_VERSION

FROM grafana/grafana-oss:${GF_VERSION}

COPY ./certs/eurofish* /etc/certs/

ENV GF_SERVER_CERT_KEY=/etc/certs/eurofish.key
ENV GF_SERVER_CERT_FILE=/etc/certs/eurofish_com_ec.pem
ENV TZ America/Guayaquil