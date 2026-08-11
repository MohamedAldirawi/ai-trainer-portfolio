# AI Data Quality Assurance

## Project Overview

This project demonstrates a structured quality-assurance process for AI training data before it is approved for downstream training or evaluation.

The workflow focuses on **accuracy, completeness, consistency, ambiguity, label correctness, evidence, and dataset readiness**.

> **Portfolio transparency:** This is a simulated portfolio exercise created to demonstrate practical AI data-quality methodology. It is not presented as paid AI employment experience.

## Objective

Establish a repeatable QA workflow that identifies data-quality problems, records evidence, applies corrective actions, and verifies that the corrected dataset satisfies predefined requirements.

## Data Quality Dimensions

| Dimension | QA Question |
|---|---|
| Accuracy | Is the information or label correct? |
| Completeness | Is required information present? |
| Consistency | Are similar cases treated the same way? |
| Relevance | Does the item belong to the intended task? |
| Clarity | Can the item be interpreted without unnecessary ambiguity? |
| Format | Does it follow the required schema or structure? |
| Label Validity | Does the assigned label match the annotation guidelines? |
| Evidence | Can the QA decision be supported by the source item? |

## QA Workflow

**Sample → Inspect → Detect → Classify → Correct → Recheck → Approve/Reject**

### 1. Inspect

Review the source text, assigned label, required schema, and annotation guidelines before making a decision.

### 2. Detect

Identify:

- Incorrect labels
- Missing labels
- Duplicate records
- Contradictory information
- Ambiguous examples
- Irrelevant records
- Formatting problems
- Unsupported annotations

### 3. Classify

Record each confirmed issue using a consistent error taxonomy and severity level.

### 4. Correct

Correct the record only when the available evidence and annotation guidelines support a clear correction. Otherwise, flag it for secondary review.

### 5. Recheck

Review corrected records independently and confirm that the correction did not introduce another problem.

### 6. Readiness Decision

The dataset receives one of three statuses:

- **Approved** — no unresolved material QA issues.
- **Needs Revision** — correctable issues remain.
- **Escalate** — the available evidence is insufficient for a reliable decision.

## Annotation QA Schema

A practical QA record can use the following fields:

| Field | Example |
|---|---|
| Record ID | 004 |
| Assigned Label | Account |
| Expected Label | Billing |
| QA Status | Fail |
| Error Type | Incorrect Label |
| Severity | Medium |
| Evidence | "get my money back" |
| Rationale | Indicates a refund/payment intent |
| Corrective Action | Relabel as Billing |
| Reviewer Confidence | High |

## Practical Case Study — Customer Support Dataset

### Sample Dataset

| ID | Customer Statement | Assigned Label | QA Finding |
|---|---|---|---|
| 1 | I was charged twice for the same transaction. | Billing | ✅ Valid |
| 2 | I cannot access my account because I forgot my password. | Account | ✅ Valid |
| 3 | The application crashes when I upload a document. | Technical Support | ✅ Valid |
| 4 | I want to get my money back for this purchase. | Account | ❌ Incorrect Label |
| 5 | My invoice shows an unexpected charge. | Billing | ✅ Valid |
| 6 | The payment issue is not clear from the customer's message. | Billing | ⚠️ Ambiguous |

### QA Analysis

**Record 4** is incorrectly labeled. The statement expresses a refund/payment intent, so it should be classified as **Billing** under the defined guidelines.

**Record 6** is ambiguous. The available information does not establish the precise issue with enough confidence, so it should be flagged rather than confidently relabeled without evidence.

### QA Decision Log

| Record | Decision | Reason |
|---|---|---|
| 4 | Relabel | Evidence supports Billing |
| 6 | Escalate | Insufficient information |

### Corrective Actions

1. Relabel Record 4 from **Account** to **Billing**.
2. Flag Record 6 for secondary review or clarification.
3. Recheck the remaining records against the same guidelines.
4. Run a final readiness review.

## Quality Metrics

A production-style QA process can track:

- **Annotation Accuracy** — proportion of reviewed records with correct labels.
- **Defect Rate** — proportion containing confirmed quality defects.
- **Ambiguity Rate** — proportion requiring escalation or clarification.
- **Correction Rate** — proportion requiring changes after QA.
- **Readiness Rate** — proportion approved after final review.

For a real dataset, these metrics should be calculated from the actual review sample rather than invented.

## Error Taxonomy

| Error Type | Example |
|---|---|
| Incorrect Label | Billing item labeled Account |
| Missing Label | Record has no classification |
| Ambiguous Data | Insufficient information for confident labeling |
| Inconsistent Label | Similar records receive different labels |
| Irrelevant Data | Record does not belong to the task |
| Formatting Error | Required schema is not followed |
| Unsupported Annotation | Label cannot be justified from the source |

## Quality Gates

Before approval, verify:

- [ ] Every reviewed record has a valid label or documented escalation.
- [ ] Labels follow the annotation guidelines.
- [ ] Material errors have been corrected.
- [ ] Ambiguous records are not falsely presented as certain.
- [ ] Corrections have been rechecked.
- [ ] The dataset meets the required schema.

## Skills Demonstrated

- AI Data Quality Assurance
- Data Validation
- Annotation QA
- Error Detection
- Data Consistency Analysis
- Ambiguity Handling
- Label Verification
- Evidence-Based Review
- Quality Control
- AI Training Data Preparation

## Professional Relevance

This project is relevant to AI Data Annotator, AI Trainer, AI Response Evaluator, Data Quality Specialist, and AI Quality Assurance roles.

## Conclusion

High-quality AI training data requires more than assigning labels. A reliable QA process must verify the source evidence, apply consistent guidelines, identify ambiguity, document errors, perform corrections carefully, and independently recheck the final dataset before approval.
