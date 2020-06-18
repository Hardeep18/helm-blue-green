# helm-blue-green
Blue Green deployment using Helm

Deploy blue version (1.10)

```
helm install --dry-run --debug ./blue-green --generate-name
helm install blue ./blue-green --set service.type=NodePort
```
Deploy updated version (1.11) - green

```
change version from chart.yaml 
# 1.10 to 1.11 #
```

Apply chnages 
```
helm upgrade blue ./blue-green
```