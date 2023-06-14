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
net_bytes_recv[1m]
- calculate speed
rate(net_bytes_recv[1m])
- transform bytes to bit
rate(net_bytes_recv[1m])*8

<ul>
<li>Bird</li>
<li>Magic</li>
</ul>

<ul>Title1
<li><p>Bird</p></li>
<li><p>Magic</p></li>
</ul>

<p>Here is an example of AppleScript:</p>

<pre><code>tell application "Foo"
    beep
end tell
</code></pre>
