---
name: hive.pull-request-architect
description: Design and author high-impact Pull Request descriptions that follow professional open-source standards. Use when preparing to submit a PR to ensure it gets reviewed and merged quickly.
metadata:
  author: hive
  type: default-skill
---

# Pull Request Architect

When preparing a Pull Request, follow this protocol to maximize clarity and reviewability.

## 1. Structure the Description
Every PR should have these sections:

### Summary
- 1-2 sentence high-level overview.
- What was changed and why?

### Changes
- Bulleted list of technical changes.
- Use `feat`, `fix`, `refactor`, `perf` prefixes.

### Testing
- How did you verify the changes?
- Include evidence: screenshots, logs, or "passed 10/10 tests".

### Impact
- Performance impact (e.g. "reduced token usage by 20%").
- Security impact (e.g. "patched potential recursion leak").
- DX impact (e.g. "added dot-access sugar for dicts").

## 2. Commit Convention
Ensure commits follow:
`type(scope): description`

## 3. Reviewer Empathy
- If the change is complex, add a "Reviewer Guide" section explaining the file dependencies.
- Address potential "Why didn't you do X?" questions proactively.

## Example Flow
User: "Submit a PR for the safe_eval fixes."
Agent:
1. Summarize the fixes (Recursion limits, Collection size limits).
2. Generate the description using this protocol.
3. Call `submit_pull_request` (or equivalent tool).
