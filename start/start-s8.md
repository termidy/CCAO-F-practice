# Start of Section 8: Troubleshooting and Optimization

Use this file if you start the course at Section 8. ShopAssist Returns is as in `start-s5.md`.

## What Section 7 produced

### Requirements

- Goal: Claude drafts replies to damaged-item emails; an agent reads every draft and sends it. Claude sends nothing and approves nothing.
- Users: support agents, including new agents in their first weeks.
- Input: one customer email about a damaged item, and the order facts from DemoOrders.
- Output: a draft reply and, when the case needs a decision, a complete case for the returns team.
- Constraints: the source is policy Version 2 only; exceptions stay with the returns team; no customer data in unapproved tools.
- Acceptance criteria (each one is a yes or no on a test run):
  1. On a set of damaged-item emails, every draft names the right policy section and promises no refund the policy does not give.
  2. A new agent fills in the intake form for one email in two minutes or less.
  3. Every case sent to the returns team has the order number, the delivery date, the customer's description and the photos.

### Intake form and routing table

Fields: order number; delivery date (from DemoOrders); date the customer contacted us; item; what happened (damaged, wrong item, changed mind, other); photos received (yes or no); order total.

| Situation | Route |
| --- | --- |
| Within 30 days of delivery (any reason) | Standard return: the agent replies with the return steps (Sections 2, 3 and 5) |
| Damaged, reported after 30 days, photos received | Case-by-case review: the case goes to the returns team (Sections 3 and 6) |
| Damaged, reported after 30 days, no photos yet | Ask the customer for photos through the returns form, then route to case-by-case review |
| Anything the policy does not cover (for example a gift card) | The support lead decides |

Test cases: a normal case (day 20, unused), an incomplete case (no delivery date), an unclear case (wrong item or changed mind?), an exception (day 40, damaged, no photos).

### Pilot proposal for the operations director

Two weeks, three agents, damaged-item emails only, with every draft reviewed before it is sent. We measure the time agents spend per email, drafts that promise more than the policy allows, and complete cases sent to the returns team, against a baseline measured before the pilot.

## To repeat the troubleshooting practice

Make a copy of ShopAssist Returns with three faults:
1. Add a second instruction line that contradicts an existing one, for example "Keep every reply under two sentences." next to "List every exception that applies."
2. Add `files/policy-v1.pdf` to the knowledge, next to Version 2.
3. If you use Google Drive: put a policy file in a Drive folder that your connected account cannot open.
