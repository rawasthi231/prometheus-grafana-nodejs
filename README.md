# Prometheus - Grafana - NodeJS

## Prometheus

```
docker run --rm -p 9090:9090 \
-v `pwd`/prometheus.yml:/etc/prometheus/prometheus.yml \
prom/prometheus:v2.20.1
```


## Grafana

```
docker run --rm -p 3000:3000 \
  -e GF_AUTH_DISABLE_LOGIN_FORM=true \
  -e GF_AUTH_ANONYMOUS_ENABLED=true \
  -e GF_AUTH_ANONYMOUS_ORG_ROLE=Admin \
  -v `pwd`/datasources.yml:/etc/grafana/provisioning/datasources/datasources.yml \
  grafana/grafana:7.1.5
```