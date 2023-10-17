### Ref
```
https://github.com/doitintl/kube-no-trouble#install
```

###
```
root@T2P-CPU016:~# sh -c "$(curl -sSL https://git.io/install-kubent)"
>>> kubent installation script <<<
> Detecting latest version
> Downloading version 0.7.0
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100 11.9M  100 11.9M    0     0   940k      0  0:00:13  0:00:13 --:--:--  990k
> Done. kubent was installed to /usr/local/bin/.

root@T2P-CPU016:~# kubent 
10:38AM INF >>> Kube No Trouble `kubent` <<<
10:38AM INF version 0.7.0 (git sha d1bb4e5fd6550b533b2013671aa8419d923ee042)
10:38AM INF Initializing collectors and retrieving data
10:38AM INF Target K8s version is 1.22.11
10:38AM INF Retrieved 147 resources from collector name=Cluster
10:38AM INF Retrieved 55 resources from collector name="Helm v3"
10:38AM INF Loaded ruleset name=custom.rego.tmpl
10:38AM INF Loaded ruleset name=deprecated-1-16.rego
10:38AM INF Loaded ruleset name=deprecated-1-22.rego
10:38AM INF Loaded ruleset name=deprecated-1-25.rego
10:38AM INF Loaded ruleset name=deprecated-1-26.rego
10:38AM INF Loaded ruleset name=deprecated-future.rego
__________________________________________________________________________________________
>>> Deprecated APIs removed in 1.25 <<<
------------------------------------------------------------------------------------------
KIND                  NAMESPACE     NAME                 API_VERSION      REPLACE_WITH (SINCE)
PodDisruptionBudget   kube-system   coredns-pdb          policy/v1beta1   policy/v1 (1.21.0)
PodDisruptionBudget   kube-system   konnectivity-agent   policy/v1beta1   policy/v1 (1.21.0)
```
