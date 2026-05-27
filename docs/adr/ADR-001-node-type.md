# ADR-001: Kubernetes Node Instance Type Selection

## Status
Accepted

## Context
CloudMart requires worker nodes that can run five microservices, Kubernetes system pods, HPA, and monitoring components. The first attempt with t3.micro caused resource limitations, so a larger instance type was needed.

## Decision
Use t3.medium instances for the EKS managed node group.

## Consequences
Positive:
- Enough CPU and memory for all services
- Better stability than t3.micro
- Supports autoscaling tests

Negative:
- Higher cost than t3.micro
- Not suitable for heavy production traffic

## Alternatives Considered
- t3.micro: Too small for EKS workloads.
- t3.small: Lower cost but limited memory.
- t3.medium: Best balance of cost and performance for this assignment.