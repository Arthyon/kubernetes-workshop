# Steps

## Create resources

`kubectl apply -f main.yaml`

## Verify that cronjob runs

`kubectl get cronjobs` and look at `LAST SCHEDULE`

## Check created jobs

- `kubectl get jobs`
- Verify that only the configured amount of jobs are kept

## Check log output of a job

`kubectl logs <pod name>`

Pod name is `<job-name>-<random suffix>`

## Clean up

`kubectl delete -f main.yaml`

# Questions

- Why should jobs started by cronjobs be idempotent?
