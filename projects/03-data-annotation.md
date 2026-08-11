# AI Data Annotation Practice

## Project Overview

This project demonstrates a structured approach to text classification and AI data annotation. The goal is to produce labels that are **accurate, consistent, reproducible, and auditable**.

> **Portfolio status:** Simulated self-directed exercise created to demonstrate an AI data-annotation workflow. It does not represent paid annotation employment.

## Objective

Create a repeatable annotation workflow that converts unstructured text into reliable labels while identifying ambiguous cases and applying quality-control checks.

## Annotation Workflow

1. Define the label taxonomy and decision rules.
2. Read each item in full before assigning a label.
3. Identify the primary intent rather than isolated keywords.
4. Assign exactly one label when the task requires single-label classification.
5. Record a concise rationale for difficult decisions.
6. Flag ambiguous or insufficiently supported examples.
7. Perform a second-pass quality check.

## Label Taxonomy

For this case study, customer-support messages are classified into three primary intents:

| Label | Definition | Typical examples |
|---|---|---|
| **Billing** | Payments, invoices, charges, refunds, or transaction disputes | Duplicate charge, refund request |
| **Technical Support** | Software, system, application, or technical-functionality problems | App crash, upload failure |
| **Account** | Login, registration, password, or account-information issues | Forgot password, cannot log in |

### Decision Rule

Choose the label that best represents the **primary reason for the user's message**. Do not classify from a single keyword when the surrounding context indicates another intent.

## Sample Dataset

| ID | Customer Statement | Label | Confidence | Rationale |
|---:|---|---|---|---|
| 1 | I was charged twice for the same order. | Billing | High | The primary issue is a duplicate payment. |
| 2 | I cannot log in to my account. | Account | High | The user cannot access the account. |
| 3 | The application crashes whenever I upload a file. | Technical Support | High | The issue is application functionality. |
| 4 | I would like to request a refund for my payment. | Billing | High | The request concerns a payment refund. |
| 5 | I forgot my password and cannot access my account. | Account | High | The access problem is caused by account credentials. |

## Annotation Quality Rubric

Each annotation can be reviewed against four dimensions:

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Label correctness | Incorrect | Partially defensible | Correct |
| Guideline consistency | Conflicts with rules | Minor inconsistency | Fully consistent |
| Rationale quality | Missing/unsupported | Partly supported | Clear and evidence-based |
| Ambiguity handling | Missed ambiguity | Ambiguity noticed but unresolved | Correctly flagged/resolved |

**Maximum:** 8 points per item.

## Ambiguous-Case Handling

Consider this example:

> "I cannot log in because the website keeps crashing after I enter my password."

Possible labels include **Account** and **Technical Support**. The correct decision depends on the annotation policy. If the taxonomy defines the primary failure as system functionality, label **Technical Support**; if it prioritizes the user's account-access intent, label **Account**.

The important training behavior is not pretending the case is unambiguous. The evaluator should document the decision rule and apply it consistently to similar cases.

## Inter-Annotator Consistency

A production annotation process should measure agreement between annotators on the same sample. A simple agreement rate can be calculated as:

**Agreement Rate = Number of Matching Labels / Total Compared Labels × 100**

For example, if two annotators agree on 19 of 20 items:

**19 / 20 × 100 = 95% agreement**

This is a descriptive quality signal; the appropriate agreement metric depends on the task and label design.

## Quality-Control Checklist

Before accepting a labeled sample:

- [ ] The label matches the defined taxonomy.
- [ ] The primary intent was considered.
- [ ] The decision is supported by the text.
- [ ] Similar cases would receive the same label.
- [ ] Ambiguous cases are flagged where necessary.
- [ ] No label was chosen solely because of a misleading keyword.

## Common Annotation Errors

### 1. Keyword Matching

**Failure:** Labeling "payment" automatically as Billing even when the message is primarily about a technical payment-page error.

**Correction:** Evaluate the complete context and primary intent.

### 2. Inconsistent Similar Cases

**Failure:** Assigning different labels to materially similar messages.

**Correction:** Revisit the taxonomy and previous decisions.

### 3. Forced Certainty

**Failure:** Treating an ambiguous example as obvious.

**Correction:** Flag the case and document the ambiguity.

### 4. Missing Quality Review

**Failure:** Treating the first annotation as final.

**Correction:** Perform a second-pass review or sample-based QA.

## Skills Demonstrated

- AI Data Annotation
- Text Classification
- Label Taxonomy Design
- Annotation Guidelines
- Contextual Analysis
- Consistency Checking
- Quality Assurance
- Ambiguity Detection
- Structured Reasoning
- Attention to Detail

## Employer-Relevant Evidence

This project demonstrates that I can approach annotation as a **quality-controlled process**, rather than simply assigning labels. The emphasis is on clear guidelines, reproducibility, ambiguity management, and reviewable decisions.

## Conclusion

Reliable AI training data depends on consistent annotation decisions and disciplined quality control. This case study demonstrates a practical methodology for creating, reviewing, and improving labeled text data.
