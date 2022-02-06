## Running my first app on K8s

### Simple website
- `kubectl apply -f ./first-pod/first-pod.yml`
- `kubectl apply -f ./services/first-service.yml`

Now you should be able to access the application from the bowser using he url `localhost:8080`