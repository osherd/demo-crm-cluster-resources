# 1 - GKE Cluster Setup & kubectl Access Guide

This guide walks you through creating a Google Kubernetes Engine (GKE) cluster and accessing it with `kubectl`.

---

## 📋 Prerequisites

- A Google Cloud project
- [Google Cloud SDK (gcloud)](https://cloud.google.com/sdk/docs/install)
- [kubectl CLI](https://kubernetes.io/docs/tasks/tools/)

---

## 1. Authenticate with Google Cloud

```bash
gcloud auth login
gcloud config set project <YOUR_PROJECT_ID>
```

## 2- Enable GKE API

```bash
gcloud services enable container.googleapis.com
```

## 3 - Create a GKE Cluster (use console) - example

```bash
gcloud container clusters create demo-cluster \
  --region us-central1 \
  --num-nodes 2 \
  --enable-ip-alias
```

## 4 - Configure kubectl Access

```bash
gcloud container clusters get-credentials <CLUSTER_NAME> \
  --region <REGION>
```
