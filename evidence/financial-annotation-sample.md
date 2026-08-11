# Evidence Sample — Financial Data Annotation

> **Status:** Simulated, self-directed portfolio exercise.

## Objective

Demonstrate structured annotation of finance-related text using explicit labels, evidence spans, and confidence.

## Annotation Schema

- **Entity Type:** financial concept / amount / metric / transaction
- **Sentiment:** positive / negative / neutral / not applicable
- **Topic:** revenue / expense / profit / cash flow / transaction / other
- **Confidence:** high / medium / low
- **Evidence Span:** exact text supporting the label

## Sample Records

| ID | Text | Topic | Entity | Evidence Span | Confidence |
|---|---|---|---|---|---|
| F01 | Revenue increased to $250,000 this year. | Revenue | $250,000 | "$250,000" | High |
| F02 | Operating expenses fell by 8%. | Expense | 8% | "Operating expenses" / "8%" | High |
| F03 | The company may face a cash-flow shortage next quarter. | Cash Flow | Cash-flow risk | "may face a cash-flow shortage" | Medium |
| F04 | Profit improved after costs were reduced. | Profit | Profit improvement | "Profit improved" | High |

## Ambiguity Rule

If the text does not provide enough evidence for a specific label, the annotator should not manufacture certainty. Use a lower confidence level or flag the item for secondary review according to the project guidelines.

## QA Check

- [x] Every label is supported by source text.
- [x] Financial terms are not inferred beyond the available evidence.
- [x] Confidence reflects evidence strength.
- [x] Numeric values are preserved exactly.

## Capability Demonstrated

Financial-domain annotation, evidence-span selection, confidence calibration, structured labeling, and annotation quality control.
