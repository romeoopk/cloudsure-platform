# ADR-006: AI Provider Strategy

## Status

Accepted

## Date

July 2026

---

# Context

CloudSure requires AI capabilities for:

- Insurance Copilot
- Claims Summaries
- Claims Investigation
- Executive Insights

Cost efficiency and provider flexibility are required.

---

# Decision

Spring AI shall be used as the abstraction layer.

Initial provider:

- Ollama

Initial models:

- Qwen3 8B
- nomic-embed-text

---

# Future Providers

CloudSure may later integrate:

- Azure OpenAI
- AWS Bedrock
- OpenAI
- Anthropic

without changing business logic.

---

# Rationale

Benefits:

- Zero development cost
- Local execution
- Provider independence

---

# Consequences

Positive:

- Reduced operating costs
- Flexible architecture

Negative:

- Reduced performance compared to larger hosted models

---