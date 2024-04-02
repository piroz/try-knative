# try-knative
knative pilot project

# setup cluster

```
brew install knative/client/kn
brew install knative-extensions/kn-plugins/quickstart
brew install kind
brew install kubernetes-cli
kn quickstart kind
kind get clusters
kind delete cluster -n knative
```

# deploy knative service

```
kind create cluster --config=cluster.yaml
kubectl cluster-info --context kind-kind
kubectl get nodes -o wide
kubectl create -f hello.yaml
kubectl get pods -o wide
kubectl get services -o wide
curl localhost:30070
kubectl delete -f hello.yaml --wait
kind delete cluster -n kind
```


