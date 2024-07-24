## Services
+ zookeeper
+ kafka-broker
+ postgres
+ keycloak
+ entities
+ core
+ dynamic-view
+ dummy
+ cadvisor
+ prometheus
+ grafana
+ elasticsearch
+ logstash
+ kibana
+ kafka-connect

## .env
```
POSTGRES_VERSION=15.7-alpine

KC_DB_PASSWORD=

KC_VERSION=25.0.1
# The link that will be used by the Grafana to redirect to the Keycloak
#KC_HOSTNAME=https://
KC_HOSTNAME=integrador.eurofish.com.ec
KC_PORT=8443
KC_REALM_NAME=grafana
KC_LOG_LEVEL=INFO
KEYCLOAK_ADMIN=admin
KEYCLOAK_ADMIN_PASSWORD=

PROMETHEUS_VERSION=v2.53.0
PROMETHEUS_PORT=9090

GF_VERSION=11.0.0
GF_LOG_LEVEL=info
GF_SERVER_HTTP_PORT=3000
GF_HOSTNAME=integrador.eurofish.com.ec
GF_ADMIN_USERNAME=admin
GF_ADMIN_PASSWORD=

PG_URL=postgresql://192.168.248.245:5432/eurofish
PG_USER=postgres
PG_PWD=3uR0F15h
MONGO_URL=mongodb://eurofish:3uR0F15h@192.168.248.245:27017
MONGO_DB=eurofish
MQTT_HOST=192.168.248.245
MQTT_PORT=1883
MQTT_PASSWD=
MQTT_USER=mosquitto
OIDC_SERVER_URL=https://integrador.eurofish.com.ec:8443/realms/EU-AUTH-SERVER-DEV
OIDC_CLIENT_ID=EU-BACKEND-MIDDLEWARE
OIDC_CLIENT_SECRET=4U6v3tByuEKCOgU0GUgnkYWqLYvWpzpZ
OIDC_TRUST_STORE_FILE=/deployments/certs/eurofish_com_ec.pfx
OIDC_TRUST_STORE_PWD=eurofish
CERT_FILE=/deployments/certs/eurofish_com_ec.pem
CERT_KEY=/deployments/certs/eurofish.key

PG_USERNAME=bi
PG_PASSWORD=
PG_URL=postgresql://154.38.178.139:5432/inventario
```