# telegraf-prometheus-grafana-basic
Installed and config prometheus

>Containers
  >telegraf
    >port=9273:9273
  >prometheus
    >port=9090:9090
  
[Data source listening]
  telegraf:9273
  [monitoring-by-prometheus]
    job="sourcer-telegraf"
    targets="telegraf:9273"
