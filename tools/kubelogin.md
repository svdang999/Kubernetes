#(Ubuntu WSL 22.04) kubelogin tool installed
```
https://aptakube.com/blog/how-to-use-azure-kubelogin
```

#1 Download the package
```
mkdir kubelogin && cd kubelogin
wget https://github.com/Azure/kubelogin/releases/download/v0.0.31/kubelogin-linux-amd64.zip
unzip kubelogin-linux-amd64.zip
```

#2 Add kubelogin shortcut to $PATH
```
ln -s /root/kubelogin/bin/linux_amd64/kubelogin /usr/bin/kubelogin
source ~/.bashrc
```

#3 convert the target AAD enabled clusters kubectl authentication method to Azure CLI
```
kubelogin convert-kubeconfig -l azurecli
cat ~/.kube/config
```


#4 Login to cluster
```
az login
az account set --subscription "Microsoft Partner Network"
az aks get-credentials --resource-group rg-infra-son-test --name aks-infra-dev
kubectl get ns
```
