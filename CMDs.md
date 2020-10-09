# Kubectl

## Inspecting a Pod's Status

### Get current status and event logs
```
kubectl desribe pods <pod-name> | grep <yaml-key-name> (e.g Status:)
```
### Get current lifecycle phase
```
kubectl get pods <pod-name> -o yaml
```
