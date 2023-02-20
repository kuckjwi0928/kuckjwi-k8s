# Preinstallation Requirements
~~~shell
# metric-server
kubectl apply -f https://github.com/kubernetes-sigs/metrics-server/releases/latest/download/high-availability-1.21+.yaml
# kafka
kubectl create namespace kafka
kubectl create -f 'https://strimzi.io/install/latest?namespace=kafka' -n kafka
# istio
istioctl install --set profile=default -y
~~~

# Run on kubernetes
~~~shell
skaffold run
~~~
