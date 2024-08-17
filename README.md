# k8s-commands
### Start minikube
```minikube start```
### Load docker image
```
docker image save -o <sample-service.tar> <sample-service:latest>
```

```minikube image load <sample-service.tar>```
## Pods
### Get all pods
```minikube kubectl -- get pods -A```
### Describe pod 
```kubectl describe pod <pod-name> -n <namespace>```
### Exec pod
```kubectl exec -it <pod-name> -- /bin/bash```
### Delete pod
```kubectl delete pod <pod-name>```
### Access direct to pod's port
```kubectl port-forward pod/<pod-name> <local>:<pod-port>```
## Service
### Apply
```kubectl apply -f <service-file.yaml>```
### Delete
```kubectl delete -f <service-file.yaml>```
### Get
```kubectl get service <service-name>```
### Get service running info
```minikube service <service-name>```
### Get service url
```minikube service <service-name> --url```
### StatefulSet
### Apply
```kubectl apply -f <statefulset-file.yaml>```
### Delete
```kubectl delete -f <statefulset-file.yaml>```
### Get
```kubectl get statefulset```
## Deployment
### Apply 
```kubectl apply -f <deployment-file.yaml>```
### Delete 
```kubectl delete -f <deployment-file.yaml>```
