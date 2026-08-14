# Sephora Agents, in compounding order

A single-page interactive artifact about **agent build order** — the argument that
when you're standing up several AI agents inside one company, the sequence you
build them in *is* the strategy.

## What it argues

Pick three agents you'd build for a retailer like Sephora. Then look one level up
from the task list: each agent's real payoff isn't the job it does, it's the
foundation it leaves behind that makes the next agent cheaper and safer to build.
Get the order right and the third agent is nearly free. Get it wrong and you pay
for the same plumbing three times.

The ground under it is Squid AI's **published** DealFlow case study — nothing in
here embellishes their phases or invents figures beyond what they've put out
publicly.

## How to read it

Open `index.html`. The three agents are laid out in build order, each with what it
does, what it leaves behind, and what that unlocks for the one after it.

The scoring engine is curated rather than open-input, on purpose: an artifact
making a careful argument shouldn't hand a live model an arbitrary prompt and let
one weak answer undercut the reasoning above it.

## Live

[compounding-order.vercel.app](https://compounding-order.vercel.app)
