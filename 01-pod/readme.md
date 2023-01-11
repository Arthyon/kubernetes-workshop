# Steps

## Create pod

`kubectl apply -f main.yaml`

## Inspect logs in pod (stdout)

`kubectl logs my-pod`

## Get pod specification

`kubectl get pod my-pod -o yaml` (or `-o json`)

## Show details about the resource

`kubectl describe pod my-pod`

## Clean up

`kubectl delete -f main.yaml`

# Questions

- Can you run init routines before starting containers in a pod?
