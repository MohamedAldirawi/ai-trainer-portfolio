# Evidence Sample — AI Response Evaluation

> **Status:** Simulated, self-directed portfolio exercise.

## Task

Evaluate an AI response to this request:

> "Explain the difference between revenue and profit to a small-business owner in simple language and give one numerical example."

## Initial AI Response

> "Revenue is the money a business makes, while profit is the money it earns. If the business makes $10,000, its profit is $10,000."

## Evaluation

| Criterion | Score | Finding |
|---|---:|---|
| Accuracy | 1/5 | Profit is incorrectly treated as equal to revenue. |
| Relevance | 5/5 | Directly addresses the requested topic. |
| Instruction following | 4/5 | Includes an example but the example is incorrect. |
| Clarity | 5/5 | Language is simple and understandable. |
| Completeness | 2/5 | Does not explain the role of expenses. |

**Total: 17/25**

## Error Annotation

| Field | Decision |
|---|---|
| Error Type | Financial conceptual / numerical error |
| Severity | High |
| Evidence | The response states that $10,000 of revenue is $10,000 of profit. |
| Rationale | Profit is determined after relevant expenses are deducted from revenue. |
| Corrective Action | Correct the definition and numerical example. |

## Improved Response

Revenue is the total amount a business generates from selling products or services. Profit is the amount left after relevant expenses are deducted from revenue.

For example, if a business has $10,000 in revenue and $7,000 in expenses, its profit is $3,000.

## Independent QA

- [x] Revenue definition is correct.
- [x] Profit definition is correct.
- [x] Numerical example is arithmetically correct.
- [x] The original instruction is satisfied.
- [x] The explanation remains simple.

**Final status: Approved**

## Capability Demonstrated

This artifact demonstrates requirement checking, rubric-based evaluation, financial-domain verification, structured error annotation, response correction, and independent quality control.
