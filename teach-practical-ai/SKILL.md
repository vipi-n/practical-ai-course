---
name: teach-practical-ai
description: Teach a practical AI course, prepare instructor materials, or build and review the associated AI, n8n, and website projects. Use for requests that identify this curriculum, a lesson ID, a project ID, or the Harbor Skills Studio capstone.
---

# Teach Practical AI

Use this curriculum to teach a beginner, help an instructor deliver a class, or build a practice project. The lesson IDs map to all 40 video topics in the public outline for Zero to Infinity with AI. The explanations, examples, exercises, answer keys, project designs, and course delivery plan were authored for this guide.

## Choose the work the user requested

| Request | Start here |
| --- | --- |
| Explain what the paid course advertises | [Public syllabus and correspondence](references/source-map.md) |
| Teach me or prepare a class | [Instructor playbook](references/instructor-playbook.md) and the requested module below |
| Build, debug, or review an n8n project | [n8n lessons](references/05-n8n.md), the selected [project blueprint](references/n8n-projects.md), and its fixtures |
| Build a practice website or combined project | [Website lessons and capstone](references/06-websites.md) and the referenced fixtures |
| Supply sample inputs, expected results, or prompt starters | [Practice kit](references/practice-kit.md) |

| Lessons | Module |
| --- | --- |
| F01–F03 | [AI concepts](references/01-ai-concepts.md) |
| T01–T10 | [Essential tools](references/02-ai-tools.md) |
| W01–W04 | [Everyday work](references/03-everyday-work.md) |
| S01–S05 | [Specialized applications](references/04-specialized-ai.md) |
| N01–N13 | [n8n and APIs](references/05-n8n.md) |
| V01–V05 | [Website building with AI](references/06-websites.md) |

Open the selected chapter and any resources it references. For a new learner without a requested starting point, begin with F01 and use the learner's job or goal to adapt the examples. In a single Markdown edition, look up the same headings and IDs within that file.

## Deliver or build

- **Tutoring.** State the skill the learner will practice. Introduce the idea, work the demo, then give the learner the exercise. Wait for their attempt before revealing the answer when tutoring interactively. Give specific feedback against the pass condition and record the result in the format in the playbook.
- **Instructor materials.** Turn the selected lesson's talk track, demo, and exercise into a ready to deliver session. Include the words to say, what to display, the handout, and a separate answer key. Use original Harbor Skills Studio examples unless the user supplies a scenario. If the user asks for a complete workshop, produce the requested materials in the current turn.
- **Build or debug.** Use the project blueprint's data contract and cases to produce the requested local artifacts or configuration steps. Start with synthetic fixtures and a manual run. Use a model stub or a local simulation when credentials or a live service are unavailable. Verify the requested behavior when the environment permits. Report the actual files, how to run them, checks performed, and what still depends on the user's environment.
- **Review.** Compare the submitted output against the expected result, call out discrepancies with evidence, and offer one revision exercise or patch as appropriate. A plausible model answer is insufficient evidence that a workflow ran.
- Use the vendor references in the source map to check current control names, supported features, pricing, and plan availability when those details affect the task. Use the user's chosen tools when they meet the project contract.
- Keep keys in the platform's credential store or environment variables. Use the supplied fictional inputs for instruction. Enable live data access, sending, public deployment, or production triggers when the user's request authorizes that specific action and the relevant credentials and destination are available.

## Example requests

- “Teach me N01 and N02 using a mock API. Give me the exercise before the solution.”
- “Prepare a 60-minute instructor session for W01 and W02, including speaker notes, a handout, and an answer key.”
- “Build P03 with mock emails. Save the implementation and show the expected output for E-101 through E-104.”
- “Review my P06 demo against the source IDs and unknown-answer test in the practice kit.”
