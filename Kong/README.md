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

#### Aurora
```
$ kubectl apply -f https://raw.githubusercontent.com/svdang999/API_Gateways/main/Kong/aurora-kong-db-less.yaml
Warning: resource namespaces/kong is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be 
used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will be patched automatically.
namespace/kong configured
Warning: resource customresourcedefinitions/ingressclassparameterses.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/ingressclassparameterses.configuration.konghq.com configured
Warning: resource customresourcedefinitions/kongclusterplugins.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation 
will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/kongclusterplugins.configuration.konghq.com configured
Warning: resource customresourcedefinitions/kongconsumergroups.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation 
will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/kongconsumergroups.configuration.konghq.com configured
Warning: resource customresourcedefinitions/kongconsumers.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will 
be patched automatically.
customresourcedefinition.apiextensions.k8s.io/kongconsumers.configuration.konghq.com configured
Warning: resource customresourcedefinitions/kongingresses.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will 
be patched automatically.
customresourcedefinition.apiextensions.k8s.io/kongingresses.configuration.konghq.com configured
Warning: resource customresourcedefinitions/kongplugins.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required 
by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/kongplugins.configuration.konghq.com configured
Warning: resource customresourcedefinitions/tcpingresses.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/tcpingresses.configuration.konghq.com configured
Warning: resource customresourcedefinitions/udpingresses.configuration.konghq.com is missing the kubectl.kubernetes.io/last-applied-configuration annotation which is required by kubectl apply. kubectl apply should only be used on resources created declaratively by either kubectl create --save-config or kubectl apply. The missing annotation will be patched automatically.
customresourcedefinition.apiextensions.k8s.io/udpingresses.configuration.konghq.com configured
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

### Delete/Uninstall Kong
```
PS C:\Users\son.dang> kubectl delete -f https://raw.githubusercontent.com/svdang999/API_Gateways/main/Kong/aurora-kong-db-less.yaml
namespace "kong" deleted
customresourcedefinition.apiextensions.k8s.io "ingressclassparameterses.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "kongclusterplugins.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "kongconsumergroups.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "kongconsumers.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "kongingresses.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "kongplugins.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "tcpingresses.configuration.konghq.com" deleted
customresourcedefinition.apiextensions.k8s.io "udpingresses.configuration.konghq.com" deleted
serviceaccount "kong-serviceaccount" deleted
role.rbac.authorization.k8s.io "kong-leader-election" deleted
clusterrole.rbac.authorization.k8s.io "kong-ingress" deleted
clusterrole.rbac.authorization.k8s.io "kong-ingress-crds" deleted
clusterrole.rbac.authorization.k8s.io "kong-ingress-gateway" deleted
clusterrole.rbac.authorization.k8s.io "kong-ingress-knative" deleted
rolebinding.rbac.authorization.k8s.io "kong-leader-election" deleted
service "kong-admin" deleted
service "kong-proxy" deleted
service "kong-validation-webhook" deleted
deployment.apps "ingress-kong" deleted
deployment.apps "proxy-kong" deleted
ingressclass.networking.k8s.io "kong" deleted
```
