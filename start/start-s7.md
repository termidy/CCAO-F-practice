# Start of Section 7: Workflow Integration and Solution Design

Use this file if you start the course at Section 7. ShopAssist Returns is as in `start-s5.md`.

## What Section 6 produced

### De-identification procedure

1. Work on a copy of the file, in a spreadsheet, before anything is uploaded.
2. Classify every column (public, internal, confidential, personal, payment card data), not the file as a whole.
3. Delete the columns the task does not need, starting with direct identifiers (name, email, phone, street address, account number, card digits).
4. Replace the order number with a running number.
5. Check whether a combination of the remaining columns (for example postal code, date and product) still points to one person. Coarsen or drop columns until it does not.
6. Upload only the copy, and only to the approved tool in your work account.

### Five questions before working with data

1. Is the tool approved for this data?
2. Is it my work account?
3. Who can see it: what does a shared link to the chat or the artifact open?
4. How long is it kept, and who sets that?
5. Whose approval is needed before anything leaves the company?

### Reply to the agency (draft, waiting for approval)

```text
Hi Nora,

Thank you for the request. We cannot send the complaint log itself: it is internal data, and our AI policy does not allow it to go to an outside workspace.

What we can do: we will prepare a short summary of the main complaint themes, with no customer or order data, in our own account. Before it goes to you, it needs approval from Tom Hale, our privacy and compliance owner. We will send it once it is approved.

Best,
Dana
```

## Files you need in this section

- `files/emails/elena-brief.txt`, `files/emails/elena-answers.txt`
- `files/policy-v2.pdf`, `files/complaint-log.csv`
