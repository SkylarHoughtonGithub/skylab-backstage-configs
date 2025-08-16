# Skylab EKS Cluster

## Overview

This EKS cluster is managed by Crossplane and deployed via ArgoCD in the **dev** environment.

## Configuration

| Parameter | Value |
|-----------|-------|
| Cluster Name | skylab |
| Environment | dev |
| Platform | eks |
| Variant | standard |
| Region | us-east-2 |
| Node Count | 1 |
| Node Size | t3.medium |

## Quick Links

- [AWS Console](https://console.aws.amazon.com/eks/home?region=us-east-2#/clusters/skylab)
- [ArgoCD Applications](https://argocd.skylarhoughtongithub.local/applications?search=skylab-crossplane-infra-dev)
- [Architecture Details](architecture.md)
- [Operations Guide](operations.md)
