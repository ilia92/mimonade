# Mining Monitoring Prometheus Advertiser - MiMonAd-e

## What this script does:
1. Monitoring mining rigs, trough the HiveOS API
   - up/down
   - hash
   - power statistics (current, voltage, etc) using [Tasmota](https://tasmota.github.io/docs/About/) flashed on [Sonoffs](https://sonoff.tech/product/diy-smart-switch/powr2/) (mainly POW R2)
3. Converting to PromQL (Prometheus) and advertising data trough a build-in, basic web server - Real time
