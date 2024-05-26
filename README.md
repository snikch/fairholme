# Fairholme Lab

## Kube Config

```sh
export CONTROL_PLANE_IP=192.168.1.224
talosctl config endpoint $CONTROL_PLANE_IP
talosctl kubeconfig .
```
