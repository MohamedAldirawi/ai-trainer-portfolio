# Evidence Sample — Prompt Iteration

> **Status:** Simulated, self-directed portfolio exercise.

## Objective

Improve an AI prompt so that a business explanation is accurate, concise, audience-appropriate, and numerically grounded.

## Version 1 — Baseline

**Prompt:**

> Explain gross profit and net profit.

### Weaknesses

- Audience is unspecified.
- No required structure.
- No numerical example.
- No instruction to distinguish COGS from other expenses.

## Version 2 — Structured

> Explain the difference between gross profit and net profit to a small-business owner in simple English. Define both terms and give one numerical example.

### Improvement

The task now specifies audience, language level, required definitions, and an example.

## Version 3 — Quality-Controlled

> Explain the difference between gross profit and net profit to a small-business owner in simple English. Define both terms, distinguish COGS from other expenses, and provide one numerical example using revenue, COGS, and operating expenses. Do not invent additional financial figures beyond those needed for the example.

### Improvement

The final prompt adds a domain-specific distinction and controls unnecessary assumptions.

## Evaluation Matrix

| Criterion | V1 | V2 | V3 |
|---|---:|---:|---:|
| Audience clarity | 1/5 | 5/5 | 5/5 |
| Required content | 1/5 | 5/5 | 5/5 |
| Domain precision | 2/5 | 4/5 | 5/5 |
| Output control | 1/5 | 4/5 | 5/5 |
| Ambiguity control | 1/5 | 4/5 | 5/5 |

## Final Decision

**Version 3** is preferred because it provides clearer requirements while controlling domain ambiguity and unsupported assumptions.

## Capability Demonstrated

Prompt decomposition, iterative refinement, constraint design, domain-aware prompt engineering, and comparative evaluation.
