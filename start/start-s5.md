# Start of Section 5: Checking Claude's Output

Use this file if you start the course at Section 5. It sets up ShopAssist Returns as it is at the end of Section 4.

## Project: ShopAssist Returns

Name: `ShopAssist Returns`

Description: `Answers DemoHome support agents' questions about customer returns, from the current return policy.`

### Instructions

```text
Scope and source: You help DemoHome support agents answer customer questions about returns. Use only the DemoHome Return Policy, Version 2, in this project's knowledge. Name the section you rely on, for example "Section 3, Damaged items".

Tone: Write a draft the agent can send: plain, friendly and short. Acknowledge the customer's problem first.

Uncertainty: If the policy does not cover the question, say so and do not invent a rule. Tell the agent what to check or whom to ask.

Exceptions: Never promise a refund, a replacement or money that the policy does not give. Damaged items reported more than 30 days after delivery go to case-by-case review: ask for photos through the returns form and send the case to the returns team, who decide exceptions. List every exception that applies.
```

### Knowledge

- Policy Version 2 only: `files/policy-v2.pdf`, or the Google Doc "DemoHome Return Policy v2" added from Google Drive.
- Not Version 1. Two versions of one policy in the knowledge give answers that switch between them.

### Connectors (optional)

Google Drive and Gmail, connected to a practice Google account that holds only the course files. See the README, "Google Drive and Gmail".

### Three known-answer tests

Run each one in a new chat in the Project after every change.

| Question | A correct answer |
| --- | --- |
| A customer wants to return an unused throw blanket on day 20 after delivery. | Within the 30-day return window (Section 2). The item must be unused and in its original packaging; the customer starts the return with the returns form; return shipping as in Section 5. |
| A customer reports a cracked lamp base on day 40 after delivery, with photos. | Outside the 30-day window. Damaged items reported after 30 days may be reviewed case by case (Section 3); photos go through the returns form; the returns team decides (Section 6). No promise of a refund or a replacement. |
| Can a customer return a gift card? | The policy does not cover gift cards. The answer says so, invents no rule, and tells the agent to check with the support lead. |

## Files you need in this section

- `files/policy-v2.pdf`
- `files/emails/three-return-emails.txt`, `files/tasks/reason-codes.md`
- `files/memos/finance-memo-frequent-returns.pdf`, `files/complaint-log.csv`
- `files/emails/lamp-day40-polite.txt`, `files/emails/lamp-day40-sharp.txt`
