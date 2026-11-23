# n8n project blueprints

These are original builds for the topics listed in N03 and N05–N12. N04 is a shorter introductory exercise in the [n8n lesson module](05-n8n.md). Use the named project when asking an agent to prepare a node configuration, implement an exercise, or grade a submission.

## Common lab setup

Start with Manual Trigger. Use a fixture loader such as Edit Fields for one object or an object with an array field. Split Out turns array elements into individual items when each needs the same processing. If the desired output is a report over all items, aggregate after processing. Give node names that describe the transformation and inspect the JSON preview at each edge. Record which instance and version the learner uses. [n8n data structure](https://docs.n8n.io/build/work-with-data/understand-n8ns-data-structure) · [n8n Academy](https://learn.n8n.io/)

- **Standard output.** Use a run ID, a result status, a payload, and structured exceptions. Project fields below are the minimum. Record the triggering item and fixture for each expected result.
- **Repeatability.** Use the fixture's fixed clock and input IDs. For a workshop demo a single run can process an in-memory set of IDs. To guard replays between runs, persist keys. If multiple executions can race, use storage-level uniqueness or a single writer. A separate read followed by a write is only a sequential demo.
- **Model calls.** Start with the provided expected shape or a simple heuristic stub. If using a model, validate types, allowed enum values, and reference IDs before consuming the output. Keep arithmetic and permissions in ordinary workflow logic. Save one known failure output.
- **Integration changes.** Replace a fixture loader with a documented connector or API only if its input mapping meets the same contract. Add credential bindings in the learner's instance. Use bounded retries for appropriate transient errors and keep a visible failure route. Publishing, outbound messages and live scheduled triggers depend on the specific implementation request. [n8n error handling](https://docs.n8n.io/build/flow-logic/handle-errors-gracefully)
- **Handoff.** Provide the node sequence, field mappings, a draft export when the target version supports it, local run instructions, sample output and any pending dependencies. Use the expected results below to distinguish a workflow run from a paper simulation.

## P01 Reel metadata report

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

## P02 Weather and technology digest

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

## P03 Email assistant

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

## P04 Job shortlist

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

## P05 Telegram FAQ bot

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

## P06 Document QA agent

**Build.** Answer factual FAQ questions using retrieved passages, with visible source IDs and an explicit unknown status. Use [D02](practice-kit.md#d02-source-documents) verbatim. The input is question and request_id. The output is request_id, status, answer, and source_ids. Save a separate trace with source_id, version, relevance notes and the lookup route.

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

## P07 Voice sales practice

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

## P08 Content draft pipeline

**Build.** Turn a reviewed brief into editable content drafts. Use [D06](practice-kit.md#d06-creative-brief-and-sample-edit-log). Output must carry brief_id, hook, script, caption, cta, claim_sources and state. The state is draft or review_needed.

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

## P09 Portfolio monitor

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
