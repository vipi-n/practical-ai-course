# Essential AI tools

Use the same known inputs across tools so learners can compare the outputs. Record which feature was available on the learner's device or account. Each exercise has a text or storyboard fallback. [Practice kit](practice-kit.md) · [Provider references](source-map.md#provider-references)

## T01 ChatGPT features and model selection

**Outcome.** Choose a chat mode for drafting, data inspection or evidence lookup and review the result against a known answer.

**Say.** “I start with the task and evidence. Drafting one paragraph takes less setup than analyzing a table. If a feature can calculate, inspect files, or look up evidence, I show exactly what it read or computed before I use the output.”

**Show.**
1. Start a fresh chat. Paste D03 or save it as a CSV and attach it if file support is available. Ask, “Identify the grain, report unusable rows, and calculate gross valid invoice, paid and unpaid amounts. Show the calculation and IDs behind the totals.”
2. Review the discovered columns and the handling of the missing amount. Confirm how the exact duplicate was recognized and whether the result is based on actual computation or a table read.
3. Ask for a one paragraph draft with the reporting limitation. If the draft uses “cash received in September,” highlight that D03 contains invoice dates only.
4. If two model modes are available, repeat with the same prompt in separate chats. Record mode, elapsed time, supported claims and arithmetic. If you need current facts, use search when available and open a cited source before reusing its claim.

**Practice.** Run the invoice prompt on D03 and produce a cleaned table, exceptions and a manager summary. State which capability you used and how you verified one number independently.

