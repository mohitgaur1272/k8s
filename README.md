# k8s
## for image change in deployment by this command 
```
kubectl set image deployment/nginx-deployment nginx=nginx:1.16.1
```
change your deployment name and image name 
### if you want to see rollout status so use this command
```
kubectl rollout status deployment/nginx-deployment
```

### if you want to see history of your deployment 
```
kubectl rollout history deployment/nginx-deployment
```


## if you want to get your previous version of your deployment 
```
kubectl rollout undo deployment/nginx-deployment
```

### if you want to go your previous version of your image so use this command 
```
kubectl rollout undo deployment/nginx-deployment --to-revision=no
```

# Scaling a Deployment
### You can scale a Deployment by using the following command:
```
kubectl scale deployment/nginx-deployment --replicas=10
```
## if you want to scalling of your deployment on based cpu utilization so use this command 
### change min and max and % of your desired state
```
kubectl autoscale deployment/nginx-deployment --min=10 --max=15 --cpu-percent=80
```

### if you want to see all resources
```
kubectl  explain --recursive  pod/deployment  | less
```

