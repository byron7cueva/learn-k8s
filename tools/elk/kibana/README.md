## Add repo

```shell
helm repo add elastic https://helm.elastic.co
```

## Download template

```shell
helm template kibana --version 7.16.2 elastic/kibana > kibana.yaml
```

## Intall with custom values

```shell
helm install kibana --version 7.16.2 elastic/kibana -f values.yaml -n elastic
```

## Install Ingress

```shell
kubectl create -f ingress.yaml
```