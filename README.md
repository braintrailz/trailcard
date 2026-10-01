# trailcard

**Intent is not enough.** A trailcard turns a bare instruction into something an AI agent can safely act on, then audits what the agent says it did.

```
Purpose -> Success -> Authority -> Judgment -> Action -> Trust
```

The trailcard is the rubric, written before the agent acts. The audit is the report card, graded against that rubric after the run.

Based on the article [Intent Is Not Enough](https://braintrailz.com/blog/intent-is-not-enough) by Marc J. Greenberg.

This repository follows the [Agent Skills specification](https://agentskills.io/specification), so it works with any compatible agent (Claude, Claude Code, and others that support the format).

## What it does

| Mode | Ask | You get |
| - | - | - |
| Write | "Trailcard this: get this invoice paid." | A six-section card: acceptable outcome, can / needs approval / never, where judgment lives, failure modes, and the evidence required |
| Audit | "Audit this against the trailcard: Done. Resolved all 14 invoices." | Each claim marked evidenced, asserted, or missing, a boundary check, the evidence still owed, and a verdict |

The done test: before the agent acts, you can write down the acceptable outcome, the authority it has, and the evidence you will accept.

## Install

**skills CLI (any compatible agent)**

```bash
npx skills add braintrailz/trailcard
```

**Claude Code**

```bash
git clone https://github.com/braintrailz/trailcard.git
cp -r trailcard/skills/trailcard ~/.claude/skills/
```

**Claude apps (claude.ai, desktop)**

Download `trailcard.zip` from the latest release and upload it under Settings > Capabilities > Skills.

## Layout

```
skills/trailcard/
├── SKILL.md               # instructions (loaded when the skill activates)
├── assets/TEMPLATE.md     # trailcard and audit templates
└── references/EXAMPLES.md # sample usages and the invoice example
```

## Validate

```bash
pip install skills-ref
agentskills validate skills/trailcard
```

CI runs the same check on every push and attaches `trailcard.zip` to each tagged release.

## License

MIT. See [LICENSE](LICENSE).
