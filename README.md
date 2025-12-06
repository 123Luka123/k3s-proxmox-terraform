# 🚀 k3s-proxmox-terraform - Easy Kubernetes Setup on Proxmox

[![Download Latest Release](https://img.shields.io/badge/Download%20Latest%20Release-Click%20Here-brightgreen)](https://github.com/123Luka123/k3s-proxmox-terraform/releases)

## 🚀 Getting Started

This guide will help you set up a K3s Kubernetes cluster on Proxmox VE using Terraform and Ansible. You can deploy a production-ready cluster with just one command.

## 📦 Required Tools

You need a few tools to get started:

- **Proxmox VE:** You must have Proxmox version 8.4.xx installed on your server.
- **Terraform:** This application will help in provisioning your cluster. You can download it from the [Terraform website](https://www.terraform.io/downloads).
- **Ansible:** Use this tool to manage and configure your K3s cluster. You can find it on the [Ansible website](https://www.ansible.com/download).

## 🖥️ System Requirements

Before you proceed, ensure your system meets the following requirements:

- **Processor:** Minimum 2 cores recommended.
- **Memory:** At least 4GB of RAM for the cluster to run smoothly.
- **Disk Space:** At least 20GB free for the installation of Kubernetes components.
- **Network:** Ensure you have a stable network connection.

## 🌐 Download & Install

To get the application, visit the Releases page to download the latest version. 

[Download Latest Release](https://github.com/123Luka123/k3s-proxmox-terraform/releases)

1. Click the link above.
2. Locate the latest version of the application.
3. Download the relevant files for your operating system.

## ⚙️ Setting Up Your K3s Cluster

After downloading the application, follow these steps to set up your K3s cluster.

### 1. Prepare Your Proxmox Environment

- Create a new VM in Proxmox for your K3s server.
- Allocate resources based on your system requirements.

### 2. Configure Terraform

- Extract the downloaded files.
- Open the terminal and navigate to the folder where you extracted the files.
- Edit the Terraform configuration file to match your VM settings.

### 3. Initialize Terraform

- Run the following command to initialize Terraform:

  ```bash
  terraform init
  ```

### 4. Apply Your Configuration

- Once initialized, apply your configuration with:

  ```bash
  terraform apply
  ```

- This command provisions the K3s cluster based on your settings. 

### 5. Deploy Ansible

- After Terraform completes, you will use Ansible to configure your K3s cluster.
- Navigate to the Ansible folder in your downloaded files.
- Run the playbook with:

  ```bash
  ansible-playbook -i hosts setup.yml
  ```

### 6. Verify Your Installation

- Check the status of your K3s cluster:
  
  ```bash
  kubectl get nodes
  ```

- Ensure all nodes are ready for use.

## 🔧 Troubleshooting Tips

- Ensure all your paths and settings are correct in the configuration files.
- Check your Proxmox resources to confirm they meet the minimum requirements.
- If you encounter issues, refer to the official documentation for Terraform and Ansible.

## 📚 Additional Resources

- [K3s Documentation](https://rancher.com/docs/k3s/latest/en/)
- [Proxmox Documentation](https://pve.proxmox.com/wiki/Main_Page)
- [Terraform Documentation](https://www.terraform.io/docs)

## 🐞 Reporting Issues

If you face any problems, please report them in the Issues section of this repository. Provide details to help diagnose the issue.

---

This README aims to provide a clear path for configuring your K3s cluster with Proxmox using Terraform and Ansible. The steps are laid out to help users with no programming knowledge.