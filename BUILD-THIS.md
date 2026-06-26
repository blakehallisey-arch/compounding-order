# BUILD-THIS.md — Sephora Agents, in Compounding Order

A single-page interactive artifact for a follow-up to Eyal Manor (CEO, Squid AI). Primary reader is Eyal. Leslie Lee will also see it, so every number must be defensible.

It answers his literal question from the call (the three agents you'd build for Sephora) and then carries it one level up: it shows the order that makes them compound, proves the method against Squid's own DealFlow rollout, and ends on an open frontier that is still in progress.

Stack matches the prior builds (First Rung, Agent Blueprint Builder): static front-end deployed to Vercel, with a serverless function proxying the Anthropic API so the key is never exposed client-side.

---

## 0. The one idea

Each agent's real payoff is not the task it does. It is the foundation it leaves behind, which makes the next agent cheaper and safer to build. So the order is the strategy.

Hold that idea above everything. Every section serves it.

Scope: this is one artifact. The deep teardown of a single rung (the credit-card agent taken all the way down to the real systems and the messy data) is a separate, optional second-conversation asset and is NOT part of this build. Do not fold it in here.

---

## 1. Page structure

One scrolling page. Six blocks, in this order. All six are static. The sixth is the curated engine, with no live API in the default build.

1. Header (the idea, stated plainly)
2. Build them in this order (the three agents, each with a CEO view and a "leaves behind" line, plus a growing foundation bar)
3. The fourth one you don't have to invent (the emergent cross-functional agent)
4. You already work this way (DealFlow validation, faithful to their published case study)
5. Where I'd take it next (the open frontier, marked in progress)
6. The curated engine: three vetted examples, static, no open input (described in section 5 below)

Visual language: copy the First Rung aesthetic. White surfaces, 0.5px hairline borders, one accent color (a teal for the foundation/compounding idea), amber only for the emergent and in-progress pieces, plain sentence headers, generous whitespace, no gradients or shadows. Plain-language section headers are mandatory. The reader should never have to decode a legend.

The single most important visual is the foundation bar that grows across the three agents (roughly 33%, 66%, 92%). It is what makes "compound" legible without words. Make it unmissable. Animate the fill on scroll-into-view if cheap to do.

---

## 2. Exact copy (locked, on-voice)

Use this copy verbatim unless Blake edits. No em dashes. Plain and concrete.

### Header

Eyebrow: Follow-up to our conversation

Title: The three agents you asked for, in the order that makes them compound.

Subline: Any model can spin up an agent that works. That stopped being the question. The question is which ones compound, and in what order. Each agent's real payoff isn't the task it does, it's the foundation it leaves behind that makes the next one cheaper and safer to build. So the order is the strategy.

Definition line (small, tertiary, directly under the subline): An agent is a loop with a stop condition, not a thing you query. Each of these triggers, decides, acts, and stops.

### Section header: Build them in this order

Each agent renders as a numbered card: name, a description that leads with what the agent does autonomously, a small monospace loop line (trigger to action to stop), a CEO greenlight line tied to a metric, and a "leaves behind" line. The two customer-or-money-touching agents (2 and 3) also carry a one-line gate marker. Below each card, the growing foundation bar. The descriptions must lead with autonomous action, never with answering, retrieving, or personalizing, so none of them reads as a chatbot or a recommendation engine.

**1. Onboarding agent**
Description: Triggers when someone is hired, builds their role-specific ramp plan, stages access for approval, schedules the right intros, tracks milestones, and escalates when something stalls. It runs the ramp, it doesn't answer questions about it.
Loop line (monospace): new hire to plan, stage access, track, escalate to stop when ramped
As CEO I'd greenlight this first: It costs almost nothing to try and it pays back every hiring cycle. Faster ramp means productive sooner. Lower first-90-day attrition means I stop paying to re-hire the same role. It's the lowest-risk way to prove agents work in a regulated environment before I point them at anything sensitive. Metrics: ramp time, 90-day retention, rehire cost avoided.
Leaves behind: the first map of the company. Who owns what, which system holds which truth. Every later agent needs that map.
Foundation bar: 33%

**2. Credit card and loyalty conversion agent**
Description: Triggers on customer and batch events and decides which prescreen offers to fire, suppress, or route, reasoning across the issuer, loyalty, and CRM data, then adapts targeting on the acceptance signal. Offer cleanup and currency reconciliation ride along.
Loop line (monospace): customer event to decide fire / suppress / route to adapt on acceptance
Gate marker (small, tertiary, under the loop line): Autonomous loop. Human approves every customer-facing send, within legal's bounds.
As CEO I'd greenlight this next: This moves margin on both sides, and margin is the thing I can't move by pricing in this category. On revenue, the card is one of my highest-margin levers, and right now advisors skip it because the value prop is too confusing to explain at the register. Clean that up and prescreen smarter and acceptance goes up. On cost, smarter real-time targeting cuts mailer spend and manual compliance cycles. Metrics: card acceptance and activation, mailer cost, reconciliation accuracy. I measurably moved acceptance and cut mailer spend on this exact problem, and I'm happy to walk through the specifics in person.
Leaves behind: a reconciled credit-and-loyalty identity layer, built on the system map from step one, plus proof the governance pattern holds in a regulated, compliance-heavy setting. Both are what earn the right to point an agent at customers next.
Foundation bar: 66%

Note for the implementer: this is Blake's real lived domain (the Unified Currency relaunch with Bread Financial). Do NOT print confidential Sephora or Bread figures: no royalty rates, no profit-share targets, no spend totals, no breakage, no exact prescreen lift percentages. Results are stated as "measurably moved, specifics available in person." The discretion is deliberate and reads as trustworthy to a CEO.

**3. Beauty-journey agent**
Description: Decides the next best action for each member across touchpoints, takes it, and adapts on the response. Not a recommendation waiting to be shown. An agent that moves the member forward, respects their permissions, and learns from what happens.
Loop line (monospace): member signal to decide and act to adapt on response
Gate marker (small, tertiary, under the loop line): Autonomous loop. Human holds the gate on anything that reaches a member.
As CEO I'd greenlight this last: I can't change what a category margin is, but I can change how much each member I already have buys, and how often. That's conversion, basket size, repeat rate, and how well I'm using Beauty Insider and the co-brand credit. It's top-line growth from members I already have, not paid acquisition. I put it last because it touches customers, and I only point an agent at customers after the first two have earned the identity and trust controls to do it safely. Metrics: conversion, average order value, repeat rate, loyalty and credit utilization.
Leaves behind: the trust and identity layer, proven first on internal onboarding and then in the regulated card program, so customer-facing is the earned last step rather than the risky first one.
Foundation bar: 92%

### Section header: The fourth one you don't have to invent

Copy: It doesn't wait for a question. Once those three connect, it watches across all of it and surfaces the thing before anyone knew to ask, when a customer-behavior shift, a loyalty-and-credit signal, and an operations signal converge into something no single team can see, then it routes or acts. This is the one I reached for in our call. It wasn't wrong, it was early. The foundation has to exist for it to watch.
Loop line (monospace): cross-domain pattern to detect to route or act (no human query)

Style: amber card, solid border. This is the reframe of the live answer Blake fumbled. Keep it confident and short.

### Section header: You already work this way

Lead line: This isn't my method. It's yours. DealFlow did exactly this:

PHASE 1: Started with the most painful bottleneck, getting sales notes into Salesforce. Ran it with a small group, proved it, expanded to hundreds.
PHASE 2: Built on that foundation by adding call transcripts to surface buying signals and deal risk. Cheaper because Phase 1 already laid the ground.
Closing line: Most companies invert it and start with the ambitious agent, then wonder why it dies in production. Painful thing first, prove it, build on the layer.

IMPORTANT: this section must stay faithful to Squid's published DealFlow case study. Do not embellish the phases or invent figures. Eyal knows the real story. If anything here drifts from their public material, cut it.

### Section header: Where I'd take it next

Card title: The agent none of your teams can build alone
Copy: Same move as the fourth one above, lifted from Sephora to your business. Support, sales, and finance each leave their own foundation. Once they connect, there's an agent that watches across all three and acts on what no single team can see. No one team owns it. No one team can build it.
In-progress note (set off, smaller): Still in progress. You understand a layer by building inside it, not by mapping it from outside. I sketched this from your public material. To actually understand it I'd want inside one real account, because the layer's real shape only shows once it's integrated. That's the part I'm working on now.

Style: amber card, dashed border. This is the only dashed element on the page. Keep it visibly thinner and less polished than the rest. It is genuinely unfinished and should read that way.

---

## 3. Honesty guardrails (non-negotiable)

- No fabricated dollar figures anywhere. Metrics are named as levers and directions (markdown rate down, in-stock up), never invented precise numbers. If Blake adds figures later, they must be his own buy-side estimates with assumptions shown.
- The DealFlow section stays faithful to the published case study.
- The frontier section stays thin and in progress. Do not over-polish the unfinished part or it stops reading as unfinished.
- The whole artifact is framed as "here's how I think, tested on the example you gave me," never "here's how you should run your roadmap." Method, not verdict.

---

## 4. The two views per agent (stacked, no toggle)

Each agent card shows two short lines, both always visible: the "As CEO I'd greenlight this" line (the metric and margin reason) and the "Leaves behind" line (the compounding reason). That is exactly how the locked copy in section 2 is written. Do not build a toggle. Stacking both lines is simpler, has no failure surface, and reads in one pass. Clarity wins over cleverness.

---

## 5. The engine, curated (build second)

The engine shows the method runs on more than the three Sephora agents, and that it can say no. That is its whole job. It does NOT need a live, open text box to do that job, and an open text box is the single biggest risk in the whole artifact.

Reasoning, stated plainly so it doesn't get re-litigated later: every other part of this artifact is curated and cannot embarrass Blake. A live engine taking arbitrary input in front of Eyal is the one component that can produce something dumb in real time, and one bad placement retroactively discredits all the curated thinking above it. The downside is asymmetric and large, the upside (it feels interactive) is small. So the engine is curated, not open.

### What to build instead
Three pre-vetted example candidates, shown as buttons. Clicking one reveals a locked, hand-written result card. No arbitrary input. Every possible output is one Blake has already read and approved. The viewer still sees the engine reason across varied cases and, critically, sees it decline one. The discrimination is visible. The grenade is gone.

### UX
Under the frontier section: a heading, "The same test on three agents I didn't pick to fit it." A subline, "It builds what compounds and rejects what doesn't. The one it rejects is the point." Optional framing line underneath: "The model can build any of these. What it can't do is decide which ones earn the next. That judgment is the job." Then three buttons in a row, each a candidate name. Click reveals that candidate's result card below, in the same visual language as the three agents. Default to the first one already expanded so the section is never empty.

### The three locked examples (use this exact content)

The visible placement chip on each card uses the same plain language as the narrative (build it / build it last / don't build it), not internal bucket names. The bucket names below are only for the optional live-mode prompt.

**Example 1 — Dispute and chargeback triage agent → build it, after the foundation**
- CEO view: bottom line. Metric: cost per dispute, resolution time. Reason: routes each dispute to the right team on first contact instead of bouncing it, which cuts handling cost and speeds resolution.
- Leaves behind: a categorized reason-code layer that a later fraud or collections agent can reuse.
- Placement chip: build it, after the foundation. Compounds: yes.
- Rationale: sits on the system map an earlier agent lays down, then deposits structure the next agent inherits.

**Example 2 — Proactive churn-save agent → build it, but last**
- CEO view: top line. Metric: retention, repeat rate. Reason: reaches at-risk customers before they lapse, protecting recurring revenue from members you already have.
- Leaves behind: consumes the identity and trust layer rather than building new foundation.
- Placement chip: build it, but last. Compounds: depends on earlier layers.
- Rationale: it acts toward customers, so it is only safe once identity, permissions, and trust are already proven. Powerful, but not first.

**Example 3 — Standalone FAQ chatbot → don't build it**
- CEO view: marginal. Metric: none durable. Reason: deflects a few questions but moves no real number you would run the company against.
- Leaves behind: nothing reusable.
- Placement chip: don't build it. Compounds: no.
- Rationale: it isn't really an agent. No loop that learns, no stopping condition tied to an outcome, nothing it leaves behind. Buys fine, builds nothing, does not lower the cost of the next solve. The engine says no, and that no is what proves it discriminates.

### Rendering
- candidate name → card title
- placement → plain-language chip matching the narrative: "build it, after the foundation" and "build it, but last" render neutral; "don't build it" renders muted with a strikethrough treatment on the name
- the CEO line, the leaves-behind line, the rationale line
- for the "don't build it" card, hide the CEO and leaves-behind rows and show only the rationale, so the "no" reads as deliberate, not empty

Because the content is locked, this section is pure static HTML and JS. No API call, no parsing, no failure surface. It cannot break in the room.

### Why this beats the live version for this reader specifically
Eyal told Blake he runs the company by staying narrow and saying no to anything without a compelling case. Shipping a controlled, vetted demonstration instead of a flashy live gamble is itself a small proof that Blake operates the way Eyal does. The disciplined version is both safer and more on-thesis.

### Optional live mode (only if Blake insists, build last, test hard)
If Blake wants it to actually call the model, do NOT use an open text box. Wire the same three buttons to call the API with their exact, tested input strings, and keep the locked card above as a cached fallback that renders if the response is anything other than clean expected JSON. Live when it works, indistinguishable when it doesn't. The system prompt and proxy below support this mode. The open-textarea version is not built under any circumstance.

If live mode is built, map the prompt's internal bucket to the plain chip the page uses: foundation and operational both render "build it, after the foundation" (neutral); customer-facing renders "build it, but last" (neutral); emergent renders "build it once the layers connect" (amber); decline renders "don't build it" (muted, strikethrough). The reader never sees the bucket names.

### System prompt (only used in optional live mode)

```
You are a build-selection engine for an enterprise AI agent platform. You evaluate
a candidate agent or workflow and place it in a build sequence.

CEO view: which margin lever does this move, top line, bottom line, or both, and the
specific operating metric. Be concrete. Never invent a dollar figure. Levers and
directions only.

Build view: what foundation does this leave behind that makes the NEXT agent cheaper
or safer to build. If it leaves nothing reusable, it does not compound.

Placement: foundation (cheap, maps systems, build early) | operational (moves margin,
depends on a foundation) | customer-facing (high trust bar, build late) | emergent
(only possible after layers connect) | decline (compounds into nothing or no real
metric, refuse it).

Rules:
- Frame as "would" and "leaves behind", never as fact about a real deployment.
- Never fabricate numbers, customer names, or results.
- A thin chatbot or one-off with no reusable layer returns "decline". Be willing to say no.
- Every field 1 to 2 sentences. Plain language. No buzzwords.

Return ONLY valid JSON, no preamble, no fences:
{
  "agent_name": "short name",
  "ceo_view": { "lever": "top line | bottom line | both", "metric": "...", "reason": "1-2 sentences" },
  "build_view": { "leaves_behind": "... or 'nothing reusable'", "compounds": true | false },
  "placement": "foundation | operational | customer-facing | emergent | decline",
  "rationale": "1-2 sentences"
}
```

---

## 6. Stack and deploy

- Front end: a single `index.html` is fine (matches Agent Academy), or a minimal Vite app. All five narrative blocks plus the curated engine are static HTML/CSS/JS. With the default curated engine, there is no required server component at all.
- Optional serverless proxy: only needed if Blake builds the optional live mode. `/api/score.js` as a Vercel function reads `ANTHROPIC_API_KEY` from `process.env` and proxies to `https://api.anthropic.com/v1/messages` with `model: "claude-sonnet-4-6"`, `max_tokens: 1024`. The key never touches the browser. If the live mode is not built, this file is not needed.
- Deploy: push to a GitHub repo under blakehallisey-arch, import to Vercel. Set `ANTHROPIC_API_KEY` only if the live mode exists. Suggested URL slug: compounding-order or sephora-agents.

### /api/score.js sketch (optional live mode only)

```js
export default async function handler(req, res) {
  if (req.method !== "POST") return res.status(405).end();
  try {
    const { candidate } = req.body;
    const r = await fetch("https://api.anthropic.com/v1/messages", {
      method: "POST",
      headers: {
        "content-type": "application/json",
        "x-api-key": process.env.ANTHROPIC_API_KEY,
        "anthropic-version": "2023-06-01"
      },
      body: JSON.stringify({
        model: "claude-sonnet-4-6",
        max_tokens: 1024,
        system: SYSTEM_PROMPT,
        messages: [{ role: "user", content: candidate }]
      })
    });
    const data = await r.json();
    const text = (data.content || []).map(b => b.text || "").join("");
    res.status(200).json({ text });
  } catch (e) {
    res.status(500).json({ error: "scoring failed" });
  }
}
```

---

## 7. Build order

1. Static narrative, all five narrative blocks, with the growing foundation bar working cleanly and both lines stacked on each agent card. This alone is a finished, shippable artifact. Stop here if time runs short.
2. The curated engine: three buttons, three locked result cards, the "don't build it" card rendered deliberately. Pure static, no API. This cannot break.
3. Deploy to Vercel. No env key needed unless the optional live mode is built. Click through the whole thing once on a phone to check it reads clean.
4. Write the email.
5. Optional, only if time and appetite: the live mode on the three vetted buttons with the locked cards as cached fallback. Test against the three exact inputs until it never shows an error. If it ever does, ship the static version.

---

## 8. The email (four sentences, no more)

Draft to adapt, not send verbatim. No em dashes.

"Your question about the three agents pulled a thread I couldn't put down. I built out how I'd actually sequence them so each one leaves a foundation that makes the next cheaper, with the CEO's reason and the metric on each. It also runs your own DealFlow rollout through the same logic, since that phased build is the pattern. The last piece is the cross-functional solve none of the three teams owns yet, which I've started on from the outside and would want a real account to finish. [link]"

The closing line is the one that matters most. It carries his question past where he left it and openly asks for the messy real account, which answers the only doubt he'd hold about you.
