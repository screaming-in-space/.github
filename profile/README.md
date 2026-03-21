# Screaming-in-Space

> Set out to build an AI that could run a factory on LV-426. Ended up building the context engine it needed to think.

We build **Continuum Engine** — a durable, observable, context-aware inference platform. The context window gets smarter the more it's used.

### The problem

Every new chat, task, or tool switch forces you to re-explain context. Longer context windows don't solve it — the right tokens at the right time do.

### The approach

Three-tier context infrastructure grounded in cognitive science. Anderson's ACT-R spreading activation — one of the most validated models of human memory — applied to AI context assembly.

| Layer | Substrate | Role |
|-------|-----------|------|
| Episodic Store | PostgreSQL | Append-only chronological truth |
| Relationship Graph | FalkorDB | Knowledge connected through typed edges |
| Semantic Retrieval | Qdrant | Vector embeddings as the entry point |

Six weighted signals assemble context: recency, reinforcement, graph proximity, confidence, structural importance, and tension detection.

### How we build

Glass box, not black box. Carpentry over hype. Everything is built in public at [threadunsafe.dev](https://threadunsafe.dev).

- .NET / C# — the core stack
- Temporal — workflow orchestration
- OpenTelemetry — observability from day one

### Repos

| Repo | Description |
|------|-------------|
| [thread-unsafe](https://github.com/screaming-in-space/thread-unsafe) | Public site and engineering brand |
