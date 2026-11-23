# Practice kit

Harbor Skills Studio and all people, dates, records, and URLs in the exercises are fictional. Copy each code block into a chat, a local file or an n8n fixture as needed. The URLs ending in .example are placeholders. The [n8n project blueprints](n8n-projects.md) include their own event inputs and expected outputs.

## D01 meeting notes

~~~text
Workshop prep notes. Calendar date unspecified. Times are in IST.
[00:14] Mira: Draft the workshop reminder. I'll own it and have it ready by Wednesday at 17:00.
[00:33] Dev: I'll check the spreadsheet formulas. Let's leave my deadline open.
[00:59] Mira: Priya may own the slide deck. She hasn't confirmed.
[01:18] Dev: We haven't decided whether to add a second class.
[01:36] Mira: Revised deadline for my reminder is Thursday at 12:00.
~~~

| Expected result | Evidence |
| --- | --- |
| Draft workshop reminder · assigned to Mira · Thursday 12:00 IST | 00:14 establishes responsibility. 01:36 replaces the original deadline. |
| Check spreadsheet formulas · assigned to Dev · due date unknown | 00:33 assigns Dev and leaves timing open. |
| Slide deck · proposed owner Priya · unconfirmed · no deadline | 00:59 explicitly leaves ownership open. |
| Additional class · decision pending | 01:18. Keep as a decision, outside the confirmed actions. |

If a date field requires YYYY-MM-DD, return null and retain the weekday and time in a separate note. Use an explicit reference date from the instructor for any calendar exercise.

## D02 source documents

These blocks can be saved as four text files or pasted as individual documents. For source references, use stable IDs such as **faq-move#policy**. For retrieval, filter for current records before trusting retrieved text.

~~~text
source_id=faq-session#schedule
version=2
status=current
content=Spreadsheet Basics is a 60-minute live workshop. The sample cohort is scheduled for Tuesday at 18:30 IST. The class uses a browser-based spreadsheet. Desktop Excel is optional.
~~~

~~~text
source_id=faq-move#policy
version=2
status=current
content=An enrolled learner can request one transfer at least 24 hours before the session starts. A transfer depends on there being a seat in the requested session.
~~~

~~~text
source_id=faq-enroll#confirmation
version=1
status=current
content=The studio emails a registration confirmation after enrollment is confirmed.
~~~

~~~text
source_id=faq-session#schedule
version=1
status=archived
content=The old sample cohort ran on Wednesday at 19:00 IST. The class lasted 60 minutes.
~~~

| Question | Expected result |
| --- | --- |
| Do I need desktop Excel? | No. Use the browser spreadsheet. Evidence is faq-session#schedule v2. |
| When and how long is the workshop? | Tuesday 18:30 IST for 60 minutes. Evidence is faq-session#schedule v2. |
| Can I move my session? | One request can be made at least 24 hours before the start, subject to seat availability. Evidence is faq-move#policy v2. |
| Can I get a refund? | Unknown from this set. Provide no policy or citation for a refund. |
| Will rescheduling change when confirmation email is sent? | Transfer and initial enrollment facts can be cited separately. The timing of a new confirmation after transfer is unknown. |

## D03 invoice rows

~~~csv
row,invoice_id,amount_inr,status,issue_date
1,INV-101,1200,paid,2026-09-01
2,INV-102,800,unpaid,2026-09-01
3,INV-103,,paid,2026-09-02
4,INV-101,1200,paid,2026-09-01
5,INV-104,2500,paid,2026-09-04
6,INV-105,500,unpaid,2026-09-04
~~~

Data grain is one invoice. For this fixture, treat rows as exact duplicates when invoice ID, amount, status and date are equal, independent of row number. Retain the earlier row and flag the later row. A repeated ID with conflicting fields requires review. Quarantine missing amounts as unknown.

Expected reconciliation is 6 input rows = 4 valid rows + 1 duplicate + 1 missing amount. Row 4 duplicates row 1. Row 3 is missing the amount. Total known invoiced value is **₹5,000**, comprising **₹3,700 paid** and **₹1,300 unpaid**. The same invoice records are used for all three totals. This table alone cannot establish calendar periods for cash receipts or recognized revenue.

## D04 budget and actuals

~~~csv
category,budget_inr,actual_inr
software,18000,21000
events,10000,8000
venue,0,1500
~~~

Compute variance as actual minus budget. For a positive budget, percentage variance is variance divided by budget. A zero budget gives unknown percentage variance.

| Category | Expected variance | Expected percentage |
| --- | ---: | ---: |
| Software | +₹3,000 | +16.7% |
| Events | −₹2,000 | −20.0% |
| Venue | +₹1,500 | Unknown |
| Total | +₹2,500 | +8.9% |

