# Steps

## Create resources

`kubectl apply -f main.yaml`

## Check that configuration is present in container

- `kubectl exec -it config-test -- /bin/sh`
- `echo $TEST1`
- `echo $TEST2`
- `cat config.yaml`

## Clean up

`kubectl delete -f main.yaml` (add `--force` if this takes a long time)

# Questions

- How are `secrets` related to config maps?
