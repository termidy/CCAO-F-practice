# Return reason codes

Every returned item gets one reason code. Only these three values are allowed:

| Code | Meaning |
| --- | --- |
| damaged | The item arrived broken, cracked, chipped or not working. |
| wrong_item | The customer received a different item, size, color or finish than they ordered. |
| changed_mind | The item is as ordered, and the customer no longer wants it. |

The table for the three return emails (`emails/three-return-emails.txt`) has one row per returned item, with these fields: order number, item, amount in US dollars, date the return was sent (YYYY-MM-DD), reason code.
