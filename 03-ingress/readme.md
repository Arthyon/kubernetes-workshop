# Steps

## Enable ingress addon

- `minikube addons enable ingress`
- When using Docker desktop, create a tunnel in a separate window: `minikube tunnel`

## Create resources

- `kubectl apply -f main.yaml`

## Wait until ingress has address

- `kubectl get ingress --watch`

## Test requests

(for docker desktop, replace <ip> with `localhost`)

- `curl http://<ip>/foo`
- `curl http://<ip>/bar`

TIP: To strip prefix before forwarding using nginx ingress, add this metadata to the ingress definition:

```yaml
annotations:
  nginx.ingress.kubernetes.io/rewrite-target: /
```

## Clean up

`kubectl delete -f main.yaml`

# Questions

- Which alternatives to ingresses can be used to expose a service?
