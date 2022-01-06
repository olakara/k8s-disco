# Services

A service provides a single point of entry for accessing one or more pods.

- Services abstract pod ip addresses from consumers
- Services provide load balance between pods
- Labels are used to associate a service with pods
- Service Types
  - ClusterIP - Expose the service on a cluster internal IP
  - NodePort - Expose the service on each node's IP at a static port
  - LoadBalancer - Provision an external IP to act as load balancer
  - ExternalName - Maps a service to a DNS name
