

# Visualization

```sh
# kiali
kubectl -n istio-system port-forward svc/kiali 20001:20001
# open http://localhost:20001

# grafana
kubectl -n istio-system port-forward svc/grafana 3000:3000
```


canary

```sh
kubectl argo rollouts promote backend -n backend


while true; do
  curl -sk https://deploy.arguswatcher.net/api/ > /dev/null
  sleep 0.5
done

watch -n 1 'for i in {1..10}; do curl -sk https://deploy.arguswatcher.net/api/; echo; done'
```