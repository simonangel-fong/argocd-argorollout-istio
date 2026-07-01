
canary

```sh
kubectl argo rollouts promote backend -n backend



watch -n 1 'for i in {1..10}; do curl -sk https://deploy.arguswatcher.net/api/; echo; done'
```