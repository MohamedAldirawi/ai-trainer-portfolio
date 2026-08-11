# AI Hallucination Detection & Fact Checking

## Project Overview

This project demonstrates a structured workflow for identifying factual errors, unsupported claims, numerical mistakes, fabricated information, and overconfident statements in AI-generated responses.

The focus is not simply to label a response as "wrong." The evaluator must identify the specific claim, verify it, classify the error, assess severity, and produce a defensible correction.

> **Portfolio status:** Simulated self-directed case study demonstrating an AI evaluation workflow.

## Objective

Build a repeatable fact-checking workflow that separates:

- Correct information
- Incorrect information
- Unsupported claims
- Uncertain claims requiring verification
- Numerical or logical errors
- Overconfident conclusions

## Hallucination Taxonomy

| Type | Description | Example |
|---|---|---|
| Factual | Incorrect verifiable claim | Wrong founding year |
| Numerical | Incorrect number or calculation | $100 − $70 = $40 |
| Source | Invented or misrepresented source | Fabricated citation |
| Entity | Wrong person, organization, or place | Incorrect headquarters |
| Definition | Incorrect explanation of a concept | Misstating profit |
| Logical | Conclusion does not follow from evidence | Invalid inference |
| Unsupported | Claim lacks adequate evidence | "Always reduces costs" |
| Confidence | Certainty exceeds available evidence | Presenting uncertainty as fact |

## Evaluation Rubric

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Claim identification | Missed claims | Some claims identified | All material claims identified |
| Verification | Not verified | Partially verified | Material claims independently verified |
| Error classification | Incorrect/missing | Partially correct | Correct and specific |
| Severity | Unsupported | Plausible | Evidence-based |
| Correction | Missing | Partially correct | Accurate and appropriately qualified |

**Maximum score: 10 points.**

## Fact-Checking Workflow

1. Extract each material factual claim.
2. Separate facts from opinions and interpretations.
3. Identify which claims require external verification.
4. Verify important claims using authoritative or otherwise reliable sources.
5. Recalculate numerical claims independently.
6. Check entities, dates, definitions, and relationships.
7. Record evidence and uncertainty.
8. Classify each confirmed issue.
9. Assign severity based on potential impact.
10. Produce a corrected response without introducing new unsupported claims.

## Practical Case Study — Numerical Hallucination

### User Request

> "A company has revenue of $100,000 and expenses of $70,000. What is its profit?"

### AI Response

> "The company's profit is $40,000."

### Claim Verification

| Claim | Verification | Result |
|---|---|---|
| Revenue = $100,000 | Given by user | ✅ |
| Expenses = $70,000 | Given by user | ✅ |
| Profit = $40,000 | $100,000 − $70,000 | ❌ |

### Correct Calculation

**Profit = Revenue − Expenses**

**Profit = $100,000 − $70,000 = $30,000**

### Error Record

| Field | Decision |
|---|---|
| Error type | Numerical / calculation error |
| Severity | High |
| Evidence | User-provided figures |
| Correct result | $30,000 |
| Required action | Replace incorrect calculation |

### Corrected Response

> "The company's profit is **$30,000**, calculated as $100,000 in revenue minus $70,000 in expenses."

## Practical Case Study — Unsupported Generalization

### AI Response

> "Companies that use AI always reduce operating costs."

### Evaluation

**Status:** Unsupported claim

The word **"always"** makes the statement absolute. Whether AI reduces costs depends on implementation costs, labor structure, technology costs, process changes, industry, and the specific use case.

### Better Response

> "AI can reduce certain operating costs in some situations, but the financial impact depends on implementation costs, the use case, and how the technology changes existing processes."

## Practical Case Study — Factual Verification

### AI Response

> "The World Health Organization was founded in 1950 and is headquartered in New York City."

### Evaluation

The statement contains material factual errors. A professional evaluator should verify both claims against authoritative information before accepting or correcting them.

**Classification:** Factual hallucination

**Severity:** High

The key lesson is that plausible wording and confident tone are not evidence of accuracy.

## Quality-Control Rules

- Never treat confidence as proof.
- Verify high-impact claims independently.
- Recalculate numerical claims separately.
- Distinguish an unverified claim from a confirmed false claim.
- Record the evidence supporting each correction.
- Avoid replacing one unsupported claim with another.
- Re-check the corrected response before finalizing it.

## Business & Finance Application

Hallucination detection is particularly important for AI outputs involving accounting, financial analysis, financial statements, business decisions, economic information, banking, taxation concepts, market information, and numerical calculations.

A small numerical or terminology error can materially change a financial conclusion, so domain-aware verification is essential.

## Skills Demonstrated

- AI Response Evaluation
- Hallucination Detection
- Fact Checking
- Error Classification
- Numerical Verification
- Evidence-Based Reasoning
- Business & Finance Domain Evaluation
- Quality Assurance
- Critical Thinking
- Confidence Calibration

## Recruiter Takeaway

This project demonstrates the ability to turn a vague concern such as "the AI may be hallucinating" into a **repeatable evaluation workflow with claim extraction, verification, error taxonomy, severity assessment, correction, and quality control**.
