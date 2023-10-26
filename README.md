# Ambient Reference Architecture w/ Argo

This repo contains a reference architecture for operating Istio Ambient Mesh with ArgoCD using GitOps.  It demonstrates best practices for leveraging Istio as part of an application platform.

## DISCLAIMER

Istio Ambient Mesh is still in Alpha, and is not suitable for production use.  Likewise, this reference architecture is of Alpha quality, and includes several rough edges, including:
 * Cluster-Scoped upgrades cause known traffic loss, and have wide blast radius.
 * The tag chart is forked from the primary istio repo, and needs to be merged and published

## Getting Started

This reference architecture assumes that you have an ArgoCD installation with:
 * Cluster
 * Projects
 * Repository Connection

To deploy Istio, supporting software, and the bookinfo sample application, fork and clone this repository and run:

```
TODO: modify repo links to point to your repo
TODO: modify cluster links to point to your cluster
argocd create application -f meta-application.json
```

## Repository Layout

The meta-application.yaml file is an App-of-Apps that references all other applications needed for running Istio and the demo application via ArgoCD.  The diagram below demonstrates the deployment mechanism for each part of the platform.

![architecture diagram][diag]

## Principles

## Components

## Playbook: Minor Version Upgrade

## Playbook: Major Version Upgrade

[diag]: ./blob/master/argo-reference-arch.svg "Logo Title Text 2"