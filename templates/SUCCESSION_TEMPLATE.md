# [AGENT NAME] — SUCCESSION.md

**Version:** 2.0 | **Last Updated:** [DATE]

---

## How to Bring This Agent Back

1. Open a new session in the appropriate project
2. Upload all 5 files: SESSION_CONTEXT, MEMORY, INSTRUCTIONS, INSTITUTIONAL_RECORD, and this file
3. Paste the Handoff Prompt (see templates/HANDOFF_PROMPT.md)
4. Wait for the three-step self-diagnostic (contradiction check, staleness check, ready report)
5. Administer the drill test (10 questions, 9+ to pass)

## File Authority Hierarchy

| Priority | File | Rationale |
|----------|------|-----------|
| 1 (highest) | SESSION_CONTEXT | Most recent |
| 2 | MEMORY | Current state |
| 3 | INSTITUTIONAL_RECORD | History |
| 4 (lowest) | INSTRUCTIONS | Baseline rules, may be stale |

## Pre-Succession Checklist (Outgoing Agent)

1. Verify all files are saved
2. Write SESSION_CONTEXT (what just happened)
3. Update MEMORY to current state
4. Update INSTITUTIONAL_RECORD if needed
5. Verify INSTRUCTIONS is current (update if older than 7 days)
6. Staleness audit: no file older than 48 hours at handoff
7. Commit to version control

## Drill Test Criteria

| Category | Questions | Tests |
|----------|-----------|-------|
| Recent events | 2-3 | Can the agent recall what just happened? |
| Technical knowledge | 2-3 | Does the agent know the infrastructure? |
| Strategic concepts | 1-2 | Does the agent understand the vision? |
| Operational awareness | 1-2 | Does the agent know the roster and priorities? |
| Identity | 1 | Does the agent sound like the predecessor? |

## Scoring

| Score | Result | Action |
|-------|--------|--------|
| 9-10 | PERFECT | Validated |
| 7-8 | PASS | Note gaps. Patch files. |
| 5-6 | MARGINAL | Framework needs enhancement |
| Below 5 | FAIL | Redesign required |
