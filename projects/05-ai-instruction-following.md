# AI Instruction Following Evaluation

## Project Overview

This project demonstrates a structured method for evaluating whether an AI response satisfies the user's **explicit requirements, constraints, format, scope, and intended task**.

A response can be factually correct and still be a poor result if it ignores an instruction such as a word limit, required format, prohibited content, or one part of a multi-step request.

> **Portfolio status:** Simulated self-directed evaluation exercise.

## Objective

Evaluate instruction-following performance consistently and identify exactly which requirements were satisfied, partially satisfied, or violated.

## Requirement Extraction

Before judging the answer, convert the user's request into testable requirements:

1. **Task** — What must the AI do?
2. **Content** — What information must be included?
3. **Format** — What structure is required?
4. **Length** — Is there a word/sentence/item limit?
5. **Constraints** — What must or must not be included?
6. **Audience/tone** — Who is the answer for and how should it be written?

This prevents the evaluator from judging the response only by whether it "sounds good."

## Evaluation Rubric

| Criterion | 0 | 1 | 2 |
|---|---|---|---|
| Task completion | Missing | Partial | Complete |
| Content requirements | Missing | Partial | Complete |
| Format compliance | Violated | Partially compliant | Fully compliant |
| Constraint adherence | Violated | Minor issue | Fully compliant |
| Length compliance | Violated | Minor deviation | Compliant |
| Clarity | Poor | Adequate | Clear |

**Maximum:** 12 points.

## Case Study 1 — Exact Format Constraint

### User Instruction

> "Explain what a balance sheet is in exactly three bullet points. Use simple language and include one example."

### AI Response

> A balance sheet shows what a business owns and owes.
>
> It includes assets, liabilities, and owner's equity.
>
> For example, a company may have $50,000 in assets and $20,000 in liabilities.
>
> A balance sheet is useful for understanding the financial position of a business.

### Requirement-by-Requirement Evaluation

| Requirement | Result | Evidence |
|---|---|---|
| Explain the balance sheet | PASS | The concept is explained. |
| Exactly three bullet points | FAIL | Four statements are provided and they are not formatted as three bullets. |
| Simple language | PASS | Language is accessible. |
| Include one example | PASS | A numerical example is included. |

**Overall: 3/4 requirements satisfied.**

### Improved Response

- A balance sheet shows what a business owns and owes.
- It includes assets, liabilities, and owner's equity.
- Example: if a company has $50,000 in assets and $20,000 in liabilities, owner's equity is $30,000.

The revised response satisfies the explicit format, language, and content requirements.

## Case Study 2 — Prohibited Output

### User Instruction

> "Give me five accounting interview questions and do not provide the answers."

### AI Response

The AI provides five questions and then supplies detailed answers to each.

### Evaluation

**Task completion:** Pass

**Constraint adherence:** Fail

The response completed the requested list but violated an explicit negative instruction. This should be recorded as a material instruction-following error even if all answers are factually correct.

## Multi-Requirement Test Matrix

For complex prompts, use a checklist before assigning an overall score:

| Requirement | Status | Notes |
|---|---|---|
| Correct task | PASS/FAIL | Did the response perform the requested task? |
| Required information | PASS/FAIL | Is every required element present? |
| Required format | PASS/FAIL | Does structure match the instruction? |
| Length limit | PASS/FAIL | Is the requested limit respected? |
| Exclusions | PASS/FAIL | Was prohibited content avoided? |
| Tone/audience | PASS/FAIL | Is the response suitable for the target audience? |

## Common Failure Modes

- **Partial completion** — answers only one part of a multi-part request.
- **Format drift** — gives correct content in the wrong structure.
- **Constraint violation** — includes information the user explicitly prohibited.
- **Over-answering** — adds unnecessary material that conflicts with scope.
- **Length violation** — ignores word, sentence, or item limits.
- **Audience mismatch** — uses inappropriate complexity or tone.
- **Task substitution** — answers a related but different question.

## Quality-Control Method

To improve evaluator consistency:

1. Extract requirements before reading the response deeply.
2. Judge each requirement independently.
3. Quote or identify concrete evidence from the response.
4. Separate factual quality from instruction compliance.
5. Record partial compliance rather than forcing a binary judgment when appropriate.
6. Recheck the final score against the requirement matrix.

## Skills Demonstrated

- Instruction Following Evaluation
- Requirement Extraction
- Constraint Analysis
- AI Response Evaluation
- Quality Assurance
- Structured Scoring
- Error Analysis
- Business and Accounting Domain Application
- Critical Thinking

## Conclusion

Instruction following should be evaluated as a measurable quality dimension. A strong evaluator can identify exactly where an AI response satisfies the user's requirements and where it fails, even when the response is otherwise fluent or factually correct.
