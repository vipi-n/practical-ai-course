# AI concepts

Three lessons cover why language models are useful, how they make mistakes, and how a document retrieval system gives an answer a source. Start with the first three fixtures as needed. [Practice kit](practice-kit.md)

## F01 Generative AI and automation

**Outcome.** Given a work goal, choose a rule, a model, or a supervised sequence of both and explain the choice.

**Say.** “I use a rule when the same input should always lead to the same decision. I can use generative AI when the task is to draft, summarize, or interpret varied language. A workflow connects steps in a defined order. An agent is useful when the model has to choose among tools based on the request. The tools still need a clear contract.”

**Show.**
1. Classify the D03 invoice rows with the fixed rule “flag missing amounts.” There is exactly one matching row and it is visible in the data.
2. Use a text model to draft a two sentence reminder using D06. Supply only the class description and its approved claims. Ask the model to leave open dates and recipients as placeholders.
3. Draw the combined flow “receive approved notes → extract the action → check the owner → create a draft.” Repeat the same input. Compare the deterministic output from the amount rule with possible differences in a drafted sentence.
4. Add a tool choice only if different requests genuinely need it. Compare “format the schedule” with “look up the schedule or transfer policy and answer the question.” Explain why the second task can benefit from retrieval.

**Practice.** Design how you would process a learner's email asking whether Excel is required. Mark which step retrieves evidence, which step drafts prose, and where a person checks the response before sending.

**Pass.** The answer identifies the browser spreadsheet rule using D02, produces a draft, and marks sending as a separate step. The learner can explain that the model's prose is variable while the source rule is stable.

## F02 How language models learn and make mistakes

**Outcome.** Explain training and inference in plain language, then detect an unsupported claim in a realistic answer.

**Say.** “During training, the model learns patterns represented by weights. During inference, it uses those weights and the context we give it to predict text in pieces called tokens. An individual conversation supplies temporary working context. A plausible sentence can still get a detail wrong, especially when the prompt assumes a fact the source never states.”

**Show.**
1. Ask “Describe Harbor Skills Studio's participation certificate” with no evidence. Read the answer and highlight any factual assertion. The model may also ask for context. Both outcomes are useful for the demo.
2. Paste D07 and ask “Using only R01–R03, state whether participation certificates are available. Cite a card ID and distinguish a question from an approved policy.”
3. Require three fields, claim, evidence and status, then check the actual quoted passage. Label the output as insufficient evidence. If the response says certificates are available, ask it to point to the sentence that asserts availability.
4. Explain that longer context can help only if it contains the right evidence. Large inputs may bury the important detail or exceed product limits. Save source excerpts and expected answers when comparing runs.

**Practice.** Compare one answer from the vague prompt with one grounded answer. Mark each factual claim as supported, contradicted or unknown. If both runs abstain, use the fabricated candidate “Certificates are available on request” as the claim to grade.

**Pass.** The learner marks certificate availability unknown, cites R03 as a question, and correctly treats R02's older class cap as superseded by R01. They can explain why the model sounding confident did not affect the result.

## F03 Retrieval augmented generation with documents

**Outcome.** Trace an answer from a retrieved passage and use a consistent fallback when evidence is missing.

**Say.** “RAG means the application finds useful passages first and then gives them to a model to draft the answer. I can inspect what was retrieved separately from the answer. A search miss, an archived source, or a misread passage all lead to different fixes.”

**Show.**
1. Load D02 as separate records. Keep source ID, version and current or archived status. Use one FAQ section per chunk in this small example.
2. Search current records for the question “Can I switch my booking?” A keyword search can miss that “switch” and “transfer” express the same idea. Demonstrate a synonym mapping or a semantic search when available.
3. Pass the transfer passage to a text model with this instruction, “Answer using the retrieved passage. Include the deadline and the seat condition. Attach the source ID. If there is no basis for the answer, say this set does not answer it.” Manually compare the resulting statement to the passage.
4. Ask for a refund. With no supporting FAQ, give a short unknown answer and explain how the learner can request a current policy. Ask for workshop time and check the current version beats the archived schedule.

**Practice.** Create three examples with expected retrieval IDs and answer status. Label a failure as retrieval, generation, or source maintenance. Show the received passages and the final text side by side.

**Pass.** The answer for transfer says one request, at least 24 hours, and seat availability with faq-move#policy. Refund abstains. The schedule uses version 2. Advance to N09 for a workflow implementation. [Retrieval in n8n](https://docs.n8n.io/build/integrate-ai/understand-ai-components/retrieve-relevant-context)
