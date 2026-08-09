# AI Instruction Following Evaluation

## Project Overview

This project demonstrates a structured approach to evaluating whether AI-generated responses correctly follow user instructions.

Instruction following is a critical component of AI response quality because a response can be factually correct while still failing to satisfy the user's requested format, scope, constraints, or objectives.

## Objective

Evaluate AI responses based on their ability to understand and follow explicit user instructions accurately and consistently.

## Evaluation Framework

Each response is evaluated across the following dimensions:

| Criterion | Description |
|---|---|
| Instruction Understanding | Correctly identifies what the user is asking for |
| Instruction Compliance | Follows the user's explicit requirements |
| Relevance | Provides information related to the requested task |
| Completeness | Addresses all important parts of the instruction |
| Format Compliance | Uses the requested structure or format |
| Constraint Adherence | Respects limitations, exclusions, and conditions |
| Clarity | Presents the result in a clear and understandable way |

## Evaluation Process

The evaluation process follows these steps:

1. Identify the user's explicit instructions.
2. Separate the main task from secondary requirements.
3. Identify required format, length, tone, and constraints.
4. Review the AI-generated response.
5. Compare the response against each requirement.
6. Identify any instruction-following failures.
7. Determine the overall quality of compliance.
8. Provide a concise explanation of the evaluation.

## Example Evaluation

### User Instruction

"Explain the difference between revenue and profit in three sentences using simple English."

### AI Response

"Revenue is the total amount of money a business earns from selling its products or services. Profit is the money left after the business pays its expenses. Therefore, revenue measures income before expenses, while profit measures what remains after expenses."

### Evaluation

**Instruction Following: Pass**

**Reasoning:**

- The response explains both concepts.
- The explanation uses simple language.
- The response contains exactly three sentences.
- The difference between revenue and profit is clearly stated.
- No unnecessary information is included.

## Example of Instruction Failure

### User Instruction

"Give me five accounting interview questions and do not provide the answers."

### AI Response

1. What is a balance sheet?
2. What is the difference between revenue and profit?
3. What is depreciation?
4. What is working capital?
5. What is a cash flow statement?

The AI then provides detailed answers to all five questions.

### Evaluation

**Instruction Following: Fail**

**Reasoning:**

The response provides the requested five questions, but it violates the explicit instruction not to provide answers.

This demonstrates why instruction following should be evaluated separately from factual accuracy.

## Common Instruction-Following Errors

AI systems may fail to follow instructions by:

- Ignoring explicit requirements
- Providing extra information that was excluded
- Using the wrong output format
- Failing to answer one part of a multi-part request
- Exceeding a requested word or sentence limit
- Misinterpreting constraints
- Changing the requested tone or style
- Answering a different question from the one asked

## Multi-Requirement Evaluation


## Practical Example

### Instruction-Following Evaluation

#### User Instruction

> "Explain what a balance sheet is in exactly three bullet points. Use simple language and include one example."

#### AI-Generated Response

> A balance sheet shows what a business owns and owes.
>
> It includes assets, liabilities, and owner's equity.
>
> For example, a company may have $50,000 in assets and $20,000 in liabilities.
>
> A balance sheet is useful for understanding the financial position of a business.

#### Instruction-Following Evaluation

| Requirement | Assessment |
|---|---|
| Explain the balance sheet | ✅ Satisfied |
| Exactly three bullet points | ❌ Not satisfied |
| Use simple language | ✅ Satisfied |
| Include one example | ✅ Satisfied |

#### Overall Assessment

**Instruction-Following Score: 3/4**

The response covers the requested topic, uses accessible language, and provides an example. However, it fails to follow the explicit formatting requirement of providing **exactly three bullet points**.

#### Improved Response

- A balance sheet shows what a business owns and owes.
- It includes assets, liabilities, and owner's equity.
- Example: if a company has $50,000 in assets and $20,000 in liabilities, its owner's equity is $30,000.

#### Result

The improved response satisfies all explicit requirements: correct topic, exactly three bullet points, simple language, and one practical example.

> **Note:** This is a simulated instruction-following evaluation created to demonstrate a structured AI evaluation workflow.


