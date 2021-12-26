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
helm install elasticsearch --version 7.16.2 elastic/elasticsearch -f values.yaml -n elastic
```

## Install Ingress

```shell
kubectl create -f ingress.yaml
```