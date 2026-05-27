# ADR-002: User Service Database Selection

## Status
Accepted

## Context
The CloudMart platform requires persistent storage for user information including authentication data, profile details, and account-related records. The database solution must integrate easily with AWS infrastructure and support scalable backend services.

## Decision
PostgreSQL on Amazon RDS was selected for the user-service database.

## Consequences

### Positive
- Managed AWS database service
- Automated backups and recovery
- High reliability and availability
- Strong relational database support
- Easy integration with Kubernetes workloads

### Negative
- Higher cost compared to local databases
- Requires network and security configuration

## Alternatives Considered
- MySQL RDS
- Self-hosted PostgreSQL in Kubernetes
- DynamoDB

PostgreSQL on RDS was selected because of reliability, scalability, and relational database features.