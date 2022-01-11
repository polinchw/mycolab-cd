# hello-github-webhook-cd

## Description

This project contains a Helm chart for Argo CD to deploy 
[hello-github-webhook](https://github.com/polinchw/hello-github-webhook) to Kubernetes.

I'm using the [Argo Image Updater](https://argocd-image-updater.readthedocs.io/en/stable/) to automatically change the manifest when a new docker image
is detected (semver for prod, digest for dev).  After the image updater changes the manifest
ArgoCD will do its usual job and deploy the new images automatically.