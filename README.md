# httpbin-chart

Using k3s helmchart resource:

```
apiVersion: k3s.cattle.io/v1
kind: HelmChart
metadata:
  name: httpbin
  namespace: kube-system
spec:
  targetNamespace: default
  chart: https://nhtzr.github.io/httpbin-chart/httpbin-0.1.0.tgz
  valuesContent: |-
    ingress:
      enabled: true
      annotations:
        kubernetes.io/ingress.class: traefik
```

