### Installation Redis on K8s
```
https://bitnami.com/stack/redis/helm
https://artifacthub.io/packages/helm/bitnami-aks/redis/17.3.12
```

### Non HA implement (Dev/Test envs)
```
helm repo add bitnami-azure https://marketplace.azurecr.io/helm/v1/repo
helm repo update
helm -n demo install redis-crew azure-marketplace/redis --set auth.password=secretpassword --set replica.replicaCount=0
```
