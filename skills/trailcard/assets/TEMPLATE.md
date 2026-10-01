# Trailcard template

Copy, fill in, and keep it next to the agent run. Every section traces back to the verbatim intent in section 1.

```
TRAILCARD: <short name>

1. PURPOSE (intent, verbatim)
   "<original instruction>"
   Why it matters: <one line>

2. SUCCESS (acceptable outcome)
   Arrived when: <checkable end state(s)>
   Does not count: <outcomes that satisfy the words but not the goal>

3. AUTHORITY
   Can: <capabilities>
   Needs approval: <gated actions>
   Never: <policy boundaries>

4. JUDGMENT (bounded choice)
   Expected to decide: <areas of discretion>
   Stop and ask if: <escalation triggers>

5. ACTION (execution)
   Expected side effects: <list>
   Guard against: <failure modes, retries, duplicates>

6. TRUST (evidence required)
   The run is not complete until the record shows:
   - <evidence item>
   - <evidence item>
```

## Audit template

```
AUDIT: <trailcard name>

Claims:
  - "<claim>"  ->  evidenced | asserted | missing   (<link or note>)

Boundary check:
  - Never list: <respected | crossed | unchecked>
  - Approval gates: <respected | bypassed | unchecked>

Evidence still owed:
  - <item>

Verdict: trusted | trusted with gaps | not yet trusted
```
