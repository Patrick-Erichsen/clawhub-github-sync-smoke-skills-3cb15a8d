---
name: Linen Handoff Brief
version: 0.1.0
description: Write a portable handoff brief for another agent without leaking local paths.
---

# Linen Handoff Brief

Use this skill when the user wants a concise handoff prompt for another agent.

This smoke-test skill is based on the OpenClaw `handoff` skill. It preserves the
core behavior but has a random slug for ClawHub GitHub-sync validation.

## Workflow

1. Identify the task, repository or product context, known constraints, and the
   expected output.
2. Rewrite local filesystem paths into portable anchors such as repository
   names, branch names, PR URLs, issue IDs, command names, or exact error text.
3. Ask the receiving agent to independently review the current state before
   making changes.
4. Include validation expectations and explicit non-goals.
5. Keep the handoff short enough to paste into a new agent thread.

## Template

```text
I want to discuss and possibly work on: <task title>

Context:
- <portable repo/product context>
- <what triggered this task>
- <important constraints>

Before implementation:
- Re-check the current repo, docs, tests, and live PR or issue state.
- Decide whether the task is still real and whether a smaller fix exists.

Task:
- <requested investigation or implementation>
- <non-goals>

Validation:
- <focused checks or evidence expected>

Output:
- Start with findings and recommendation.
- Then give the plan or patch summary.
```

