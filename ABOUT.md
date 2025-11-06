# K3s on Proxmox VE - Automated Kubernetes Cluster Deployment

🚀 **Automated Infrastructure-as-Code solution for deploying production-ready K3s Kubernetes clusters on Proxmox VE**

## Overview

This project provides a complete, automated solution for deploying K3s Kubernetes clusters on Proxmox VE using Terraform and Ansible. It's designed for developers, homelab enthusiasts, and organizations looking to quickly spin up lightweight, production-ready Kubernetes clusters with minimal manual intervention.

## ✨ Key Features

- **🚀 Fully Automated Deployment** - Single command cluster provisioning
- **🔄 Infrastructure-as-Code** - Reproducible deployments using Terraform
- **⚡ Lightweight K3s** - Optimized Kubernetes distribution for edge and resource-constrained environments
- **🔧 Customizable Architecture** - Flexible control plane and worker node configuration
- **🔒 Secure by Default** - SSH key authentication and secure token generation
- **📊 Production Ready** - Includes proper resource allocation and network configuration
- **🛠️ Latest Provider Support** - Compatible with telmate/proxmox v3.0.2-rc05

## 🏗️ Architecture

### Default Cluster Configuration
- **Control Plane**: 1 node (2 vCPU, 4GB RAM, 15GB disk)
- **Worker Nodes**: 3 nodes (1 vCPU, 2GB RAM, 10GB disk each)
- **K3s Version**: v1.34.1+k3s1
- **Network**: 192.168.1.180-187
- **Storage**: ZFS (local-zfs)
- **Custom VM IDs**: Starting from 500

### Technology Stack
- **Terraform** - Infrastructure provisioning
- **Ansible** - Configuration management
- **Proxmox VE** - Virtualization platform
- **K3s** - Lightweight Kubernetes distribution
- **Ubuntu 24.04** - Base operating system

## 🚀 Quick Start

```bash
# Clone and deploy
git clone https://github.com/yourusername/k3s-proxmox-terraform
cd k3s-proxmox-terraform

# Configure your variables
cp terraform.tfvars.example terraform.tfvars
nano terraform.tfvars  # Add your Proxmox API token

# Deploy the cluster
./deploy.sh
```

## 🎯 Use Cases

### 🏠 Homelab & Learning
- Perfect for learning Kubernetes concepts
- Cost-effective cluster for personal projects
- Ideal for CI/CD pipeline testing

### 🔬 Development & Testing
- Rapid environment provisioning for development teams
- Consistent testing environments
- Microservices development and testing

### 🌐 Edge Computing
- Lightweight footprint suitable for edge locations
- Resource-efficient for constrained environments
- Distributed application deployment

## 🔧 Customization

The project is highly configurable:

- **Cluster Size**: Scale workers up or down
- **Resource Allocation**: Adjust CPU, memory, and disk sizes
- **Network Configuration**: Custom IP ranges and subnets
- **VM IDs**: Avoid conflicts with existing VMs
- **K3s Version**: Use any supported K3s release

## 📁 Project Structure

```
k3s-proxmox-terraform/
├── main.tf                 # Main Terraform configuration
├── variables.tf            # Variable definitions
├── outputs.tf             # Output definitions
├── terraform.tfvars       # Your configuration (gitignored)
├── deploy.sh              # Automated deployment script
├── ansible/
│   ├── inventory.yml      # Ansible inventory
│   └── k3s-install.yml    # K3s installation playbook
└── docs/
    ├── DEPLOYMENT_GUIDE.md # Complete deployment guide
    └── pve-info-checklist-example.md # Proxmox setup template
```

## 🛡️ Security Features

- **API Token Authentication** - Secure Proxmox API access
- **SSH Key Authentication** - No password-based SSH
- **Random K3s Token Generation** - Secure cluster joining
- **Network Isolation** - Configurable network segmentation
- **Resource Limits** - Prevent resource exhaustion

## 📚 Documentation

- **[README.md](README.md)** - Quick start and basic usage
- **[docs/DEPLOYMENT_GUIDE.md](docs/DEPLOYMENT_GUIDE.md)** - Complete step-by-step guide
- **[docs/pve-info-checklist-example.md](docs/pve-info-checklist-example.md)** - Proxmox setup checklist

## 🤝 Contributing

Contributions are welcome! Please feel free to submit pull requests, open issues, or suggest improvements.

## 📄 License

MIT License - feel free to use this project for personal or commercial purposes.

## ⭐ Support

If you find this project useful, please give it a star! ⭐

---

**Deploy your Kubernetes cluster in minutes, not hours!** 🚀
