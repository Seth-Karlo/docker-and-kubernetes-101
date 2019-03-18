These are the commands. See the screen / deck for more info

```
kubectl config set-cluster workshop --insecure-skip-tls-verify=true --server https://<replace>
kubectl config set-credentials bkwi-admin --username <username> --password <password>
kubectl config set-context workshop --cluster workshop --user <username>
kubectl config use-context workshop

kubectl get node
```

