# Scout Karpenter NodePool Test

EKS Karpenter NodePool fixtures for testing Scout `locate-karpenter-node` against EC2 rightsizing recommendations.

## Layout

- `clusters/prod/karpenter/nodepool-default.yaml` — NodePool that allows `m5.2xlarge`
- `clusters/prod/karpenter/ec2nodeclass-default.yaml` — EC2NodeClass referenced by the NodePool

## Matching EC2 nodes

Nodes provisioned by this pool look like:

| Field | Value |
| --- | --- |
| Instance type | `m5.2xlarge` |
| Region | `us-east-1` |
| NodePool | `default` |
| EC2NodeClass | `default` |
| Cluster | `scout-karpenter-test` |
