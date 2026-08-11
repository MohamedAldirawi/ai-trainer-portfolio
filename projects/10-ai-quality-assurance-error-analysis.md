# AI Quality Assurance & Error Analysis

## Project Overview

This project demonstrates a structured quality-assurance workflow for reviewing AI-generated responses, identifying actual errors, classifying them, determining severity, analyzing likely causes, and verifying corrections.

A central principle is **do not classify an apparent error until it has been independently verified**.

> **Portfolio status:** Simulated self-directed QA case study.

## Objective

Create a repeatable QA process that produces consistent, evidence-based decisions about AI response quality.

## Error Taxonomy

| Category | Description |
|---|---|
| Factual | Verifiable information is incorrect |
| Numerical | Arithmetic or numerical result is wrong |
| Logical | Conclusion does not follow from evidence |
| Instruction Following | Explicit user requirement is not satisfied |
| Relevance | Response contains material unrelated content |
| Completeness | Required information is missing |
| Formatting | Required structure is not followed |
| Hallucination | Unsupported or fabricated information |
| Domain-specific | Error in accounting, finance, business, or another domain |

## Severity Framework

| Severity | Decision rule |
|---|---|
| Critical | Could materially mislead a high-impact decision or fundamentally invalidate the answer |
| High | Major error affecting the core answer |
| Medium | Meaningful issue that reduces reliability or usefulness |
| Low | Minor issue with limited practical impact |

## QA Workflow

**User Request → Expected Requirements → AI Response → Independent Verification → Error Detection → Classification → Severity → Root Cause → Correction → Re-test → Final Decision**

## Practical Case Study — Financial Calculation

### User Request

> "A company has revenue of $500,000, COGS of $300,000, and operating expenses of $120,000. Calculate operating profit."

### AI Response

> "Operating profit = $500,000 − $300,000 = $200,000."

### Independent Verification

The AI response calculates gross profit but stops before deducting operating expenses.

**Correct formula:**

Operating Profit = Revenue − COGS − Operating Expenses

**$500,000 − $300,000 − $120,000 = $80,000**

### Error Record

| Field | Decision |
|---|---|
| Error type | Domain-specific / numerical reasoning |
| Severity | High |
| Root cause | Incomplete processing of the financial formula |
| Correct result | $80,000 |
| Correction required | Yes |

## Practical Case Study — Apparent Error That Is Actually Correct

### User Request

> "A company has $50,000 in revenue and $35,000 in expenses. What is its profit margin?"

### AI Response

> "Profit is $15,000, so profit margin is 30%."

### Verification

Profit = $50,000 − $35,000 = **$15,000**

Profit Margin = $15,000 ÷ $50,000 × 100 = **30%**

### Final QA Decision

**Pass — no error confirmed.**

This case is deliberately important: an evaluator may initially suspect a calculation error, but independent verification shows that the response is correct.

## Root Cause Analysis

When a real error is confirmed, investigate likely causes:

- Misread user requirement
- Incorrect formula selection
- Missing context
- Arithmetic mistake
- Concept confusion
- Unsupported assumption
- Failure to process all input information
- Instruction-following failure

The root cause should be supported by the observed response rather than guessed.

## Error Log Template

| ID | Category | Severity | Evidence | Root Cause | Action |
|---|---|---|---|---|---|
| E001 | Numerical | High | Wrong calculation | Arithmetic/formula error | Recalculate |
| E002 | Instruction | Medium | Wrong format | Requirement missed | Reformat |
| E003 | Factual | High | Incorrect claim | Verification failure | Fact-check |
| E004 | Relevance | Low | Unrelated content | Scope control failure | Remove |

## Correction Verification

A correction is not complete until the evaluator checks that:

1. The original error is fixed.
2. The correction does not introduce a new error.
3. All user requirements are still satisfied.
4. Numerical values remain consistent.
5. The final response is clear and relevant.

## QA Metrics for Larger Evaluations

For a larger evaluation set, useful metrics include:

- Pass rate
- Error rate
- Critical/high-severity error rate
- Error-category distribution
- Correction success rate
- Re-review failure rate
- Agreement between evaluators

## Business & Finance QA Checks

Financial responses require additional checks for:

- Accounting terminology
- Formula selection
- Numerical calculations
- Units and currencies
- Revenue/profit distinctions
- Asset/liability classification
- Cash-flow interpretation
- Financial-ratio definitions
- Unsupported business conclusions

## Skills Demonstrated

- AI Quality Assurance
- Error Analysis
- Root Cause Analysis
- Response Evaluation
- Financial Analysis
- Accounting
- Numerical Verification
- Data Annotation
- Fact Checking
- Quality Control
- Structured Reasoning

## Recruiter Takeaway

This project demonstrates an important AI-training capability: **systematic quality control**. The evaluator does not rely on intuition alone; they verify the output, document evidence, classify errors consistently, correct them, and perform a second quality check.
