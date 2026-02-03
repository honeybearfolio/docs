---
title: "Creating Rules"
weight: 20
description: "Automate your transaction categorization with powerful rules."
---

# Creating Rules

Transaction rules allow you to automate the process of organizing your finances. By defining criteria, you can automatically categorize transactions, update payees, or add notes as soon as data enters the system.

## How Rules Work

A rule consists of **Conditions** (the "If" part) and **Actions** (the "Then" part).

> **Logic**: If [Condition A] [AND/OR] [Condition B] is met -> Then perform [Action].

### Rule Priority

Rules are executed in order of specific priority. If multiple rules apply to the same transaction, they will apply in sequence. You can manage the priority order in the rules list.

## Creating a Rule

1. Navigate to the **Rules** section in the application.
2. Click **Add Rule**.
3. Define your **Conditions** and **Actions**.
4. Save the rule.

### Conditions (The "If")

You can match transactions based on the following fields:
- Payee
- Category
- Notes
- Amount
- Date

#### Text Operators
For text fields (like Payee, Category, Notes), you can use:
- **Equals** / **Not Equals**: Exact match.
- **Contains** / **Not Contains**: Partial match.
- **Starts With** / **Ends With**: Matches the beginning or end of the text.
- **Is Empty** / **Is Not Empty**: Checks for presence of data.

#### Number Operators
For numeric fields (like Amount), you can use:
- **Equals** / **Not Equals**
- **Greater Than** / **Less Than**
- **Is Empty** / **Is Not Empty**

#### Logic
You can combine multiple conditions using:
- **AND**: All conditions must be true for the rule to run.
- **OR**: At least one condition must be true for the rule to run.

### Actions (The "Then")

When a rule matches, you can automatically update the transaction. You can set:
- **Category**: assign a category (e.g., "Groceries").
- **Payee**: clean up bank descriptions (e.g., set "AMZ* Marketplace" to "Amazon").
- **Notes**: add custom tags or comments.
- **Date** or **Amount**: (Less common, but possible).

## Example

**Scenario**: You want to categorize all coffee shop visits as "Dining Out".

1. **Condition**: If **Payee** *Contains* "Starbucks"
2. **Action**: Set **Category** To "Dining Out"

With this rule, every time you import a transaction containing "Starbucks", it will automatically be categorized.
