```
kubectl config set-cluster workshop --insecure-skip-tls-verify=true --server https://<replace>
kubectl config set-credentials bkwi-admin --username <username> --password <password>
kubectl config set-context workshop --cluster workshop --user <username>
kubectl config use-context workshop

# To verify:
kubectl get node
```

Run your image on Kubernetes:
```
$ kubectl run my-website --image eu.gcr.io/pur-owit-playground/bkwi:lab01
```


Port-forward to your deployment
` $ kubectl port-forward my-website-<randomid> 9000:80`


```
$ kubectl set image deployment my-website *=eu.gcr.io/pur-owit-playground/bkwi:lab02
$ # Escape the asterisk if you need to
$ kubectl set image deployment my-website \*=eu.gcr.io/pur-owit-playground/bkwi:lab02
```
