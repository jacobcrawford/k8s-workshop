# Pod tasks
We cant to create our first running container on Kubernetes. This will be the simple curl pod to use for inspecting within the cluster.

1. Create a Curl pod from the manifest file in [curl.yaml](../resources/curl.yaml)
1. Create the Nginx pod from the manifest file in [pod.yaml](../resources/pod.yaml)
1. Look at the pods logs for Nginx
    a. What version of nginx is running?
1. Change the version to `1.24.0` and deploy the Pods again
1. Describe the Nginx pod and find the ClusterIP
1. Attach terminal to the Curl container and call the endpoint for the Nginx pod on port 80
1. Delete the Nginx pod and create it again
1. Curl the Nginx pod again
    a. Did something change?
1. Go to [service tasks](../tasks/task2.md)