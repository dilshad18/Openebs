# OpenEBS Control Plane Deployment

This manifest comprises configurations for deploying the OpenEBS control plane components, along with associated Custom Resources (CRs) & Role-Based Access Control (RBAC) rules.

## Instructions

- To Create Openebs Deployment in Openebs Namespace
  
```bash
kubectl apply -f openebs.yaml
```
### Deployment Notes

- It will create a local hostpath-based Persistent Volume suitable for a single node Kubernetes Cluster.

### File Descriptions

- `01-openebs-namespace.yaml`: Creates the OpenEBS namespace.
- `02-openebs-maya-serviceaccount.yaml`: Creates the Maya Service Account within the OpenEBS namespace.
- `03-openebs-clusterrole.yaml`: Defines a ClusterRole for operations on Kubernetes pods, deployments, and storage resources.
- `04-openebs-clusterrolebinding.yaml`: Binds the Service Account with the defined Role Privileges.
- `05-openebs-localpv-provisioner-deployment.yaml`: Deploys the OpenEBS LocalPV provisioner.
- `06-openebs-storageclass.yaml`: Defines the OpenEBS StorageClass with default settings.

## Notes

- Ensure appropriate context and permissions while deploying these manifests.
- Customize the configurations as needed before deployment.
