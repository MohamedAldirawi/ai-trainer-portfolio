# Project 02 — Prompt Engineering & Iterative Refinement

## Project Type

**Simulated portfolio case study / self-directed practice**

## Objective

Design and refine prompts that produce responses that are more accurate, relevant, consistent, and aligned with explicit user requirements.

The focus is not on writing longer prompts. It is on identifying ambiguity, adding only useful constraints, and evaluating whether the revised prompt improves the expected output.

## Task Scenario

A small-business owner asks an AI assistant to explain the difference between **revenue and profit** to a beginner.

### Original Prompt

> Explain profit and revenue.

### Problems in the Original Prompt

| Issue | Risk |
|---|---|
| No target audience | Response may be too technical or too basic |
| No required scope | Important distinctions may be omitted |
| No output structure | Responses may be inconsistent |
| No practical example | Concept may remain abstract |
| No length guidance | Response may be unnecessarily long |

## Prompt Refinement

### Version 1 — Basic

> Explain the difference between revenue and profit.

### Version 2 — Structured

> Explain the difference between revenue and profit for a beginner in business. Use simple language, define both terms, explain their relationship, and provide one practical numerical example. Keep the answer concise and use clear headings.

### Version 3 — Evaluation-Oriented

> Act as a business fundamentals instructor. Explain the difference between revenue and profit for a beginner with no accounting background. Define each term precisely, explain the relationship between them, and provide one small-business numerical example. Use the format: **Definition → Difference → Example → Key takeaway**. Avoid unnecessary accounting terminology and do not introduce concepts that are not needed to answer the question.

## Why Version 3 Is Stronger

It specifies:

- **Role:** business fundamentals instructor
- **Audience:** beginner with no accounting background
- **Objective:** explain and distinguish two concepts
- **Accuracy requirement:** precise definitions
- **Evidence requirement:** numerical example
- **Output format:** four explicit sections
- **Constraints:** avoid unnecessary terminology and scope expansion

## Evaluation Rubric

The expected output can be evaluated using a 25-point rubric:

| Criterion | Weight | What good performance means |
|---|---:|---|
| Accuracy | 5 | Definitions and example are financially correct |
| Relevance | 5 | Every part directly supports the requested explanation |
| Instruction Following | 5 | Required structure, audience, and constraints are followed |
| Clarity | 5 | Beginner can understand the explanation without specialist knowledge |
| Completeness | 5 | Revenue, profit, relationship, and example are all covered |

### Decision Rule

- **22–25:** Strong response
- **18–21:** Acceptable; minor refinement recommended
- **13–17:** Needs improvement
- **0–12:** Major revision required

## Example Expected Output

### Definition

**Revenue** is the income a business generates from selling goods or services before expenses are deducted.

**Profit** is the amount remaining after the relevant business expenses are deducted from revenue.

### Difference

Revenue measures the value generated from sales, while profit measures what remains after expenses.

### Example

A small business generates **$10,000 in revenue** and has **$7,000 in expenses**.

- Revenue = $10,000
- Expenses = $7,000
- Profit = $3,000

### Key takeaway

A business can have high revenue but low profit if its expenses are high.

## Quality Review of the Example

| Criterion | Score | Rationale |
|---|---:|---|
| Accuracy | 5/5 | Definitions and calculation are correct |
| Relevance | 5/5 | No unnecessary concepts are introduced |
| Instruction Following | 5/5 | Uses the requested structure and beginner-friendly language |
| Clarity | 5/5 | Terms are explained in plain language |
| Completeness | 5/5 | Covers definitions, difference, example, and takeaway |
| **Total** | **25/25** | **Strong** |

## Failure Modes to Watch For

During prompt evaluation, the reviewer should look for:

1. **Definition drift** — treating revenue as profit.
2. **Calculation errors** — incorrect subtraction in the example.
3. **Audience mismatch** — using unexplained accounting terminology.
4. **Instruction failure** — ignoring the required structure.
5. **Scope creep** — adding unrelated financial concepts.
6. **Unsupported claims** — presenting assumptions as universal rules.

## Refinement Workflow

1. Define the user objective.
2. Identify ambiguity in the original prompt.
3. Add the minimum useful context.
4. Specify audience and output requirements.
5. Add relevant constraints.
6. Generate or review the resulting response.
7. Score the response against a fixed rubric.
8. Identify failure modes.
9. Refine the prompt.
10. Re-evaluate the revised output.

## Business & Finance Applications

The same workflow can be applied to:

- Financial statement explanations
- Accounting classification
- Budget analysis
- Business case evaluation
- Financial ratio explanations
- Market and business research prompts
- Financial-data interpretation
- Customer-support knowledge tasks

## Skills Demonstrated

- Prompt engineering
- Prompt refinement
- Instruction design
- Evaluation rubric design
- Output-quality assessment
- Error identification
- Business and finance reasoning
- Structured analytical thinking

## Portfolio Integrity Note

This is a **simulated portfolio case study created through self-directed practice**. It demonstrates a repeatable prompt-design and evaluation methodology; it does not claim professional employment experience as an AI prompt engineer.
