# ADR-003: Kubernetes Deployment Strategy

## Status
Accepted

## Context
CloudMart microservices require zero-downtime deployment support and high availability during updates. Kubernetes deployments must support scaling, rolling updates, and automated recovery.

## Decision
Use Kubernetes Deployments with RollingUpdate strategy.

## Consequences

### Positive
- Zero-downtime deployments
- Safer updates
- Automatic pod replacement
- Better application availability
- Supports autoscaling

### Negative
- Slightly slower deployment process
- Requires additional Kubernetes configuration

## Alternatives Considered
- Recreate deployment strategy
- Blue/Green deployments
- Canary deployments

RollingUpdate was selected because it provides stable deployments with minimal complexity.