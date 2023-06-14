# prometheus_grafana
## User manuals, packages

[telegraf]
<ol>plugin:
  https://github.com/influxdata/telegraf</ol>
[prometheus]
<ol>get_start:
  https://prometheus.io/docs/prometheus/latest/getting_started/
github:
  https://github.com/prometheus/prometheus</ol>


## PromQL
[filtering]
<ol><pre><code>ping_average_response_ms{service_name!='github'}
ping_average_response_ms{service_name='amazon',url='amazon.cn'}</code></pre></ol>

[filtering-with-regex]
<ol><pre><code>ping_average_response_ms{url=~"^amazon.*"}
ping_average_response_ms{url!~"^amazon.*"}
#double filtering
ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}
#filter by value
ping_average_response_ms{url=~"^amazon.*",url!~"amazon.com"}>50
</code></pre></ol>

[vector=range]
<ol><pre><code>net_bytes_recv[1m]
#calculate speed
rate(net_bytes_recv[1m])
#transform bytes to bit
rate(net_bytes_recv[1m])*8</code></pre></ol>
