# CloudMart Disaster Recovery Plan

## Objective
Ensure CloudMart services can recover quickly from failures, outages, or infrastructure issues.

## Recovery Strategies

### Kubernetes Self-Healing
Kubernetes automatically recreates failed pods and maintains desired replica counts.

### Multiple Replicas
Critical services run with multiple replicas to improve availability.

### Rolling Updates
Rolling deployments reduce downtime during updates.

### AWS Managed Services
AWS EKS and ECR provide highly available managed infrastructure.

### Backup Strategy
- Store source code in GitHub
- Store Docker images in ECR
- Use database backups for persistent data
- Maintain Infrastructure as Code configurations

## Failure Scenarios

### Pod Failure
Kubernetes automatically recreates failed pods.

### Node Failure
Pods are rescheduled to healthy worker nodes.

### Application Failure
Liveness probes restart unhealthy containers.

### Region Failure
Future improvement: deploy multi-region architecture.

## Recovery Time Objective (RTO)
Approximately 5–15 minutes for most failures.

## Recovery Point Objective (RPO)
Minimal data loss depending on database backup frequency.