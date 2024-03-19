# Getting Started
## Create kind cluster
~~~shell
$ kind create cluster --config ./kind/cluster.yaml
~~~
## Install the nginx-ingress controller
~~~shell
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/kind/deploy.yaml
~~~
