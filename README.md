# CCAO-F practice: the DemoHome support team in the Claude app

Practice files for the hands-on lessons of the **Claude Certified Associate - Foundations (CCAO-F) Exam Prep** course. Every practice lesson is recorded in the Claude app (claude.ai on the web) with these files, so you can repeat each step on your own account.

There is no code here and nothing to install: you download the files and upload them to Claude, the way the lessons do.

**Everything here is fictional.** DemoHome, DemoAgency, DemoOrders, DemoParcel and DemoFreight are made-up companies; the people, orders, emails, policies, memos and numbers are invented for the course. `orders-export-raw.csv` holds made-up personal data on purpose, for the de-identification practice. Any resemblance to real people or companies is a coincidence.

## The story in one paragraph

DemoHome is an online store for home goods (lamps, kitchenware, textiles, small furniture), based in the US and shipping to the EU. Its support team answers customer emails about orders, returns and damaged items. In the course, the team moves its repeated returns work into the Claude app: first prompts in chat, then a Claude Project called **ShopAssist Returns** with the return policy as knowledge, then checks, a data procedure and a tested intake prototype. The running case: a ceramic table lamp (SKU HG-2207, order DH-418207) arrived with a cracked base, and the customer writes on day 40 after delivery. The return window is 30 days.

## What is here

| Folder | What it is |
| --- | --- |
| [`files/`](files/) | The practice files: the return policy (two versions), the complaint log, the order export, customer and team emails, memos and task sheets. |
| [`start/`](start/) | One file per section, `start-s2.md` to `start-s8.md`: the ShopAssist Returns instruction and the knowledge files expected at the start of that section, and what the earlier sections produced. Use it if you join the course in the middle. |
| [`lessons.md`](lessons.md) | Which practice lesson uses which file. |

## The files

| File | What it is | Used in |
| --- | --- | --- |
| `files/policy-v1.pdf` | DemoHome return policy, Version 1 (March 2026): Sections 1-3 and 6. The support lead decides exceptions. | Sections 1-4 |
| `files/policy-v2.pdf` | Version 2, effective October 1, 2026: Sections 1-6. The returns team decides exceptions; new sections on carrier damage claims and return shipping. | Sections 4-8 |
| `files/complaint-log.csv` | The support team's complaint log for Q3 2026 (July to September). No personal data. | Sections 2, 5, 6, 7 |
| `files/orders-export-raw.csv` | An export from the order system with made-up personal data. Only for the de-identification practice. | Section 6 |
| `files/order-status.csv` | The status of the orders in the order-status emails. | Section 3 |
| `files/emails/` | Customer emails, the returns team's email about Version 2, the agency's request, the operations director's brief and answers. | Sections 2-7 |
| `files/memos/finance-memo-frequent-returns.pdf` | A one-page finance memo, "Frequent returns are a sign of abuse". | Section 5 |
| `files/memos/ai-use-policy.pdf` | DemoHome's one-page AI use policy. | Section 6 |
| `files/tasks/` | Task sheets: four tasks for four features, classification labels, reason codes, criteria for order-status replies. | Sections 2, 3, 5 |
| `files/catch-up/` | If you join later: the checked complaint summary and the whole three-step chat from Section 2, and the requirements from Section 7, as recorded. | Sections 3, 5, 7, 8 |
| `files/project/instruction-short.txt` | The first, short instruction of ShopAssist Returns. | Section 4 |
| `files/drive/DemoHome Return Policy v2.docx` | Version 2 as a shared document for Google Drive. Its return shipping table is a picture. | Section 4 |

The customer emails mention photos; the photos are not included. Treat "photos attached" as a fact of the case.

## How to use it

1. Download the repository: **Code > Download ZIP**, then unzip it. Or `git clone https://github.com/termidy/CCAO-F-practice.git`.
2. Open [claude.ai](https://claude.ai) and start a new chat for every try, as the lessons do. Attach a file with the **+** button in the message box, or paste its text.
3. Projects: create one with **Projects > New project**, then add files to its knowledge and write its instructions. The exact text for each section is in `start/`.
4. Upload only these course files. Never upload real customer or company data to practise.

### On the Free plan

You can repeat almost every practice on the Free plan. As of November 2026:

- Free has the Sonnet and Haiku models. Opus and Fable need a paid plan.
- Research (multi-step research with sources), search across past chats, and RAG for very large Project knowledge need a paid plan. Web search in a normal chat is on every plan.
- Projects are on every plan; Free allows up to 5.
- Artifacts (for example the Docs template) and file creation (.docx, .xlsx, PDF) are on every plan. Sharing an artifact by link needs a paid plan.
- The Google Drive and Gmail connectors are available on every plan on the web.

Where a lesson uses a paid feature, the video marks it "paid plan"; on Free, watch that step and repeat the rest. Plans and menus change: if a setting is not where the lesson shows it, look for it by its name in Settings.

### Google Drive and Gmail

The connector practice uses a Google account that holds only course files. To repeat it, use a separate practice Google account, not your personal one:

1. In Google Drive, create a folder named **DemoHome Policies** and upload `files/drive/DemoHome Return Policy v2.docx`. Open it as a Google Doc.
2. Put the returns team's email into the mailbox: send yourself an email with the subject and text of `files/emails/returns-team-v2-date.txt`.
3. In Claude, connect Google Drive and Gmail to that account, and connect only what the task needs.

## License

The files are free to use for learning.
