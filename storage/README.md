# Storage

- Volumes are used to store state/data and use it in a pod
- A pod can have multiple volumes attached to it
- containers rely on a mountPath to access a volume
- K8s supports:
  - Volumes
  - PersistentVolumes
  - PersistentVolumeClaims
  - StorageClasses

- Volumes & volume mounts
  - A volume references a storage location
  - It must have a unique name
  - Volume mount is used to reference a volume

- Volume Types
  - emptyDir -> Empty directory for storing data. Useful for sharing files between containers running in a pod.
  - hostPath -> Pod mounts into the node's filesystem
  - nfs -> A NFS share mounted into the pod
  - configMap / secrets - Special type of volumes that provide pod with access to K8s resources
  - persistentVolumeClaims -> abstracted persistent storage that can be used by pods
  - cloud -> cluster wide storage

- StorageClass
  - It's used to define different "classes" of storage
  - Act as a storage template
  - Supports dynamic provisioning of PersistentVolumes
  

- StorageClass Workflow
  1. Create Storage Class (YML file)
  2. Create PersistentVolumeClaim that references StorageClass
  3. Kubernetes uses StorageClass provisioner to provission a PersistentVolume
  4. Storage provisioned, PersistentVolume created and bound to PersistentVolumeClaim
  5. Pod volume references the PersistentVolumeClaim

- ConfigMaps
  - Provides a way to store configurations and provide it to containers.
  - Configs can be stored in files, provided through command-line or ConfigMap manifest
  - ConfigMaps can be accessed from a pod using 
    - Environment variables ( key/value )
    - ConfigMap volumes ( access as files )
  


