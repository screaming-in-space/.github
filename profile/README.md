# Screaming-in-Space

> Set out to build a long running AI agentic system that could be used in a game engine in order to run a factory on LV-426.
> Ended up building the context engine it needed to think.

---

Hello traveler!

We are building the **Continuum Engine** - a durable, observable, context-aware inference platform.

A system where context window gets smarter the more it's used.

## The problem

Every new chat, task, or tool switch forces you to re-explain context. Longer context windows don't solve it - they just give the model more hay to search for the needle. The right tokens at the right time do. This is critical for long running sessions too!

## The approach

Three-tier context infrastructure grounded in cognitive science.

Anderson's **ACT-R** spreading activation - one of the most validated models of human memory - applied to AI context assembly. Memories aren't retrieved by brute-force search. They're activated by association, weighted by use, and decay when they stop being relevant.

Continuum Engine does the same thing with tokens.

```
┌─────────────────────────────────────────────────────────────┐
│                     CONTEXT ASSEMBLY                        │
│                                                             │
│  Recency · Reinforcement · Graph Proximity                  │
│  Confidence · Structural Importance · Tension Detection     │
│                                                             │
│  Six weighted signals. One context window.                  │
└────────────────┬──────────────────────┬─────────────────────┘
                 │                      │
    ┌────────────▼──────┐  ┌────────────▼──────────┐
    │  Relationship     │  │  Semantic Retrieval    │
    │  Graph            │  │                        │
    │  ────────────     │  │  ──────────────────    │
    │  FalkorDB         │  │  Qdrant                │
    │  Knowledge linked │  │  Vector embeddings as  │
    │  through typed    │  │  the entry point       │
    │  edges            │  │                        │
    └─────────┬─────────┘  └────────────┬───────────┘
              │                         │
              └────────────┬────────────┘
                           │
              ┌────────────▼────────────┐
              │  Episodic Store         │
              │  ──────────────         │
              │  PostgreSQL             │
              │  Append-only            │
              │  chronological truth    │
              └─────────────────────────┘
```

## How we build

Glass box, not black box. Carpentry over hype.

Everything is built in public at **[threadunsafe.dev](https://threadunsafe.dev)**.

**Stack** - .NET / C# · Temporal (workflow orchestration) · OpenTelemetry (observability from day one)

## Repos

| Repo | What it is |
|------|------------|
| **[continuum-engine](https://github.com/screaming-in-space/continuum-engine)** | The engine itself - context assembly, memory tiers, inference orchestration |
| **[mu-th-ur-6000](https://github.com/screaming-in-space/mu-th-ur-6000)** | Durable AI agent - Temporal workflows, M.E.AI, pgvector, SignalR relay, .NET Aspire |
| **[agent-tools](https://github.com/screaming-in-space/agent-tools)** | Shared Claude Code skills for bootstrapping AI-assisted repos |
| **[thread-unsafe](https://github.com/screaming-in-space/thread-unsafe)** | Public site and engineering brand |

---

<sub>Built in the open. Documented as we go. No hype, just work.</sub>
