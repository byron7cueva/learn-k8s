## Add repo

```shell
helm repo add elastic https://helm.elastic.co
```

## Download template

```shell
helm template filebeat --version 7.16.2 elastic/filebeat > filebeat.yaml
```

## Intall with custom values

```shell
helm install filebeat --version 7.16.2 elastic/filebeat -f values.yaml
```

## Uninstall

```shell
helm uninstall filebeat
```