# Environment Strategy

**Project:** CloudSure - AI Native Insurance Platform

---

# Purpose

Defines all environments used throughout the software development lifecycle.

---

# Environment Overview

```text
Local

↓

Development

↓

Test

↓

Staging

↓

Production
```

---

# Local Environment

## Purpose

Developer productivity.

---

## Platform

```text
MacBook
Docker
Kind
```

---

## Services

- PostgreSQL
- MongoDB
- Redis
- Kafka
- Ollama
- Spring Boot Services

---

# Development Environment

## Purpose

Shared integration environment.

---

## Goals

- Integration testing
- Team validation

---

# Test Environment

## Purpose

System testing.

---

## Activities

- Functional Testing
- API Testing
- Automated Tests

---

# Staging Environment

## Purpose

Production simulation.

---

## Activities

- User Acceptance Testing
- Performance Testing
- Release Validation

---

# Production Environment

## Purpose

Live customer traffic.

---

## Platform

```text
AWS EKS
```

---

# Configuration Strategy

Application configuration separated by profile.

Examples:

```text
local
dev
test
staging
prod
```

---

# Data Strategy

Production data never copied directly to lower environments.

---

# Secrets Strategy

Local:

```text
Environment Variables
```

AWS:

```text
Secrets Manager
```

---

# Promotion Path

```text
Local

↓

Dev

↓

Test

↓

Staging

↓

Production
```

---

# Environment Ownership

| Environment | Owner |
|-------------|--------|
| Local | Developer |
| Dev | Engineering Team |
| Test | QA Team |
| Staging | Operations Team |
| Production | Platform Team |

---