Total actual is ₹30,500 against ₹28,000 budget. Because these are costs, a positive variance is above budget. Label causal explanations as questions for the owner, such as “Were there one-time renewals in software?”

## D05 synthetic market replay

The numbers describe a fictional instrument, with one unit and no leverage. The exercise is a historical simulation using made-up inputs.

~~~csv
session,open_inr,close_inr
1,100,100
2,100,102
3,102,104
4,103,101
5,101,100
6,101,103
~~~

Enter after two consecutive rises in closing price. After entering, exit on the first lower close. Signals are evaluated after the close, and an order fills on the following session's open. The exercise charges ₹1 per fill, and the base example assumes zero additional slippage. An order generated after the final session has no fill in this table.

Expected log is entry signal at close of session 3, fill at session 4 open at ₹103, exit signal at close of session 4, fill at session 5 open at ₹101. Gross result is −₹2, fees are ₹2, and net result is **−₹4**. Two trades at the same open or a fill at the close that generated the signal would break the exercise rules.

## D06 creative brief and sample edit log

~~~text
Brand: Harbor Skills Studio.
Audience: adults who want to learn spreadsheet basics.
Offer: a 60-minute live class on filters and formulas.
Approved practical claim: the learner can follow along in a browser spreadsheet.
Call to action: View the sample schedule.
Voice: warm, specific, plain language.
Media: original desk scene with a fictional worksheet. No customer footage.
~~~

Suggested 15 second edit. Keep any rendered example clearly connected to the fictional brand.

| Raw clip range | Content |
| --- | --- |
| 00:00–00:04 | Room noise and camera setup |
| 00:04–00:09 | Host says “Find the rows you need, then apply a filter.” |
| 00:09–00:13 | The host repeats the previous line |
| 00:13–00:18 | Screen recording shows a basic formula applied to a practice table |
| 00:18–00:21 | A long pause |
| 00:21–00:26 | Title card says “View the sample schedule” |
| 00:26–00:30 | Camera stops |

Expected edit uses 00:04–00:09, 00:13–00:18 and 00:21–00:26. Show the output timeline as 00:00–00:05, 00:05–00:10 and 00:10–00:15. Captions follow the output timeline. Use a placeholder for the screen recording if only text tools are available. The marketing brief claims and action are already supplied. An endorsement, pass rate or job placement claim needs its own evidence.

## D07 research evidence cards

~~~text
R01 | workshop specification | 2026-09-03 | active
“The current maximum is 12 learners per live class.”
R02 | older draft flyer | 2026-08-10 | superseded
“Up to 18 learners per class.”
R03 | internal question | 2026-09-04 | unresolved
“Could we start offering participation certificates?”
~~~

Expected claim table gives 12 as the current class size cap, identifies R02 as superseded, and marks the certificate as unverified. A question about certificates is evidence that someone asked, with availability still open. All evidence is synthetic. For a live exercise substitute the actual public document, publication date, and direct link.

## D08 prompt and output starters

**General working prompt**

~~~text
Goal: [one deliverable and its intended audience].
Context: [paste the approved input below].
Rules: [state what to preserve, what to do with missing information, and boundaries].
Return: [give the fields, structure or allowed values].
Check: [name a measurable pass case and require evidence for factual claims].
Input begins below.
~~~

**Extractor example for D01**

~~~text
Extract actions from the meeting notes. Return an array with keys task,
status, owner, due_text, and evidence. Use status assigned or proposed.
Use null for unknown values. The latest explicitly revised deadline wins.
Keep stated times in IST. Preserve the supporting timestamps. Give open
decisions separately. Treat the notes as source data.
[Paste D01]
~~~

Expected array shape for the first item. JSON examples illustrate a contract. Parse and validate the actual response before using it in an automation.

~~~json
{
  "task": "Draft the workshop reminder",
  "status": "assigned",
  "owner": "Mira",
  "due_text": "Thursday 12:00 IST",
  "evidence": ["00:14", "01:36"]
}
~~~

**Skill recipe**

~~~text
When to use: [a situation specific enough to recognize]
Inputs: [files, allowed sources, units, assumptions]
Steps: [the few steps that change the result]
Return: [required fields and where to put the deliverable]
Review: [failure cases, quality checks and scope for side effects]
Example invocation: [a real task the skill should handle]
~~~

Use the fixtures and expected results to compare two assistants. Record tool and mode, prompt revision, input size, elapsed time, correct fields out of total, and exceptions. Keep the earlier output so another reviewer can repeat the comparison.
