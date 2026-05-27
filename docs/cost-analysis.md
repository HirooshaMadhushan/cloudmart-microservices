# CloudMart Cost Analysis

## AWS Services Used

| Service | Purpose |
|---|---|
| Amazon EKS | Kubernetes cluster management |
| Amazon EC2 | Worker nodes |
| Amazon ECR | Docker image registry |
| Elastic Load Balancer | Public frontend access |
| CloudWatch | Monitoring and logs |
| IAM | Access management |

## Estimated Monthly Cost

| Resource | Estimated Cost |
|---|---|
| EKS Cluster | $73/month |
| 2 x t3.medium EC2 Instances | $60/month |
| ECR Storage | $5/month |
| Load Balancer | $18/month |
| CloudWatch | $10/month |

## Estimated Total
Approximately $160–$180 per month depending on traffic and storage usage.

## Cost Optimization Strategies
- Use auto scaling
- Remove unused resources
- Use spot instances for non-production workloads
- Limit container resource usage
- Use lifecycle policies in ECR