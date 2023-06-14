# prometheus_grafana
### user manuals, packages

[telegraf]
plugin:
  https://github.com/influxdata/telegraf

[prometheus]
get_start:
  https://prometheus.io/docs/prometheus/latest/getting_started/
github:
  https://github.com/prometheus/prometheus


# PromQL
[filtering]
ping_average_response_ms{service_name!='github'}
ping_average_response_ms{service_name='amazon',url='amazon.cn'}

[filtering-with-regex]
ping_average_response_ms{url=~"^amazon.*"}
ping_average_response_ms{url!~"^amazon.*"}
#double filtering
ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}
#filter by value
ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}>50

[vector=range]
net_bytes_recv[1m]
# calculate speed
rate(net_bytes_recv[1m])
# transform bytes to bit
rate(net_bytes_recv[1m])*8
