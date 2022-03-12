## Add repo

```shell
helm repo add elastic https://helm.elastic.co
```

## Download template

```shell
helm template elasticsearch --version 7.16.2 elastic/elasticsearch > elasticsearch.yaml
```

## Intall with custom values

```shell
helm install elasticsearch --version 7.16.2 elastic/elasticsearch -f values.yaml -n kc-elk
kubectl get pods --namespace=kc-elk -l app=elasticsearch-master -w2
helm --namespace=kc-elk test elasticsearch
```

## Uninstall

```shell
helm uninstall elasticsearch -n kc-elk
```

## Install Ingress

```shell
kubectl create -f ingress.yaml
```

kubectl label nodes worker node=tools
kubectl get nodes --show-labels