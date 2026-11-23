# Building websites with AI

Build a small original site from a brief, preview each revision, and decide how to publish and measure it. Use the same fictional workshop throughout. The [capstone](#website-and-faq-capstone) combines the web work with a read only FAQ assistant. [Practice kit](practice-kit.md) · [Provider references](source-map.md#provider-references)

## V01 Introduction to vibe coding

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

## V02 Refining websites with Hostinger and Claude Code

**Outcome.** Use either a visual builder or an AI coding agent to improve the same preview against concrete acceptance conditions.

**Say.** “A visual builder gives me a managed edit and preview experience. A coding agent edits project files I can version and review. I compare how I would make and check the same change in each setting.”

**Show.**
1. Use the V01 brief and initial page. For a Hostinger Website Builder route, start in a draft or preview if the account supports it. Arrange the title, CTA, schedule and FAQ. Inspect the mobile layout before publishing is considered.
2. For a Claude Code route, open a scratch project or existing authorized repo. Ask the agent to read the HTML and CSS, propose the smallest change to the layout, and implement it where authorized. Ask for a description of the changed lines plus a local preview command.
3. Apply the same improvement in the available route. For example, put the CTA before the long explanation in reading order, make its focus visible, and ensure the schedule stays legible at 360 px.
4. Record the previous and new preview. Keep accepted copy and page behavior in a short brief the next agent can read. Describe the other route in steps if it is unavailable.

**Practice.** Deliver one revised version, a before and after note and five checks for layout, content and interaction.

**Pass.** The display has no horizontal overflow at 360 px, heading order is coherent, and the learner can explain where edits and publishing settings live on their chosen route. [Hostinger Website Builder](https://www.hostinger.com/website-builder) · [Claude Code documentation](https://code.claude.com/docs/en/overview)

## V03 Deploying a site with domain, hosting and DNS

**Outcome.** Deploy a preview or produce a deployment worksheet showing how domain records, TLS and the hosting service fit together.

**Say.** “Hosting serves files. DNS tells a visitor where the name should point. TLS lets the visitor connect with HTTPS. I check the host's instructions before changing DNS and keep a record of how I could undo the change.”

**Show.**
1. Identify the site entry point and build output. Use the provider preview URL or a local preview for class. Record the expected status, base path and asset paths under the chosen deployment.
2. Draw a map from the registrar and nameservers to the authoritative DNS zone, hosting target and HTTPS certificate. For a subdomain, a CNAME commonly points to a hostname. A and AAAA point to IPv4 and IPv6 addresses. Use the hosting provider's instructions for the apex and any domain verification records.
3. Write a DNS worksheet with record name, type, target, TTL, reason and rollback. Copy real record values from the verified hosting setup only when the user has authorized using that domain. For the lab use reserved placeholders and show how a reader would verify the route.
4. After an approved deployment, inspect the public endpoint, TLS, redirects, relative links and broken assets. Allow for cached DNS results. Preserve links for both the preview and final site when applicable.

**Practice.** Choose a static host or the visual builder's hosting and prepare the worksheet. Include the steps to diagnose a site loading over the preview URL while a custom domain still fails.

**Pass.** The worksheet states the correct record types, puts certificate verification after pointing the domain at the configured host, and identifies what should be restored for rollback. The learner can distinguish their observed result from a plan. [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart) · [Cloudflare DNS records](https://www.cloudflare.com/learning/dns/dns-records/)

## V04 SEO and Google Search Console

**Outcome.** Create a basic search readiness checklist and interpret what an inspection result would establish.

**Say.** “I write a page that describes what a person can do, then make it easy to find and read. Search Console can tell me what Google observed about a verified site. I keep an indexing request separate from the result of indexing.”

**Show.**
1. Write a descriptive HTML title such as “Spreadsheet Basics Live Class | Harbor Skills Studio,” a brief description grounded in D06, a visible H1 and link text that describes the action. Use one canonical URL only after confirming the intended deployment URL.
2. On a live or sample deployment, check that the page loads and its navigation uses real links. Check the canonical, sitemap and access controls for agreement. Explain that robots rules control crawler access. If exclusion is desired, choose the appropriate supported measure for the page's access and indexing goals.
3. In an authorized Search Console property, inspect the exact final URL and review the indexed result and live test. Record any blocking reason Google shows. Submit a sitemap or request indexing only when that maintenance work is in scope. For local practice use mock states “live fetchable,” “current canonical points elsewhere,” and “access restricted.”
4. Ask AI for three title and description alternatives using the supplied facts. Check the chosen wording and remove unsupported guarantees. Review links after publishing changes.

**Practice.** Give an SEO audit with one content correction and one technical check, then write a brief response to a mock “URL is not on Google” result.

**Pass.** Titles and copy describe the correct class, the URL used in the check is exact, and the learner can distinguish crawling, eligibility and observed indexing. [Google SEO starter guide](https://developers.google.com/search/docs/fundamentals/seo-starter-guide) · [Search Console URL Inspection](https://support.google.com/webmasters/answer/9012289)

## V05 Website measurement with Google Analytics

**Outcome.** Define a measurable site interaction, validate the event and interpret a small report.

**Say.** “I pick a question first. For this site I want to know how often visitors choose to look at the sample schedule. A page load, a click and a registration each answer different questions.”

**Show.**
1. Plan one event called `schedule_view`. Define it precisely for this lab as a user activation of the primary schedule CTA. Include non-personal fields `page_id=workshop` and `placement=hero`. Keep the event independent of typing into a form.
2. For local practice, capture the event with a local logger. Test a page load, click and keyboard activation in separate runs. Each deliberate activation should log once. A duplicate listener or a load event should not increase the count.
3. With an authorized analytics setup, use the practice GA4 property and web stream. Install the approved tag in the chosen builder or site, respecting consent controls used on the page. Verify the debug event and its parameters with the current provider UI before looking at a normal report. Avoid sending private text or identifying fields in event parameters.
4. Interpret an example of 20 sessions and 5 distinct sessions with a schedule_view event as 25% of sessions. Show why counting all events as distinct sessions overstates engagement if some people click twice.

**Practice.** Submit an event dictionary and trace. If using a local logger, label it as local. State what the event can measure and one question that a registration event would answer.

**Pass.** The selected CTA causes one event per deliberate activation, the page load generates none, and the reported metric shows the correct denominator. [Google Analytics setup](https://support.google.com/analytics/answer/9304153)

## Website and FAQ capstone

**Brief.** Build a small public-style workshop page for Harbor Skills Studio and a locally previewed FAQ assistant with an evidence trail. Use D02 as the source of truth for answers and D06 for page copy. Use the W01 prompt pattern for constraints, P06 for question answering, and V01–V05 for design, deployment readiness and measurement.

### Functional contract

| Area | Required behavior |
| --- | --- |
| Public page preview | Display class name, purpose, schedule and the “View the sample schedule” CTA. Date is a sample, so show only the Tuesday time and IST from D02. |
| Navigation and accessibility | Use semantic sections, readable contrast, labelled question input, visible keyboard focus and one region announcing the returned answer. The primary link works at 360 px and desktop widths. |
| FAQ | Accept a question and return status, answer and source IDs. Give an answer from the current schedule or transfer policy, or say the fixture leaves a question open. |
| Failure state | If the assistant is unavailable, show a short status message and leave the workshop schedule readable. |
| Measurement | Log `schedule_view` once per CTA activation in local practice mode. |
| Delivery | Provide a project folder or code as requested, startup steps, fixture and evidence from the acceptance cases. If the user requests hosting, provide the actual preview or deployment handoff once authorized. |

### Build order

1. Create the visual path first using the files produced in V01. Put the schedule and the software requirement on the page as normal text so they remain visible while the FAQ component loads.
2. Add a question field and an output region. Define the response schema with request_id, status, answer and source_ids. Show the answer and source IDs as text. Ensure a source ID remains recognizable and test keyboard operation.
3. For the default local route, create a fixture adapter over D02 and map known questions deterministically. Return unknown for gaps in the fixture. To build the n8n route, connect the frontend to a dedicated read only question endpoint implementing P06. Keep credentials server side and choose either an approved same origin endpoint or the frontend's local fixture adapter.
4. Add the event from V05. Use the browser console or a local event collection file to view the sample events. Keep user typed FAQ content outside the event. Prepare SEO text and a publication worksheet if the exercise includes them.
5. Run the acceptance cases with synthetic inputs. In the handoff record which mode, local fixture or n8n, produced the outputs. Show how to reproduce a successful result, an unsupported question and an unavailable assistant state.

### Acceptance cases

| Case | Expected result |
| --- | --- |
| Open the local page at 360 px and 1440 px | Title, schedule and CTA are readable in both. |
| Tab to the primary link and press Enter | The schedule location is reached and the local logger records exactly one schedule_view. |
| “Do I need desktop Excel?” | Answer says desktop Excel is optional; cite faq-session#schedule v2. |
| “Can I move my session?” | Include one request, at least 24 hours, and seat availability; cite faq-move#policy. |
| “Can I get a refund?” | Visible unknown status and no source or promise for a refund. |
| Force a retrieval error or disconnect the adapter | Show an unavailable result while the page and schedule remain usable. |
| Compare current and archived data | Tuesday 18:30 IST appears. Wednesday only appears when explicitly reviewing the archived record. |

**Instructor check.** Ask the learner to replace a single source fact, verify that both the page and assistant agree, and explain how the FAQ source and page copy should be kept in sync. Grade with the [instructor playbook](instructor-playbook.md).
