# Repolex Knowledge Graph of scrapy-plugins/scrapy-dotpersistence

RDF knowledge graph data for [scrapy-plugins/scrapy-dotpersistence](https://github.com/scrapy-plugins/scrapy-dotpersistence), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy-plugins/scrapy-dotpersistence
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9b55f05e80809e13b3da9e9dc69416848cbc5fc1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9b55f05e80809e13b3da9e9dc69416848cbc5fc1
│           └── chunk-001.nq.gz
├── blob
│   ├── 1da73020d5a31d33331a88a07a1a989f16356ee0.nq.gz
│   ├── 2504d51baae076858f97419d5aae12fc3f8fe626.nq.gz
│   ├── 268b0db80e6caec2e2d84de05e1675f4449b1645.nq.gz
│   ├── 38728bfc523892186d10987332d28967e0c2ccbd.nq.gz
│   ├── 591e61993c1053aa07264e5a43a7d897c7ed72f8.nq.gz
│   ├── 8ec2dba4775fe0e66541e4f2abb223e0bea97223.nq.gz
│   ├── 9561fb1061f6de114633c70871232a6896dcbe8a.nq.gz
│   ├── a523ff4132ae7d1e755a7a0770bfcf964e99dae9.nq.gz
│   ├── a94e417938c6ae7ea68bbffb9510366d218891ce.nq.gz
│   ├── bc0f5224befd732d3f8be6627ecb44dc5ecd44fe.nq.gz
│   ├── c90d382bc7e5d4248f44c014bf02cddab140e646.nq.gz
│   ├── d2e2b036b1e3cd61a31044d3b79c8bfded1699dd.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9b55f05e80809e13b3da9e9dc69416848cbc5fc1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[scrapy-plugins/scrapy-dotpersistence](https://github.com/scrapy-plugins/scrapy-dotpersistence)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
