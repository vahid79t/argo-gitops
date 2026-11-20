# Nginx Helm chart for Argo CD

Upload the `helm-lab` folder to the root of `vahid79t/argo-gitops` on the `master` branch.

In Argo CD > NEW APP:
- Name: helm-nginx-app
- Project: default
- Sync: Automatic
- Repository: https://github.com/vahid79t/argo-gitops.git
- Revision: master
- Path: helm-lab/nginx-chart
- Cluster: https://kubernetes.default.svc
- Namespace: helm-demo
- Helm release name: helm-demo
- Sync option: CreateNamespace=true

The default replica count is 2. Change `helm-lab/nginx-chart/values.yaml` and commit to test GitOps.
