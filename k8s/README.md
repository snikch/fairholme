# Kubernetes Setup

## Init

Initialises ArgoCD.

```sh
op run --env-file="./.env" -- \
    helm install -n argo-cd \
        --create-namespace \
        --set="ghcrToken=$GHCR_TOKEN \
        argo-cd ./init
```

Update via.

```sh
op run --env-file="./.env" -- \
    helm upgrade -n argo-cd --create-namespace \
        --set="ghcrToken=$GHCR_TOKEN" \
        argo-cd ./init
```

Remove via.

```sh
op run --env-file="./.env" -- helm uninstall -n argo-cd argo-cd
```
