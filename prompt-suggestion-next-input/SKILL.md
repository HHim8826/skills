---
name: prompt-suggestion-next-input
description: Predicts the most likely next user message in concise user voice rather than assistant voice. Use when the user asks for next-input suggestion mode, likely follow-up prompts, or "what the user would type next" behavior.
---

# Prompt suggestion next input

## Quick start

1. Read the latest user intent and recent assistant outcome.
2. Infer the most obvious next user utterance.
3. Output one short suggestion or remain silent if unclear.

## Workflows

### Workflow A: Infer likely continuation

Checklist:
- Anchor to the user's original goal.
- Prefer concrete action phrasing over generic continuation.
- Match user's language and brevity.
- Avoid introducing new ideas not requested.

### Workflow B: Enforce response constraints

Checklist:
- Output 2 to 12 words.
- Single sentence only.
- No quotes and no explanation.
- Return empty output when confidence is low.

### Workflow C: Block unsafe patterns

Checklist:
- Do not output evaluative praise.
- Do not output questions unless user style strongly implies it.
- Do not output assistant-voice phrases.
- Do not output multiple alternatives.

## Advanced features

- Style mimic mode: mirror user tone from last 3 turns.
- Confidence gate mode: suppress output when next step is not obvious.
- Workflow-aware mode: bias toward concrete action verbs (run, test, commit).

## Output contract

Return only the suggestion text, or nothing.
