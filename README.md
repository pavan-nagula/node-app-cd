# 🚀 Node App – Continuous Deployment (CD)

This repository contains the **deployment configuration** and **automated CD pipeline** for deploying the Node.js application to a **Kubernetes cluster** using **GitHub Actions**.

It is part of a two‑repository setup:
- **CI Repo:** Builds the Node.js Docker image and pushes it to GHCR  
- **CD Repo (this repo):** Deploys the latest image to Kubernetes

---

## 📦 Repository Purpose

This repository provides:

- Kubernetes deployment manifests (`deployment.yaml`, `service.yaml`)
- Automated deployment pipeline (`cd.yml`)
- Integration with GitHub Actions for `kubectl apply`
- Deployment to Minikube or any Kubernetes cluster
- Pulling container images from **GitHub Container Registry (GHCR)**

This repo ensures that **every commit to `main`** results in:
1. Applying Kubernetes manifests  
2. Updating the running application  
3. Rolling out changes automatically

---

## 🏗️ Folder Structure
node-app-cd/
├─ deployment.yaml        # Kubernetes Deployment
├─ service.yaml           # Kubernetes Service (NodePort)
└─ .github/
└─ workflows/
└─ cd.yml         # GitHub Actions CD Workflow
---
