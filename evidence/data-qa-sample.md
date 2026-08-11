# Evidence Sample — AI Data Quality Assurance

> **Status:** Simulated, self-directed portfolio exercise.

## QA Dataset

| ID | Text | Assigned Label | QA Decision |
|---|---|---|---|
| D01 | I was charged twice for one purchase. | Billing | Pass |
| D02 | I forgot my password and cannot sign in. | Account | Pass |
| D03 | I want my money back for this purchase. | Account | Fail — relabel to Billing |
| D04 | There is a problem with my payment. | Billing | Escalate — insufficient detail |
| D05 | The mobile application crashes during upload. | Technical Support | Pass |

## Defect Log

| Record | Defect | Severity | Action |
|---|---|---|---|
| D03 | Incorrect label | Medium | Relabel to Billing |
| D04 | Ambiguous source | Medium | Secondary review |

## Readiness Decision

**Status: Needs Revision**

The sample is not approved until D03 is corrected and D04 is resolved or explicitly accepted under the project's ambiguity policy.

## Recheck Procedure

1. Confirm the corrected label for D03.
2. Review D04 with the annotation guideline.
3. Check similar records for consistent treatment.
4. Recalculate the defect count after correction.
5. Approve only when no unresolved material issue remains.

## Capability Demonstrated

Dataset inspection, defect logging, ambiguity handling, corrective action, recheck design, and readiness decisions.
