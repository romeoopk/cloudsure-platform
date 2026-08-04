# Deployment Diagram

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Defines physical deployment architecture.

---

# Local Development

```text
MacBook

    |

Docker

    |

Kind Cluster

    |

--------------------------------------

Spring Services

Kafka

Redis

PostgreSQL

MongoDB

Ollama

Prometheus

Grafana

Tempo

Loki
```

---

# AWS Deployment

```text
Internet

     |

AWS Load Balancer

     |

Amazon EKS

     |

------------------------------------------------

Identity Service

Customer Service

Policy Service

Claims Service

Document Service

Fraud Service

AI Service

Executive Insights Service

Notification Service

------------------------------------------------

Amazon RDS

Amazon S3

Amazon MSK

ElastiCache Redis

Secrets Manager
```

---

# Kubernetes Structure

Namespace examples:

```text
cloudsure-core

cloudsure-ai

cloudsure-observability
```

---

# Observability Deployment

```text
Prometheus

Grafana

Tempo

Loki

OpenTelemetry Collector
```

---

# CI/CD Deployment Flow

```text
GitHub

    |

GitHub Actions

    |

Build Docker Images

    |

Push Images

(ECR)

    |

Helm Upgrade

    |

Deploy To EKS
```

---

# Scaling Model

Services scale independently.

Examples:

```text
Claims Service

3 Pods
→
30 Pods
```

```text
AI Service

2 Pods
→
10 Pods
```

based on workload.

---

# Future Enhancements

- Multi-Region EKS
- Disaster Recovery Region
- GitOps Deployment
- Service Mesh
- Canary Releases

---