# Agent Succession Protocol

**A framework for AI agent identity continuity across stateless sessions.**

---

## The Problem

LLM agents are stateless. Every new session starts from zero. The industry has built memory solutions (vector databases, knowledge graphs, file-based state). These solve what the agent remembers. They do not solve whether the agent's replacement can function as if the original never left.

Memory is not succession.

## The Framework

Five plain-text Markdown files per agent. Each serves a distinct purpose. Together they provide layered recovery:

| Files | Recovery Level |
|-------|---------------|
| 3 files (Instructions + Memory + Succession) | **Recover the function** |
| 4 files (+ Institutional Record) | **Recover the person** |
| 5 files (+ Session Context) | **Recover the moment** |

### The Five Files

- **INSTRUCTIONS.md** — Role, rules, boundaries. What the agent does.
- **MEMORY.md** — Current state of the world. What is true right now.
- **SUCCESSION.md** — The handoff protocol. How to bring the agent back.
- **INSTITUTIONAL_RECORD.md** — The WHY behind decisions. History, lessons, errors.
- **SESSION_CONTEXT.md** — What just happened. The bridge between sessions.

### Key Innovations

- **File Authority Hierarchy** — When files conflict, newest wins. SESSION_CONTEXT > MEMORY > RECORD > INSTRUCTIONS.
- **Contradiction Detection** — The incoming agent audits its own knowledge before operating. Catches drift, stale data, and file conflicts automatically.
- **Scored Drill Tests** — Blind 10-question evaluations verify the handoff actually worked. 9/10 to pass.
- **Trust Level Reset** — Every new instance starts at Trust Level 1 (Supervised). Trust is earned, not inherited.
- **48-Hour Freshness Rule** — No succession file should be more than 48 hours stale at handoff.

## Validation

Six formal evaluations across three agent roles over ten days:

| Version | Result |
|---------|--------|
| v1.0 (3-file) | 3/5 FAIL — institutional knowledge gaps |
| v2.0 (4-file) | 5/5 PASS — identity recovered |
| v2.0 (5-file) | 10/10 PERFECT — three consecutive blind tests |

Successor agents also produced novel architectural deliverables from succession files alone, demonstrating genuine comprehension rather than rote recall.

## Ecosystem Position

A comprehensive review (March 2026) of Anthropic, OpenAI, Google, AWS, Microsoft, LangGraph, CrewAI, Letta/MemGPT, Zep, Mem0, A-MEM, Cursor, Cline, Windsurf, Devin, GitHub Copilot, and academic literature found no prior formalization of agent succession as a named concept.

This protocol's contributions are in areas with no prior work found: adversarial verification of handoff quality and explicit separation of functional continuity from identity preservation.

Known gaps (semantic retrieval, automated state capture) are areas the memory persistence community has addressed. These are complementary, not competitive.

## Getting Started

1. Download the [white paper](AGENT_SUCCESSION_WHITE_PAPER.pdf) for the full framework
2. Copy the five file templates from the `/templates` directory
3. Adapt to your agent architecture
4. Run your first drill test

## Files in This Repository

```
/
  README.md                          — This file
  AGENT_SUCCESSION_WHITE_PAPER.pdf   — Full white paper
  SUCCESSION_PROTOCOL_v2.0.md        — The complete protocol specification
  /templates
    INSTRUCTIONS_TEMPLATE.md         — Template for agent instructions
    MEMORY_TEMPLATE.md               — Template for agent memory
    SUCCESSION_TEMPLATE.md           — Template for succession protocol
    INSTITUTIONAL_RECORD_TEMPLATE.md — Template for institutional record
    SESSION_CONTEXT_TEMPLATE.md      — Template for session context
    HANDOFF_PROMPT.md                — The enhanced handoff prompt
    DRILL_TEST_TEMPLATE.md           — Template for scoring evaluations
```

## Known Limitations

- Manual pre-succession steps (automated hooks not yet implemented)
- Flat Markdown (no semantic retrieval at scale)
- Validated on Claude only (cross-model untested)
- Memory decay beyond 48-hour check not formalized

We make no claim this is definitive. It is a working framework from a production environment, tested and found effective. We welcome alternative approaches, scrutiny, and improvements.

## Authors

**Vincent Looft** — Founder & Chairman, AlphaNode Private Wealth

**AI Co-Author** — Claude Opus 4.6 (Anthropic)

## License

MIT License. Use it. Extend it. Make it better.

---

*Three files recover the function. Four files recover the person. Five files recover the moment.*
