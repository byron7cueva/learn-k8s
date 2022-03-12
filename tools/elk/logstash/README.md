## Add repo

```shell
helm repo add elastic https://helm.elastic.co
```

## Download template

```shell
helm template logstash --version 7.16.2 elastic/logstash > logstash.yaml
```

## Intall with custom values

```shell
helm install logstash --version 7.16.2 elastic/logstash -f values.yaml -n kc-elk
```

## Uninstall

```shell
helm uninstall logstash -n kc-elk
```