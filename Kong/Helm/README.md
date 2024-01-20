Install Kong DBLess with Helm

Ref
```
https://github.com/Kong/charts/blob/main/charts/kong/values.yaml
```

Steps install
```
helm repo add kong https://charts.konghq.com
helm repo update
helm -n kong-infra-dev list
helm -n kong-infra-dev install kong-dev kong/kong -f https://github.com/svdang999/API_Gateways/raw/main/Kong/Helm/kong-3.5-values.yaml
```

Example
```
root@HNCWIN11:~/tmp# helm -n kong-infra-dev install kong-dev kong/kong -f https://github.com/svdang999/API_Gateways/raw/main/Kong/Helm/kong-3.5-values.yaml
NAME: kong-dev
LAST DEPLOYED: Sat Jan 20 17:34:39 2024
NAMESPACE: kong-infra-dev
STATUS: deployed
REVISION: 1
TEST SUITE: None
NOTES:
To connect to Kong, please execute the following commands:

HOST=$(kubectl get svc --namespace kong-infra-dev kong-dev-kong-proxy -o jsonpath='{.status.loadBalancer.ingress[0].ip}')
PORT=$(kubectl get svc --namespace kong-infra-dev kong-dev-kong-proxy -o jsonpath='{.spec.ports[0].port}')
export PROXY_IP=${HOST}:${PORT}
curl $PROXY_IP

Once installed, please follow along the getting started guide to start using
Kong: https://docs.konghq.com/kubernetes-ingress-controller/latest/guides/getting-started/

WARNING: Kong Manager will not be functional because the Admin API is not
enabled. Setting both .admin.enabled and .admin.http.enabled and/or
.admin.tls.enabled to true to enable the Admin API over HTTP/TLS.
```
