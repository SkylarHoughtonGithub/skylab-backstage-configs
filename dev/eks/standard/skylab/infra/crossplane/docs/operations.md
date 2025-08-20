
# Operations Guide

## ArgoCD Integration

**Application Name**: `{cluster-name}-crossplane-infra-dev`

## Monitoring

### Health Checks
```bash
# Check ArgoCD application
kubectl get applications -n argocd | grep skylab

# Check Crossplane resources
kubectl get composite -A
kubectl get managed -A | grep skylab
```

### Accessing the Cluster
```bash
# Get connection secret
kubectl get secret skylab-conn -n crossplane-system -o yaml

# Update kubeconfig (after extracting from secret)
aws eks update-kubeconfig --region us-east-2 --name skylab
```

## Scaling

### Node Group Scaling
The node group can be scaled by updating the Crossplane composition:
- **Current Size**: 1
- **Min Size**: 1
- **Max Size**: 1

## Backup & Recovery

### Cluster State
- Infrastructure is code-managed via Crossplane
- Application state should be backed up separately
- EKS control plane is managed by AWS
