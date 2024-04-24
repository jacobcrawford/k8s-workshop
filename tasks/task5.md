# Future tasks
We have scratched the surface of Kubernetes resources involving compute, network and storage. So many different Kubernetes resources and concepts exist that its hard to choose what to look at next. Here are a few options:
1. GitOps - Deploy the manifest files from Git instead of applying with Kubectl
    a. [ArgoCD](https://argo-cd.readthedocs.io/en/stable/getting_started/) is the most used operator for GitOps
1. Network LoadBalancer - Uses actual IP addesses and not port opening like NodePort, which is more scalable for production
    a. [Metallb](https://medium.com/groupon-eng/loadbalancer-services-using-kubernetes-in-docker-kind-694b4207575d) is mostly used for bare metal and hobby setups
1. Container Network - Networking between containers have so many features. 
a. [Cilium](https://docs.cilium.io/en/stable/installation/kind/), which is the de facto standard can be installed in Kind (Though not in WSL)
1.  Templating and package managing
    a. [Helm](https://helm.sh/) is way to package and share K8s template files for more complex applications
1. Dig in to the [CNCF landscape](https://landscape.cncf.io/) to find all kinds of K8s platform application that are used arround the world
