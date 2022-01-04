# First Pod

## Creating / Applying the pod

`kubectl apply -f ./first-pod.yml`

## Port forward to expose the port for external access

`kubectl port-forward pod/mywebserver 8080:80`

## Delete / Destory the pod

`kubectl delete -f ./first-pod.yml`

