# Cluster with k3s

## Install

**Master:**

```shell
# Install
curl -sfL https://get.k3s.io | sh -s - --no-deploy traefik --write-kubeconfig-mode 644 --node-name master1 --write-kubeconfig /home/$USER/.kube/config

# Get nodes
kubectl get nodes

# Get token
sudo cat /var/lib/rancher/k3s/server/node-token
```

**Worker:**

```shell
curl -sfL https://get.k3s.io | K3S_URL="IP_SERVER_K3S" K3S_TOKEN="TOKEN" sh -
sudo systemctl status k3s-agent
```


## Uninstall

**Master:**

```shell
/usr/local/bin/k3s-uninstall.sh
```

**Worker:**

```shell
/usr/local/bin/k3s-agent-uninstall.sh
```