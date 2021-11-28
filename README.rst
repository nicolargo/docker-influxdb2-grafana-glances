InfluxDB2 + Grafana + Glances stack
===================================

.. image:: https://raw.githubusercontent.com/nicolargo/docker-influxdb2-grafana-glances/main/data/grafana-dashboard1.png

.. image:: https://raw.githubusercontent.com/nicolargo/docker-influxdb2-grafana-glances/main/data/grafana-dashboard2.png

Get the stack (only once):

.. code-block:: console

    git clone https://github.com/nicolargo/docker-influxdb2-grafana-glances.git
    cd docker-influxdb2-grafana-glances
    docker pull grafana/grafana
    docker pull influxdb
    docker pull glances

Run your stack:

.. code-block:: console

    sudo mkdir -p /srv/docker/influxdb2-grafana/grafana/data
    sudo mkdir -p /srv/docker/influxdb2-grafana/influxdb2/data
    docker-compose up -d
    sudo chown -R 1000:1000 /srv/docker/influxdb2-grafana/grafana/data

Show me the logs:

.. code-block:: console

    docker-compose logs

Stop it:

.. code-block:: console

    docker-compose stop
    docker-compose rm

Update it:


.. code-block:: console

    git pull
    docker pull grafana/grafana
    docker pull influxdb
    docker pull glances
