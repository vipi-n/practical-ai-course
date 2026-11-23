# Instructor playbook

## Choose a delivery path

The default learner can use a browser and a spreadsheet and is new to programming. The portable starting setup is one text assistant, a text editor, a browser, and the [practice kit](practice-kit.md). Run a tabletop simulation or a local mock for any vendor workflow the learner cannot access. Introduce an API, local models, or a coding agent as the corresponding exercise calls for it.

| Delivery plan | Sequence and work product |
| --- | --- |
| First session, about 60 minutes | F01 (15 min), W01 (20 min), and W02 (20 min), then a five minute exit ticket. Hand in a revised prompt and a verified claim table. |
| Everyday productivity, three sessions | F01–F03, then T01–T04 and T10 with W01/W02, then W03/W04. Hand in a reusable instruction file and a meeting follow up with traceable decisions. |
| Automation, four sessions | N01–N04 on data and node setup, N05–N08 on small workflows, N09–N12 on agents and monitoring, N13 on assisted implementation and review. Choose one project, satisfy its pass cases, and explain its failure route. |
| Complete course, six units | Follow F, T, W, S, N, V in that order. Allow roughly 2–4 hours per unit except n8n, which can take 6–9 hours if the learner builds multiple projects. Give the capstone another 3–5 hours if requested. This is an estimate for the independent exercises. |

Ask the learner to do three short tasks before the first session: turn a vague request into a deliverable, name a fact they'd verify before sending output, and identify a repetitive workflow with a clear input and result. Use the answers to set the starting level. A strong learner can begin at W03 or N01 and use F02/F03 as reference.

## Teach a lesson

1. Open with a real task and a measurable goal. For W01, tell the learner, “By the end of this session, you can extract verified owners and deadlines from confusing notes.”
2. Say the talk track and show the input verbatim. Ask the learner to predict a common bad output, such as a deadline invented from a phrase like “I'll look at it.”
3. Run the worked example in small steps. Explain what you changed, then highlight a concrete output field before and after the change. If a feature is unavailable, use the fallback and keep the same output contract.
4. Give the learner the practice part, plus time to try it. If they stall, point to one field or one failing case. Surface the answer key after the attempt when teaching interactively. When preparing class materials, keep the answer key under its own heading.
5. Close with an exit ticket. Ask the learner to name one condition that should trigger a refusal to guess, a manual review, or a different tool. Record observed evidence of the skill.

Default lesson timing for a short class is 2 minutes for the goal, 4 for the concept, 6 for the demo, 8 for practice, and 3 for feedback. Adjust the time to the scope. For a full course writing request, turn each lesson into a script, a learner handout, and an answer key with consistent outputs. Reuse the examples so learners can compare methods across tools.

## Review and grade

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

## Teach monthly update sessions

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
