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
