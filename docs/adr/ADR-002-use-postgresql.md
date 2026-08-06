# ADR-002: Adopt PostgreSQL As Primary Relational Database

## Status

Accepted

## Date

July 2026

---

# Context

CloudSure requires:

- Transactional consistency
- Strong relational modeling
- ACID guarantees
- Cloud portability

---

# Decision

PostgreSQL will be the primary transactional database.

---

# Rationale

PostgreSQL provides:

- Mature ecosystem
- Strong SQL support
- ACID transactions
- Open source licensing
- Cloud portability

---

# Usage

Primary usage:

- Customers
- Policies
- Claims
- Executive Metrics

---

# Consequences

Positive:

- Reliable transactional processing
- Strong community support

Negative:

- Horizontal scaling requires additional strategies

---