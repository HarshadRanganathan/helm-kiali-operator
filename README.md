# helm-kiali-operator

Helm chart for setting up Kiali Operator in your EKS cluster.

## Install/Upgrade Chart

Run below commands to install/upgrade the chart.

```bash
helm upgrade -i kiali-operator . -n kiali-operator --values=stages/shared-values.yaml
```
