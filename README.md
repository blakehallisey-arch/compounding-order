# Squid AI — "Sephora Agents, in compounding order"

A single-page interactive artifact built as a **follow-up to Eyal Manor (CEO, Squid
AI)** after a call. Primary reader is Eyal; Leslie Lee will also see it, so every
number must be defensible.

## What it argues

It answers Eyal's literal question from the call — the three agents you'd build for
Sephora — then carries it one level up: **the order you build them in is the
strategy.** Each agent's real payoff isn't the task it does, it's the foundation it
leaves behind that makes the next agent cheaper and safer to build.

## The page

One scrolling page, six static blocks:
1. Header — the idea, stated plainly
2. The three agents, in compounding order (each with a CEO view + a "leaves behind"
   line + a growing **foundation bar** — ~33% → 66% → 92%, the key visual)
3. The fourth agent you don't have to invent (the emergent cross-functional one)
4. "You already work this way" — DealFlow validation, faithful to Squid's published
   case study
5. Where I'd take it next (the open frontier, marked in progress)
6. The curated engine — three vetted static examples

## Design

Copies the **First Rung** aesthetic: white surfaces, 0.5px hairline borders, one
teal accent for the compounding idea, amber only for emergent / in-progress pieces,
plain sentence headers, generous whitespace, no gradients or shadows. Copy is locked
and on-voice (no em dashes). Full spec + verbatim copy in `BUILD-THIS.md`.

## Stack

Static front-end deployed to Vercel, with a serverless function (`api/score.js`)
proxying the Anthropic API so the key never touches the browser — same stack as
First Rung and Agent Blueprint Builder.
