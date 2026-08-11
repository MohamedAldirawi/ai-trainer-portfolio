# Project 01 — AI Response Evaluation

## Project Type

**Simulated portfolio case study / self-directed practice**

## Objective

Demonstrate a repeatable method for evaluating AI-generated responses against explicit quality criteria, identifying weaknesses, and producing a justified improved version.

## Evaluation Framework

Each response is reviewed across five dimensions:

| Criterion | Weight | Review question |
|---|---:|---|
| Accuracy | 5 | Are the claims and calculations correct? |
| Relevance | 5 | Does the response directly answer the user's request? |
| Instruction Following | 5 | Does it satisfy the explicit requirements and constraints? |
| Clarity | 5 | Is the explanation understandable and logically organized? |
| Completeness | 5 | Are the important requested elements covered? |

**Maximum score: 25 points**

### Rating Bands

- **22–25:** Strong
- **18–21:** Acceptable with minor improvements
- **13–17:** Needs improvement
- **0–12:** Major revision required

## Test Case

### User Request

> Explain the difference between revenue and profit in simple business terms, and give one practical example.

### AI-Generated Response

> Revenue is the amount of money a business earns from selling its products or services. Profit is the money left after subtracting expenses from revenue. For example, if a company has $10,000 in sales and spends $7,000 on expenses, its profit is $3,000.

## Evaluation

| Criterion | Score | Assessment |
|---|---:|---|
| Accuracy | 5/5 | The definitions and numerical example are correct. |
| Relevance | 5/5 | The response directly addresses the requested distinction and example. |
| Instruction Following | 5/5 | It uses simple language and provides one practical example. |
| Clarity | 5/5 | The explanation is concise and easy to understand. |
| Completeness | 4/5 | It covers the core concepts but could make the revenue-before-expenses distinction more explicit. |
| **Total** | **24/25** | **Strong** |

## Strengths Identified

- Correct distinction between revenue and profit.
- Correct arithmetic: $10,000 − $7,000 = $3,000.
- Directly answers the user's question.
- Uses accessible language.
- Includes the requested practical example.

## Improvement Opportunity

The response is already strong, but the definition of revenue can be made more precise by explicitly stating that revenue is measured **before the relevant expenses are deducted**. The improved version should preserve the original simplicity rather than adding unnecessary accounting detail.

## Improved Response

Revenue is the total income a business generates from selling its products or services **before expenses are deducted**.

Profit is the amount remaining after the business deducts its expenses from revenue.

**Example:**

- Revenue: $10,000
- Expenses: $7,000
- Profit: $3,000

**Key takeaway:** Revenue shows how much the business generated from sales, while profit shows what remains after expenses.

## Second-Pass Quality Check

| Check | Result |
|---|---|
| Definitions accurate | Pass |
| Calculation accurate | Pass |
| Directly answers request | Pass |
| Beginner-friendly | Pass |
| No unnecessary scope expansion | Pass |
| Practical example included | Pass |

**Final assessment: 25/25 — Strong response.**

## Error Taxonomy Used

For future evaluations, errors can be classified as:

- **Factual error** — incorrect statement of fact.
- **Reasoning error** — conclusion does not follow from the information provided.
- **Calculation error** — incorrect arithmetic or quantitative reasoning.
- **Instruction-following error** — explicit user requirement is missed.
- **Relevance error** — unnecessary or unrelated content dominates the answer.
- **Clarity error** — correct information is difficult to understand.
- **Completeness error** — an important requested element is missing.
- **Unsupported claim** — claim is presented without adequate basis.

## Evaluation Workflow

1. Parse the user request.
2. Extract explicit requirements and constraints.
3. Review the AI response.
4. Score each criterion independently.
5. Identify specific errors or weaknesses.
6. Explain the reasoning behind each score.
7. Produce an improved response where appropriate.
8. Perform a second-pass quality check.
9. Record the final score and improvement rationale.

## Skills Demonstrated

- AI response evaluation
- Quality assessment
- Rubric design and application
- Instruction-following analysis
- Factuality checking
- Error taxonomy development
- Structured feedback
- Analytical reasoning
- Business and finance domain knowledge

## Portfolio Integrity Note

This is a **simulated portfolio case study created through self-directed practice**. It demonstrates a structured evaluation methodology and does not claim professional employment experience in AI training.
