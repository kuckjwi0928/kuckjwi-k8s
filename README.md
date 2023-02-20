# Preinstallation Requirements
~~~shell
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
