### Helm install syntax
```
helm repo add wiremind https://wiremind.github.io/wiremind-helm-charts
helm repo update
helm install cerebro-test wiremind/cerebro --version 2.0.3 -f custom-values.yaml
```
