# Docker-compose files for a simple uptodate
# InfluxDB
# + Grafana stack

Get the stack (only once):

```
git clone https://github.com/emonindonesia/docker-influxdb-grafana && cd docker-influxdb-grafana

```

Run your stack:

```
docker run docker/compose:1.24.0 version

docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v "$PWD:$PWD" -w="$PWD" docker/compose:1.24.0 up -d

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

