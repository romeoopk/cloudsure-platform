# RAID Log

**Project:** CloudSure - AI Native Insurance Platform  
**Version:** 1.0  
**Status:** Active  
**Owner:** Project Manager  
**Last Updated:** July 2026

---

# Purpose

The RAID Log is a centralized project management artifact used to track:

- Risks
- Assumptions
- Issues
- Dependencies

The log provides visibility into project health and supports proactive decision making.

---

# RAID Overview

## Risks

Potential future events that may negatively impact the project.

---

## Assumptions

Conditions believed to be true for planning purposes.

---

## Issues

Current problems requiring action.

---

## Dependencies

Items that the project relies upon for successful delivery.

---

# Risks

| ID | Description | Owner | Priority | Status |
|----|-------------|---------|----------|---------|
| R-001 | Project complexity exceeds available delivery capacity | Project Manager | High | Open |
| R-002 | AWS infrastructure costs exceed planned budget | Architecture Lead | Medium | Open |
| R-003 | Excessive technology adoption slows project delivery | Architecture Lead | High | Open |
| R-004 | AI costs increase during future cloud deployments | AI Lead | Medium | Mitigated |
| R-005 | Security implementation delayed until late phases | Architecture Lead | High | Open |
| R-006 | Event-driven architecture becomes inconsistent across services | Architecture Lead | Medium | Open |
| R-007 | Observability implementation delayed | Platform Engineer | Medium | Open |
| R-008 | Scalability assumptions remain unvalidated | Architecture Lead | Medium | Open |

---

# Assumptions

| ID | Assumption | Owner |
|----|------------|---------|
| A-001 | Java 21 remains the approved platform baseline | Architect |
| A-002 | Spring Boot remains the primary application framework | Architect |
| A-003 | Kubernetes will be used for container orchestration | Platform Engineer |
| A-004 | Docker or OrbStack remains available during development | Platform Engineer |
| A-005 | Ollama remains available for local AI development | AI Lead |
| A-006 | PostgreSQL will support transactional workloads | Database Lead |
| A-007 | Kafka will serve as event backbone | Architecture Lead |
| A-008 | AWS remains the target cloud platform | Architecture Lead |

---

# Issues

| ID | Description | Owner | Priority | Status |
|----|-------------|---------|----------|---------|
| I-001 | No active project issues identified | Project Manager | Low | Open |

---

# Dependencies

| ID | Dependency | Owner | Status |
|----|------------|---------|---------|
| D-001 | Java 21 | Engineering Team | Available |
| D-002 | Maven | Engineering Team | Available |
| D-003 | Docker / OrbStack | Platform Team | Available |
| D-004 | Kind Kubernetes | Platform Team | Pending |
| D-005 | Helm | Platform Team | Pending |
| D-006 | PostgreSQL | Database Team | Planned |
| D-007 | Redis | Platform Team | Planned |
| D-008 | Kafka | Platform Team | Planned |
| D-009 | MongoDB | Database Team | Planned |
| D-010 | Ollama | AI Team | Planned |
| D-011 | GitHub Actions | Platform Team | Planned |
| D-012 | AWS Account | Cloud Team | Future Phase |

---

# RAID Review Process

## Weekly

Conducted during:

- Sprint Planning
- Sprint Review

Activities:

- Review Issues
- Review Risks
- Identify New Dependencies
- Validate Assumptions

---

## Monthly

Conducted during:

- Project Health Review
- Architecture Review

Activities:

- Reassess Risk Priority
- Close Resolved Issues
- Validate Assumptions

---

## Quarterly

Conducted during:

- Steering Committee Review

Activities:

- Strategic Risk Analysis
- Delivery Readiness Assessment

---

# Escalation Rules

Escalation is required when:

- A risk becomes an active issue.
- A dependency threatens a milestone.
- A critical issue remains unresolved for more than one sprint.
- Budget, security, or compliance impacts are identified.

---

# Related Documents

- Risk Register
- Risk Management Plan
- Change Management Plan
- Milestone Register
- Project Management Plan

---