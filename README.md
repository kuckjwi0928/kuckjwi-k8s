# Preparations
~~~shell
# metric-server
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/components.yaml
# kafka
kubectl create namespace kafka
kubectl create -f 'https://strimzi.io/install/latest?namespace=kafka' -n kafka
# istio
istioctl install -f ./istio/operator.yaml
~~~

# Run on kubernetes
~~~shell
skaffold run
~~~
