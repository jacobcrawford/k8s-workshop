# Service tasks
A running Pod in a Kubernetes cluster will change its IP all when it gets recreated so we cannot trust it will stay the same. Services will fix this problem for us.
1. Create a Service from the manifest file in [service.yaml](../resources/service.yaml)
1. Describe the Service
    a. A Service will have bound to the correct Pod when the "Endpoints" section have the Pods IP address
1. Fix the label selector to match the Pods label and apply the Service again
    a. Did the "Endpoint" section change?
1. Attach terminal to the Curl pod again and Curl the service by its name and the port `<service-name>:<port>`
    a. A service has a `port` which it exposes and a `targetPort` which it sends forwards to on the Pod
1. Change the Service type to NodePort and apply service again
1. Curl "localhost:8080" from WSL