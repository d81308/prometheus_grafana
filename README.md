# prometheus-setup objectives
for testing net over 2000 case alerting

# Simulation server down
<pre><code> # stop host1 server
  docker stop host1
</code></pre>

# Simulation over loading
<pre><code># use docker sh
docker ps
docker exec -it host1 sh
# into host1 sh
ping telegraf
# if need more loading
ping telegraf -s 1024</code></pre>
