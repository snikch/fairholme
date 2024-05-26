# Kubernetes Setup

## Init

Initialises ArgoCD.

```sh
op run --env-file="./.env" -- \
    helm install -n argocd \
        --create-namespace \
        --set="ghcrToken=$GHCR_TOKEN \
        argocd ./init
```

Update via.

```sh
op run --env-file="./.env" -- \
    helm upgrade -n argocd --create-namespace \
        --set="ghcrToken=$GHCR_TOKEN" \
        argocd ./init
```

Remove via.

```sh
op run --env-file="./.env" -- helm uninstall -n argocd argocd
```
