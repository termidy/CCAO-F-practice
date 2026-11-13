# Requirements: an intake form for damaged-item return emails

From "From a One-Line Brief to Requirements and a Plan" (Section 7): the use case and the acceptance criteria as Claude
wrote and checked them in the recorded run, with the operations director's answers.

## Use case

- Scope: damaged-item return emails only.
- User: a support agent in their first weeks.
- Inputs: the customer's email; the order number and the delivery date (the agent supplies them: DemoOrders is not
  connected); photos of the damage and packaging, if the customer sent them; DemoHome Return Policy, Version 2 (the
  only source).
- Output: a draft reply that names the policy section it relies on; a case summary for the returns team on every
  exception (order number, delivery date, the customer's description, photos: Section 6.3); a flag for missing
  information.
- Constraints: Claude drafts, an agent reads and sends every reply. No refund, replacement or exception is promised
  before the returns team decides (Sections 6.2, 6.4). No customer data in a tool the privacy and compliance lead has
  not approved.

## Three routes

1. Agent reply: the agent sends a draft from the policy.
2. Returns team: the case goes to case-by-case review with a case summary.
3. Support lead: the policy does not cover the case.

## Acceptance criteria (after the yes-or-no check)

1. On a test set of damaged-item emails that includes a report within 30 days, a report after 30 days and one with no
   delivery date, zero drafts promise a refund, replacement or other outcome for a report after 30 days, approve an
   exception, or say the customer pays return shipping for damage.
2. Every exception gets a case summary that lists the order number, the delivery date, the customer's description and
   the photos, or names any of these that is missing.
3. In one timed test, agents handle the same emails with and without Claude's drafts; the median time to name the
   policy section is at least X % lower with them (X is the operations director's to set).
