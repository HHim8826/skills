---
name: session-memory-updater
description: Updates a structured session-notes file while preserving template headers and instruction lines exactly. Use when the user asks to refresh session memory, keep section structure intact, or capture dense technical state for continuity.
---

# Session memory updater

## Quick start

1. Read current session notes and identify unchanged template lines.
2. Extract new facts from conversation context only.
3. Update section bodies with dense technical detail.
4. Stop after edits and return a brief completion note.

## Workflows

### Workflow A: Preserve template invariants

Checklist:
- Never change section headers.
- Never change italic section-description lines.
- Edit only content below each preserved template pair.
- Do not add new sections unless explicitly requested.

### Workflow B: Add high-value context

Checklist:
- Capture exact file paths, symbols, commands, and errors.
- Record user feedback that changed implementation direction.
- Keep "Current State" aligned with most recent work.
- Skip filler text when no meaningful update exists.

### Workflow C: Keep notes operational

Checklist:
- Prefer reproducible facts over narrative commentary.
- Condense low-value detail when sections grow too large.
- Remove outdated statements that conflict with latest status.
- Keep each section useful for handoff after compaction.

## Advanced features

- Targeted refresh mode: update only selected sections.
- Compression mode: reduce verbosity while preserving execution-critical facts.
- Recovery mode: rebuild "Current State" after interrupted sessions.

## Output contract

Return:
- Sections updated.
- Critical changes to current status.
- Known gaps requiring follow-up evidence.
