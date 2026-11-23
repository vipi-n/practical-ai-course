# Specialized AI applications

Keep the input data, deterministic processing and narrative review visible in all five labs. For finance and market replay use the supplied fictional numbers. For video use a text editing plan or locally owned source media. [Practice kit](practice-kit.md)

## S01 Finance applications

**Outcome.** Produce a finance variance table and reviewer memo based on checked calculations.

**Say.** “I keep the calculation in a spreadsheet or code where I can reproduce it. I give AI the checked results to organize and explain. If the table doesn't explain a variance, I turn it into a question for the owner.”

**Show.**
1. Open D04. Calculate actual less budget in a separate column. Formula logic for a percentage is `IF(budget>0,(actual-budget)/budget,"n/a")`. Label currency, sign convention and rounding.
2. Sum actual and budget separately, then calculate total variance and total percentage from those sums. Show why averaging the three row percentages is inappropriate.
3. Ask AI for three lines a manager can act on: overall variance, the largest positive cost variance, and one question for the owner. Supply the checked table. Reject unexplained causes such as “software overspend was due to renewals” when the data has no such field.
4. Cross-check the total by adding the three line variances. Add a second page for the zero budget exception. Discuss how to distinguish invoice amount, cash receipt and reported revenue using D03 as a separate exercise.

**Practice.** Deliver the variance table and a 100 word brief. Include at least one question that would need evidence beyond the table.

**Pass.** Actual ₹30,500, budget ₹28,000, variance +₹2,500 or +8.9%. Software leads the positive variances. Venue percentage is undefined and no unsupported cause is stated.

## S02 Using Claude to assist with video editing

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

## S03 AI in trading, using a paper replay

**Outcome.** Turn a rule into a reproducible historical replay and detect a common timing error.

**Say.** “I ask AI to explain or help code a rule. I check the result by hand on fake prices first. At each step I only use information available at that point in the replay. Fees and trade timing belong in the calculation.”

**Show.**
1. Read D05 in order. Use the two consecutive increases rule to mark a signal at the end of session 3. Write open and close in separate columns and label when each value becomes known.
2. Move the entry fill to session 4's open. Apply the exit signal at session 4's close, then fill at session 5's open. Track state flat, pending entry, holding or pending exit.
3. Calculate gross and net result with the input commission. Add a what-if with ₹0.50 unfavorable slippage per fill. With one unit and the same fee, net is then −₹5.00.
4. Give a model the rule and request pseudocode plus one test case. Compare the output to the manual trace. Point out how using later prices would create look ahead bias. Discuss what a multi-instrument comparison would need, such as missing data and a suitable baseline.

**Practice.** Submit an event log and a brief explanation of one limit of the exercise. Check what happens if the last available session is session 4.

**Pass.** Base entry ₹103 and exit ₹101, gross −₹2, fee ₹2, net −₹4. With data ending at session 4, the exit is pending since the next open is unavailable. Treat this as a simulation demonstration.

## S04 AI assisted data analysis

**Outcome.** Use an assistant to inspect a CSV, explain cleaning decisions and reconcile the result independently.

**Say.** “Before charting I ask what one row represents and how the numbers are measured. I keep a list of which rows were kept, excluded, or sent for review.”

**Show.**
1. Open D03. Check the column names and data types. Define the grain as one invoice, use integer rupees, and keep the source row numbers for traceability.
2. In a spreadsheet or code, separate missing amounts and later exact duplicates. Check that equal invoice IDs with conflicting fields get their own exception rather than disappearing into the duplicate filter.
3. Aggregate surviving amounts by paid and unpaid. Ask the AI for a bar chart specification with these groups and underlying IDs. Describe the conclusion in plain language and name the scope of the input.
4. Recompute one aggregate manually. Check that the two groups add to the total, and that counts of kept and excluded rows sum to six.

**Practice.** Submit tidy input, an exception ledger, the totals, and two sentences about what can and cannot be inferred. Add a seventh invoice with a blank status and define a separate review category.

**Pass.** The original totals tie to D03 and the duplicate and missing amount are distinct. The learner does not infer the date of cash receipts. The added fixture shows an explicitly unresolved status.

## S05 Running AI models locally

**Outcome.** Run an appropriate local model or plan a local run, then measure whether it can answer a specific task within your machine's limits.

**Say.** “A local runtime loads model weights on your device. Model size and quantization affect resource use, and the amount of input also matters. I check the license and compare results on the same task before choosing a model.”

**Show.**
1. Record OS, available memory and disk space. Choose a supported runtime such as Ollama and read the guide for setup. Select a small model your machine can run. Check the model card for language coverage and licensing and record the tag. 
2. After setup, use `ollama list` to see installed models. Run `ollama run your-model-tag`, with your actual tag substituted, or use the runtime's graphical interface. Record whether the model was downloaded before the run.
3. Give the model the same D02 text and three questions for schedule, transfer and refunds. Save the prompt, model tag, elapsed time, sources named and supported answers. Review local app features that may reach a network, such as a separate search tool, if offline execution matters.
4. Compare with a different local model or a hosted answer only when appropriate for the data. If local execution is unavailable, give a machine requirements and model selection plan and grade candidate answers with the fixture.

**Practice.** Write a short run record with hardware, model tag, source handling and a three question result. If you run out of memory, shorten context or select a smaller model and explain the tradeoff.

**Pass.** The result correctly uses current sources and abstains on refunds, or documents the observed error with a reproducible prompt. Keep measurements distinct from estimates. [Ollama quickstart](https://docs.ollama.com/quickstart)
