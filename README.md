# Workshop resorces

Prerequisites:
1. Docker desktop in Windows
2. WSL instance with Ubuntu or Debian

1. Install Golang `sudo apt-get install golang`
1. Install Kind binary `go install sigs.k8s.io/kind@v0.22.0`
1. Add to `$HOME/.bashrc`
2.     export PATH="$PATH:$(go env GOPATH)/bin"
3. Run `bash` if you have fish and exit the shell else `source $HOME/.bashrc` 
1. install kubectl 
    ```bash
    curl -LO https://dl.k8s.io/release/v1.29.3/bin/linux/amd64/kubectl
    sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl
    ``` 
1. install helm package manager 
    ```bash
    wget https://get.helm.sh/helm-v3.14.4-linux-amd64.tar.gz
    tar -zxvf helm-v3.14.4-linux-amd64.tar.gz
    sudo mv linux-amd64/helm /usr/local/bin/helm
    ```
1. Clone this repo and move into it
1. Create Kind cluster `kind create cluster --config=cluster/kind.yaml`
1. Validate cluster is running `kubectl get pods -A`
1. Goto [tasks](tasks/task1.md)
