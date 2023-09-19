## Deploy Kong dbless mode
```
kubectl apply -f https://github.com/svdang999/API_Gateways/blob/main/Kong/kong-db-less.yaml
```
### Example
```
PS C:\Users\son.dang> kubectl apply -f https://raw.githubusercontent.com/Kong/kubernetes-ingress-controller/master/deploy/sin
gle/all-in-one-dbless.yaml
namespace/kong created
customresourcedefinition.apiextensions.k8s.io/ingressclassparameterses.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/kongclusterplugins.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/kongconsumergroups.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/kongconsumers.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/kongingresses.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/kongplugins.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/tcpingresses.configuration.konghq.com created
customresourcedefinition.apiextensions.k8s.io/udpingresses.configuration.konghq.com created
serviceaccount/kong-serviceaccount created
role.rbac.authorization.k8s.io/kong-leader-election created
clusterrole.rbac.authorization.k8s.io/kong-ingress created
clusterrole.rbac.authorization.k8s.io/kong-ingress-crds created
clusterrole.rbac.authorization.k8s.io/kong-ingress-gateway created
clusterrole.rbac.authorization.k8s.io/kong-ingress-knative created
rolebinding.rbac.authorization.k8s.io/kong-leader-election created
clusterrolebinding.rbac.authorization.k8s.io/kong-ingress created
clusterrolebinding.rbac.authorization.k8s.io/kong-ingress-crds created
clusterrolebinding.rbac.authorization.k8s.io/kong-ingress-gateway created
clusterrolebinding.rbac.authorization.k8s.io/kong-ingress-knative created
service/kong-admin created
service/kong-proxy created
service/kong-validation-webhook created
deployment.apps/ingress-kong created
deployment.apps/proxy-kong created
ingressclass.networking.k8s.io/kong created
```
