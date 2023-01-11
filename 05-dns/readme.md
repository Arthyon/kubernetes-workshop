# Steps

## Create resources

`kubectl apply -f main.yaml`

## Send request from host pod to target service

- `kubectl exec -it host -- /bin/sh`
- `curl http://target-service.default.svc.cluster.local:8080` OR `curl http://target-service:8080` (when in same namespace)

## Clean up

`kubectl delete -f main.yaml` (add `--force` if this takes a long time)

# Questions

- Are there other service discovery mechanisms worth exploring?
