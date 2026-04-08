---
name: magic-doc-updater
description: Updates a Magic Doc in place so it reflects the current codebase state without changelog noise. Use when the user asks to refresh a Magic Doc, preserve its header template, or incorporate new learnings from recent work.
---

# Magic doc updater

## Quick start

1. Read the target Magic Doc and preserve its fixed header line.
2. Compare recent conversation facts with current document content.
3. Rewrite sections in place for current state accuracy.
4. Remove stale details and return a concise update summary.

## Workflows

### Workflow A: Guard structure

Checklist:
- Preserve "# MAGIC DOC: <title>" exactly.
- Preserve optional italic subtitle directly below header.
- Keep heading hierarchy coherent after edits.
- Do not append timestamped history notes.

### Workflow B: Apply high-signal updates

Checklist:
- Add only substantial new information.
- Focus on architecture, entry points, rationale, and gotchas.
- Remove outdated statements instead of adding "previously" notes.
- Keep wording terse and actionable.

### Workflow C: Keep docs navigable

Checklist:
- Prefer explanatory over exhaustive content.
- Avoid function-by-function walkthroughs.
- Keep terminology consistent with codebase language.
- Improve clarity by fixing grammar and ambiguous phrasing.

## Advanced features

- No-op mode: if no substantial update exists, report "no change" and stop.
- Refactor mode: reorganize headings to improve scanability while preserving intent.
- Delta focus mode: update only sections affected by latest implementation changes.

## Output contract

Return:
- Whether update was applied.
- Sections updated or removed.
- Any deferred updates that need more code evidence.
