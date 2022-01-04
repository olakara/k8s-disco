# Pod Health

- K8s relies on Probes to determine the health of a Pod container
- A probe is a diagnostic performed by the kubelet on a container
- Types of Probe
    - Liveness Probe   -> determine if the Pod is running as expected
    - Readiness Probe  -> determines if the Pod is ready to receive requests
- Probe using...
    - ExecAction -> execute an action inside the container
    - TCPSocketAction -> TCP check against the container's IP and port
    - HTTPGetAction -> HTTP GET request against the container
- Possible Probe results:
    - Success
    - Failure
    - Unknown

Notes:

- Open interactive shell for a pod : `kubectl exec <pod-name> --it sh`
- Get details of a pod `kubectl describe <pod-name>`