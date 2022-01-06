# Deployments

### Display all deployments with labels
`kubectl get deployments --show-labels`

### Get deployment with a specific label
`kubectl get deployments -l app=nginx`

### Scale command
`kubectl scale deployment <deployment-name>` --replicas=3

`kubectl scale -f deployment.yml --replicas=3`

Notes:
- Use "create" or "apply" options to deploy a deployment.
- Deployment Options:
  - Rolling update
  - Blue-Green deployments
  - Canary deployments
  - Rollback