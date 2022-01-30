# Namespaces

- Namespaces provides a mechanism for isolating groups of resources within a single cluster. 
- Names of resources must be unique within a namespace.
- Namespace based scoping is applicable only for namespaced objects like deployments, services etc. Its not applicable for nodes, persistentvolumns etc
- Namespaces cannot be nested inside one another.
- Each k8s resource can only be in one namespace.
- Default namespace are `default`, `kube-node-lease`, `kube-public`, `kube-system`.
- `kube-system` is used for storing objects created by k8s system.
- `kube-public` is readable by all the users. This is mostly used by objects that should be visible & readable throughout the whole cluster.
- `kube-node-lease` is used for holding lease objects associated with each node.
- `default` The default namespace for objects with no other namespace

## Viewing Namespaces

`kubectl get namespaces` - List the current namespaces in the cluster

## Creating Namespaces

`kubectl create namespace <namespace-name>`

To create a new namespace using YAML:

````
apiVersion: v1
kind: Namespace
metadata:
  name: <namespace-name>
````

Command to create the namespace using the above YAML

`kubectl create -f <file-name>.yml`
 
## Deleting Namespaces

`kubectl delete namespaces <namespace-name>`