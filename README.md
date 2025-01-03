# DevOps Setup with Vagrant Ansible

A development environment setup project that creates a local Kubernetes cluster using Vagrant and Ansible. This project is designed for learning purposes, allowing developers to experiment with Kubernetes in a controlled environment.

## Features

- Automated Kubernetes cluster setup
- Master node configuration
- Docker installation and configuration
- Calico network plugin integration
- Swap disable configuration for Kubernetes
- Automatic kubeconfig setup

## Prerequisites

Before you begin, ensure you have the following installed on your system:
- [Vagrant](https://www.vagrantup.com/downloads)
- [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html)
- [VirtualBox](https://www.virtualbox.org/wiki/Downloads)

## Installation

1. Clone this repository:
    ```bash
    git clone https://github.com/prabhakaran-jm/devops-setup-with-vagrant-ansible.git
    cd devops-setup-with-vagrant-ansible
    ```

2. Initialize the Vagrant environment:
    ```bash
    vagrant up
    ```

3. The Ansible playbook will automatically run during the Vagrant provisioning process.

## Project Structure

├── kubernetes-setup/
│ ├── master-playbook.yml # Ansible playbook for master node setup
│ └── [other configuration files]
├── Vagrantfile # Vagrant configuration
└── README.md


## What Gets Installed

The following components are automatically installed and configured:
- Docker CE
- Kubernetes components (kubelet, kubeadm, kubectl)
- Calico network plugin
- Required dependencies and packages

## Usage

### Starting the Cluster   

```bash
vagrant up
```

### Accessing the Cluster


```bash
kubectl get nodes
```         

### Stopping the Cluster
```bash
vagrant halt
```

### Destroying the Cluster
```bash
vagrant destroy -f
```

## Configuration

The master node is configured with the following specifications:
- IP Address: 192.168.50.10
- Pod Network CIDR: 192.168.0.0/16
- Network Plugin: Calico

## Troubleshooting

If you encounter any issues:
1. Ensure all prerequisites are properly installed
2. Check if VirtualBox is running correctly
3. Verify that your system has enough resources
4. Check the Vagrant and Ansible logs for error messages

## Contributing

Feel free to submit issues and enhancement requests!

## Note

This setup is intended for learning and development purposes only. It is not recommended for production use.



