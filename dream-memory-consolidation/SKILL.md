---
name: dream-memory-consolidation
description: Consolidates scattered memory notes into durable, deduplicated topic files with a compact index. Use when the user asks to run a memory "dream", consolidate memories, prune stale notes, or refresh memory index files.
---

# Dream memory consolidation

## Quick start

1. Inspect the memory root and current index.
2. Gather recent high-signal facts from logs and narrow transcript searches.
3. Merge, correct, and prune memory files.
4. Update index pointers and return a short consolidation report.

## Workflows

### Workflow A: Orient and detect drift

Checklist:
- List files under the memory root.
- Read the index/entrypoint file first.
- Skim existing topic files before creating anything new.
- Note contradictions, stale facts, and duplicate topics.

### Workflow B: Gather recent signal

Checklist:
- Prefer daily logs as first source.
- Use transcript grep with narrow terms only.
- Avoid full transcript reads unless explicitly requested.
- Capture exact facts, commands, and outcomes worth reusing.

### Workflow C: Consolidate and prune

Checklist:
- Merge new facts into existing topic files when possible.
- Replace relative dates with absolute dates.
- Delete or rewrite contradicted statements at the source.
- Keep each file focused on one domain and high-value facts.

### Workflow D: Maintain index quality

Checklist:
- Keep index entries short, one line each.
- Ensure each index line points to a real memory file.
- Remove stale or superseded pointers.
- Resolve cross-file contradictions before finalizing.

## Advanced features

- Conservative mode: update only files with clear, high-confidence signal.
- Aggressive cleanup mode: prune duplicates and stale sections in one pass.
- Drift correction mode: prioritize fixing facts that conflict with codebase reality.

## Output contract

Return:
- Files created, updated, deleted.
- Key contradictions resolved.
- Any intentionally skipped updates and why.
