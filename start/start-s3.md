# Start of Section 3: Choosing Features and Models, Managing Context

Use this file if you start the course at Section 3.

## Project

None yet.

## What Section 2 produced: three tested prompts

### 1. A customer reply (six parts)

Attach `files/policy-v1.pdf` to the message, then send this text (in a new chat each time):

```text
Task: Write a reply to the customer email below.
Context: DemoHome is an online store for home goods. You are drafting for a support agent, who will check the reply before sending it. Use only the Policy text.
Audience: The customer, who is upset and is not an expert in our policy.
Constraints: Do not promise a refund, a replacement or anything the policy does not give. If a fact is missing, leave a gap in [brackets] instead of inventing it.
Format: A short email of three short paragraphs, with no headings.
Success criteria: The reply acknowledges the damage, says what the policy allows, names the next step, and promises no refund.

Policy text: the attached file, policy-v1.pdf

Customer message:
<paste emails/lamp-day40.txt here, from the Subject line on>
```

### 2. A classifier with a contrasting pair

Send this text in a new chat each time, then paste the five emails of `files/emails/classify-five-emails.txt` under "Emails:" (the From lines can stay or go):

```text
Label each customer email with one label: Order issue, Return request or Billing. Answer with one line per email: the email number and the label.

Two examples at the border between Order issue and Return request:
"My package has not arrived and the tracking has not moved for a week." -> Order issue
"The vase arrived broken and I would like to send it back." -> Return request

Emails:
<paste emails/classify-five-emails.txt here>
```

Without the two examples, the cracked lamp (email 2) was labelled Order issue in all three runs of the lesson; with them, Return request in all three.

### 3. A chain of three steps, with a check after the first

All three in one chat. Step 1, with `files/complaint-log.csv` attached:

```text
Step 1 of 3: a summary I will check against the data.

Summarize the attached complaint-log.csv: the reasons for complaints, and how many days after delivery customers complain, above all about damaged items. Use only the data in the file. At most 8 bullet points. Start each bullet with [count] if you counted it from the records, or [inference] if it is your reading of them.
```

Check: open `files/complaint-log.csv` in a table (GitHub shows it as one; "Search this file" filters the rows, for example by `damaged`) and compare every count you rely on with the rows. Write what you found at the start of step 2. Step 2, with `files/policy-v1.pdf` attached:

```text
Step 2 of 3. I checked the summary against the CSV: the five late complaints, the six damaged records with no delivery date and the duplicate are right. Keep the six undated records as a stated limit.

Now compare three options for damaged items, using only the checked summary above and the attached policy-v1.pdf:
A) keep the 30-day window as it is,
B) a 45-day window,
C) the 30-day window plus the damaged-item exception (Section 3.3: a case-by-case review after day 30).
For each option: which of the logged damaged complaints it covers, what it costs or risks, and what the data cannot tell us.
```

If your check found a wrong number, say which one and give the right figure instead of "are right". Step 3:

```text
Step 3 of 3. Write a one-page recommendation to Elena Brooks, the operations director, who decides on the return window for damaged items. Use only the checked summary and the comparison above. Give one clear recommendation, the numbers it rests on, and the limits of the data in plain words.
```

The checked summary and the whole chat of the recorded run are in `files/catch-up/complaint-summary.md` and `files/catch-up/long-chat.md`.

## Files you need in this section

- `files/tasks/four-tasks.md`, `files/policy-v1.pdf`
- `files/emails/order-status-emails.txt`, `files/emails/order-status-hard.txt`, `files/order-status.csv`, `files/tasks/order-status-criteria.md`
