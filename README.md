# Docker-compose files for a simple InfluxDB & Grafana stack

The instructions are specifically for a GCE instance with a Container Optimized OS.

InfluxDB is this simple configuration is not password protected. Grafana user/pass starts with admin/admin 


1. Get the stack:

```
git clone https://github.com/emonindonesia/docker-influxdb-grafana && cd docker-influxdb-grafana

```

2. Install docker-compose:

```
docker run docker/compose:1.24.0 version

```

3. Run your stack:

```

docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v "$PWD:$PWD" -w="$PWD" docker/compose:1.24.0 up -d

```

Show me the logs:

```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v "$PWD:$PWD" -w="$PWD" docker/compose:1.24.0 logs
```

Stop it:

```
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v "$PWD:$PWD" -w="$PWD" docker/compose:1.24.0 stop
docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v "$PWD:$PWD" -w="$PWD" docker/compose:1.24.0 rm
```

Update it:

```
git pull
docker pull grafana/grafana
docker pull influxdb

```

