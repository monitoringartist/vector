# Netflix/vector

Vector is an on-host performance monitoring framework which exposes hand picked high resolution metrics to every engineer’s browser. https://github.com/Netflix/vector

Please donate to author, so he can continue to publish other awesome projects
for free:

[![Paypal donate button](http://jangaraj.com/img/github-donate-button02.png)]
(https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=8LB6J222WRUZ4)

# GitHub page

Just visit http://monitoringartist.github.io/vector/ and use it.

# Dockerized version

With [Caddy webserver](https://github.com/mholt/caddy) (recommended):
```
docker run \
  -d \
  --name vector \
  -p 80:80 \
  monitoringartist/vector:latest
```

With nginx (vector Docker image is only used as a volume only):

```
# start vector-storage
docker run  \
  -d \
  --name vector-storage \
  monitoringartist/vector:latest true
# start vector-nginx
docker run \
  -d \
  --name vector-nginx \
  --volumes-from vector-storage \
  -p 80:80 \
  nginx:latest
```

# Author

[Devops Monitoring Expert](http://www.jangaraj.com 'DevOps / Docker / Kubernetes / AWS ECS / Zabbix / Zenoss / Terraform / Monitoring'),
who loves monitoring systems, which start with letter Z. Those are Zabbix and Zenoss.

Professional devops / monitoring services:

[![Monitoring Artist](http://monitoringartist.com/img/github-monitoring-artist-logo.jpg)]
(http://www.monitoringartist.com 'DevOps / Docker / Kubernetes / AWS ECS / Zabbix / Zenoss / Terraform / Monitoring')
