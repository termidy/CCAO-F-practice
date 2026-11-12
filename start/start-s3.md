# Start of Section 3: Choosing Features and Models, Managing Context

Use this file if you start the course at Section 3.

## Project

None yet.

## What Section 2 produced: three tested prompts

### 1. A customer reply (six parts)

```text
Task: Write a reply to the customer email below.
Context: DemoHome is an online store for home goods. You are drafting for a support agent, who will check the reply before sending it. Use only the policy text below.
Audience: The customer, who is upset and is not an expert in our policy.
Constraints: Do not promise a refund, a replacement or anything the policy does not give. If a fact is missing, leave a gap in [brackets] instead of inventing it.
Format: A short email of three short paragraphs, with no headings.
Success criteria: The reply acknowledges the damage, says what the policy allows, names the next step, and promises no refund.

Policy text:
<paste the text of policy-v1.pdf here, or attach the file>

Customer message:
<paste emails/lamp-day40.txt here>
```

### 2. A classifier with a contrasting pair

```text
Label each customer email with exactly one label: Order issue, Return request or Billing.

Order issue: the question is about an order's status, a delay, a missing package or an address change.
Return request: the customer wants to send an item back or asks how returns work.
Billing: the question is about money: a charge, a double charge, a refund that has not arrived, an invoice.

Two examples at the border between Order issue and Return request:
"My package has not arrived and the tracking has not moved for a week." -> Order issue
"The vase arrived broken and I would like to send it back." -> Return request

Answer with one line per email: the email number and the label.

Emails:
<paste emails/classify-five-emails.txt here>
```

### 3. A chain of three steps, with a check after the first

1. Summarize the reasons and the timing of the complaints in `complaint-log.csv`, using only the data. Mark every statement that is a count and every statement that is an inference.
2. Check: open the CSV in a spreadsheet, filter by dates, and compare every count in the summary with the table. Fix the summary before going on. Keep its limits (for example, records with no delivery date) in the text.
3. Compare three options for damaged items (a 30-day window, a 45-day window, the 30-day window with the damaged-item exception), then write a one-page recommendation from the checked summary.

## Files you need in this section

- `files/tasks/four-tasks.md`, `files/policy-v1.pdf`
- `files/emails/order-status-emails.txt`, `files/emails/order-status-hard.txt`, `files/order-status.csv`, `files/tasks/order-status-criteria.md`
