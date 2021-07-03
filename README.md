# helm-kiali-operator

Helm chart for setting up Kiali Operator in your EKS cluster.

Table of Contents
=================

   * [helm-kiali-operator](#helm-kiali-operator)
      * [Pre-requisites](#pre-requisites)
         * [Namespace](#namespace)
         * [Config Updates](#config-updates)
      * [Install/Upgrade Chart](#installupgrade-chart)

## Pre-requisites

### Namespace

Create a new namespace `kiali-operator` where we will install operator.

```bash
kubectl create namespace kiali-operator
```

### Config Updates

In `shared-values.yaml` file available inside `stages` folder, add values for below settings:

|||
|--|--|
|accessible_namespaces |Add your app namespaces |
|prometheus.url |Update to your prometheus service url running in the cluster |

## Install/Upgrade Chart

Run below commands to install/upgrade the chart.

```bash
helm upgrade -i kiali-operator . -n kiali-operator --values=stages/shared-values.yaml
```
