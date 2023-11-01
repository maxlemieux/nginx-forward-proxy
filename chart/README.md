# About

Helm chart for [hinata/nginx-forward-proxy](https://github.com/hinata/nginx-forward-proxy).

Forwarding proxy for testing Kubernetes applications.

# Install

Clone the repo:

```
git clone git@github.com:maxlemieux/nginx-forward-proxy.git
```

Install the chart:

```
cd nginx-forward-proxy/chart
helm install -n nginx hinata-nginx-forward-proxy . -f values.yaml --create-namespace
```

Test the proxy from a container in the cluster, with:
```
curl -x http://nginx-forward-proxy.nginx.svc:80 http://example.com
curl -x http://nginx-forward-proxy.nginx.svc:80 https://example.com
```
