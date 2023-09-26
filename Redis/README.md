### Installation Redis on K8s
```
https://bitnami.com/stack/redis/helm
https://artifacthub.io/packages/helm/bitnami-aks/redis/17.3.12
```

```
helm repo add azure-marketplace
helm -n demo install redis-crew azure-marketplace/redis --set auth.password=secretpassword
```
