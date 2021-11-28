# Docker-compose files for a simple uptodate
## InfluxDB2 + Grafana + Glances

.. image:: ../data/grafana-dashboard1.png

.. image:: ../data/grafana-dashboard2.png

Get the stack (only once):

```
git clone https://github.com/nicolargo/docker-influxdb2-grafana-glances.git
cd docker-influxdb2-grafana-glances
docker pull grafana/grafana
docker pull influxdb
docker pull glances
```

Run your stack:

```
sudo mkdir -p /srv/docker/influxdb2-grafana/grafana/data
sudo mkdir -p /srv/docker/influxdb2-grafana/influxdb2/data
docker-compose up -d
sudo chown -R 1000:1000 /srv/docker/influxdb2-grafana/grafana/data
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
docker pull glances
```

