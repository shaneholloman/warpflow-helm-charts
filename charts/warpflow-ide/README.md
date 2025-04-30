# Warpflow IDE chart

Helm chart for Warpflow as IDE with a persistent storage or an external database (for example PostgreSQL).

## Quick start

Install the chart:

```sh
helm repo add warpflow https://warpflow-ai.github.io/warpflow-helm-charts
helm repo update
helm install warpflow-ide warpflow/warpflow-ide -n warpflow --create-namespace
```

## Examples

See more examples in the [examples directory](https://github.com/warpflow-ai/warpflow-helm-charts/tree/main/examples/warpflow-ide).
