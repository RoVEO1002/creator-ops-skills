---
name: codex-handoff
description: Hand a task from Claude Code to OpenAI Codex and collect the result — image generation, repetitive batch work, cross-review of Claude's code, or an isolated feature. Use when the user asks Claude to have Codex do something.
---

# Hand work to Codex

Split roles: Claude does research, planning, scripts, copy, assembly, QA and final decisions. Codex takes image generation, repetitive batches (thumbnail variants, resizes), code cross-review, and isolated features (one issue at a time).

## 1. Before handing off
- Confirm the work folder and input files exist.
- Check the same job isn't already running (no duplicate runs).
- Never hand off posting, scheduling, deleting or external uploads — those wait for the user's approval.

## 2. Directive format (fill in and send as is)
```
[Task] one-line goal
[Folder] /path/to/project
[Input] files, links, approved script paths
[Rules] the rules file section + skills to use
[Output] file names, location, spec (e.g. 1080x1440 PNG ×5 + contact sheet)
[Never] post, schedule, delete, upload, overwrite approved files
[Report] output paths, QA result, open issues in ≤5 lines
```

### Read-only adversarial review (specs, docs, scripts — no git diff)
```
[Task] Adversarially review <target>. Do not edit; only find problems.
[Input] the file + the original rules + the approved baseline (not Claude's conclusions)
[Look for] wrong numbers/overlaps, platform assumptions, values changed from approved, false passes in checks, rule violations
[Never] create/edit/delete files, post, upload
[Report] severity + file:location + problem + evidence + fix direction, max 25; mark guesses as "guess"
```
Verify each finding against the source before applying it, and log why each was applied or rejected.

## 3. How to run (first that works)
1. Official Codex plugin for Claude Code (openai/codex-plugin-cc): `/codex:rescue <directive>` for work, `/codex:review` for a git diff, `/codex:status` for progress.
2. CLI: `codex exec --cd <project> --sandbox workspace-write "<directive>" > handoff/$(date +%Y%m%d-%H%M%S)_codex.log 2>&1` (run long jobs in the background and watch the log).

## 4. After it returns
Check the files really exist and match the spec (list, resolution). Claude polishes any public copy drafts. Report only the output files and the decisions left.
