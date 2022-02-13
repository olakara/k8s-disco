## Running my first app on K8s

### Simple website
- `kubectl apply -f .\deployments\first-deployment.yml`
- `kubectl apply -f .\services\loadbalancer.service.yml`

Now you should be able to access the application from the bowser using he url `localhost:8080`

## A Webserver with static site

- `kubectl apply -f .\deployment.yml`
- `kubectl apply -f .\loadbalancer.service.yml`

