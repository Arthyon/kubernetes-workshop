# Steps

## Create deployment

`kubectl apply -f main.yaml`

## Get deployment info

`kubectl get deployment my-deployment`

## Change replicas

- Change `replicas` to something else
- `kubectl apply -f main.yaml`
- `kubectl get deployment my-deployment`

## Delete pod

- `kubectl delete pod <pod-name>`
- Verify that a new pod is created

## Clean up

`kubectl delete -f main.yaml`

# Questions

- Is there a way to auto scale pods based on metrics?
