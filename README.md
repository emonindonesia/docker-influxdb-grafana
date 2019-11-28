# Docker-compose files for a simple uptodate
# InfluxDB
# + Grafana stack

Get the stack (only once):

```
git clone https://github.com/emonindonesia/gke-influxdb-grafana
cd docker-influxdb-grafana
docker pull grafana/grafana
docker pull influxdb

```

Run your stack:

```
sudo mkdir -p /srv/docker/grafana/data
docker-compose up -d
sudo chown -R 472:472 /srv/docker/grafana/data

```

Show me the logs:

```
docker-compose logs
```

Stop it:

```
docker-compose stop
docker-compose rm
```

Update it:

```
git pull
docker pull grafana/grafana
docker pull influxdb

```

