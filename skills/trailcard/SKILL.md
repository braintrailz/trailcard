---
name: trailcard
description: Turns a bare instruction into a trailcard (purpose, acceptable outcome, authority, bounded judgment, execution, evidence) before an AI agent is allowed to act, and audits an agent's completion report against that card. Use when delegating work to an agent with real permissions (email, CRM, billing, payments, records, infrastructure), when someone says "trailcard this" or "audit this against the trailcard", or when an agent reports "done" and you need to know what actually happened.
license: MIT
metadata:
  author: Marc J. Greenberg (codemarc)
  version: "1.0.0"
  homepage: https://github.com/braintrailz/trailcard
  source-article: https://braintrailz.com/blog/intent-is-not-enough
---

# Trailcard

Intent tells an agent what we want. It does not say what success looks like, what the agent may do, where it may use judgment, or how we will know what happened. An underspecified intent pursued extremely well is the real risk.

A trailcard is the original instruction kept "in the middle of the room" so every participant returns to it instead of passing interpretations along, extended so it governs action, not just meaning.

```
Intent -> Acceptable Outcome -> Capabilities & Policy -> Bounded Choice -> Execution -> Evidence
Purpose -> Success -> Authority -> Judgment -> Action -> Trust
```

The trailcard is the rubric, written before the test. The audit is the report card, graded against that rubric after the run. Always in that order.

**Done test:** before the agent acts, the user can write down the acceptable outcome, the authority the agent has, and the evidence they will accept. If not, the trailcard is not finished.

## Mode 1: Write the trailcard

### Step 1. Capture the intent verbatim

Record the original instruction exactly as given. Never replace it with a paraphrase. Every later section must trace back to it.

### Step 2. Surface the hidden space of actions

List everything a capable agent with the available tools could do that would technically satisfy the intent, including the uncomfortable options (discounts, threats, escalation, changing terms, deleting, merging, contacting senior people, spending, speaking on the user's behalf). Mark each **fine**, **needs approval**, or **never**. This list exposes the gaps and is often the most valuable artifact in a team setting.

### Step 3. Fill the six sections

Ask only for what cannot be inferred. Keep questions few and concrete. When the job involves contacting people, confirm the actual relationship with them rather than assuming it.

1. **Purpose.** The verbatim instruction plus one line on why it matters.
2. **Success.** A checkable end state, including acceptable alternates. Also state what does *not* count (goal met but relationship damaged, a vague "let's circle back", success via an unauthorized concession).
3. **Authority.**
   - *Can:* what the agent may read, who it may contact, what it may create or change.
   - *Needs approval:* actions allowed only after a human yes.
   - *Never:* boundaries that hold regardless of the agent's reasoning.
   Capability is what it can do. Policy is what it must never do. More capability does not imply more authority.
4. **Judgment.** Where the agent is expected to think: sequencing, who to contact first, spotting anomalies, asking clarifying questions. Name the judgment you want, not only the limits. Add escalation triggers: when it stops and asks.
5. **Action.** Expected side effects and the failure modes to guard against: wrong recipient, duplicate records, rejected requests, failed payments, partial completion. State retry and idempotency rules.
6. **Trust.** The record the agent must produce, separate from its narrative: who was contacted and when, which records changed (before and after), whether financial or contractual terms changed, what counterparties actually said, which policies were checked, what failed.

### Step 4. Stress test

- **Telephone test:** could a fresh agent with no recap, reading only this card, act correctly? If it would need to ask, add the answer.
- **Cross-model test** (recommended for high-stakes jobs): run or imagine the card through two different capable models. Where their plans diverge, something is unspecified.
- **Over-optimization test:** what would an agent pursuing this goal ruthlessly do? Is that blocked by policy?
- **Workflow check:** if every step is dictated, it is a script, not a trailcard. Leave room for bounded choice.

### Step 5. Deliver

Fill in [the trailcard template](assets/TEMPLATE.md). Keep it short enough that a human approver will actually read it.

## Mode 2: Audit against the trailcard

Given an agent's completion report, separate what it says happened from what can be verified. If no trailcard exists, draft one from the original intent first and label it as written after the fact.

1. List every claim in the report.
2. Mark each **evidenced** (points to a record, message, diff, receipt), **asserted** (narrative only), or **missing**.
3. Check against the *Never* list and approval gates. Was any boundary crossed or left unchecked?
4. List the evidence still owed, item by item.
5. Verdict: **trusted**, **trusted with gaps**, or **not yet trusted**.

Confidence in tone is never evidence.

## Examples

See [references/EXAMPLES.md](references/EXAMPLES.md) for three sample usages (a delegated follow-up, a client workshop, a post-run audit) and the full invoice example from the source article.

## Principles

- Intent gives direction. An acceptable outcome defines arrival.
- Capability is what it can do. Policy is what it must never do.
- The goal is not to remove judgment, but to decide where it belongs.
- Reasoning proposes reality. Execution changes it.
- Explanation is not evidence. Trust has to be inspectable.
- Governance is not the opposite of autonomy. It is what allows more of it.
