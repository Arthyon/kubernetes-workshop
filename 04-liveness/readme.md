# Steps

## Create resources

`kubectl apply -f main.yaml`

## Check that pod runs

`kubectl get pod liveness-exec`

## Remove /tmp/healthy-file

- `kubectl exec -it liveness-exec -- /bin/sh`
- `rm /tmp/healthy`

## Check that pod is considered unhealthy

- `kubectl describe pod liveness-exec`
- `kubectl get pod liveness-exec` and watch restart count

## Clean up

`kubectl delete -f main.yaml` (add `--force` if this takes a long time)

# Questions

- What other types of probes can be used, and for what purpose?
