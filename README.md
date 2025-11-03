# Kubeflow On-Premises Deployment

This repository contains Kubernetes manifests and configurations for deploying Kubeflow on-premises with production-level capabilities.

## Overview

Kubeflow is an open-source machine learning platform designed to orchestrate complex ML workflows on Kubernetes. This repository provides the necessary configurations to deploy and manage Kubeflow components in an on-premises Kubernetes environment.

## Current Components

### Applications (`apps/`)
- **Central Dashboard**: Web-based UI for managing Kubeflow resources and workflows
  - Includes OAuth2 proxy integration for authentication
  - Istio service mesh integration for secure communication
- **Jupyter**: Jupyter notebook environment for ML development
  - Jupyter Web App for browser-based notebook access
  - Notebook Controller for managing notebook lifecycles

### GitOps with ArgoCD (`argocd/`)
- App-of-Apps pattern for managing Kubeflow deployments
- Declarative application management using ArgoCD
- Automated synchronization and deployment workflows

## Architecture

This deployment follows GitOps principles using ArgoCD to manage the Kubeflow installation. The configuration supports:

- **Production-ready setup**: Designed for enterprise on-premises environments
- **Service mesh integration**: Uses Istio for secure service-to-service communication
- **Authentication**: OAuth2 proxy integration for user authentication
- **Modular deployment**: Component-based installation using Kustomize overlays

## Getting Started

> **Note**: This repository is currently under active development. Initial focus is on establishing core components (Jupyter notebooks and central dashboard).

### Prerequisites
- Kubernetes cluster (on-premises)
- ArgoCD installed and configured
- Istio service mesh (recommended)

### Deployment
The applications are managed through ArgoCD using the app-of-apps pattern. Deploy the main application definition to bootstrap the entire Kubeflow installation.

## Project Status

🚧 **In Development** - Currently implementing foundational components:
- ✅ Central Dashboard manifests
- ✅ Jupyter Web App and Notebook Controller
- 🔄 Additional ML platform components (planned)

## Contributing

This is an active development project focused on production-ready Kubeflow deployment patterns for on-premises environments.