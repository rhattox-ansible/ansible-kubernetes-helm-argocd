# ansible-k8s-argocd

Installs Argo CD using its Helm chart and Argo Rollouts using the official
Kubernetes installation manifests. This playbook does not install the Argo CD CLI.

## Layout

```text
main.yaml
defaults/main.yaml
meta/main.yml
tasks/main.yaml
tasks/0-install-argocd.yaml
tasks/1-install-argo-rollouts.yaml
templates/argocd-values.yaml
```

The root playbook loads defaults and includes the task dispatcher. The dispatcher
reports progress and includes the installation tasks. Galaxy role metadata is in
`meta/main.yml`. Customize Helm values in `templates/argocd-values.yaml`.

## Usage

Requires Ansible, the `kubernetes.core` collection, Helm, kubectl, Kubernetes Python
dependencies, and access to a Kubernetes cluster.

```bash
ansible-playbook main.yaml
```
