# Kubectl

## Shortcuts

### Use an Alias for kubectl
```
alias k=kubectl
```
### Setting a Context & Namespace
```
kubectl config set-context <context-of-question> --namespace=<namespace-of question>
```
### Resource Short Names

#### Usage of ns instead of namespaces
```
kubectl get ns
```
#### Usage of pvc instead of persistenvolumeclaim
```
kubectl describe pvc claim
```
### Killing Kubernetes Objects
```
kubectl delete pod <pod-name> --grace-period=0 --force
```
### Finding Object Information - grep is your friend!

#### Get pods contextual information based on number of lines and text
```
kubectl describe pods | grep -C 10 "author=John Doe"
```
```
kubectl get pods -o yaml | grep -C 5 labels:
```


## Inspecting a Pod's Status

### Get current status and event logs
```
kubectl desribe pods <pod-name> | grep <yaml-key-name> (e.g Status:)
```
### Get current lifecycle phase
```
kubectl get pods <pod-name> -o yaml
```
