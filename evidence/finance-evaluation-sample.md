# Evidence Sample — Business & Finance AI Evaluation

> **Status:** Simulated, self-directed portfolio exercise.

## Task

Evaluate an AI-generated financial analysis using a small set of provided figures.

### Source Figures

- Revenue: $500,000
- Cost of Goods Sold: $300,000
- Operating Expenses: $120,000

## Expected Calculations

**Gross Profit = $500,000 − $300,000 = $200,000**

**Operating Profit = $200,000 − $120,000 = $80,000**

## AI Response Under Review

> "The company has $200,000 gross profit and $80,000 operating profit. Therefore, its net profit is $80,000."

## Evaluation

| Criterion | Result | Reason |
|---|---|---|
| Gross profit | Pass | $500,000 − $300,000 = $200,000. |
| Operating profit | Pass | $200,000 − $120,000 = $80,000. |
| Net profit conclusion | Fail | Net profit cannot be established from the supplied figures alone if other items such as interest or taxes may apply. |
| Assumption control | Fail | The response treats operating profit as net profit without sufficient evidence. |

## Error Annotation

**Error Type:** Unsupported financial conclusion  
**Severity:** High  
**Evidence:** The source provides revenue, COGS, and operating expenses but does not provide all possible items needed to establish net profit.  
**Action:** Retain the correct operating-profit calculation and qualify the net-profit conclusion.

## Corrected Output

> "Gross profit is $200,000 and operating profit is $80,000 based on the figures provided. Net profit cannot be determined reliably from these figures alone because additional items, such as interest and taxes, may affect the final result."

## QA Check

- [x] Arithmetic independently verified.
- [x] Gross profit verified.
- [x] Operating profit verified.
- [x] Unsupported net-profit claim removed.
- [x] Assumption limitation stated.

**Final status: Approved after correction**

## Capability Demonstrated

This evidence demonstrates domain-aware AI evaluation, independent numerical verification, assumption control, error classification, and financially accurate correction.
