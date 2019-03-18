1. Create the dashboard

```
kubectl apply -f https://raw.githubusercontent.com/kubernetes/dashboard/v1.10.1/src/deploy/recommended/kubernetes-dashboard.yaml
```


Create an additional admin service account
```
kubectl apply -f  dashboard-service-account.yml

```

Get a token to logon
```
kubectl -n kube-system describe secret $(kubectl -n kube-system get secret | grep admin-user | awk '{print $1}')
```

Startup a proxy
```
kubectl proxy
```


Open up the dashboard
```
http://localhost:8001/api/v1/namespaces/kube-system/services/https:kubernetes-dashboard:/proxy/
```



