# Architecture

## Infrastructure Components

### Networking
- **VPC**: `skylab-vpc` (192.168.0.0/16)
- **Subnets**: 
  - `skylab-us-east-2a` (192.168.10.0/24)
  - `skylab-us-east-2c` (192.168.11.0/24)
- **Internet Gateway**: `skylab-igw`
- **Route Table**: `skylab-public-rt`

### Security
- **Security Group**: `skylab-sg`
- **Cluster Role**: `skylab-cluster-role`
- **Node Role**: `skylab-node-role`

### Compute
- **EKS Cluster**: `skylab` (Kubernetes 1.28)
- **Node Group**: `skylab-nodegroup`

## Crossplane Resources

This cluster is defined as a Crossplane Composition that creates and manages all AWS resources automatically.

### Connection Secret
Cluster credentials are stored in:
- **Namespace**: `crossplane-system`
- **Secret**: `skylab-conn`
