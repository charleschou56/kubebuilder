# Kubebuilder
Use kubebuilder to implement the operator

## Install dep - Binary Installation
```bash
$ curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh
```

## Install kustomize
```bash
$ curl -s "https://raw.githubusercontent.com/kubernetes-sigs/kustomize/master/hack/install_kustomize.sh"  | bash
```

## Install kubebuilder
```bash
# download kubebuilder and install locally.
$ curl -L -o kubebuilder https://go.kubebuilder.io/dl/latest/$(go env GOOS)/$(go env GOARCH)
$ chmod +x kubebuilder && sudo mv kubebuilder /usr/local/bin/
```

# Use Kubebuilder
```bash
$ go mod init programming-kubernetes.info/m/v2
$ kubebuilder init --domain programming-kubernetes.info --license apache2 --owner "Programming Kubernetes authers"
$ kubebuilder create api --group cnat --version v1alpha1 --kind At
$ kubectl create ns cnat && kubectl config set-context $(kubectl config current-context) --namespace=cnat
```

## Install CRD
```bash
$ make install
```

## Run controller
```bash
$ make run
```

## Create CRD
```bash
$ kubectl apply -f config/crd/bases/cnat.programming-kubernetes.info_ats.yaml
```

## Create resource object
```bash
kubectl apply -f config/samples/cnat_v1alpha1_at.yaml
```