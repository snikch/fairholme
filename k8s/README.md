# Kubernetes Setup

## Init

Initialises ArgoCD.

```sh
helm install -n argo-cd --create-namespace argo-cd .
```

Update via.

```sh
helm upgrade -n argo-cd --create-namespace argo-cd .
```

Remove via.

```sh
helm uninstall -n argo-cd argo-cd
```
