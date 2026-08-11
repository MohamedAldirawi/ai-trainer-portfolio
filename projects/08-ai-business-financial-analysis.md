# AI Business & Financial Analysis

## Project Overview

This project demonstrates how accounting and financial-analysis knowledge can be applied to AI evaluation tasks involving calculations, financial relationships, business reasoning, assumptions, and interpretation.

The evaluator does not only check whether an answer contains the correct number. The workflow verifies the calculation, accounting relationship, assumptions, interpretation, and alignment with the user's request.

> **Portfolio status:** Simulated self-directed case study demonstrating domain-aware AI evaluation.

## Objective

Evaluate whether AI-generated business and financial analysis is:

- Numerically accurate
- Financially and logically sound
- Relevant to the business question
- Complete enough for the requested task
- Clear about assumptions and limitations

## Analytical Workflow

1. Extract the financial inputs.
2. Identify the required metric or accounting relationship.
3. Perform the calculation independently.
4. Compare the AI calculation with the verified result.
5. Check terminology and accounting logic.
6. Review assumptions and missing information.
7. Evaluate the business interpretation.
8. Record errors and recommend corrections.

## Core Evaluation Rubric

| Criterion | Weight | What is checked |
|---|---:|---|
| Numerical accuracy | 25% | Arithmetic and formulas |
| Financial logic | 20% | Correct accounting relationships |
| Interpretation | 20% | Conclusion follows from results |
| Relevance | 15% | Answers the requested business question |
| Completeness | 10% | Important inputs and limitations considered |
| Clarity | 10% | Explanation is understandable |

## Practical Case Study — Profitability Analysis

### User Request

> "A company generated $120,000 in revenue. COGS was $70,000, operating expenses were $30,000, and interest and taxes totaled $5,000. Calculate gross profit and net profit and explain the difference."

### AI Response

> "Gross profit is $50,000 and net profit is $15,000. Gross profit is revenue minus COGS, while net profit is what remains after operating expenses, interest, and taxes."

### Independent Verification

| Metric | Calculation | Verified result |
|---|---|---:|
| Gross profit | $120,000 − $70,000 | **$50,000** |
| Net profit | $50,000 − $30,000 − $5,000 | **$15,000** |
| Gross margin | $50,000 ÷ $120,000 | **41.7%** |
| Net margin | $15,000 ÷ $120,000 | **12.5%** |

### Evaluation

| Criterion | Result |
|---|---|
| Numerical accuracy | Pass |
| Financial logic | Pass |
| Interpretation | Pass |
| Relevance | Pass |
| Completeness | Pass |
| Clarity | Pass |

**Overall assessment: 5/5 — Pass**

## Practical Case Study — Inventory / COGS

### Inputs

- Opening inventory: $80,000
- Purchases: $250,000
- Closing inventory: $70,000

### Verification

**COGS = Opening Inventory + Purchases − Closing Inventory**

**COGS = $80,000 + $250,000 − $70,000 = $260,000**

### AI Evaluation Check

An AI answer should use the correct inventory relationship and should not confuse purchases with COGS.

## Common AI Financial Errors

| Error | Example | Evaluation response |
|---|---|---|
| Calculation error | Wrong subtraction | Recalculate independently |
| Formula error | Wrong numerator/denominator | Verify formula |
| Concept confusion | Revenue treated as profit | Check definitions |
| Ratio confusion | Gross margin vs net margin | Verify metric definition |
| Cash/profit confusion | Cash movement treated as profit | Check accounting context |
| Unsupported conclusion | Profit increase means business is healthier | Request supporting evidence |
| Missing assumption | No period or currency specified | Flag limitation |

## Assumption Control

A domain-aware evaluator should identify assumptions such as:

- Reporting period
- Currency
- Whether figures are totals or averages
- Whether taxes and interest are included
- Whether the requested profit measure is gross, operating, or net
- Whether sufficient data is available for a reliable conclusion

When the information is insufficient, the evaluator should **state the limitation rather than inventing an assumption silently**.

## Error Analysis Workflow

**Input → Formula/Rule → Independent Calculation → AI Comparison → Domain Check → Interpretation Check → Final Decision**

## Skills Demonstrated

- Accounting
- Financial Analysis
- Business Analysis
- Numerical Reasoning
- AI Response Evaluation
- Domain-Aware Quality Assurance
- Error Detection
- Assumption Analysis
- Data Interpretation
- Structured Reasoning

## Recruiter Takeaway

This project demonstrates a practical combination of **finance/accounting domain expertise and AI evaluation methodology**. The strongest evidence is the independent verification step: the evaluator checks the AI's calculations and reasoning instead of simply accepting a plausible-looking answer.
