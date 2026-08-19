# gitops-demo-app

Simple Nginx Helm Chart used as the application source for multi-cluster GitOps with ArgoCD.

---

## Purpose

This repository contains a basic Helm chart that is deployed to multiple Kubernetes clusters (kind + GKE) using ArgoCD.

It serves as the **single source of truth** for the application in a GitOps workflow.

---

## Chart Structure

```text
gitops-demo-app/
├── Chart.yaml
├── values.yaml
├── templates/
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   └── ...
└── .helmignore

How it is used

ArgoCD watches this repository
Any change pushed to the main branch is automatically synced
Deployed to:
Local kind cluster
Google Kubernetes Engine (GKE)



Deployed by
Project: Multi-Cluster GitOps with ArgoCD
Author: Sumer Pathan
text