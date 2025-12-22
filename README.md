# ansible-k8s-argocd

Ansible collection for managing ArgoCD on Kubernetes clusters.

## Roles

### cli
Installs the ArgoCD CLI tool on the target host. Tasks include:
- Downloading the ArgoCD CLI binary from official GitHub releases
- Installing the binary to the specified path
- Checking the installation
- Displaying the installed ArgoCD CLI version

### chart
Installs and manages ArgoCD on your Kubernetes cluster using the official Helm chart. Tasks include:
- Adding the ArgoCD Helm chart repository
- Creating the ArgoCD namespace in Kubernetes
- Installing or upgrading ArgoCD using the Helm chart with custom values (see `roles/chart/templates/argocd-values.yaml`)

## Usage

Add this collection to your Ansible playbook and use the provided roles to automate ArgoCD installation and management.

```sudo apt install python3-kubernetes```
