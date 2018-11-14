## docker-cleanup

Cleans up exited containers and dangling images/volumes running as a DaemonSet (`docker-clean.yml`).

### Env
In the DaemonSet (`docker-clean.yml`) you can set `DOCKER_CLEAN_INTERVAL` to modify the interval when it cleans up exited containers and dangling images/volumes; defaults to 30min (1800s).

### Deployment

```
kubectl --context CONTEXT -n kube-system apply -f rbac.yml
kubectl --context CONTEXT -n kube-system apply -f docker-clean.yml
```
