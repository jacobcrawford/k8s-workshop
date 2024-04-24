# Storage tasks
Changes to a Pod will be removed because the Pods are stateless and will be created from the container image not an old container. If we want Pods to keep some state when they die, we need persistent storage.
1. Create a Persisten Volume Claim from the manifest file in [pvc.yaml](../resources/pvc.yaml)
1. Use `kubectl explain deployment` to get information on how to mount the PVC (look for volumes and volumeMounts)
1. Mount the PVC to the path `/etc/k8s-volume`
1. Attach terminal to one of the pods and write something to a file at `/etc/k8s-volume/test`
1. Destroy the Pod 
1. Attach terminal to one of the pods and read the file at `/etc/k8s-volume/test`
    a. You see that the content is the same, and should be the same in all Pods, no matter how many times they die.