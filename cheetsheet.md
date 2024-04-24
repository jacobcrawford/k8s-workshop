# Most used commands
1. Deploy resource from file: `kubectl apply -f <filename>` 
1. List resources: `kubectl get <resource>`   
    a. resource could be Pod, Service, Deployment, Namespace etc    
    b. See all valid values for `<resource>` with `kubectl api-resources` 
1. Get information about specific deployed resource `kubectl describe <resource> <name>`
1. Delete a specific deployed resource `kubectl delete <resource> <name>` 
1. Look at a pods logs: `kubectl logs <pod-name>`
1. Attach the terminal to a running Pod `kubectl exec -it <pod-name> -- /bin/bash`
1. Call an endpoint in a container: `curl <endpoint>:<port>`
1. Explan a Kubernetes resource to know how to structure the yaml: `kubectl explain <resource>.<path>`