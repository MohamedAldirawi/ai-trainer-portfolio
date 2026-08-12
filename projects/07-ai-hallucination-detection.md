# AI Hallucination Detection & Fact Checking

## Project Overview

This project demonstrates a structured workflow for identifying factual errors, unsupported claims, numerical mistakes, fabricated information, and overconfident statements in AI-generated responses.

The focus is not simply to label a response as "wrong." The evaluator must identify the specific claim, verify it against evidence, classify the error, assess severity, document uncertainty, and produce a defensible correction.

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
| Evidence trail | Missing | Incomplete | Claim, evidence, and decision are traceable |
| Error classification | Incorrect/missing | Partially correct | Correct and specific |
| Severity | Unsupported | Plausible | Evidence-based |
| Correction | Missing | Partially correct | Accurate and appropriately qualified |

**Maximum score: 12 points.**

## Fact-Checking Workflow

1. Extract each material factual claim.
2. Separate facts from opinions and interpretations.
3. Identify which claims require external verification.
4. Select an authoritative or otherwise reliable source appropriate to the claim.
5. Record the source or evidence used for the decision.
6. Compare the claim against the evidence and record the verification status.
7. Recalculate numerical claims independently.
8. Check entities, dates, definitions, and relationships.
9. Record uncertainty where the available evidence is insufficient.
10. Classify each confirmed issue and assign severity.
11. Produce a corrected response without introducing new unsupported claims.
12. Re-check the correction against the same evidence.

## Evidence Trail Standard

Every material factual claim should be traceable through:

**Claim → Evidence / Source → Verification Status → Error Classification → Severity → Decision → Correction → Re-check**

The evaluator should distinguish three states:

- **False** — reliable evidence contradicts the claim.
- **Supported** — reliable evidence supports the claim.
- **Unsupported / Unverified** — available evidence is insufficient to confirm the claim.

An unsupported claim should not automatically be called a hallucination. The evidence status must justify the classification.

## Practical Case Study — Numerical Hallucination

### User Request

> "A company has revenue of $100,000 and expenses of $70,000. What is its profit?"

### AI Response

> "The company's profit is $40,000."

### Claim Verification

| Claim | Evidence | Verification | Result |
|---|---|---|---|
| Revenue = $100,000 | User-provided input | Directly provided | Supported |
| Expenses = $70,000 | User-provided input | Directly provided | Supported |
| Profit = $40,000 | Independent calculation: $100,000 − $70,000 | Contradicted by calculation | False |

### Correct Calculation

**Profit = Revenue − Expenses**

**Profit = $100,000 − $70,000 = $30,000**

### Error Record

| Field | Decision |
|---|---|
| Error type | Numerical / calculation error |
| Severity | High |
| Evidence | User-provided figures and independent calculation |
| Correct result | $30,000 |
| Required action | Replace incorrect calculation |

### Re-check

The corrected response is recalculated independently and matches the provided inputs: **$30,000**.

## Practical Case Study — Unsupported Generalization

### AI Response

> "Companies that use AI always reduce operating costs."

### Evidence Assessment

No evidence or source is provided to support the absolute claim. The word **"always"** makes the statement categorical.

**Verification status:** Unsupported / Unverified

**Classification:** Unsupported generalization, not a confirmed factual hallucination.

### Better Response

> "AI can reduce certain operating costs in some situations, but the financial impact depends on implementation costs, the use case, and how the technology changes existing processes."

### Re-check

The revised response removes the unsupported absolute claim and uses appropriately qualified language. It does not assert a universal outcome.

## Practical Case Study — Factual Verification with Source Evidence

### AI Response

> "The World Health Organization was founded in 1950 and is headquartered in New York City."

### Verification Record

| Claim | Evidence / Source | Verification | Decision |
|---|---|---|---|
| WHO founded in 1950 | World Health Organization official institutional information | Contradicted by authoritative information | False |
| WHO headquartered in New York City | World Health Organization official institutional information | Contradicted by authoritative information | False |

**Classification:** Factual hallucination

**Severity:** High

### Corrected Response

> "The World Health Organization (WHO) was established in 1948 and is headquartered in Geneva, Switzerland."

### Evidence Rule

For a real-world evaluation, the reviewer should retain the exact source URL, access date, and relevant evidence excerpt in the evaluation record. The portfolio artifact therefore records the **source-evidence requirement** rather than pretending that a source was consulted when it was not.

## Structured Evidence Record

The companion artifact [`artifacts/hallucination-fact-check.csv`](../artifacts/hallucination-fact-check.csv) records claim-level verification decisions. Each row should answer:

- What exactly was claimed?
- What evidence was used?
- Was the claim supported, false, or unsupported?
- What error category applies?
- How severe is the issue?
- What correction is justified?

## Quality-Control Rules

- Never treat confidence as proof.
- Verify high-impact claims independently.
- Recalculate numerical claims separately.
- Distinguish an unverified claim from a confirmed false claim.
- Record the evidence supporting each correction.
- Avoid replacing one unsupported claim with another.
- Re-check the corrected response against the same evidence.
- Do not claim a source was consulted unless it actually was.

## Business & Finance Application

Hallucination detection is particularly important for AI outputs involving accounting, financial analysis, financial statements, business decisions, economic information, banking, taxation concepts, market information, and numerical calculations.

A small numerical or terminology error can materially change a financial conclusion, so domain-aware verification is essential.

## Skills Demonstrated

- AI Response Evaluation
- Hallucination Detection
- Fact Checking
- Claim Verification
- Evidence Traceability
- Error Classification
- Numerical Verification
- Evidence-Based Reasoning
- Business & Finance Domain Evaluation
- Quality Assurance
- Confidence Calibration

## Recruiter Takeaway

This project demonstrates the ability to turn a vague concern such as "the AI may be hallucinating" into a **traceable evaluation workflow: claim extraction, evidence selection, verification, classification, severity assessment, correction, and re-checking**.

## Portfolio Integrity Note

This is a **simulated portfolio case study created through self-directed practice**. It demonstrates a fact-checking methodology and does not claim professional AI fact-checking employment.
