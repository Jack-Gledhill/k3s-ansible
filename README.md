# Hydra Ansible

## Installing ArgoCD

While Hydra uses ArgoCD to manage its deployments via [this repository](https://github.com/constellation-net/hydra), these playbooks do not install ArgoCD for you. 
This is because the process is not very straightforward, and is honestly just better done manually.

You can install ArgoCD by following the [documentation](https://argo-cd.readthedocs.io/en/stable/getting_started/#3-access-the-argo-cd-api-server).
A few things to note about the installation procedure:

- Traefik and MetalLB are not yet installed, so you will need to use `kubectl port-forward` to access the ArgoCD UI
- The GitOps repo contains some manifests that will expose ArgoCD via Traefik, so make sure that (and MetalLB) are installed ASAP