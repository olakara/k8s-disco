kubectl controls the k8s cluster manager

k8s documentation: https://kubernetes.io/docs/reference/kubectl/overview/

## Basic commands
- create : Used to create a resource from a file or from standard input
  - Example 1: `kubectl create -f <file-name>.yml` Create a pod using the data in the YAML file
  - Example 2: `kubectl create -f <file-name>.json` Create a pos using the data in the JSON file
  - Create command can be used to create other k8s resources like `clusterrole`, `deployment`, `job`, `ingress`, `quota`, `namespace`, `secret`, `service` etc

- run : Create & run a particular image in a pod on the cluster.
  - Example 1: `kubectl run <pod-name> --image=nginx` starts a new nginx pod
  - Example 2: `kubectl run <pod-name> --image=hazelcast --port=5701` startes the pod and let the container expose port 5701

- set : Set specific features on objects


- explain: Get documentation for a resource
  - Example:  `kubectl explain pod` displays documentation about pod with description and field details

- get : Display one or many resources
  - Example 1: `kubectl get all` provides all basic information on all the objects in the cluster
  - Example 2: `kubectl get pods` lists all pods 
  - Example 3: `kubectl get pods -o wide` list all pods with more information
  - Example 4: `kubectl get pod <pod-name> -o json` get details of the named pod in the json format
  - Example 5: `kubectl get rc,services` list all the replication controllers and services together



