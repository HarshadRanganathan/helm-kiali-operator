# helm-kiali-operator

Helm chart for setting up Kiali Operator in your EKS cluster.

## Pre-requisites

### Namespace

Create a new namespace `kiali-operator` where we will install operator.

```bash
kubectl create namespace kiali-operator
```

## Install/Upgrade Chart

Run below commands to install/upgrade the chart.

```bash
helm upgrade -i kiali-operator . -n kiali-operator --values=stages/shared-values.yaml
```
