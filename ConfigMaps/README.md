# ConfigMaps & Secrets

## ConfigMaps

- Provides a way to store configurations and provide it to containers.
- Configs can be stored in files, provided through command-line or ConfigMap manifest
- ConfigMaps can be accessed from a pod using
- Environment variables ( key/value )
- ConfigMap volumes ( access as files )

## Providing Configs
- Store in a file. Filename will become the key, and contents will become the value
- Provide through the command line
- ConfigMap manifest (YML)

## How to create a ConfigMap ?
- Defining values in ConfigMap manifest
  - YML definition of ConfigMap with name and data.
  - Can create the configuration through `kubectl create -f <filename>.yml`.
- Defining key/values in config file 
  - Key/Value pairs are defined in a file
  - Filename will become the key 
  - Can create the configuration through `kubectl create configmap <name> --from-file=<filename>`
- Defining key/values in environment file
  - Can create the configuration through `kubectl create configmap <name> --from-env-file=<filename>`
- Defining through command line
  - Creating cofiguration through command line `kubectl create configmap <name> --from-literal=apiUrl=https://example`

## Get ConfigMap
- `kubectl get cm` cam be used to get a ConfigMap and view its contents
- Example: `kubectl get cm <name> -o yaml`
- 
