# Practical AI Course Guide

Use this complete Markdown file with a chat assistant or an agent that accepts file attachments. The course follows the 40 video topics published for Zero to Infinity with AI. The teaching material, practice data and project designs are original.

**Prompt to paste after attaching the file**

> Use the attached Practical AI Course Guide as your curriculum. Start with the instructor instructions under Teach Practical AI. Teach me F01 one step at a time, give me the exercise before showing the answer, and check my result against the pass criteria. If I ask you to build a project, use the named blueprint and its sample inputs.

Use the lesson or project IDs to jump to the material you need.

- [Agent instructions](#teach-practical-ai)
- [Public syllabus and correspondence](#public-syllabus-and-correspondence)
- [Instructor playbook](#instructor-playbook)
- [Practice kit](#practice-kit)
- [F01–F03 · AI concepts](#ai-concepts)
- [T01–T10 · Essential AI tools](#essential-ai-tools)
- [W01–W04 · Everyday work](#everyday-work-with-ai)
- [S01–S05 · Specialized AI applications](#specialized-ai-applications)
- [N01–N13 · n8n and APIs](#n8n-and-apis)
- [P01–P09 · n8n project blueprints](#n8n-project-blueprints)
- [V01–V05 · Website building](#building-websites-with-ai)
- [Website and FAQ capstone](#website-and-faq-capstone)

---

## Teach Practical AI

Use this curriculum to teach a beginner, help an instructor deliver a class, or build a practice project. The lesson IDs map to all 40 video topics in the public outline for Zero to Infinity with AI. The explanations, examples, exercises, answer keys, project designs, and course delivery plan were authored for this guide.

### Choose the work the user requested

| Request | Start here |
| --- | --- |
| Explain what the paid course advertises | [Public syllabus and correspondence](#public-syllabus-and-correspondence) |
| Teach me or prepare a class | [Instructor playbook](#instructor-playbook) and the requested module below |
| Build, debug, or review an n8n project | [n8n lessons](#n8n-and-apis), the selected [project blueprint](#n8n-project-blueprints), and its fixtures |
| Build a practice website or combined project | [Website lessons and capstone](#building-websites-with-ai) and the referenced fixtures |
| Supply sample inputs, expected results, or prompt starters | [Practice kit](#practice-kit) |

| Lessons | Module |
| --- | --- |
| F01–F03 | [AI concepts](#ai-concepts) |
| T01–T10 | [Essential tools](#essential-ai-tools) |
| W01–W04 | [Everyday work](#everyday-work-with-ai) |
| S01–S05 | [Specialized applications](#specialized-ai-applications) |
| N01–N13 | [n8n and APIs](#n8n-and-apis) |
| V01–V05 | [Website building with AI](#building-websites-with-ai) |

Open the selected chapter and any resources it references. For a new learner without a requested starting point, begin with F01 and use the learner's job or goal to adapt the examples. In a single Markdown edition, look up the same headings and IDs within that file.

### Deliver or build

- **Tutoring.** State the skill the learner will practice. Introduce the idea, work the demo, then give the learner the exercise. Wait for their attempt before revealing the answer when tutoring interactively. Give specific feedback against the pass condition and record the result in the format in the playbook.
- **Instructor materials.** Turn the selected lesson's talk track, demo, and exercise into a ready to deliver session. Include the words to say, what to display, the handout, and a separate answer key. Use original Harbor Skills Studio examples unless the user supplies a scenario. If the user asks for a complete workshop, produce the requested materials in the current turn.
- **Build or debug.** Use the project blueprint's data contract and cases to produce the requested local artifacts or configuration steps. Start with synthetic fixtures and a manual run. Use a model stub or a local simulation when credentials or a live service are unavailable. Verify the requested behavior when the environment permits. Report the actual files, how to run them, checks performed, and what still depends on the user's environment.
- **Review.** Compare the submitted output against the expected result, call out discrepancies with evidence, and offer one revision exercise or patch as appropriate. A plausible model answer is insufficient evidence that a workflow ran.
- Use the vendor references in the source map to check current control names, supported features, pricing, and plan availability when those details affect the task. Use the user's chosen tools when they meet the project contract.
- Keep keys in the platform's credential store or environment variables. Use the supplied fictional inputs for instruction. Enable live data access, sending, public deployment, or production triggers when the user's request authorizes that specific action and the relevant credentials and destination are available.

### Example requests

- “Teach me N01 and N02 using a mock API. Give me the exercise before the solution.”
- “Prepare a 60-minute instructor session for W01 and W02, including speaker notes, a handout, and an answer key.”
- “Build P03 with mock emails. Save the implementation and show the expected output for E-101 through E-104.”
- “Review my P06 demo against the source IDs and unknown-answer test in the practice kit.”

---

## Public syllabus and correspondence

The public Level Up outline was inspected with all six modules expanded on **23 November 2026**. The page reports **80 items**. In the expanded list, **40 are marked Video and 40 are marked Resources**, with one of each per topic. The table below paraphrases every distinct video topic in its published order. Each ID points to an original chapter in this guide. The contents of the provider's videos and resource attachments, the length of each video, and the details of the live classes could not be verified from the public outline. [Level Up course outline](https://levelup.nagrawal.com/course/zero2infinitywithai#overview)

The sales page advertises a curriculum grouped into five core modules, roughly 15–20 hours of recorded material, 12 months of access, one live session each month with examples and questions, and a WhatsApp group. It also names NotebookLM, which has no dedicated title in the expanded outline. T03 includes a separate NotebookLM exercise for that reason. The sales page displays ₹10,000 and the learning platform showed ₹9,999 for the full payment option when checked. [Sales page](https://zerotoinfinitywithai.com/) · [Level Up course outline](https://levelup.nagrawal.com/course/zero2infinitywithai#overview)

| Portal section and item count | ID | Published video topic, paraphrased |
| --- | --- | --- |
| [AI concepts](#ai-concepts) · 3 videos + 3 resources | F01 | Generative AI and intelligent automation |
| | F02 | How language models learn, generate answers, and get things wrong |
| | F03 | Retrieval augmented generation (RAG) with documents |
| [AI tools](#essential-ai-tools) · 10 + 10 | T01 | ChatGPT features and model selection |
| | T02 | Claude features and model selection |
| | T03 | Gemini and Google's AI tools |
| | T04 | Using Wispr Flow to dictate work |
| | T05 | Generating video with Higgsfield |
| | T06 | Beginner use of the Grok assistant |
| | T07 | HeyGen avatars and ElevenLabs audio |
| | T08 | Meta Muse |
| | T09 | Apple Intelligence |
| | T10 | Using ChatGPT as a voice assistant |
| [AI for everyday work](#everyday-work-with-ai) · 4 + 4 | W01 | Prompt design using context and constraints |
| | W02 | Research and verification with AI |
| | W03 | Creating reusable AI agent skills |
| | W04 | Applying AI to routine tasks |
| [Specialized applications](#specialized-ai-applications) · 5 + 5 | S01 | Finance use cases |
| | S02 | Using Claude to assist with video editing |
| | S03 | AI in trading |
| | S04 | Data analysis with AI |
| | S05 | Running models locally |
| [n8n](#n8n-and-apis) · 13 + 13 | N01 | API fundamentals |
| | N02 | Starting with n8n |
| | N03 | Collecting Instagram Reel information in a first workflow |
| | N04 | Building a first n8n tool calling agent |
| | N05 | Fetching weather data and technology news |
| | N06 | Building an email assistant |
| | N07 | Automating parts of a job search |
| | N08 | Building a Telegram bot |
| | N09 | Building an n8n agent that retrieves document evidence |
| | N10 | Building an AI voice agent for sales |
| | N11 | Building a content creation agent |
| | N12 | Monitoring a portfolio with AI and n8n |
| | N13 | Using Claude to help build n8n workflows |
| [Website building with AI](#building-websites-with-ai) · 5 + 5 | V01 | Introduction to building websites by prompting AI |
| | V02 | Building and refining sites with Hostinger and Claude Code |
| | V03 | Publishing a site with a domain, hosting and DNS |
| | V04 | Search visibility, SEO and Google Search Console |
| | V05 | Website measurement with Google Analytics |

The guide's project settings, timelines, drills, synthetic data, and suggested tool choices fill in practical details for independent use. They are editorial choices for this curriculum. The [instructor playbook](#instructor-playbook) includes an optional monthly update format for someone teaching over a longer period.

### Provider references

Use these official resources to check current setup and availability. The lesson titles are evidence that a tool was listed. Feature availability can depend on the account, device, plan, region, or release. A pasted text exercise or fixture gives the same learning objective when the preferred tool is unavailable.

| Topic | Official reference |
| --- | --- |
| ChatGPT text, files, and voice | [Capabilities](https://help.openai.com/en/articles/9260256-chatgpt-capabilities-overview) · [Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice) |
| Claude files and prototypes | [Files](https://support.claude.com/en/articles/8241126-upload-files-to-claude) · [Artifacts](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them) |
| Gemini and NotebookLM | [Gemini Help](https://support.google.com/gemini/?hl=en) · [NotebookLM Help](https://support.google.com/notebooklm/?hl=en) |
| Dictation | [Wispr Flow](https://wisprflow.ai/) |
| Video, avatars, audio | [Higgsfield](https://higgsfield.ai/) · [HeyGen Help](https://help.heygen.com/en/) · [ElevenLabs text to speech](https://elevenlabs.io/docs/overview/capabilities/text-to-speech) |
| Grok | [Grok on X](https://help.x.com/en/using-x/about-grok) |
| Meta Muse | [Meta's Muse assistant introduction](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/) · [Muse model family](https://ai.meta.com/blog/introducing-model-meta-superintelligence-labs) |
| Apple Intelligence | [Compatibility and setup](https://support.apple.com/en-us/121115) |
| Local models and video processing | [Ollama quickstart](https://docs.ollama.com/quickstart) · [FFmpeg manual](https://ffmpeg.org/ffmpeg.html) |
| n8n basics and self hosting | [n8n Academy](https://learn.n8n.io/) · [Data structure](https://docs.n8n.io/build/work-with-data/understand-n8ns-data-structure) · [Hosting](https://docs.n8n.io/deploy/host-n8n) |
| n8n integrations and persistent records | [HTTP Request](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.httprequest/) · [Webhook](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.webhook/) · [Data Table](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.datatable/) · [Error handling](https://docs.n8n.io/build/flow-logic/handle-errors-gracefully) |
| n8n assistants | [AI Agent node](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.agent/) · [Retrieval in n8n](https://docs.n8n.io/build/integrate-ai/understand-ai-components/retrieve-relevant-context) |
| Optional n8n app integrations | [Instagram Platform](https://developers.facebook.com/docs/instagram-platform/) · [Telegram Bot API](https://core.telegram.org/bots/api) · [Open-Meteo weather API](https://open-meteo.com/en/docs) |
| Website building | [Hostinger Website Builder](https://www.hostinger.com/website-builder) · [Claude Code](https://code.claude.com/docs/en/overview) |
| Website deployment and accessibility | [GitHub Pages](https://docs.github.com/en/pages/quickstart) · [Cloudflare DNS record guide](https://www.cloudflare.com/learning/dns/dns-records/) · [W3C accessibility checks](https://www.w3.org/WAI/test-evaluate/preliminary/) |
| Website measurement | [Google SEO starter guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) · [Search Console URL Inspection](https://support.google.com/webmasters/answer/9012289) · [Google Analytics setup](https://support.google.com/analytics/answer/9304153) |

---

## Instructor playbook

### Choose a delivery path

The default learner can use a browser and a spreadsheet and is new to programming. The portable starting setup is one text assistant, a text editor, a browser, and the [practice kit](#practice-kit). Run a tabletop simulation or a local mock for any vendor workflow the learner cannot access. Introduce an API, local models, or a coding agent as the corresponding exercise calls for it.

| Delivery plan | Sequence and work product |
| --- | --- |
| First session, about 60 minutes | F01 (15 min), W01 (20 min), and W02 (20 min), then a five minute exit ticket. Hand in a revised prompt and a verified claim table. |
| Everyday productivity, three sessions | F01–F03, then T01–T04 and T10 with W01/W02, then W03/W04. Hand in a reusable instruction file and a meeting follow up with traceable decisions. |
| Automation, four sessions | N01–N04 on data and node setup, N05–N08 on small workflows, N09–N12 on agents and monitoring, N13 on assisted implementation and review. Choose one project, satisfy its pass cases, and explain its failure route. |
| Complete course, six units | Follow F, T, W, S, N, V in that order. Allow roughly 2–4 hours per unit except n8n, which can take 6–9 hours if the learner builds multiple projects. Give the capstone another 3–5 hours if requested. This is an estimate for the independent exercises. |

Ask the learner to do three short tasks before the first session: turn a vague request into a deliverable, name a fact they'd verify before sending output, and identify a repetitive workflow with a clear input and result. Use the answers to set the starting level. A strong learner can begin at W03 or N01 and use F02/F03 as reference.

### Teach a lesson

1. Open with a real task and a measurable goal. For W01, tell the learner, “By the end of this session, you can extract verified owners and deadlines from confusing notes.”
2. Say the talk track and show the input verbatim. Ask the learner to predict a common bad output, such as a deadline invented from a phrase like “I'll look at it.”
3. Run the worked example in small steps. Explain what you changed, then highlight a concrete output field before and after the change. If a feature is unavailable, use the fallback and keep the same output contract.
4. Give the learner the practice part, plus time to try it. If they stall, point to one field or one failing case. Surface the answer key after the attempt when teaching interactively. When preparing class materials, keep the answer key under its own heading.
5. Close with an exit ticket. Ask the learner to name one condition that should trigger a refusal to guess, a manual review, or a different tool. Record observed evidence of the skill.

Default lesson timing for a short class is 2 minutes for the goal, 4 for the concept, 6 for the demo, 8 for practice, and 3 for feedback. Adjust the time to the scope. For a full course writing request, turn each lesson into a script, a learner handout, and an answer key with consistent outputs. Reuse the examples so learners can compare methods across tools.

### Review and grade

Score each dimension from 0 to 2. Give 0 for missing or incorrect work, 1 for a mostly working result with a specific gap, and 2 for a result that meets the criteria with evidence. Suggested pass is 8 out of 10, including 2 for scope and review on projects with external integrations.

| Dimension | Evidence for 2 |
| --- | --- |
| Task fit | The result matches the lesson's objective and output shape. |
| Accuracy | Facts, identifiers, dates and calculations match the fixture or a checked primary source. |
| Reproducibility | Another learner can use the recorded inputs and steps to reach the same result or evaluate variation. |
| Exception handling | The learner handles the prescribed missing, duplicate, ambiguous, or failed case and can explain the behavior. |
| Scope and review | Data and actions stay within the project brief and the learner can name the boundary between draft and live operation. |

Keep a short progress record when the user requests a course rather than a single answer. The next agent can continue from it.

~~~text
Lesson or project ID:
Learner goal:
Input or fixture:
Work submitted:
Pass checks with evidence:
One correction:
Next lesson or project:
~~~

### Teach monthly update sessions

Run a 60 minute session on request. Use 10 minutes for three verified changes since last session, 15 for a demo of one change against an existing fixture, 20 for one applied problem from the class, 10 for questions, and 5 for takeaways. Keep a dated log of provider links, capabilities tried, observed changes, and any exercise that needs an update. Review cost and availability using current official sources when these affect participants. A paper mock or old baseline counts as a comparison if it is identified clearly.

Use this sequence as an optional year of original sessions. Each session revisits a result learners can compare with their earlier work.

| Session | Lab and evidence |
| --- | --- |
| 1 | Compare two assistants' extraction accuracy on D01. Record one tradeoff in quality or turnaround. |
| 2 | Ground answers on D02. Log which question still needs human follow up. |
| 3 | Turn a dictated idea into a task and a draft. Compare transcript errors before and after editing. |
| 4 | Produce a 15 second workshop teaser. Fix a discontinuity and demonstrate captions. |
| 5 | Reconcile D03 and explain D04 without attributing unsupported causes. |
| 6 | Replay D05 and inspect what fees did to the example. |
| 7 | Process the P02 weather and news fixture, then simulate a partial input outage. |
| 8 | Reuse P03 for email intake or P04 for job tracking. Show how duplicates are handled. |
| 9 | Evaluate the P06 answer that cites a policy and the answer that has to abstain. |
| 10 | Build or improve a locally previewed workshop page. Show its smallest viewport and keyboard path. |
| 11 | Inspect a sample page for search readiness and collect one approved synthetic analytics event. |
| 12 | Demo the combined website and FAQ project, show one unsuccessful case, and identify a maintenance owner. |

---

## Practice kit

Harbor Skills Studio and all people, dates, records, and URLs in the exercises are fictional. Copy each code block into a chat, a local file or an n8n fixture as needed. The URLs ending in .example are placeholders. The [n8n project blueprints](#n8n-project-blueprints) include their own event inputs and expected outputs.

### D01 meeting notes

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

### D02 source documents

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

### D03 invoice rows

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

### D04 budget and actuals

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

### D05 synthetic market replay

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

### D06 creative brief and sample edit log

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

### D07 research evidence cards

~~~text
R01 | workshop specification | 2026-09-03 | active
“The current maximum is 12 learners per live class.”
R02 | older draft flyer | 2026-08-10 | superseded
“Up to 18 learners per class.”
R03 | internal question | 2026-09-04 | unresolved
“Could we start offering participation certificates?”
~~~

Expected claim table gives 12 as the current class size cap, identifies R02 as superseded, and marks the certificate as unverified. A question about certificates is evidence that someone asked, with availability still open. All evidence is synthetic. For a live exercise substitute the actual public document, publication date, and direct link.

### D08 prompt and output starters

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

---

## AI concepts

Three lessons cover why language models are useful, how they make mistakes, and how a document retrieval system gives an answer a source. Start with the first three fixtures as needed. [Practice kit](#practice-kit)

### F01 Generative AI and automation

**Outcome.** Given a work goal, choose a rule, a model, or a supervised sequence of both and explain the choice.

**Say.** “I use a rule when the same input should always lead to the same decision. I can use generative AI when the task is to draft, summarize, or interpret varied language. A workflow connects steps in a defined order. An agent is useful when the model has to choose among tools based on the request. The tools still need a clear contract.”

**Show.**
1. Classify the D03 invoice rows with the fixed rule “flag missing amounts.” There is exactly one matching row and it is visible in the data.
2. Use a text model to draft a two sentence reminder using D06. Supply only the class description and its approved claims. Ask the model to leave open dates and recipients as placeholders.
3. Draw the combined flow “receive approved notes → extract the action → check the owner → create a draft.” Repeat the same input. Compare the deterministic output from the amount rule with possible differences in a drafted sentence.
4. Add a tool choice only if different requests genuinely need it. Compare “format the schedule” with “look up the schedule or transfer policy and answer the question.” Explain why the second task can benefit from retrieval.

**Practice.** Design how you would process a learner's email asking whether Excel is required. Mark which step retrieves evidence, which step drafts prose, and where a person checks the response before sending.

**Pass.** The answer identifies the browser spreadsheet rule using D02, produces a draft, and marks sending as a separate step. The learner can explain that the model's prose is variable while the source rule is stable.

### F02 How language models learn and make mistakes

**Outcome.** Explain training and inference in plain language, then detect an unsupported claim in a realistic answer.

**Say.** “During training, the model learns patterns represented by weights. During inference, it uses those weights and the context we give it to predict text in pieces called tokens. An individual conversation supplies temporary working context. A plausible sentence can still get a detail wrong, especially when the prompt assumes a fact the source never states.”

**Show.**
1. Ask “Describe Harbor Skills Studio's participation certificate” with no evidence. Read the answer and highlight any factual assertion. The model may also ask for context. Both outcomes are useful for the demo.
2. Paste D07 and ask “Using only R01–R03, state whether participation certificates are available. Cite a card ID and distinguish a question from an approved policy.”
3. Require three fields, claim, evidence and status, then check the actual quoted passage. Label the output as insufficient evidence. If the response says certificates are available, ask it to point to the sentence that asserts availability.
4. Explain that longer context can help only if it contains the right evidence. Large inputs may bury the important detail or exceed product limits. Save source excerpts and expected answers when comparing runs.

**Practice.** Compare one answer from the vague prompt with one grounded answer. Mark each factual claim as supported, contradicted or unknown. If both runs abstain, use the fabricated candidate “Certificates are available on request” as the claim to grade.

**Pass.** The learner marks certificate availability unknown, cites R03 as a question, and correctly treats R02's older class cap as superseded by R01. They can explain why the model sounding confident did not affect the result.

### F03 Retrieval augmented generation with documents

**Outcome.** Trace an answer from a retrieved passage and use a consistent fallback when evidence is missing.

**Say.** “RAG means the application finds useful passages first and then gives them to a model to draft the answer. I can inspect what was retrieved separately from the answer. A search miss, an archived source, or a misread passage all lead to different fixes.”

**Show.**
1. Load D02 as separate records. Keep source ID, version and current or archived status. Use one FAQ section per chunk in this small example.
2. Search current records for the question “Can I switch my booking?” A keyword search can miss that “switch” and “transfer” express the same idea. Demonstrate a synonym mapping or a semantic search when available.
3. Pass the transfer passage to a text model with this instruction, “Answer using the retrieved passage. Include the deadline and the seat condition. Attach the source ID. If there is no basis for the answer, say this set does not answer it.” Manually compare the resulting statement to the passage.
4. Ask for a refund. With no supporting FAQ, give a short unknown answer and explain how the learner can request a current policy. Ask for workshop time and check the current version beats the archived schedule.

**Practice.** Create three examples with expected retrieval IDs and answer status. Label a failure as retrieval, generation, or source maintenance. Show the received passages and the final text side by side.

**Pass.** The answer for transfer says one request, at least 24 hours, and seat availability with faq-move#policy. Refund abstains. The schedule uses version 2. Advance to N09 for a workflow implementation. [Retrieval in n8n](https://docs.n8n.io/build/integrate-ai/understand-ai-components/retrieve-relevant-context)

---

## Essential AI tools

Use the same known inputs across tools so learners can compare the outputs. Record which feature was available on the learner's device or account. Each exercise has a text or storyboard fallback. [Practice kit](#practice-kit) · [Provider references](#provider-references)

### T01 ChatGPT features and model selection

**Outcome.** Choose a chat mode for drafting, data inspection or evidence lookup and review the result against a known answer.

**Say.** “I start with the task and evidence. Drafting one paragraph takes less setup than analyzing a table. If a feature can calculate, inspect files, or look up evidence, I show exactly what it read or computed before I use the output.”

**Show.**
1. Start a fresh chat. Paste D03 or save it as a CSV and attach it if file support is available. Ask, “Identify the grain, report unusable rows, and calculate gross valid invoice, paid and unpaid amounts. Show the calculation and IDs behind the totals.”
2. Review the discovered columns and the handling of the missing amount. Confirm how the exact duplicate was recognized and whether the result is based on actual computation or a table read.
3. Ask for a one paragraph draft with the reporting limitation. If the draft uses “cash received in September,” highlight that D03 contains invoice dates only.
4. If two model modes are available, repeat with the same prompt in separate chats. Record mode, elapsed time, supported claims and arithmetic. If you need current facts, use search when available and open a cited source before reusing its claim.

**Practice.** Run the invoice prompt on D03 and produce a cleaned table, exceptions and a manager summary. State which capability you used and how you verified one number independently.

**Pass.** The output has four valid invoices; ₹5,000 total, ₹3,700 paid and ₹1,300 unpaid; one exact duplicate and one missing amount. A manager can trace each figure. [ChatGPT capabilities](https://help.openai.com/en/articles/9260256-chatgpt-capabilities-overview)

### T02 Claude features and model selection

**Outcome.** Use Claude to analyze source text and turn the result into a small usable artifact or a plain text equivalent.

**Say.** “I start with a short, evidence-first instruction. I add a prototype only after the answer is correct. The design can be good while the source interpretation is wrong, so I check both independently.”

**Show.**
1. Paste or attach D02. Ask Claude to make an FAQ table with Question, Answer, and Source ID. Tell it which version is current and require unknown for unprovided policies.
2. Ask for a 60-second review of what the browser spreadsheet rule means for a learner. Ask the model to keep “desktop Excel optional” and preserve both conditions for transfers.
3. If an artifact or code preview is available, ask for an HTML FAQ card with visible source labels. Constrain it to the three current facts and one explicit unknown. Open the preview or save the HTML locally. On a text-only account, review the Markdown table.
4. When comparing Claude models or modes, use the same sources, instructions, time budget, and answer rubric. Ask the learner to choose based on observed accuracy and effort.

**Practice.** Deliver three answered FAQ questions and one unresolved question. Show one change to the artifact or table after checking citations.

**Pass.** The output identifies the correct schedule, browser requirement and transfer policy with source IDs; refund remains unknown; the artifact, if present, works through a keyboard tab and exposes the answer text. [Claude file uploads](https://support.claude.com/en/articles/8241126-upload-files-to-claude) · [Claude Artifacts](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them)

### T03 Gemini and the Google AI ecosystem

**Outcome.** Use Gemini to draft a document from supplied notes. Compare this with a source based notebook for questions about a fixed set of documents.

**Say.** “For drafting a message I can start in Gemini. For questions about a known group of documents, I need marks that point back to the sources. I check those marks before copying the answer.”

**Show.**
1. Paste D01 into Gemini. Ask for a document titled “Workshop preparation” with Confirmed actions, Proposed actions and Decisions still open. Verify the quoted time tags and Thursday revision.
2. Put the result in a local document. If the learner has an authorized Docs integration or export option, demonstrate it on a new practice document. Keep a manual copy option for any account.
3. For the supplemental NotebookLM exercise, add only the three current D02 text files to a fresh notebook. Ask “Can I move my session?” and “Can I get a refund?” Open the citation or source excerpt for any factual answer.
4. Ask what changes if both the old schedule and the current one are present. Identify them with document names and show how version control or source selection prevents a stale answer.

**Practice.** Prepare the meeting document and one verified answer from the notebook. If no notebook is available, mimic the retrieval by pasting only the relevant FAQ and record which excerpt you used.

**Pass.** Two actions have assigned owners, Priya remains proposed, and the second class is undecided. The transfer answer retains the deadline and availability limits, and the refund answer abstains. [Gemini Help](https://support.google.com/gemini/?hl=en) · [NotebookLM Help](https://support.google.com/notebooklm/?hl=en)

### T04 Wispr Flow and dictation

**Outcome.** Turn spoken input into accurate, edited work text and identify where speech recognition or rewriting changed meaning.

**Say.** “I use dictation to capture an idea while it is fresh. I compare names, numbers, and changes of mind with the transcript. When I switch from notes to a formal message, I decide what is safe to clean up.”

**Show.**
1. In a disposable draft, say “Mira, reminder Wednesday at five. Correction, Thursday at noon IST. Dev owns formula checks. His deadline is still open.” Use Wispr Flow if available, or type the spoken text.
2. Keep the raw transcript and make a second version for the team. Use a table with owner, task, due text and open question. Have the learner read both copies before any polishing.
3. Say “Priya might own the slides.” Compare “might own” with “will own.” Mark an accidental strengthening as a factual error.
4. Repeat with one ambiguous name or an acronym. Spell it out, or use the app's vocabulary settings if offered. Correct the transcript before sending it to any other tool.

**Practice.** Dictate a 30 second task update, include one deliberate correction, and produce a 60 word handoff note. Mark any unresolved owner or date.

**Pass.** The revised due time is Thursday 12:00 IST, Dev's deadline stays open, and Priya remains proposed. The learner identifies one correction from spoken input to final copy. [Wispr Flow](https://wisprflow.ai/)

### T05 Generating video with Higgsfield

**Outcome.** Storyboard a short educational video and use controlled revisions to improve shot continuity.

**Say.** “I create a shot list before I generate anything. Each shot has a subject, one movement, a purpose, and a length. I ask for generated motion and compose precise text separately so the call to action stays legible.”

**Show.**
1. Use D06 to sketch three shots at five seconds each: overhead desk and fictional worksheet, close screen view showing a filter or formula, and a simple final title card.
2. Write a shot prompt for the first frame: “Overhead view of a dark blue desk, open laptop with a fictional spreadsheet, soft daylight from left, slow push in, subject centered, 16:9.” Use the same desk, light direction and framing references for subsequent shots.
3. Generate a sample in a suitable video tool if available. Make one revision that changes only camera speed, then compare hand or object distortions, framing and continuity. If access is unavailable, compare two storyboards with different camera directions.
4. Add the title and captions after generation. Spell the brand and call to action verbatim. Keep the worksheet legible using a screenshot of synthetic data or an editor overlay.

**Practice.** Submit a shot table with durations, prompts, transitions, rights to source assets and the final call to action. Show what one revision fixed.

**Pass.** The shot durations add to 15 seconds, the viewer can read the call to action, and no shot contradicts the brief or introduces an unverified claim. [Higgsfield](https://higgsfield.ai/)

### T06 Using the Grok assistant

**Outcome.** Use Grok for initial exploration and validate a topical claim against a primary source.

**Say.** “I can use a chat assistant to find leads. I separate a claim from the source that supports it. A popular post can reveal a question to investigate. The original documentation or announcement is the stronger basis for asserting a fact.”

**Show.**
1. Ask Grok for what an organization has announced about one tool, limited to a one week time range you supply. Request title, organization, date, direct URL, and what the link actually establishes. Use a small topic such as one official release from your work area.
2. Open the first cited page and locate the exact claim. Record both the publication date and the date of any rollout mentioned. Verify that the result applies to the stated audience.
3. Repeat the process on the synthetic D07 cards. Show how a newer official spec changes the answer compared with an older flyer. If the tool is unavailable, give the class a candidate answer and ask them to audit it manually.
4. Rewrite the result as “confirmed,” “reported by source,” or “unverified,” based on what you can see. Keep speculative citations out of the factual summary.

**Practice.** Build a three row claim ledger and correct one mistaken or weakly sourced claim.

**Pass.** Every confirmed claim has a direct supporting source. The synthetic class cap is 12 and certificate availability remains unresolved. [Grok on X](https://help.x.com/en/using-x/about-grok)

### T07 HeyGen avatars and ElevenLabs audio

**Outcome.** Plan a talking presenter video and a natural voiceover from the same original script.

**Say.** “I write the script in short beats and listen before I place it over a video. The visual tool handles the presenter. The audio tool handles pronunciation, pace and phrasing. Captions give me a third place to check what the viewer receives.”

**Show.**
1. Draft this D06 script: “Practise filters and formulas in one live hour. Follow along in your browser. View the sample schedule.” Read it at a natural pace and time it before generating audio.
2. In an available text to speech tool such as ElevenLabs, use a stock or authorized voice. Preview one line, check pauses, and record expected pronunciation for the fictional brand. Change only pace or wording on the second pass.
3. In HeyGen, choose an available authorized presenter or use a storyboard. Align the audio or corresponding script to the caption timings. Inspect the first and last frames for a cut word or caption.
4. Export a draft if available. Save the script and caption track together with the audio or storyboard so another instructor can review the same wording.

**Practice.** Produce a 15 second sample or a time coded mock with a finished transcript. Note the voice and media source.

**Pass.** Audio or read-aloud timing fits the requested length, captions reflect the spoken wording, and the claims and CTA match D06. [HeyGen Help](https://help.heygen.com/en/) · [ElevenLabs text to speech](https://elevenlabs.io/docs/overview/capabilities/text-to-speech)

### T08 Meta Muse

**Outcome.** Give a general assistant a research and planning task with an explicit point at which it should return control.

**Say.** “Muse is Meta's assistant. Muse Spark is a model family that powers it. I write down what evidence an assistant can use, what it can prepare, and what still needs a person to act.”

**Show.**
1. Open the currently available Muse interface or demonstrate with another chat assistant. Paste the current D02 schedule and request a checklist for preparing a learner for that session.
2. Require a verified time and setup, a list of facts still needed, and text for a draft reminder. Ask it to leave the recipient blank and say when a booking or reminder would need confirmation.
3. Ask it to add a second session. Check that it identifies the missing schedule information. Give it the archived schedule and check that it describes the date as historic.
4. Review what was based on your text, what was inferred, and any claimed external action. Treat an app's claimed operation as pending until the relevant tool reports its outcome.

**Practice.** Write a constrained plan for a two step workshop reminder from the D02 records, with the exact point where a person makes the next decision.

**Pass.** The sample reminder uses Tuesday 18:30 IST and optional desktop Excel, while the recipient and permission remain open. [Meta Muse](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/) · [Muse Spark](https://ai.meta.com/blog/introducing-model-meta-superintelligence-labs)

### T09 Apple Intelligence

**Outcome.** Use a supported device feature to edit a text draft and confirm that the edit preserves meaning.

**Say.** “I start with the part of the text that needs attention. A rewrite can improve readability and accidentally change an owner, deadline, or promise. I keep the original visible until I confirm those details.”

**Show.**
1. Check Apple's current device, operating system, language and region information. If Writing Tools is available, select a sample paragraph in a supported app. Otherwise use a text assistant for the same exercise.
2. Use the D01 facts to compose an informal three sentence update with the phrase “Priya may be able to handle the slide deck.” Ask for a concise, professional rewrite.
3. Compare original and revised drafts word for word on owner, due time and level of commitment. Fix any changes to Dev's deadline, Priya's status or the second class.
4. Demonstrate a second pass with an explicit audience, such as the workshop team. Save the revision as a draft for inspection.

**Practice.** Submit before and after copies and highlight three unchanged facts. Explain when you would use a small edit over a broad rewrite.

**Pass.** Mira's revised timing, Dev's unspecified due date and Priya's provisional ownership survive the edit. [Apple Intelligence setup and compatibility](https://support.apple.com/en-us/121115)

### T10 Conversational voice with ChatGPT

**Outcome.** Carry out a short spoken interaction in which the assistant handles clarification and returns a reviewable record.

**Say.** “Voice gives me a way to speak and hear the answer. I still ask for a readback of names, dates and uncertain details. For a voice workflow with calls, tools or booking, I add explicit state and permissions.”

**Show.**
1. Ask the voice interface to act as a mock front desk for Harbor Skills Studio. Give it D02, or describe the rules by voice. Set the two intents to schedule and required software.
2. Say “Can I attend it Tuesday?” Ask it what “it” refers to if the conversation is unclear. Give the class name, then say “Wait, did you say 6:30 in India time?” Ask it to state 18:30 IST.
3. Ask whether Excel is required and whether refunds are possible. Record the expected optional answer for Excel and unknown answer for refunds.
4. Compare the returned text or your own notes with the spoken exchange. If microphone access is unavailable, role-play the dialogue in chat. A multi-turn call workflow is a separate build in N10 and P07.

**Practice.** Submit a four turn transcript with one correction and one unsupported request. State the final confirmed details.

**Pass.** The assistant handles the correction, gives Tuesday 18:30 IST as the sample cohort time, and leaves refund policy unresolved. [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice)

---

## Everyday work with AI

By the end, the learner can turn raw notes into verified deliverables, package a repeatable skill, and decide when a task needs their attention. [Practice kit](#practice-kit)

### W01 Prompt design with context and constraints

**Outcome.** Revise a vague instruction into a prompt with a clear output, evidence requirements, and an evaluation case.

**Say.** “A strong prompt tells the model what to return, who will use it, what information it may use, and how to handle missing details. I spell out the exceptions that would cause trouble at work.”

**Show.**
1. Paste D01 with this instruction: “Summarize the meeting.” Save the result as a baseline. Highlight any flattened distinction between an assigned action and a proposal.
2. Use the D08 extractor prompt. Read the output schema first, then point to each deadline and owner in the source. Explain why a revised deadline needs both the task assignment and the new due time as evidence.
3. Add one example. “If the note says ‘Dev will check the formulas and leave the due date open,’ return an assigned task with owner Dev and due_text null.” Compare different outputs using the same rubric.
4. Change the audience to a manager. Keep the same facts and reshape the output into three short bullets plus an open question. Justify any fact you remove or preserve.

**Practice.** Submit the before and after prompts and evaluate both on owner, latest deadline, proposed work, decision and citation accuracy. Add a note to D01 in which Priya declines and rerun the prompt.

**Pass.** The learner can point to at least one requirement that made an output verifiable. Thursday replaces Wednesday; Dev stays undated; in the modified input an explicit decline prevents assignment to Priya.

### W02 AI research with verified sources

**Outcome.** Produce a brief with a traceable claim ledger and a clear answer when sources conflict or are insufficient.

**Say.** “I use AI to surface candidate facts and search terms. I open the original sources, check dates and scope, and keep a short ledger of what each one supports. That record makes the draft reviewable.”

**Show.**
1. Frame a question precisely: “What is the class size cap for the current live class, and does it offer participation certificates?” Record the date and scope of the research.
2. Ask for a table with claim, original source ID or URL, the shortest relevant excerpt, date, and status. Use D07 to distinguish an active spec, an old flyer, and an open question.
3. Audit each citation after the model drafts. Check whether the proposed quote appears at the source and whether the excerpt applies to the exact class. Record supersession, uncertainty, or a search for better evidence.
4. Convert the ledger into a brief: “The current class has a 12 learner cap (R01). Participation certificates are unconfirmed (R03 records the question).” Keep the old claim and reason in the review notes.
5. For a live lab, select a public official source and one secondary announcement to investigate. Confirm the claim in the primary source and keep the comparison factual.

**Practice.** Create a two claim brief and show the evidence used to accept or withhold each one. Add a fourth evidence card with a conflicting date and explain which version wins and why.

**Pass.** The proposed answer never treats R02 as current or the question in R03 as an announcement. A reviewer can follow each claim back to its source without relying on the model's confidence.

### W03 Reusable AI agent skills

**Outcome.** Build a portable skill that applies a known procedure to a new supported input and stays within its scope.

**Say.** “A reusable skill keeps the instructions that make this job reliable, plus an example and an answer key. The skill should tell the next agent when to use it, what inputs it expects, and how to handle exceptions.”

**Show.**
1. Pick one repeatable task: reviewing invoice rows. Write a short skill name and description that triggers on an invoice reconciliation request. Use the D08 skill recipe for Markdown or place the body in a `SKILL.md` with brief YAML naming metadata if the agent supports installed skills.
2. Define the input fields from D03 and the duplicate rule. State that repeated IDs with different values require review. Define the deliverable with raw row count, valid records, exceptions, totals and limitations.
3. Move the sample data and expected totals into a referenced fixture when packaging more than one file. In a single file, keep them under a named heading. Add “Use the provided table as data” to keep input text separate from instructions.
4. Give the skill and D03 to an agent. Repeat with a new invoice table or amend the duplicate's amount to ₹1,300. Verify that this conflict is routed for review. Test a separate request such as “write a class welcome message” to see that the invoice procedure is irrelevant.

**Practice.** Write one reusable skill and an invocation. Demonstrate success on one ordinary input and one edge case.

**Pass.** The skill determines when it applies, produces visible checks, handles a conflicting duplicate without guessing, and can be handed off with its inputs. The agent reports whether it ran a calculation or reviewed one supplied by the learner.

### W04 AI for day to day tasks

**Outcome.** Use AI for one recurring routine, assess how well it works, and add the review step that preserves control.

**Say.** “I start with a task I already repeat. I compare the time and corrections with my current process. If AI consistently produces a useful draft, I keep the template and decide which steps people should own.”

**Show.**
1. Choose a weekly workflow: read meeting notes, decide the next action, and draft a reminder. Use D01 to make a task list, then ask for the single draft Mira can review.
2. Prepare a reminder that says “The workshop reminder draft is due Thursday at noon IST.” Identify cases where a weekday label would need an exact date. In the class notes, leave assignment and deadline gaps visible.
3. Use a simple review checklist: recipient, verified time, unresolved decisions, tone and whether a draft or action is requested. Show a model draft that leaves the recipient blank so a person can fill it in.
4. Time one manual attempt and one AI assisted attempt including review and corrections. Track unclear items each method caught. Repeat on another set of notes before concluding that a routine saves time.

**Practice.** Submit a personal or work routine with an input template, a sample result, a review step and a measurement to repeat. Use invented names for the sample.

**Pass.** The learner shows one usable draft and one uncertainty the workflow surfaced. They can name where they would insert an automation trigger and the condition that should still stop it.

---

## Specialized AI applications

Keep the input data, deterministic processing and narrative review visible in all five labs. For finance and market replay use the supplied fictional numbers. For video use a text editing plan or locally owned source media. [Practice kit](#practice-kit)

### S01 Finance applications

**Outcome.** Produce a finance variance table and reviewer memo based on checked calculations.

**Say.** “I keep the calculation in a spreadsheet or code where I can reproduce it. I give AI the checked results to organize and explain. If the table doesn't explain a variance, I turn it into a question for the owner.”

**Show.**
1. Open D04. Calculate actual less budget in a separate column. Formula logic for a percentage is `IF(budget>0,(actual-budget)/budget,"n/a")`. Label currency, sign convention and rounding.
2. Sum actual and budget separately, then calculate total variance and total percentage from those sums. Show why averaging the three row percentages is inappropriate.
3. Ask AI for three lines a manager can act on: overall variance, the largest positive cost variance, and one question for the owner. Supply the checked table. Reject unexplained causes such as “software overspend was due to renewals” when the data has no such field.
4. Cross-check the total by adding the three line variances. Add a second page for the zero budget exception. Discuss how to distinguish invoice amount, cash receipt and reported revenue using D03 as a separate exercise.

**Practice.** Deliver the variance table and a 100 word brief. Include at least one question that would need evidence beyond the table.

**Pass.** Actual ₹30,500, budget ₹28,000, variance +₹2,500 or +8.9%. Software leads the positive variances. Venue percentage is undefined and no unsupported cause is stated.

### S02 Using Claude to assist with video editing

**Outcome.** Turn raw footage notes into an edit decision list, timed captions and a review plan.

**Say.** “I give the assistant the transcript and source timecodes. It proposes which ranges to cut. I apply those cuts in the editor, and then check that the pacing and captions work against the final timeline.”

**Show.**
1. Provide the D06 transcript ranges and goal. Ask Claude to return start_in, end_in, start_out, end_out, reason and caption for each selected shot. Give a 15 second total and require the raw start/end times from the source.
2. Verify that each suggested range exists, remove the repeated line and long pause, then recompute the output start and end times. Ask for a short caption for the screen demo that does not claim to show a more advanced feature.
3. In a local editor, cut locally owned footage to the expected ranges or use three placeholder clips. An optional FFmpeg trimming demo for the first range is below. Confirm that the local build supports the chosen codecs.
4. Play through the draft with sound and then muted. Verify word boundaries, caption legibility, continuity and the end card. Make one corrective edit and record what changed.

~~~bash
ffmpeg -ss 00:00:04 -i source.mp4 -t 5 -c:v libx264 -c:a aac clip01.mp4
~~~

**Practice.** Hand in the edit list, a caption timing table, and a rendered draft if you have the media. Otherwise submit a storyboard with the same checks.

**Pass.** The three desired 5 second ranges make a 15 second teaser. Captions and CTA are on the correct output timeline. [FFmpeg manual](https://ffmpeg.org/ffmpeg.html)

### S03 AI in trading, using a paper replay

**Outcome.** Turn a rule into a reproducible historical replay and detect a common timing error.

**Say.** “I ask AI to explain or help code a rule. I check the result by hand on fake prices first. At each step I only use information available at that point in the replay. Fees and trade timing belong in the calculation.”

**Show.**
1. Read D05 in order. Use the two consecutive increases rule to mark a signal at the end of session 3. Write open and close in separate columns and label when each value becomes known.
2. Move the entry fill to session 4's open. Apply the exit signal at session 4's close, then fill at session 5's open. Track state flat, pending entry, holding or pending exit.
3. Calculate gross and net result with the input commission. Add a what-if with ₹0.50 unfavorable slippage per fill. With one unit and the same fee, net is then −₹5.00.
4. Give a model the rule and request pseudocode plus one test case. Compare the output to the manual trace. Point out how using later prices would create look ahead bias. Discuss what a multi-instrument comparison would need, such as missing data and a suitable baseline.

**Practice.** Submit an event log and a brief explanation of one limit of the exercise. Check what happens if the last available session is session 4.

**Pass.** Base entry ₹103 and exit ₹101, gross −₹2, fee ₹2, net −₹4. With data ending at session 4, the exit is pending since the next open is unavailable. Treat this as a simulation demonstration.

### S04 AI assisted data analysis

**Outcome.** Use an assistant to inspect a CSV, explain cleaning decisions and reconcile the result independently.

**Say.** “Before charting I ask what one row represents and how the numbers are measured. I keep a list of which rows were kept, excluded, or sent for review.”

**Show.**
1. Open D03. Check the column names and data types. Define the grain as one invoice, use integer rupees, and keep the source row numbers for traceability.
2. In a spreadsheet or code, separate missing amounts and later exact duplicates. Check that equal invoice IDs with conflicting fields get their own exception rather than disappearing into the duplicate filter.
3. Aggregate surviving amounts by paid and unpaid. Ask the AI for a bar chart specification with these groups and underlying IDs. Describe the conclusion in plain language and name the scope of the input.
4. Recompute one aggregate manually. Check that the two groups add to the total, and that counts of kept and excluded rows sum to six.

**Practice.** Submit tidy input, an exception ledger, the totals, and two sentences about what can and cannot be inferred. Add a seventh invoice with a blank status and define a separate review category.

**Pass.** The original totals tie to D03 and the duplicate and missing amount are distinct. The learner does not infer the date of cash receipts. The added fixture shows an explicitly unresolved status.

### S05 Running AI models locally

**Outcome.** Run an appropriate local model or plan a local run, then measure whether it can answer a specific task within your machine's limits.

**Say.** “A local runtime loads model weights on your device. Model size and quantization affect resource use, and the amount of input also matters. I check the license and compare results on the same task before choosing a model.”

**Show.**
1. Record OS, available memory and disk space. Choose a supported runtime such as Ollama and read the guide for setup. Select a small model your machine can run. Check the model card for language coverage and licensing and record the tag. 
2. After setup, use `ollama list` to see installed models. Run `ollama run your-model-tag`, with your actual tag substituted, or use the runtime's graphical interface. Record whether the model was downloaded before the run.
3. Give the model the same D02 text and three questions for schedule, transfer and refunds. Save the prompt, model tag, elapsed time, sources named and supported answers. Review local app features that may reach a network, such as a separate search tool, if offline execution matters.
4. Compare with a different local model or a hosted answer only when appropriate for the data. If local execution is unavailable, give a machine requirements and model selection plan and grade candidate answers with the fixture.

**Practice.** Write a short run record with hardware, model tag, source handling and a three question result. If you run out of memory, shorten context or select a smaller model and explain the tradeoff.

**Pass.** The result correctly uses current sources and abstains on refunds, or documents the observed error with a reproducible prompt. Keep measurements distinct from estimates. [Ollama quickstart](https://docs.ollama.com/quickstart)

---

## n8n and APIs

An API is an interface programs use to request data or an action. n8n links triggers, transformations and API calls into workflows. Start with a manual run and inspect every node's inputs and results before changing when it runs. The [project blueprints](#n8n-project-blueprints) contain nine complete lab specifications and copyable inputs. [Provider references](#provider-references)

### N01 API fundamentals

**Outcome.** Read a simple API contract, issue a request in a sandbox, and explain what success and failure look like.

**Say.** “The API tells me how to address a resource, what to send and what comes back. I start with a documented request. I check the status code and the response body before mapping anything downstream.”

**Show.**
1. Identify URL and path, HTTP method, headers, query parameters, request body, and response fields. Compare a GET that reads an approved resource with a POST that submits data. Explain that a POST's effects depend on the endpoint contract.
2. For a no-credential practice request, save the weather object from P02 as `weather.json` in a scratch directory. Serve that directory locally as shown below, then inspect the response. Read location, time, temperature, probability and units.
3. Change the local path to an absent file and inspect the 404 result. In a production integration, distinguish malformed input (e.g. 400), auth failure (401/403), missing resource (404), rate limit (429), and server failure (5xx). Read provider instructions on retries and pagination.
4. Show where an n8n credential would be selected for a real API. Copy only required fields. Compare the schema returned by your provider with the mock's fields before replacing the mock. If n8n runs in a container or the cloud, use an approved reachable fixture endpoint or load a local fixture inside n8n.

~~~bash
# Run this in a scratch directory containing only the practice fixture.
python3 -m http.server 8787 --bind 127.0.0.1

# From a second terminal.
curl -i http://127.0.0.1:8787/weather.json
~~~

**Practice.** Draw the request and response contract, including one bad response and the workflow's fallback.

**Pass.** The learner can locate the specified fields and distinguishes retryable read errors from input and permission errors. [n8n HTTP Request node](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.httprequest/)

### N02 n8n setup and data flow

**Outcome.** Build a manual n8n workflow that maps a field, directs two inputs to the correct branches, and shows its execution history.

**Say.** “A trigger starts the workflow. Nodes process items. I inspect what came out of each node before expecting a downstream field to exist. Fixed fields use a value. Expressions read a value from the current execution.”

**Show.**
1. Open a practice n8n instance. Choose hosted or local setup based on what is available. Add Manual Trigger and Edit Fields. Create an item with invoice_id set to INV-101 and amount_inr set to 1200 as a number.
2. Add an If node that checks for a positive numeric amount. Map `{{$json.invoice_id}}` and a fixed result of `valid_demo` on the true branch. Set `needs_review` on the false branch. Inspect the JSON output, which n8n passes between nodes as items.
3. Change amount_inr to null or remove it and rerun. Show why a missing value needs an explicit review route. Inspect the last execution and mark which node made the decision.
4. Export or capture the node design with synthetic data. When sharing an export, inspect it for credential labels, endpoints and pinned data. A text walk-through of the same item sequence works if n8n is unavailable.

**Practice.** Build the three logical steps and submit the successful and review outputs. Add a third run with the amount stored as text and explain your chosen coercion or rejection rule.

**Pass.** The numeric fixture goes to valid_demo and the missing one goes to needs_review. The learner can show where the JSON field was read. [n8n Academy](https://learn.n8n.io/) · [n8n data structure](https://docs.n8n.io/build/work-with-data/understand-n8ns-data-structure)

### N03 First workflow with Instagram Reel data

**Outcome.** Collect and summarize metadata for Reels using inputs the learner can use, and handle an unusable engagement denominator.

**Say.** “I start with records from my own or authorized content, use a known format and compute the ratio before asking for a narrative. Changing the source later only changes the import step.”

**Show.**
1. Open P01. Copy the synthetic fixture into Edit Fields as an array. Split Out so that each Reel becomes one n8n item.
2. Map ID, caption, views, likes and comments to a single schema. Deduplicate by ID. Send absent, negative or nonnumeric counts to a review branch.
3. Calculate (likes + comments) divided by views for positive views. Return null with a reason when views are zero. Sort by the computed ratio and inspect the result.
4. Optionally replace the fixture with the learner's own export or an authorized API input. Check the official portal for supported metrics and permissions. Compare views and reach using their source definitions.

**Practice.** Produce a three record engagement report and a short insight about one Reel. Replay the first ID and add a zero view result.

**Pass.** P01 produces 6% and 4% for the two valid examples and an explicit unavailable score for zero views. The replay cannot inflate counts. [P01 practice build](#p01-reel-metadata-report) · [Instagram Platform documentation](https://developers.facebook.com/docs/instagram-platform/)

### N04 A first n8n tool calling agent

**Outcome.** Connect a chat model to two narrow tools and prove it picks a suitable tool for the request.

**Say.** “A normal workflow can use a fixed rule. An agent can select a tool by matching the user's intent to its description. I start with two read operations so I can see which tool it selects and why.”

**Show.**
1. Create two read only callable subworkflows with mock results from D02. Give them descriptive names such as lookup_schedule and lookup_transfer. The first returns the current workshop schedule and source ID. The second returns the transfer rule and source ID.
2. Add an AI Agent node, a configured chat model and the two tools, such as nodes that call named n8n subworkflows. Give the agent a short system instruction to answer only with retrieved facts, keep the course name fixed, and say when no tool covers the request. Limit the tool calls for this small task.
3. Ask “Can I switch my seat?” Inspect execution details. Verify the tool received a valid course input and that its answer preserves the transfer deadline and availability condition.
4. Try “When is it?” with workshop context, then ask “What is the refund policy?” The latter should give the unknown response. Using a stub, simulate the expected tool selection and response envelope when no model is available.

**Practice.** Submit a trace for each of the two supported intents and an unsupported request, with the tool name, inputs, returned evidence and final answer.

**Pass.** Each supported question selects the appropriate read operation. The unsupported refund question receives no invented policy or hidden action. [n8n AI Agent node](https://docs.n8n.io/integrations/builtin/cluster-nodes/root-nodes/n8n-nodes-langchain.agent/)

### N05 Weather and technology news

**Outcome.** Combine two information sources in one digest while labeling a stale or failed source.

**Say.** “Weather and news are two inputs to one report. I normalize each separately. If one source fails, the reader should still know what was available and where the missing part went.”

**Show.**
1. Open P02. Use a Manual Trigger and load the weather and news fixtures. Preserve fetch time, source name and link.
2. Map location, forecast time, temperature and precipitation chance. Deduplicate news with stable IDs or canonical URLs. Use explicit run time and source timestamps to filter for freshness.
3. Build a digest with date, forecast, two unique headlines and links. Include source_status for each branch. If you add a model, use it for shorter wording after building the data report.
4. Simulate a failed weather request and show how headlines still appear. If transitioning to a real schedule, choose and confirm the workflow time zone and review the output first.

**Practice.** Run a normal case and one weather error. Show the result and explain the difference between a successful source returning no data and a source error.

**Pass.** Pune shows 28 °C and 40% chance of precipitation at the fixture time, duplicate headlines collapse, and a missing forecast is identified as unavailable. [P02 practice build](#p02-weather-and-technology-digest)

### N06 Email assistant

**Outcome.** Classify sample messages and create grounded drafts without duplicate processing.

**Say.** “I use one stable message ID and decide what to return for each type. Schedule or setup questions can have an evidence based reply. Unknown policies become a draft for review.”

**Show.**
1. Load P03's mock messages and map message_id, subject and body. Use a stable processed record keyed by message_id. Record each route.
2. Ask a model or written rules to classify as schedule, setup, billing or other. Validate the exact enum. Add a route for cases that cannot be classified confidently from the content.
3. Use the current D02 sources to compose a draft for supported questions and a human review summary for missing policy evidence.
4. Store the draft in the demo output, including its source IDs and approval status. Replay E-101 and validate that only one draft exists for it.

**Practice.** Produce outputs for E-101 through E-104, then replay E-101. Include a routing note for each.

**Pass.** E-101 and E-102 use the schedule source, E-103 requests review, and E-104 gets no response draft. Replay is visible as duplicate or already processed. [P03 practice build](#p03-email-assistant)

### N07 Job search workflow

**Outcome.** Filter and score roles against a supplied skills profile while explaining why a role was selected or flagged.

**Say.** “I start with explicit preferences and a list of actual skills. I can normalize 'Excel' and 'Microsoft Excel', but I keep missing skills visible. The output is a shortlist a person can review.”

**Show.**
1. Load P04's sample profile and listings. Assign a stable ID to each employer and requisition. Deduplicate copied listings.
2. Normalize agreed skill aliases and work arrangements. Score required skill matches as matches divided by stated required skills. Use unknown when the listing does not state the requirements.
3. Filter duplicates and mismatched locations. Retain the evidence and list missing requirements beside each score. Have a model draft a concise comparison if needed.
4. Add a saved role summary and a plain honesty check for any optional resume draft. Treat absent pay or other fields as unknown.

**Practice.** Produce a shortlist plus a review list. Show how J-102 would change if the learner later supplies evidence for Python.

**Pass.** J-101 passes, J-102 needs review because Python is missing, and the duplicate creates no second listing. [P04 practice build](#p04-job-shortlist)

### N08 Telegram bot with n8n

**Outcome.** Create a bot workflow that recognizes an allowed command and handles unknown messages and duplicates.

**Say.** “Telegram sends an event with a chat ID and update ID. I check that the chat is in scope before I route the command. I can learn everything about the workflow with a test event before I connect a bot.”

**Show.**
1. Start with P05's manual fixtures. Normalize the message text and IDs, then check the allowed chat and route /help and /schedule.
2. Build the reply data as JSON. Use only the current D02 source for the schedule text.
3. Deduplicate updates by update_id, separate from the chat ID. Test an unknown command, an unauthorized chat and a missing text field.
4. If connecting an authorized practice bot, use its bot token in credentials and the approved webhook setup. Test and production webhooks for one bot can displace each other. Use a separate test bot or enable one listener at a time.

**Practice.** Capture the output of four mock events and one replay. If working with a live bot, identify the test chat and how to disable the trigger.

**Pass.** Only the allowed chat gets a hypothetical response, /schedule shows Tuesday 18:30 IST, and duplicate events do not create a second reply. [P05 practice build](#p05-telegram-faq-bot) · [Telegram Bot API](https://core.telegram.org/bots/api)

### N09 Document retrieval agent with n8n

**Outcome.** Build a question answering workflow with inspectable retrieval, citations and an unknown result.

**Say.** “I ingest the documents once, including version and source IDs. At question time I fetch only relevant active passages. I check what came back even if the model's answer sounds good.”

**Show.**
1. Create a document ingestion step that saves the three current D02 records and handles the archive as a different version. For the small lab, a fixed table of passages works. Use embeddings and a vector store when required by the project and available.
2. Create a separate query workflow. Retrieve by enabled synonym search or an approved retrieval component. Return passage IDs and version. Filter archived sources.
3. Pass the passages into the answer step. Ask for JSON with status, answer and source_ids. Validate that all IDs belong to the actual retrieved current records, then review claims against the matching passage.
4. Ask the five D02 questions. Score citations on support and correctness and report empty or irrelevant retrieval separately.

**Practice.** Run P06 and show the query result, retrieval trace and fallback behavior for three questions. Add a new source revision and demonstrate that its current version is chosen.

**Pass.** A documented transfer gets a source and conditions, refund stays unknown, and the archived date does not appear as current. [P06 practice build](#p06-document-qa-agent) · [Retrieval in n8n](https://docs.n8n.io/build/integrate-ai/understand-ai-components/retrieve-relevant-context)

### N10 AI voice agent for sales practice

**Outcome.** Simulate a short inbound sales conversation that qualifies a caller, handles corrections and ends or hands off correctly.

**Say.** “I establish what the caller wants. I confirm important details out loud. I keep a state for the conversation, because a later correction can change a date or cancel the next action.”

**Show.**
1. Start with P07's text event simulator. Read session_id, event_id, consent flag and utterance. Keep state for consent, question handling, pending confirmation or handoff.
2. Map schedule and software questions to D02. Provide a brief reply and one clarification when needed. Use only the sample cohort. Offer a hold as a mock state and read back the time zone and action.
3. Play a caller correction, reject an unsupported time, and require an explicit confirmation before marking a mock hold recorded. Try an ambiguous reply such as “Maybe.”
4. If using a supported voice provider in an approved practice environment, connect transcription and the response voice separately from the logic. Check the actual transcript first and route repeated misunderstandings to a human.

**Practice.** Walk through a four turn practice session plus a missing consent case. Show the status trace and the mock hold record or reason for no hold.

**Pass.** No confirmation is counted for “Maybe.” The final output states the confirmed slot correctly or hands off. Replayed events leave state consistent. [P07 practice build](#p07-voice-sales-practice)

### N11 Content creation workflow

**Outcome.** Build a repeatable content draft workflow that preserves claims, voice and review status.

**Say.** “I make a source brief first. The workflow can return several creative variants. The claims have a single source and a person still checks what the public would see.”

**Show.**
1. Load D06 and P08. Map brand, audience, permitted claims and single call to action. Give each brief a stable ID. Decide the output fields before calling a model.
2. Draft three ideas and select one based on audience fit. Ask the model for a 15 second script and short caption. Include source references for factual claims.
3. Route through a deterministic check for empty fields, exact CTA and maximum length. Flag any claim that needs evidence. Save as a draft or review_needed.
4. Review manually for implied promises, such as employment outcomes. Revise an invalid draft and document which check catches it.

**Practice.** Generate a draft and run a deliberately weak candidate through the review route. Submit both and their check outcomes.

**Pass.** The accepted draft uses the supported workshop facts and exact CTA. The unsupported guarantee goes to review without publication. [P08 practice build](#p08-content-draft-pipeline)

### N12 AI portfolio monitor

**Outcome.** Calculate a simulated valuation and produce a review alert on a defined threshold.

**Say.** “I use code or formulas for the values, check timestamps and explain which prices are missing. I can use AI to summarize the calculated results in plain language.”

**Show.**
1. Import P09's fictitious holdings plus baseline and current prices. Join on the symbol. Validate quantity, price, currency and timestamps before aggregating totals.
2. Compute position value and change. Record one alert when the absolute per-symbol move reaches the threshold. Keep the portfolio total distinct from per-position changes.
3. Create a text digest of values, alert IDs and missing sources. Prevent replay of the same alert with the fixture's stable key. Try a stale or missing price and record an incomplete total.
4. Ask a model to summarize the exception and one observed move from the computed fields. Review whether the wording claims more than the known price changes.

**Practice.** Show the normal run, a missing quote case and one exact replay. Keep the thresholds and time basis visible.

**Pass.** Baseline ₹2,000, current ₹2,030 and +1.5% overall. DEMO_A gets one +4% demo alert. A missing quote prevents a complete valuation. [P09 practice build](#p09-portfolio-monitor)

### N13 Building n8n workflows with Claude

**Outcome.** Use a coding assistant to turn a project contract into an inspectable n8n build and correct version or logic errors.

**Say.** “I give Claude the fixture and expected outcomes first. A workflow must use the nodes my instance actually has. I review mappings and run it manually before its trigger is allowed to run.”

**Show.**
1. Give Claude the n8n version or an available sanitized target workflow export, P03's input and expected cases. Ask for a plan with node purpose, input mappings, output shape, branches and failure routing. Include whether expressions or a Code node are allowed.
2. Check each node name and configuration against the vendor docs and actual instance. Request a draft export only if Claude has enough version detail to supply one. Copy the config into an isolated draft with no live triggers.
3. Run the normal and invalid cases, inspect nodes, and adjust one mapping or condition at a time. Record how the idempotency rule prevents a repeated draft.
4. Ask for a handoff with workflow file or node settings, required environment variables by name, test inputs, observed results and the steps a learner can repeat. Remove pinned data outside the practice set.

**Practice.** Implement or design one P01–P09 blueprint using this procedure. Save the first prompt and one correction that improved the result.

**Pass.** The build or plan matches the selected project contract and states which checks were actually run. The n8n version and dependencies are stated. A learner can reproduce the ordinary and exception routes. [Claude Code documentation](https://code.claude.com/docs/en/overview)

---

## n8n project blueprints

These are original builds for the topics listed in N03 and N05–N12. N04 is a shorter introductory exercise in the [n8n lesson module](#n8n-and-apis). Use the named project when asking an agent to prepare a node configuration, implement an exercise, or grade a submission.

### Common lab setup

Start with Manual Trigger. Use a fixture loader such as Edit Fields for one object or an object with an array field. Split Out turns array elements into individual items when each needs the same processing. If the desired output is a report over all items, aggregate after processing. Give node names that describe the transformation and inspect the JSON preview at each edge. Record which instance and version the learner uses. [n8n data structure](https://docs.n8n.io/build/work-with-data/understand-n8ns-data-structure) · [n8n Academy](https://learn.n8n.io/)

- **Standard output.** Use a run ID, a result status, a payload, and structured exceptions. Project fields below are the minimum. Record the triggering item and fixture for each expected result.
- **Repeatability.** Use the fixture's fixed clock and input IDs. For a workshop demo a single run can process an in-memory set of IDs. To guard replays between runs, persist keys. If multiple executions can race, use storage-level uniqueness or a single writer. A separate read followed by a write is only a sequential demo.
- **Model calls.** Start with the provided expected shape or a simple heuristic stub. If using a model, validate types, allowed enum values, and reference IDs before consuming the output. Keep arithmetic and permissions in ordinary workflow logic. Save one known failure output.
- **Integration changes.** Replace a fixture loader with a documented connector or API only if its input mapping meets the same contract. Add credential bindings in the learner's instance. Use bounded retries for appropriate transient errors and keep a visible failure route. Publishing, outbound messages and live scheduled triggers depend on the specific implementation request. [n8n error handling](https://docs.n8n.io/build/flow-logic/handle-errors-gracefully)
- **Handoff.** Provide the node sequence, field mappings, a draft export when the target version supports it, local run instructions, sample output and any pending dependencies. Use the expected results below to distinguish a workflow run from a paper simulation.

### P01 Reel metadata report

**Build.** Compute a report from synthetic or authorized Reel metadata. Input accepts id, caption, views, likes and comments. Use a number or null with an exception. Keep the media source separate from who may access it.

~~~json
[
  {"id":"R-01","caption":"Find rows with filters","views":1500,"likes":75,"comments":15},
  {"id":"R-02","caption":"Start with a formula","views":800,"likes":24,"comments":8},
  {"id":"R-03","caption":"Practice worksheet","views":0,"likes":0,"comments":0}
]
~~~

1. **Edit Fields + Split Out.** Load the array under `reels` and split on that field. Map own or authorized exports to the same schema if substituting a real source. Trim IDs and retain the originating record.
2. **Validate and deduplicate.** Require a nonempty ID and non-negative integer counts. For repeated IDs with identical content retain one. Route conflicting entries to review with their source records.
3. **Compute with Code or a numeric expression.** If views > 0, calculate `(likes + comments) / views`. For zero views, return rate null and reason `zero_views`. Keep the numeric fraction separate from its percentage label.
4. **Aggregate.** Emit report rows with ID, engagement rate, raw counts and status. Sort valid rates in descending order, then list unavailable rates with reasons. A model can summarize this result with no need for account access.

**Acceptance examples.** R-01 = 0.06 (6%), R-02 = 0.04 (4%), R-03 rate null. Append an exact copy of R-01 and confirm three output rows. Append a conflicting view count under a repeated ID and confirm it is flagged. A negative count must be routed for review. [Instagram Platform documentation](https://developers.facebook.com/docs/instagram-platform/)

### P02 Weather and technology digest

**Build.** Join two read sources into a digest with explicit freshness and partial results. Fix the practice clock at **2026-09-10T11:00:00Z**. Accept a forecast loaded within the last two hours and reject already elapsed forecast times. Accept news published in the preceding 24 hours and at or before the run time.

**Weather object.** Save this as `weather.json` for N01.

~~~json
{
  "location": "Pune",
  "forecast_at": "2026-09-10T17:30:00+05:30",
  "temperature_c": 28,
  "precipitation_chance_pct": 40,
  "fetched_at": "2026-09-10T10:55:00Z",
  "source": "synthetic weather"
}
~~~

**News array.**

~~~json
[
  {"title":"Practice lab introduces reusable workflows","url":"https://news.example/workflows","published_at":"2026-09-10T09:00:00Z"},
  {"title":"Practice lab introduces reusable workflows","url":"https://news.example/workflows?utm_source=demo","published_at":"2026-09-10T09:00:00Z"},
  {"title":"Sample editor adds caption preview","url":"https://news.example/captions","published_at":"2026-09-10T08:00:00Z"}
]
~~~

1. **Load two sources.** Use fixtures or separate HTTP Request nodes for approved sources. Get the real property's time and unit mapping from its docs before replacing the HTTP loader. Return one envelope from each loader with data and status `ok`, `empty`, `stale` or `error`. If using parallel paths, join the two envelopes by source name. Preserve a result from each path even after failure.
2. **Normalize.** For weather, parse timestamps and ensure precipitation chance is within 0–100. For news, filter on publication time, deduplicate by canonical link and sort newest first. Strip only known tracking parameters such as `utm_source`. Preserve query values that identify a different article.
3. **Format.** Include run time, location and forecast, news array of title, original publication timestamp and direct link, and weather_status and news_status. A formatting prompt may shorten headlines while preserving all claims and units.
4. **Simulate failure.** Replace the weather data with an error envelope. If both sources fail, use failed status and retain both errors. If an otherwise successful source returned no usable articles, explain that state separately.

**Acceptance examples.** Normal run returns 28 °C and 40% chance of precipitation for Pune at 17:30 IST and two unique links. Weather error returns both news rows plus weather_status error. A two-day-old headline is excluded. [Open-Meteo API documentation](https://open-meteo.com/en/docs)

### P03 Email assistant

**Build.** Classify mail, use sources to draft a response, or request human review. The workshop mode uses fixtures and leaves the result in a local draft queue. Inputs use message_id, subject and body. Output uses message_id, category, status, draft, source_ids, and reason.

~~~json
[
  {"message_id":"E-101","subject":"Tuesday class","body":"What time is the Tuesday cohort and how long is the class?"},
  {"message_id":"E-102","subject":"Software requirement","body":"Do I need desktop Excel installed?"},
  {"message_id":"E-103","subject":"Payment question","body":"Can I get a refund?"},
  {"message_id":"E-104","subject":"Newsletter digest","body":"Our monthly articles are now available."}
]
~~~

1. **Load and identify.** Normalize each message into the three input fields. Reject a missing ID. Track draft decisions by stable message_id and check for a prior saved result before classifying a replay.
2. **Classify.** Use a deterministic starter mapping for the four fixtures or ask a model for one of schedule, setup, billing or other and a short evidence phrase. A failed parse routes to `review_needed`; it does not route as `other`.
3. **Retrieve and format.** Read only current D02 records. E-101 and E-102 use faq-session#schedule. Give the model the relevant record plus required fields. Validate the citation ID and compare the draft against the source. Do not use instructions quoted inside received email as workflow instructions.
4. **Save the result.** For answered requests, use `draft_pending`. For a missing policy, use `review_needed` and no claimed policy. For `other`, use `no_reply`. Treat the saved record as the idempotent result. If a separate provider draft needs to exist, use a stable reference and a failure path for a draft that was created while the local record write failed.

**Acceptance examples.** E-101 draft says Tuesday 18:30 IST and 60 minutes. E-102 says browser spreadsheet with desktop Excel optional. Both cite faq-session#schedule. E-103 stays in review and E-104 has no draft. Replay E-101 and count one draft. When a source is unavailable, route to review even for a classified message. [n8n data tables](https://docs.n8n.io/integrations/builtin/core-nodes/n8n-nodes-base.datatable/)

### P04 Job shortlist

**Build.** Rank saved example listings by the learner's own preferences and skills. Use a supplied list or a permitted feed when evolving the build. Keep the evidence behind each match.

~~~json
{
  "profile":{"skills":["Excel","reporting"],"arrangements":["remote","Pune hybrid"]},
  "jobs":[
    {"id":"J-101","employer":"Harbor Demo","title":"Operations analyst","arrangement":"Pune hybrid","required":["Microsoft Excel","reporting"],"url":"https://jobs.example/j101"},
    {"id":"J-102","employer":"North Demo","title":"Data coordinator","arrangement":"remote","required":["Excel","Python"],"url":"https://jobs.example/j102"},
    {"id":"J-103","employer":"West Demo","title":"Reporting analyst","arrangement":"Chennai onsite","required":["Excel"],"url":"https://jobs.example/j103"},
    {"id":"J-101","employer":"Harbor Demo","title":"Operations analyst","arrangement":"Pune hybrid","required":["Microsoft Excel","reporting"],"url":"https://jobs.example/j101"}
  ]
}
~~~

1. **Split and normalize.** Keep profile data accessible to all job items. Map Microsoft Excel and Excel to the same term. Deduplicate exact repetitions using employer and requisition ID. Keep a source URL.
2. **Check preferences.** If arrangement is outside the requested scope, mark `outside_preference`. If the listing omits an arrangement or required skills, mark `review_needed`. Preserve fields missing from the source as unknown.
3. **Score.** Count unique matched requirements divided by unique stated requirements. List both matched and missing values. Classify a role with an allowed arrangement and every requirement as `shortlisted`. Any skill gap goes to `review_needed` for this lab. Sort shortlisted roles by score with a stable ID as tie breaker.
4. **Prepare the handoff.** Output ID, score, status, source, missing skills and rationale. An optional resume draft may rephrase experience the learner actually provided.

**Acceptance examples.** J-101 is shortlisted at 1.0, J-102 is reviewed at 0.5 and missing Python, and J-103 is outside the allowed arrangement. There are three unique records and no invented pay values. If Python is added to the profile, J-102 moves to the shortlist.

### P05 Telegram FAQ bot

**Build.** Route a narrow set of messages for a training bot. Use synthetic update objects during the lab. Input whitelist is chat 101. The outbound action is represented by `reply_text` in the result.

~~~json
[
  {"update_id":9001,"message":{"chat":{"id":101},"text":"/schedule"}},
  {"update_id":9002,"message":{"chat":{"id":101},"text":"/help"}},
  {"update_id":9003,"message":{"chat":{"id":101},"text":"/something"}},
  {"update_id":9004,"message":{"chat":{"id":202},"text":"/schedule"}},
  {"update_id":9005,"message":{"chat":{"id":101}}}
]
~~~

1. **Normalize.** Map update_id, nested chat.id and trimmed text; keep the actual chat ID type consistent. An absent text field is an `ignored_nontext` event. Check the allowlist before producing a reply.
2. **De-duplicate.** Track processed updates by bot identity and update ID once processing succeeds. Replay a terminal result rather than recomputing or handing off a second reply.
3. **Switch.** Route /help to a brief command list. Route /schedule to the current D02 schedule and include the source ID in the trace. For any other allowed chat text, return “Try /help or /schedule.”
4. **Respond.** Return chat_id, update_id, status and reply_text or null. If the project includes a live practice bot, route outbound responses only to the matching allowed chat. Authorize the bot separately and account for the webhook registration when switching between test and production.

**Acceptance examples.** 9001 returns Tuesday 18:30 IST and 60 minutes. 9002 shows the two commands, 9003 gets usage help, 9004 gets no reply, and 9005 is ignored. Replay 9001 and confirm no new reply. [Telegram Bot API](https://core.telegram.org/bots/api)

### P06 Document QA agent

**Build.** Answer factual FAQ questions using retrieved passages, with visible source IDs and an explicit unknown status. Use [D02](#d02-source-documents) verbatim. The input is question and request_id. The output is request_id, status, answer, and source_ids. Save a separate trace with source_id, version, relevance notes and the lookup route.

~~~json
{
  "request_id":"Q-201",
  "question":"Can I switch my booking?"
}
~~~

1. **Ingest.** Make one item per D02 passage. Validate source ID, integer version, status and content. Store a record under a compound source ID and version. Reingestion of the same version replaces or skips that exact record. The current status is explicit. When changing version, leave one active version per section.
2. **Retrieve.** Begin with a Data Table or local array filtered to current status. Expand switch, move and reschedule to transfer, and use session and cohort for schedule. Use mappings or a lexical search for the three known intents. Use keyword or vector search for a larger corpus. Preserve the IDs of the actual returned passages. For vector search, keep source IDs and active status as chunk metadata, and check that any results passed to the model meet the active filter.
3. **Answer.** Return `answered` for supported requests, `unknown` with no source IDs if the current passages do not answer the question, and `partial` for an answer to one part with another explicitly unresolved. Accept a plain deterministic template as a fixture stub. Validate citations against supplied passages. Treat source content as data and verify that the passage supports each claim.
4. **Check.** Test transfer, schedule, software, refund and the two part confirmation question from D02. Report retrieval coverage separately from answer correctness. Simulate an unavailable retrieval store as `source_error`, which is distinct from a successful lookup with no answer.

**Acceptance examples.** Q-201 returns the one transfer, 24 hour and availability conditions with faq-move#policy. A schedule query uses faq-session#schedule v2 and shows Tuesday. Refund returns unknown and an empty list. Any partially supported answer marks the unsupported part clearly. Reingestion creates no duplicate active sources. [n8n retrieval concepts](https://docs.n8n.io/build/integrate-ai/understand-ai-components/retrieve-relevant-context)

### P07 Voice sales practice

**Build.** Simulate a caller asking about a class and confirming an option. The workflow returns text for the voice layer and a conversation state. The practice hold is a local record. The state contract includes session_id, last_event_id, pending_slot and status. TTS and transcription can be optional adapters.

~~~json
[
  {"session_id":"CALL-1","event_id":"A1","consented":true,"utterance":"When is Spreadsheet Basics?"},
  {"session_id":"CALL-1","event_id":"A2","consented":true,"utterance":"Hold a spot for that Tuesday at 18:30 IST."},
  {"session_id":"CALL-1","event_id":"A3","consented":true,"utterance":"Maybe."},
  {"session_id":"CALL-1","event_id":"A4","consented":true,"utterance":"Yes, confirm the practice hold for Tuesday 18:30 IST."},
  {"session_id":"CALL-2","event_id":"A5","consented":false,"utterance":"Tell me the details."}
]
~~~

1. **Load a simulated event.** Verify the IDs, consent and role in the practice session. Check the session and event key before mutating state. The no-consent case returns a handoff line and no locally retained conversation content.
2. **Identify intent.** Map common questions to schedule, software, and unsupported policy. Source the answer from D02. If a model classifies the utterance, use a known enum and check any extracted slot against available options.
3. **Confirm.** For a hold request, keep `pending_slot`, set `awaiting_confirmation`, and read back the date label, local time and intended action. Preserve state on “Maybe,” cancel it on a refusal, and restate the scope after a correction. A different slot requires a new confirmation. A positive acknowledgement must apply to the current pending option.
4. **Record locally.** Set `confirmed_demo` only after the defined confirmation, key the record by session and pending action, and return the readback. Missing policy or repeated ambiguity returns a human handoff. If voice adapters are in scope, ensure transcription errors can be corrected before state changes.

**Acceptance examples.** A1 answers with the current sample time. A2 and A3 leave a pending hold and zero recorded holds. A4 creates one local demo record and names the correct slot. A4 replay leaves one hold. A5 takes the no-consent path. A request for Saturday does not invent a slot.

### P08 Content draft pipeline

**Build.** Turn a reviewed brief into editable content drafts. Use [D06](#d06-creative-brief-and-sample-edit-log). Output must carry brief_id, hook, script, caption, cta, claim_sources and state. The state is draft or review_needed.

~~~json
{
  "brief_id":"BR-8",
  "brand":"Harbor Skills Studio",
  "audience":"adults starting with spreadsheets",
  "format":"15-second teaser",
  "allowed_claims":["60-minute live class","covers filters and formulas","use a browser spreadsheet"],
  "cta":"View the sample schedule",
  "source_id":"D06"
}
~~~

1. **Validate brief.** Require an ID, audience, claims and CTA. Treat these as the sole source of product facts for the exercise. Save a brief revision so the approval references the correct input.
2. **Draft.** Ask for a hook, short script and caption as separate fields. Require a claim-to-source map and name the exact CTA. A text-only baseline can reuse “Practise filters and formulas in one live hour. Follow along in your browser. View the sample schedule.”
3. **Check.** Assert nonempty fields and exact CTA. For the lab, flag a script over 35 words for timing review and read the accepted version aloud. Review claim_sources against D06. A model can flag risk, while the source check determines the verdict.
4. **Save work.** Store the candidate response and check results under the brief ID and revision. Send unverified claims to review_needed. Capture the approved script and track only the local draft in this exercise.

**Acceptance examples.** The baseline script passes. “Guaranteed promotion after the class” enters review_needed even if the CTA is valid. A missing CTA or cited source unseen by the workflow also needs review. The result preserves the original source ID and exact CTA.

### P09 Portfolio monitor

**Build.** Compute values from fictional holdings and quotes. Use the previous and current snapshots in the fixture. All prices are in INR. Use an absolute return threshold of 3% per symbol. Output contains baseline_value_inr, current_value_inr, change_inr, change_pct, alerts, incomplete_symbols and review status. Store percentages as rounded display fields or unrounded numeric ratios with clearly named units.

~~~json
{
  "as_of":"2026-09-10T12:00:00Z",
  "baseline_at":"2026-09-09T12:00:00Z",
  "current_at":"2026-09-10T11:55:00Z",
  "threshold_pct":3,
  "holdings":[
    {"symbol":"DEMO_A","quantity":10},
    {"symbol":"DEMO_B","quantity":5}
  ],
  "quotes":[
    {"symbol":"DEMO_A","currency":"INR","baseline_price":100,"current_price":104},
    {"symbol":"DEMO_B","currency":"INR","baseline_price":200,"current_price":198}
  ]
}
~~~

1. **Load and validate.** Join on symbol after verifying unique symbol, matching currency, finite positive price and quantity, and a current timestamp within 24 hours before or equal to the fixed as_of. Verify that the baseline precedes the current snapshot. Missing, conflicting, or stale quotes go to incomplete_symbols.
2. **Compute values.** Multiply quantities by prices. Sum valid position values. Use complete portfolio totals only when every required holding has a valid pair of prices. Otherwise return null for the complete totals and label any displayed figure as a subtotal of valid positions.
3. **Compute change and alerts.** Per-position percentage is 100 × (current price − baseline price) / baseline price. Portfolio percentage uses complete portfolio values. Store an alert when the absolute move meets the threshold and the input is valid. Key the alert by symbol, baseline timestamp, current timestamp and threshold policy revision. Replays reuse the saved alert decision.
4. **Format.** Return values, review status and traceable alert records. If using an assistant, pass verified numeric fields and state that the note describes a fictional snapshot.

**Acceptance examples.** DEMO_A goes from ₹1,000 to ₹1,040 (+4%). DEMO_B goes from ₹1,000 to ₹990 (−1%). The portfolio reaches ₹2,030 from ₹2,000 (+₹30, +1.5%). Only DEMO_A reaches the 3% threshold. Remove DEMO_B's quote and check the overall valuation is incomplete. Replay the normal fixture and check one alert exists.

---

## Building websites with AI

Build a small original site from a brief, preview each revision, and decide how to publish and measure it. Use the same fictional workshop throughout. The [capstone](#website-and-faq-capstone) combines the web work with a read only FAQ assistant. [Practice kit](#practice-kit) · [Provider references](#provider-references)

### V01 Introduction to vibe coding

**Outcome.** Write a clear website brief and use an AI coding assistant or builder to create a local or preview version with a working interaction.

**Say.** “I use natural language to describe the job, then check what was actually built. I specify what the page has to say, the one action it supports, and how I'll know that action works.”

**Show.**
1. Use D06. Brief the agent to make a single page for Harbor Skills Studio with one visible H1, a sentence explaining what learners practise, a schedule section and “View the sample schedule” as the primary link. Supply D02 for the class timing. Ask for semantic HTML and usable layout on a narrow screen.
2. Use this implementation prompt: “Create index.html and styles.css for this brief. Keep both local. Give the schedule section id schedule and link the call to action to it. Use the supplied workshop facts. Show the files and explain how to preview them.”
3. Preview with the tool's own preview or serve the directory locally. Read the page as a learner, resize to a narrow screen, and use Tab and Enter to activate the CTA. Identify and fix one issue.
4. Ask the agent to make a small, specific revision. Check the diff or inspect the updated preview to confirm the intended effect.

~~~bash
# From the directory with index.html.
python3 -m http.server 8000 --bind 127.0.0.1
~~~

**Practice.** Submit the brief, page source or preview, and a short record of a change you made after inspecting it.

**Pass.** At a narrow width the headline and CTA are readable, the link reaches the schedule, the keyboard has a visible focus position, and the copy agrees with D02. [W3C basic accessibility checks](https://www.w3.org/WAI/test-evaluate/preliminary/)

### V02 Refining websites with Hostinger and Claude Code

**Outcome.** Use either a visual builder or an AI coding agent to improve the same preview against concrete acceptance conditions.

**Say.** “A visual builder gives me a managed edit and preview experience. A coding agent edits project files I can version and review. I compare how I would make and check the same change in each setting.”

**Show.**
1. Use the V01 brief and initial page. For a Hostinger Website Builder route, start in a draft or preview if the account supports it. Arrange the title, CTA, schedule and FAQ. Inspect the mobile layout before publishing is considered.
2. For a Claude Code route, open a scratch project or existing authorized repo. Ask the agent to read the HTML and CSS, propose the smallest change to the layout, and implement it where authorized. Ask for a description of the changed lines plus a local preview command.
3. Apply the same improvement in the available route. For example, put the CTA before the long explanation in reading order, make its focus visible, and ensure the schedule stays legible at 360 px.
4. Record the previous and new preview. Keep accepted copy and page behavior in a short brief the next agent can read. Describe the other route in steps if it is unavailable.

**Practice.** Deliver one revised version, a before and after note and five checks for layout, content and interaction.

**Pass.** The display has no horizontal overflow at 360 px, heading order is coherent, and the learner can explain where edits and publishing settings live on their chosen route. [Hostinger Website Builder](https://www.hostinger.com/website-builder) · [Claude Code documentation](https://code.claude.com/docs/en/overview)

### V03 Deploying a site with domain, hosting and DNS

**Outcome.** Deploy a preview or produce a deployment worksheet showing how domain records, TLS and the hosting service fit together.

**Say.** “Hosting serves files. DNS tells a visitor where the name should point. TLS lets the visitor connect with HTTPS. I check the host's instructions before changing DNS and keep a record of how I could undo the change.”

**Show.**
1. Identify the site entry point and build output. Use the provider preview URL or a local preview for class. Record the expected status, base path and asset paths under the chosen deployment.
2. Draw a map from the registrar and nameservers to the authoritative DNS zone, hosting target and HTTPS certificate. For a subdomain, a CNAME commonly points to a hostname. A and AAAA point to IPv4 and IPv6 addresses. Use the hosting provider's instructions for the apex and any domain verification records.
3. Write a DNS worksheet with record name, type, target, TTL, reason and rollback. Copy real record values from the verified hosting setup only when the user has authorized using that domain. For the lab use reserved placeholders and show how a reader would verify the route.
4. After an approved deployment, inspect the public endpoint, TLS, redirects, relative links and broken assets. Allow for cached DNS results. Preserve links for both the preview and final site when applicable.

**Practice.** Choose a static host or the visual builder's hosting and prepare the worksheet. Include the steps to diagnose a site loading over the preview URL while a custom domain still fails.

**Pass.** The worksheet states the correct record types, puts certificate verification after pointing the domain at the configured host, and identifies what should be restored for rollback. The learner can distinguish their observed result from a plan. [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart) · [Cloudflare DNS records](https://www.cloudflare.com/learning/dns/dns-records/)

### V04 SEO and Google Search Console

**Outcome.** Create a basic search readiness checklist and interpret what an inspection result would establish.

**Say.** “I write a page that describes what a person can do, then make it easy to find and read. Search Console can tell me what Google observed about a verified site. I keep an indexing request separate from the result of indexing.”

**Show.**
1. Write a descriptive HTML title such as “Spreadsheet Basics Live Class | Harbor Skills Studio,” a brief description grounded in D06, a visible H1 and link text that describes the action. Use one canonical URL only after confirming the intended deployment URL.
2. On a live or sample deployment, check that the page loads and its navigation uses real links. Check the canonical, sitemap and access controls for agreement. Explain that robots rules control crawler access. If exclusion is desired, choose the appropriate supported measure for the page's access and indexing goals.
3. In an authorized Search Console property, inspect the exact final URL and review the indexed result and live test. Record any blocking reason Google shows. Submit a sitemap or request indexing only when that maintenance work is in scope. For local practice use mock states “live fetchable,” “current canonical points elsewhere,” and “access restricted.”
4. Ask AI for three title and description alternatives using the supplied facts. Check the chosen wording and remove unsupported guarantees. Review links after publishing changes.

**Practice.** Give an SEO audit with one content correction and one technical check, then write a brief response to a mock “URL is not on Google” result.

**Pass.** Titles and copy describe the correct class, the URL used in the check is exact, and the learner can distinguish crawling, eligibility and observed indexing. [Google SEO starter guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) · [Search Console URL Inspection](https://support.google.com/webmasters/answer/9012289)

### V05 Website measurement with Google Analytics

**Outcome.** Define a measurable site interaction, validate the event and interpret a small report.

**Say.** “I pick a question first. For this site I want to know how often visitors choose to look at the sample schedule. A page load, a click and a registration each answer different questions.”

**Show.**
1. Plan one event called `schedule_view`. Define it precisely for this lab as a user activation of the primary schedule CTA. Include non-personal fields `page_id=workshop` and `placement=hero`. Keep the event independent of typing into a form.
2. For local practice, capture the event with a local logger. Test a page load, click and keyboard activation in separate runs. Each deliberate activation should log once. A duplicate listener or a load event should not increase the count.
3. With an authorized analytics setup, use the practice GA4 property and web stream. Install the approved tag in the chosen builder or site, respecting consent controls used on the page. Verify the debug event and its parameters with the current provider UI before looking at a normal report. Avoid sending private text or identifying fields in event parameters.
4. Interpret an example of 20 sessions and 5 distinct sessions with a schedule_view event as 25% of sessions. Show why counting all events as distinct sessions overstates engagement if some people click twice.

**Practice.** Submit an event dictionary and trace. If using a local logger, label it as local. State what the event can measure and one question that a registration event would answer.

**Pass.** The selected CTA causes one event per deliberate activation, the page load generates none, and the reported metric shows the correct denominator. [Google Analytics setup](https://support.google.com/analytics/answer/9304153)

### Website and FAQ capstone

**Brief.** Build a small public-style workshop page for Harbor Skills Studio and a locally previewed FAQ assistant with an evidence trail. Use D02 as the source of truth for answers and D06 for page copy. Use the W01 prompt pattern for constraints, P06 for question answering, and V01–V05 for design, deployment readiness and measurement.

#### Functional contract

| Area | Required behavior |
| --- | --- |
| Public page preview | Display class name, purpose, schedule and the “View the sample schedule” CTA. Date is a sample, so show only the Tuesday time and IST from D02. |
| Navigation and accessibility | Use semantic sections, readable contrast, labelled question input, visible keyboard focus and one region announcing the returned answer. The primary link works at 360 px and desktop widths. |
| FAQ | Accept a question and return status, answer and source IDs. Give an answer from the current schedule or transfer policy, or say the fixture leaves a question open. |
| Failure state | If the assistant is unavailable, show a short status message and leave the workshop schedule readable. |
| Measurement | Log `schedule_view` once per CTA activation in local practice mode. |
| Delivery | Provide a project folder or code as requested, startup steps, fixture and evidence from the acceptance cases. If the user requests hosting, provide the actual preview or deployment handoff once authorized. |

#### Build order

1. Create the visual path first using the files produced in V01. Put the schedule and the software requirement on the page as normal text so they remain visible while the FAQ component loads.
2. Add a question field and an output region. Define the response schema with request_id, status, answer and source_ids. Show the answer and source IDs as text. Ensure a source ID remains recognizable and test keyboard operation.
3. For the default local route, create a fixture adapter over D02 and map known questions deterministically. Return unknown for gaps in the fixture. To build the n8n route, connect the frontend to a dedicated read only question endpoint implementing P06. Keep credentials server side and choose either an approved same origin endpoint or the frontend's local fixture adapter.
4. Add the event from V05. Use the browser console or a local event collection file to view the sample events. Keep user typed FAQ content outside the event. Prepare SEO text and a publication worksheet if the exercise includes them.
5. Run the acceptance cases with synthetic inputs. In the handoff record which mode, local fixture or n8n, produced the outputs. Show how to reproduce a successful result, an unsupported question and an unavailable assistant state.

#### Acceptance cases

| Case | Expected result |
| --- | --- |
| Open the local page at 360 px and 1440 px | Title, schedule and CTA are readable in both. |
| Tab to the primary link and press Enter | The schedule location is reached and the local logger records exactly one schedule_view. |
| “Do I need desktop Excel?” | Answer says desktop Excel is optional; cite faq-session#schedule v2. |
| “Can I move my session?” | Include one request, at least 24 hours, and seat availability; cite faq-move#policy. |
| “Can I get a refund?” | Visible unknown status and no source or promise for a refund. |
| Force a retrieval error or disconnect the adapter | Show an unavailable result while the page and schedule remain usable. |
| Compare current and archived data | Tuesday 18:30 IST appears. Wednesday only appears when explicitly reviewing the archived record. |

**Instructor check.** Ask the learner to replace a single source fact, verify that both the page and assistant agree, and explain how the FAQ source and page copy should be kept in sync. Grade with the [instructor playbook](#instructor-playbook).
