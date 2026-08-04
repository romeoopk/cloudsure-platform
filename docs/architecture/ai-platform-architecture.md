# AI Platform Architecture

**Project:** CloudSure - AI Native Insurance Platform

**Version:** 1.0

---

# Purpose

This document defines the AI architecture used by CloudSure.

The platform adopts an AI-native approach in which artificial intelligence augments business operations, improves customer experiences, and generates measurable business value.

AI acts as a decision-support system and not as an autonomous decision maker.

---

# AI Principles

## Human-in-the-Loop

AI provides recommendations.

Humans make final business decisions.

Examples:

- Claim Approval
- Claim Rejection
- Fraud Escalation

---

## Explainability

AI outputs must be explainable.

Recommendations should include:

- Supporting data
- Documents consulted
- Confidence score

---

## Auditability

AI-generated recommendations shall be stored for future review.

---

## Provider Agnostic Architecture

CloudSure shall avoid vendor lock-in.

Supported providers may include:

- Ollama
- Azure OpenAI
- AWS Bedrock
- OpenAI
- Anthropic

---

# Initial AI Stack

## LLM Platform

```text
Ollama
```

---

## Chat Model

```text
Qwen3 8B
```

---

## Embedding Model

```text
nomic-embed-text
```

---

## Framework

```text
Spring AI
```

---

## Vector Database

```text
PostgreSQL + pgvector
```

---

# AI Architecture

```text
                    Users
                       |
                       v

                 AI Service
                       |
          --------------------------
          |                        |
          v                        v

       RAG Engine            Agent Layer
          |                        |
          --------------------------
                       |
                       v

                  Spring AI
                       |
                       v

                    Ollama
                       |
                       v

                 Qwen3 Model

```

---

# AI Components

## RAG Platform

Responsible for:

- Document ingestion
- Embedding generation
- Similarity search
- Context retrieval

---

## Agent Platform

Responsible for:

- Tool calling
- Multi-step workflows
- Business recommendations

---

## Embedding Platform

Responsible for:

- Text embeddings
- Semantic search
- Knowledge indexing

---

# Knowledge Sources

CloudSure shall support:

## Policy Documents

Examples:

- Auto Policies
- Home Policies
- Life Policies

---

## Coverage Documents

Examples:

- Coverage Terms
- Exclusions
- Deductibles

---

## Claim Guidelines

Examples:

- Claim Procedures
- Review Standards

---

## Fraud Manuals

Examples:

- Investigation Procedures
- Risk Indicators

---

# AI Capabilities

## Insurance Copilot

Customer-facing assistant.

---

## Claims Investigation Assistant

Adjuster support.

---

## Fraud Investigation Assistant

Fraud support.

---

## Executive Insights Assistant

Executive dashboard support.

---

# Future Enhancements

Potential future additions:

- Multi-Agent Systems
- Bedrock Integration
- Local Fine-Tuning
- Agent Memory
- Voice Interfaces

---