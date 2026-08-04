# Deployment Architecture

**Project:** CloudSure - AI Native Insurance Platform

**Version:** 1.0

---

# Purpose

This document defines the deployment architecture used by CloudSure across local development and AWS environments.

CloudSure follows cloud-native deployment principles based on:

- Containers
- Kubernetes
- Infrastructure as Code
- Continuous Delivery

---

# Deployment Strategy

CloudSure supports:

```text
Local Development
Test Environment
Staging Environment
Production Environment
```

through a consistent Kubernetes deployment model.

---

# High-Level Deployment Architecture

```text
Developer

     |

 Docker Images

     |

 Container Registry

     |

 Kubernetes

     |

 Spring Boot Services
```

---

# Containerization

All services shall be packaged as Docker images.

Examples:

- Identity Service
- Customer Service
- Policy Service
- Claims Service
- AI Service

---

# Kubernetes Platform

CloudSure will use Kubernetes as the standard runtime platform.

---

# Local Development

Platform:

```text
Kind
```

Infrastructure:

```text
MacBook
Docker
Kind
Helm
```

---

# AWS Deployment

Platform:

```text
Amazon EKS
```

Supporting Services:

```text
Amazon ECR
Amazon RDS
Amazon S3
Secrets Manager
CloudWatch
```

---

# Deployable Components

## Stateless Components

- Identity Service
- Customer Service
- Policy Service
- Claims Service
- Fraud Service
- Notification Service
- AI Service
- Executive Insights Service

---

## Stateful Components

- PostgreSQL
- MongoDB
- Redis
- Kafka

---

# Kubernetes Resources

Each service shall contain:

```text
Deployment
Service
ConfigMap
Secret
Ingress
```

---

# Helm Strategy

Every service shall have its own Helm chart.

Examples:

```text
identity-service-chart

claims-service-chart

ai-service-chart
```

---

# Ingress Strategy

External traffic enters through:

```text
Ingress Controller
```

Future:

```text
AWS ALB Controller
```

---

# Scaling Strategy

Horizontal scaling shall be supported.

Examples:

```text
Claims Service

2 Pods
→
20 Pods
```

based on load.

---

# CI/CD Integration

Deployment flow:

```text
GitHub Commit

      |

GitHub Actions

      |

Docker Build

      |

Container Registry

      |

Helm Deployment

      |

Kubernetes
```

---

# Availability Goals

Target:

```text
99.9%
```

service availability.

---

# Future Enhancements

- Multi-Region Deployments
- GitOps with ArgoCD
- Service Mesh
- Canary Deployments
- Blue/Green Deployments

---