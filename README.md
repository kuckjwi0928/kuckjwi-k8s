# Getting started
## istio
~~~shell
$ istioctl operator init
$ kubectl apply -f ./istio/istio-operator.yaml
$ kubectl create namespace local
$ kubectl label namespace local istio-injection=enabled
~~~
## metric-server
~~~shell
$ helm repo add metrics-server https://kubernetes-sigs.github.io/metrics-server/
$ helm upgrade --install metrics-server metrics-server/metrics-server --namespace kube-system
~~~
## cert-manager
~~~shell
$ helm install \
  cert-manager jetstack/cert-manager \
  --namespace cert-manager \
  --create-namespace \
  --version v1.14.4 \
  --set installCRDs=true
$ kubectl apply -f ./self-signed-cert/cluster-issuer.yaml
~~~
## kafka
~~~shell
$ helm install kafka oci://registry-1.docker.io/bitnamicharts/kafka --values ./kafka/values.yaml --create-namespace --namespace kafka
~~~
