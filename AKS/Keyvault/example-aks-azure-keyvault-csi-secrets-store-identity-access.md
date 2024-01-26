### Deployment
```
root@HNCWIN11:~# kubectl apply -f https://raw.githubusercontent.com/svdang999/Kubernetes/main/AKS/example-csi-secrets-store-identity-access.yaml
secretproviderclass.secrets-store.csi.x-k8s.io/azure-kvname-user-msi created

root@HNCWIN11:~# kubectl apply -f https://raw.githubusercontent.com/svdang999/Kubernetes/main/AKS/example-csi-secrets-store-identity-access-pod.yaml
pod/busybox-secrets-store-inline-user-msi created
```

### Check results
```
/ # ls /mnt/secrets-store/
default

/ # cat /mnt/secrets-store/default
MyAKSExampleSecret/ #
```
