+++
draft = false
title = "GitLab"
description="GitLab"
language = "en"
tags = [
    "charts",
    "kubernetes"
]
date = "2017-01-01T13:10:52-05:00"
type = "doc"
[menu.doc]
  Identifer = "gitlab"
  Weight = 2
  Parent = "Charts"
+++

## Resource Group

The canadian location will soon offer the Kubernetes managed service.

```sh
  az group create --name stck8s \
                  --location eastus \
                  --tags stck8s
```

## Cluster

Right now we only need to launch GitLab so can simply set a cluster size of 1.
GitLab does have a few dependencies though so lets give the cluster the
following specifications:

* 4xVCPU
* 14 GB memory
* SSD premium

```sh
  az aks create --resource-group stck8s \
                --name stck8s \
                --node-count 1 \
                --generate-ssh-keys \
                --node-vm-size Standard_DS3_v2_Promo \
                --node-osdisk-size 64 \
                --tags stck8s
```

## Azure CLI context

Once the cluster is up we need to give the azure cli the correct context:

```sh
  az aks get-credentials --resource-group stck8s \
                         --name=stck8s
```

## Patch to Storage Class

There is currently a bug with the default storage class set on the Cluster
via AKS. Any persistent volume claim that doesn't specify a specific
storageClass will fail on a default deployment.

* https://github.com/Azure/AKS/issues/48

```sh
  kubectl patch storageclass default -p '{"metadata": {"annotations":{"storageclass.kubernetes.io/is-default-class":"true"}}}'
```

## Helm Install

Until the charts repository is setup please follow the current workflow:

```sh
git clone https://gitlab.sylus.ca/devops/charts
cd charts/gitlab-omnibus
helm install --name gitlab -f values-new.yaml .
```

## Helm Upgrade

Should you need to make any changes you can upgrade existing infra:

```sh
helm upgrade gitlab -f values-new.yaml .
```
