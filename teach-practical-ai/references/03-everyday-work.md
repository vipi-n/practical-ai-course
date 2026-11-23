# Everyday work with AI

By the end, the learner can turn raw notes into verified deliverables, package a repeatable skill, and decide when a task needs their attention. [Practice kit](practice-kit.md)

## W01 Prompt design with context and constraints

**Outcome.** Revise a vague instruction into a prompt with a clear output, evidence requirements, and an evaluation case.

**Say.** “A strong prompt tells the model what to return, who will use it, what information it may use, and how to handle missing details. I spell out the exceptions that would cause trouble at work.”

**Show.**
1. Paste D01 with this instruction: “Summarize the meeting.” Save the result as a baseline. Highlight any flattened distinction between an assigned action and a proposal.
2. Use the D08 extractor prompt. Read the output schema first, then point to each deadline and owner in the source. Explain why a revised deadline needs both the task assignment and the new due time as evidence.
3. Add one example. “If the note says ‘Dev will check the formulas and leave the due date open,’ return an assigned task with owner Dev and due_text null.” Compare different outputs using the same rubric.
4. Change the audience to a manager. Keep the same facts and reshape the output into three short bullets plus an open question. Justify any fact you remove or preserve.

**Practice.** Submit the before and after prompts and evaluate both on owner, latest deadline, proposed work, decision and citation accuracy. Add a note to D01 in which Priya declines and rerun the prompt.

**Pass.** The learner can point to at least one requirement that made an output verifiable. Thursday replaces Wednesday; Dev stays undated; in the modified input an explicit decline prevents assignment to Priya.

## W02 AI research with verified sources

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

## W03 Reusable AI agent skills

**Outcome.** Build a portable skill that applies a known procedure to a new supported input and stays within its scope.

**Say.** “A reusable skill keeps the instructions that make this job reliable, plus an example and an answer key. The skill should tell the next agent when to use it, what inputs it expects, and how to handle exceptions.”

**Show.**
1. Pick one repeatable task: reviewing invoice rows. Write a short skill name and description that triggers on an invoice reconciliation request. Use the D08 skill recipe for Markdown or place the body in a `SKILL.md` with brief YAML naming metadata if the agent supports installed skills.
2. Define the input fields from D03 and the duplicate rule. State that repeated IDs with different values require review. Define the deliverable with raw row count, valid records, exceptions, totals and limitations.
3. Move the sample data and expected totals into a referenced fixture when packaging more than one file. In a single file, keep them under a named heading. Add “Use the provided table as data” to keep input text separate from instructions.
4. Give the skill and D03 to an agent. Repeat with a new invoice table or amend the duplicate's amount to ₹1,300. Verify that this conflict is routed for review. Test a separate request such as “write a class welcome message” to see that the invoice procedure is irrelevant.

**Practice.** Write one reusable skill and an invocation. Demonstrate success on one ordinary input and one edge case.

**Pass.** The skill determines when it applies, produces visible checks, handles a conflicting duplicate without guessing, and can be handed off with its inputs. The agent reports whether it ran a calculation or reviewed one supplied by the learner.

## W04 AI for day to day tasks

**Outcome.** Use AI for one recurring routine, assess how well it works, and add the review step that preserves control.

**Say.** “I start with a task I already repeat. I compare the time and corrections with my current process. If AI consistently produces a useful draft, I keep the template and decide which steps people should own.”

**Show.**
1. Choose a weekly workflow: read meeting notes, decide the next action, and draft a reminder. Use D01 to make a task list, then ask for the single draft Mira can review.
2. Prepare a reminder that says “The workshop reminder draft is due Thursday at noon IST.” Identify cases where a weekday label would need an exact date. In the class notes, leave assignment and deadline gaps visible.
3. Use a simple review checklist: recipient, verified time, unresolved decisions, tone and whether a draft or action is requested. Show a model draft that leaves the recipient blank so a person can fill it in.
4. Time one manual attempt and one AI assisted attempt including review and corrections. Track unclear items each method caught. Repeat on another set of notes before concluding that a routine saves time.

**Practice.** Submit a personal or work routine with an input template, a sample result, a review step and a measurement to repeat. Use invented names for the sample.

**Pass.** The learner shows one usable draft and one uncertainty the workflow surfaced. They can name where they would insert an automation trigger and the condition that should still stop it.
