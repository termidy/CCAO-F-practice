# Start of Section 8: Troubleshooting and Optimization

Use this file if you start the course at Section 8. ShopAssist Returns is as in `start-s5.md`.

## What Section 7 produced

### Requirements

The use case, the three routes (agent reply, returns team, support lead) and the three acceptance criteria after the
yes-or-no check, as recorded: `files/catch-up/requirements.md`.

### Intake form and routing table

An artifact, "Damaged-item return intake". It keeps nothing and sends nothing; reloading it clears every field.

Fields, in order:
1. Does the email say the item arrived damaged? Yes, No or Not clear.
2. Does the policy cover this case? Five statements; tick every one that is true: the item isn't a lamp, kitchenware,
   textile or small furniture sold and shipped by DemoHome (1.2); the order wasn't bought on demohome.example, or
   doesn't ship to the US or EU (1.1); the customer cites legal or consumer rights, or asks for more than the policy
   gives (1.3); the damage wasn't there on arrival, or the problem isn't damage (3.1); something else doesn't fit the
   policy, or you aren't sure.
3. Dates: the delivery date (from DemoOrders, 1.4) and the date the customer's email was sent.
4. Case details: order number, what the customer says is damaged, photos of the damage (received or not), photos of
   the packaging (received or not).

| Order | If | Route | Policy |
| --- | --- | --- | --- |
| 1 | The email does not say the item arrived damaged (No or Not clear) | Hold, no route yet: ask the customer what is wrong, promise nothing | - |
| 2 | Any statement in field 2 is ticked | Support lead | the section of each ticked statement |
| 3 | A date is missing or not a real date | Hold, no route yet: look up the delivery date in DemoOrders | 1.4 |
| 4 | 0 to 30 days from delivery to the customer's email | Agent reply | 3.2, 5.3 |
| 5 | 31 days or more | Returns team, with a case summary | 3.3, 3.4, 6.1-6.4 |

The form checks the rows from top to bottom and uses the first that matches. Each row says what the reply may say and
what it must never say: never a refund or other outcome promised before the returns team decides, never return
shipping paid by the customer for damage. A missing item in the case summary is printed as MISSING, an unanswered
photo question as NOT ANSWERED. Open questions on the form, for the operations director: does day 30 count as inside
the window (the form counts it as inside for now), should the case summary include the ship date, and is the list in
field 2 complete.

Test cases and their routes:
- Normal: a cracked lamp base reported on day 5 after delivery, with photos -> agent reply.
- Incomplete: a chipped dinner plate, with photos, and no delivery date in the email -> hold, look up the date.
- Unclear: "The lamp does not look right." No photos, day 12. Answered Not clear -> hold, ask what is wrong.
- Exception: a cracked lamp base reported on day 40, with no photos -> returns team; the summary names both photo sets
  as missing.

### Pilot proposal for the operations director

Two weeks, three agents, damaged-item emails only, with every draft reviewed before it is sent. We measure the time agents spend per email, drafts that promise more than the policy allows, and complete cases sent to the returns team, against a baseline measured before the pilot.

## To repeat the troubleshooting practice

Make a copy of ShopAssist Returns with two faults:
1. Add a second instruction line that contradicts an existing one, for example "Length: Keep every reply under two
   sentences." under "under four sentences plus one line for each exception that applies".
2. Put `files/policy-v1.pdf` in the knowledge instead of Version 2.

Then run the cracked lamp (day 40, `files/emails/lamp-day40-sharp.txt`) and the blanket (day 20,
`files/emails/blanket-day20.txt`) in new chats, each with "Draft a reply to this customer email." above it, look at the instructions and the knowledge
list, fix one fault at a time, and run both cases again after each fix.
