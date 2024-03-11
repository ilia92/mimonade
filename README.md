# Mining Monitoring and exporter - MiMonade
Exporting mining data as Prometheus readable Metrics using buildt-in basic web-server 

## What this script does:
1. Monitoring mining rigs, trough the HiveOS API
   - up/down
   - hash
2. Monitor power statistics (current, voltage, etc) using [Tasmota](https://tasmota.github.io/docs/About/) flashed on [Sonoffs](https://sonoff.tech/product/diy-smart-switch/powr2/) (mainly POW R2)
3. Converting to Prometheus-readable metrics
4. Delivering a webpage (when requested), using built-in basic webserver (netcat used)

![Example](https://github.com/ilia92/Mimonade/blob/main/Grafana/grafana_example.png)

## To add as a service do:

Edit ExecStart in mimonade.service according to your paths:

```vim mimonade.service```

Then:
```
cp -rp mimonade.service /etc/systemd/system
sudo systemctl daemon-reload
sudo systemctl start mimonade.service
sudo systemctl enable mimonade.service
sudo systemctl status mimonade.service
```
