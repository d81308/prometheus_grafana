# prometheus_grafana
### user manuals, packages

[telegraf]
plugin:
  https://github.com/influxdata/telegraf
<br />
[prometheus]
get_start:
  https://prometheus.io/docs/prometheus/latest/getting_started/
  <br />
github:
  https://github.com/prometheus/prometheus


# PromQL
[filtering]
<ol>ping_average_response_ms{service_name!='github'}
ping_average_response_ms{service_name='amazon',url='amazon.cn'}</ol>
<br />

[filtering-with-regex]
ping_average_response_ms{url=~"^amazon.*"}
ping_average_response_ms{url!~"^amazon.*"}
<ol>double filtering
</ol>
<br />
  ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}
- filter by value
ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}>50
<br />

[vector=range]
net_bytes_recv[1m]
- calculate speed
rate(net_bytes_recv[1m])
- transform bytes to bit
rate(net_bytes_recv[1m])*8
