# Repolex Knowledge Graph of datasette/datasette-auth-tailscale

RDF knowledge graph data for [datasette/datasette-auth-tailscale](https://github.com/datasette/datasette-auth-tailscale), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download datasette/datasette-auth-tailscale
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7520939af6eff6c804135a73926bb621027c8314
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7520939af6eff6c804135a73926bb621027c8314
│           └── chunk-001.nq.gz
├── blob
│   ├── 0fdbe51e254df923bd9778e8a25a786ba130b560.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 814a3a4283a1bed8467d85b8e2986854d22fa38d.nq.gz
│   ├── b40b34b07efa8231db3a1a789a6cab56bc6e4989.nq.gz
│   ├── b965021a231f865d7eba14c51a4a865f15cc72fc.nq.gz
│   ├── bf041f0d72dfa3585fa88b534dc6b9d608525c34.nq.gz
│   ├── d4269c27fe9b058bc3ffab8aff808e5dbd09ba03.nq.gz
│   ├── d725e1317742200bc9a2af65e5f89e625bbc321f.nq.gz
│   └── eb22e74eaaaf0edc4aa2c0f8900a55750d1660f9.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7520939af6eff6c804135a73926bb621027c8314.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 15 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[datasette/datasette-auth-tailscale](https://github.com/datasette/datasette-auth-tailscale)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
