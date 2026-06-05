---
name: Cobalt Session Map
version: 0.1.0
description: Summarize local agent session transcripts into a concise map for review.
---

# Cobalt Session Map

Use this skill when the user wants a short, reviewable map of an agent session
or transcript before sharing it with another person.

This smoke-test skill is based on the OpenClaw `session-viewer` skill. It keeps
the same intent, but uses a random slug for ClawHub GitHub-sync validation.

## Workflow

1. Ask for the transcript file or pasted transcript if the user has not provided
   one.
2. Identify the session goal, important decisions, files or systems touched, and
   unresolved questions.
3. Return a concise summary with:
   - goal
   - timeline
   - decisions
   - validation evidence
   - follow-up items
4. Do not modify the transcript or source files unless the user explicitly asks.

## Output Shape

```text
Goal: <one sentence>

Timeline:
- <short event>

Decisions:
- <decision and rationale>

Evidence:
- <command, URL, screenshot, or observed output>

Follow-ups:
- <remaining item>
```

