---
title: MoltCore
description: Local-first orchestration runtime for TypeScript — compose operator requests, provider selection, orchestration, automation, memory, and tool routing from one package.
author: MoltCore
ms.date: 2026-04-04
ms.topic: overview
keywords:
  - moltcore
  - orchestration
  - typescript
  - local-first
---

## Welcome to MoltCore

MoltCore is a private Node.js 22 and TypeScript package that gives you a single control plane for local-first operator workflows. One import wires together provider scoring, orchestration primitives, channel adapters, memory storage, MCP integration, and tool routing so you spend time on your product instead of the plumbing.

## What we build

| Package | Purpose |
|---------|---------|
| `@moltcore/core` | Shared control-plane contract, runtime dispatch helpers, and orchestration primitives |
| `@moltcore/channels` | Channel adapters for connecting operators to external surfaces |
| `@moltcore/memory` | Local memory store with retrieval and context injection |
| `@moltcore/mcp` | MCP facade for registering and invoking tool servers |
| `@moltcore/tools` | Built-in tools available to every operator |

## Core capabilities

* Compose operator requests through a single `dispatchQuery()` call
* Score and select providers at runtime with `recommendProvider()`
* Execute registered tools via `executeTool()`
* Connect MCP servers with `connectMcpServer()`
* Bootstrap the full runtime from one `bootstrap()` entry point

## Get started

```bash
# Install dependencies
pnpm install

# Validate your environment
pnpm lint && pnpm typecheck && pnpm test && pnpm build
```

Full documentation lives in the `docs/` directory and can be previewed locally with `pnpm docs:build`.

## Resources

* [Getting Started](../docs/getting-started.md) — install, validate, and run your first command
* [Architecture](../docs/architecture.md) — module layout and request flow
* [Orchestration](../docs/orchestration.md) — orchestration module deep dive
* [CLI and API](../docs/cli-and-api.md) — concrete command and import reference
* [Experimental Modules](../docs/experimental-modules.md) — gated learning, governance, and Composio surfaces

## Contributing

MoltCore is currently a private project. If you have access, open a branch, run the full validation suite (`pnpm lint`, `pnpm test`, `pnpm typecheck`, `pnpm build`, `pnpm docs:build`), and submit a pull request. Keep docs and runtime behavior aligned — both must pass before merging.
