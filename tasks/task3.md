# Deployment tasks
Something very important when we have an application that customers depend on is that its always available, even though errors happens like a Pod crashes or a whole server dies.

1. Create the Nginx deployment from the manifest file in [pod.yaml](../resources/deployment.yaml) 
    a. How many pods do we have now?
1. Change the replication factor to 3 and apply the Deployment again. 
    a. How many pods do we have now?
1. While watching all pods in one terminal update the Nginx version to `1.24.0`
    a. You should see that the update does not remove all Pods at once but waits for new ones to come up. This means that the application is always available even during an update. 
1. Attach terminal to one of the Nginx pod
    a. Install vim `apt update && apt install vim`
    b. Open /usr/share/nginx/html/index.html and make some changes. These should show when you curl the endpoint a few times.
1. Kill the Pod you changed
    a. Does curl still show the change?
1. Go to [Storage tasks](../tasks/task4.md)