**Pass.** The output has four valid invoices; ₹5,000 total, ₹3,700 paid and ₹1,300 unpaid; one exact duplicate and one missing amount. A manager can trace each figure. [ChatGPT capabilities](https://help.openai.com/en/articles/9260256-chatgpt-capabilities-overview)

## T02 Claude features and model selection

**Outcome.** Use Claude to analyze source text and turn the result into a small usable artifact or a plain text equivalent.

**Say.** “I start with a short, evidence-first instruction. I add a prototype only after the answer is correct. The design can be good while the source interpretation is wrong, so I check both independently.”

**Show.**
1. Paste or attach D02. Ask Claude to make an FAQ table with Question, Answer, and Source ID. Tell it which version is current and require unknown for unprovided policies.
2. Ask for a 60-second review of what the browser spreadsheet rule means for a learner. Ask the model to keep “desktop Excel optional” and preserve both conditions for transfers.
3. If an artifact or code preview is available, ask for an HTML FAQ card with visible source labels. Constrain it to the three current facts and one explicit unknown. Open the preview or save the HTML locally. On a text-only account, review the Markdown table.
4. When comparing Claude models or modes, use the same sources, instructions, time budget, and answer rubric. Ask the learner to choose based on observed accuracy and effort.

**Practice.** Deliver three answered FAQ questions and one unresolved question. Show one change to the artifact or table after checking citations.

**Pass.** The output identifies the correct schedule, browser requirement and transfer policy with source IDs; refund remains unknown; the artifact, if present, works through a keyboard tab and exposes the answer text. [Claude file uploads](https://support.claude.com/en/articles/8241126-upload-files-to-claude) · [Claude Artifacts](https://support.claude.com/en/articles/17153992-what-are-artifacts-and-how-do-i-use-them)

## T03 Gemini and the Google AI ecosystem

**Outcome.** Use Gemini to draft a document from supplied notes. Compare this with a source based notebook for questions about a fixed set of documents.

**Say.** “For drafting a message I can start in Gemini. For questions about a known group of documents, I need marks that point back to the sources. I check those marks before copying the answer.”

**Show.**
1. Paste D01 into Gemini. Ask for a document titled “Workshop preparation” with Confirmed actions, Proposed actions and Decisions still open. Verify the quoted time tags and Thursday revision.
2. Put the result in a local document. If the learner has an authorized Docs integration or export option, demonstrate it on a new practice document. Keep a manual copy option for any account.
3. For the supplemental NotebookLM exercise, add only the three current D02 text files to a fresh notebook. Ask “Can I move my session?” and “Can I get a refund?” Open the citation or source excerpt for any factual answer.
4. Ask what changes if both the old schedule and the current one are present. Identify them with document names and show how version control or source selection prevents a stale answer.

**Practice.** Prepare the meeting document and one verified answer from the notebook. If no notebook is available, mimic the retrieval by pasting only the relevant FAQ and record which excerpt you used.

**Pass.** Two actions have assigned owners, Priya remains proposed, and the second class is undecided. The transfer answer retains the deadline and availability limits, and the refund answer abstains. [Gemini Help](https://support.google.com/gemini/?hl=en) · [NotebookLM Help](https://support.google.com/notebooklm/?hl=en)

## T04 Wispr Flow and dictation

**Outcome.** Turn spoken input into accurate, edited work text and identify where speech recognition or rewriting changed meaning.

**Say.** “I use dictation to capture an idea while it is fresh. I compare names, numbers, and changes of mind with the transcript. When I switch from notes to a formal message, I decide what is safe to clean up.”

**Show.**
1. In a disposable draft, say “Mira, reminder Wednesday at five. Correction, Thursday at noon IST. Dev owns formula checks. His deadline is still open.” Use Wispr Flow if available, or type the spoken text.
2. Keep the raw transcript and make a second version for the team. Use a table with owner, task, due text and open question. Have the learner read both copies before any polishing.
3. Say “Priya might own the slides.” Compare “might own” with “will own.” Mark an accidental strengthening as a factual error.
4. Repeat with one ambiguous name or an acronym. Spell it out, or use the app's vocabulary settings if offered. Correct the transcript before sending it to any other tool.

**Practice.** Dictate a 30 second task update, include one deliberate correction, and produce a 60 word handoff note. Mark any unresolved owner or date.

**Pass.** The revised due time is Thursday 12:00 IST, Dev's deadline stays open, and Priya remains proposed. The learner identifies one correction from spoken input to final copy. [Wispr Flow](https://wisprflow.ai/)

## T05 Generating video with Higgsfield

**Outcome.** Storyboard a short educational video and use controlled revisions to improve shot continuity.

**Say.** “I create a shot list before I generate anything. Each shot has a subject, one movement, a purpose, and a length. I ask for generated motion and compose precise text separately so the call to action stays legible.”

**Show.**
1. Use D06 to sketch three shots at five seconds each: overhead desk and fictional worksheet, close screen view showing a filter or formula, and a simple final title card.
2. Write a shot prompt for the first frame: “Overhead view of a dark blue desk, open laptop with a fictional spreadsheet, soft daylight from left, slow push in, subject centered, 16:9.” Use the same desk, light direction and framing references for subsequent shots.
3. Generate a sample in a suitable video tool if available. Make one revision that changes only camera speed, then compare hand or object distortions, framing and continuity. If access is unavailable, compare two storyboards with different camera directions.
4. Add the title and captions after generation. Spell the brand and call to action verbatim. Keep the worksheet legible using a screenshot of synthetic data or an editor overlay.

**Practice.** Submit a shot table with durations, prompts, transitions, rights to source assets and the final call to action. Show what one revision fixed.

**Pass.** The shot durations add to 15 seconds, the viewer can read the call to action, and no shot contradicts the brief or introduces an unverified claim. [Higgsfield](https://higgsfield.ai/)

## T06 Using the Grok assistant

**Outcome.** Use Grok for initial exploration and validate a topical claim against a primary source.

**Say.** “I can use a chat assistant to find leads. I separate a claim from the source that supports it. A popular post can reveal a question to investigate. The original documentation or announcement is the stronger basis for asserting a fact.”

**Show.**
1. Ask Grok for what an organization has announced about one tool, limited to a one week time range you supply. Request title, organization, date, direct URL, and what the link actually establishes. Use a small topic such as one official release from your work area.
2. Open the first cited page and locate the exact claim. Record both the publication date and the date of any rollout mentioned. Verify that the result applies to the stated audience.
3. Repeat the process on the synthetic D07 cards. Show how a newer official spec changes the answer compared with an older flyer. If the tool is unavailable, give the class a candidate answer and ask them to audit it manually.
4. Rewrite the result as “confirmed,” “reported by source,” or “unverified,” based on what you can see. Keep speculative citations out of the factual summary.

**Practice.** Build a three row claim ledger and correct one mistaken or weakly sourced claim.

**Pass.** Every confirmed claim has a direct supporting source. The synthetic class cap is 12 and certificate availability remains unresolved. [Grok on X](https://help.x.com/en/using-x/about-grok)

## T07 HeyGen avatars and ElevenLabs audio

**Outcome.** Plan a talking presenter video and a natural voiceover from the same original script.

**Say.** “I write the script in short beats and listen before I place it over a video. The visual tool handles the presenter. The audio tool handles pronunciation, pace and phrasing. Captions give me a third place to check what the viewer receives.”

**Show.**
1. Draft this D06 script: “Practise filters and formulas in one live hour. Follow along in your browser. View the sample schedule.” Read it at a natural pace and time it before generating audio.
2. In an available text to speech tool such as ElevenLabs, use a stock or authorized voice. Preview one line, check pauses, and record expected pronunciation for the fictional brand. Change only pace or wording on the second pass.
3. In HeyGen, choose an available authorized presenter or use a storyboard. Align the audio or corresponding script to the caption timings. Inspect the first and last frames for a cut word or caption.
4. Export a draft if available. Save the script and caption track together with the audio or storyboard so another instructor can review the same wording.

**Practice.** Produce a 15 second sample or a time coded mock with a finished transcript. Note the voice and media source.

**Pass.** Audio or read-aloud timing fits the requested length, captions reflect the spoken wording, and the claims and CTA match D06. [HeyGen Help](https://help.heygen.com/en/) · [ElevenLabs text to speech](https://elevenlabs.io/docs/overview/capabilities/text-to-speech)

## T08 Meta Muse

**Outcome.** Give a general assistant a research and planning task with an explicit point at which it should return control.

**Say.** “Muse is Meta's assistant. Muse Spark is a model family that powers it. I write down what evidence an assistant can use, what it can prepare, and what still needs a person to act.”

**Show.**
1. Open the currently available Muse interface or demonstrate with another chat assistant. Paste the current D02 schedule and request a checklist for preparing a learner for that session.
2. Require a verified time and setup, a list of facts still needed, and text for a draft reminder. Ask it to leave the recipient blank and say when a booking or reminder would need confirmation.
3. Ask it to add a second session. Check that it identifies the missing schedule information. Give it the archived schedule and check that it describes the date as historic.
4. Review what was based on your text, what was inferred, and any claimed external action. Treat an app's claimed operation as pending until the relevant tool reports its outcome.

**Practice.** Write a constrained plan for a two step workshop reminder from the D02 records, with the exact point where a person makes the next decision.

**Pass.** The sample reminder uses Tuesday 18:30 IST and optional desktop Excel, while the recipient and permission remain open. [Meta Muse](https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/) · [Muse Spark](https://ai.meta.com/blog/introducing-model-meta-superintelligence-labs)

## T09 Apple Intelligence

**Outcome.** Use a supported device feature to edit a text draft and confirm that the edit preserves meaning.

**Say.** “I start with the part of the text that needs attention. A rewrite can improve readability and accidentally change an owner, deadline, or promise. I keep the original visible until I confirm those details.”

**Show.**
1. Check Apple's current device, operating system, language and region information. If Writing Tools is available, select a sample paragraph in a supported app. Otherwise use a text assistant for the same exercise.
2. Use the D01 facts to compose an informal three sentence update with the phrase “Priya may be able to handle the slide deck.” Ask for a concise, professional rewrite.
3. Compare original and revised drafts word for word on owner, due time and level of commitment. Fix any changes to Dev's deadline, Priya's status or the second class.
4. Demonstrate a second pass with an explicit audience, such as the workshop team. Save the revision as a draft for inspection.

**Practice.** Submit before and after copies and highlight three unchanged facts. Explain when you would use a small edit over a broad rewrite.

**Pass.** Mira's revised timing, Dev's unspecified due date and Priya's provisional ownership survive the edit. [Apple Intelligence setup and compatibility](https://support.apple.com/en-us/121115)

## T10 Conversational voice with ChatGPT

**Outcome.** Carry out a short spoken interaction in which the assistant handles clarification and returns a reviewable record.

**Say.** “Voice gives me a way to speak and hear the answer. I still ask for a readback of names, dates and uncertain details. For a voice workflow with calls, tools or booking, I add explicit state and permissions.”

**Show.**
1. Ask the voice interface to act as a mock front desk for Harbor Skills Studio. Give it D02, or describe the rules by voice. Set the two intents to schedule and required software.
2. Say “Can I attend it Tuesday?” Ask it what “it” refers to if the conversation is unclear. Give the class name, then say “Wait, did you say 6:30 in India time?” Ask it to state 18:30 IST.
3. Ask whether Excel is required and whether refunds are possible. Record the expected optional answer for Excel and unknown answer for refunds.
4. Compare the returned text or your own notes with the spoken exchange. If microphone access is unavailable, role-play the dialogue in chat. A multi-turn call workflow is a separate build in N10 and P07.

**Practice.** Submit a four turn transcript with one correction and one unsupported request. State the final confirmed details.

**Pass.** The assistant handles the correction, gives Tuesday 18:30 IST as the sample cohort time, and leaves refund policy unresolved. [ChatGPT Voice](https://help.openai.com/en/articles/20001274-chatgpt-voice)
