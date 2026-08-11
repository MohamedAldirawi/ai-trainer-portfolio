# Business & Finance AI Training

## Project Overview

This project demonstrates how accounting, finance, economics, and business knowledge can be applied to AI training and response evaluation.

The focus is on **domain accuracy, numerical reasoning, terminology, assumptions, and instruction following** in business and finance tasks.

> **Portfolio status:** Simulated self-directed exercise demonstrating domain application to AI training. It does not claim professional AI employment experience.

## Objective

Develop a repeatable framework for evaluating AI-generated business and finance responses and identifying errors that a general evaluator might miss without domain knowledge.

## Domain Coverage

- Accounting
- Financial Analysis
- Financial Management
- Business Administration
- Economics
- Digital Economy
- Financial Markets
- Banking and Financial Services
- Marketing
- E-commerce
- Business Operations

## Domain Evaluation Framework

| Criterion | What the evaluator checks |
|---|---|
| Financial accuracy | Definitions, calculations, and relationships are correct |
| Terminology | Accounting and finance terms are used appropriately |
| Numerical reasoning | Arithmetic and financial logic are correct |
| Assumptions | Missing information and assumptions are identified |
| Relevance | The response answers the actual business question |
| Clarity | The explanation is understandable to the target audience |
| Instruction following | Required format, scope, and constraints are respected |

## Case Study: Gross Profit vs Net Profit

### User Request

> "What is the difference between gross profit and net profit? Give a simple numerical example."

### AI-Generated Response

> "Gross profit is revenue minus the cost of goods sold. Net profit is the amount remaining after all business expenses, including operating expenses, interest, and taxes, are deducted."

### Evaluation

| Criterion | Assessment | Score |
|---|---|---:|
| Financial accuracy | Core definitions are correct. | 5/5 |
| Terminology | Appropriate accounting terminology is used. | 5/5 |
| Relevance | Directly answers the question. | 5/5 |
| Completeness | No numerical example was provided despite the instruction. | 3/5 |
| Clarity | Concise and understandable. | 5/5 |
| Instruction following | Misses an explicit requirement. | 4/5 |

**Total: 27/30**

### Domain-Based Improvement

A stronger answer is:

> "Gross profit is revenue minus cost of goods sold (COGS). Net profit is what remains after all applicable expenses, such as operating expenses, interest, and taxes, are deducted.
>
> Example: if revenue is $20,000 and COGS is $12,000, gross profit is $8,000. If other applicable expenses total $5,000, net profit is $3,000."

### Why This Matters

A response can be factually correct but still fail the task because it omits an explicit requirement. Domain evaluation therefore combines **subject-matter correctness with instruction-following**.

## Case Study: Numerical Reasoning

### Scenario

A company reports:

- Revenue: $500,000
- Cost of Goods Sold: $300,000
- Operating Expenses: $120,000

The expected calculation is:

**Gross Profit = $500,000 − $300,000 = $200,000**

**Operating Profit = $200,000 − $120,000 = $80,000**

### Evaluation Checks

An evaluator should verify:

1. Whether the arithmetic is correct.
2. Whether COGS was deducted before operating expenses.
3. Whether the response incorrectly calls operating profit "net profit".
4. Whether any additional assumptions are stated.
5. Whether the calculation is explained clearly.

## Domain Error Taxonomy

Common business-and-finance AI errors include:

- **Definition error** — incorrect explanation of a financial concept.
- **Calculation error** — incorrect arithmetic or formula application.
- **Classification error** — confusing assets, liabilities, revenue, expenses, or cash flows.
- **Terminology error** — using related financial terms as if they were interchangeable.
- **Assumption error** — presenting an unstated assumption as a fact.
- **Instruction error** — failing to satisfy the requested business task.
- **Reasoning error** — reaching a conclusion unsupported by the provided figures.

## Quality-Control Procedure

For each finance response:

1. Identify the exact user requirement.
2. Verify definitions against established accounting concepts.
3. Recalculate numerical results independently.
4. Check terminology and classification.
5. Identify assumptions or missing data.
6. Score the response against the rubric.
7. Produce an improved answer when needed.
8. Perform a final consistency check.

## Professional Relevance

This project demonstrates a useful combination of **domain expertise and AI evaluation methodology**. It is especially relevant to AI Trainer, AI Data Annotator, AI Response Evaluator, and Business & Finance AI Specialist roles where financial knowledge improves evaluation quality.

## Skills Demonstrated

- Accounting Domain Knowledge
- Financial Analysis
- Business Reasoning
- Numerical Verification
- AI Response Evaluation
- Error Taxonomy Design
- Quality Assurance
- Prompt and Instruction Analysis
- Structured Feedback
- Critical Thinking

## Conclusion

Domain-aware AI evaluation requires more than checking whether an answer sounds plausible. The evaluator must verify terminology, calculations, assumptions, reasoning, and compliance with the user's requirements.
