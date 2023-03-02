# kubebuilder
Use kubebuilder to implement the operator

# Install dep - Binary Installation
```bash
$ curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh
```

# Install kustomize
```bash
$ curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh"  | bash
```

# Install kubebuilder
```bash
# download kubebuilder and install locally.
$ curl -L -o kubebuilder https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)
$ chmod +x kubebuilder && sudo mv kubebuilder /usr/local/bin/
```