# Hybrid Kubernetes Platform — AWS & On-Prem Simulation

## 📌 Project Overview

This project demonstrates the design and implementation of a hybrid Kubernetes platform spanning cloud and on-premises environments. The objective is to simulate real-world enterprise container platforms that support consistent workload deployment, infrastructure automation and scalable orchestration across multiple environments.

Infrastructure provisioning is automated using Terraform, which deploys AWS networking components and EC2 compute instances to host a self-managed Kubernetes cluster bootstrapped via kubeadm. In parallel, an on-premises Kubernetes environment is simulated using virtualized infrastructure, enabling hybrid deployment and platform engineering use cases.

---

## 🏗️ Architecture

The hybrid platform consists of:

- Cloud Kubernetes cluster hosted on AWS EC2
- On-prem Kubernetes cluster (VM-based simulation)
- Terraform-provisioned infrastructure
- kubeadm-based cluster bootstrap
- Pod networking via Calico CNI

> Architecture diagram will be added in upcoming commits.

---

## ⚙️ Technology Stack

- Kubernetes (kubeadm)
- Terraform (Infrastructure as Code)
- AWS EC2 / VPC
- Docker (Container runtime)
- Calico (CNI networking)
- Linux (Ubuntu)

---

## 📁 Repository Structure

terraform/ → Infrastructure provisioning code
kubeadm/ → Cluster bootstrap scripts
architecture/ → Design diagrams
README.md → Project documentation


---

## 🚀 Infrastructure Provisioning

Terraform provisions the following AWS components:

- Custom VPC network
- Subnet segmentation
- EC2 master node
- EC2 worker nodes

### Deploy Infrastructure

```bash
terraform init
terraform plan
terraform apply


🚧 Project Status

Infrastructure provisioning and cluster bootstrap are currently in progress.

Upcoming updates will include:

ArgoCD GitOps deployment model

Helm-based application packaging

Ingress controller implementation

Observability stack (Prometheus + Grafana)

Disaster recovery and backup testing
