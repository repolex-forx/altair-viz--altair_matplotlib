# Repolex Knowledge Graph of altair-viz/altair_matplotlib

RDF knowledge graph data for [altair-viz/altair_matplotlib](https://github.com/altair-viz/altair_matplotlib), parsed by [repolex](https://repolex.ai).

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
rlex download altair-viz/altair_matplotlib
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 531daf18cd71c59fb4690dc09d42d8ff0075a1bb
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 531daf18cd71c59fb4690dc09d42d8ff0075a1bb
│           └── chunk-001.nq.gz
├── blob
│   ├── 0d263e78ea479d4474d4317bba26724b135499f4.nq.gz
│   ├── 104a27fb68063f69cb7eeec529c72ba374bf35f4.nq.gz
│   ├── 22da14ae71520517affef9f6a116c407723c4a24.nq.gz
│   ├── 4e279d348048adcc65ff69cfd3607459f3efbf31.nq.gz
│   ├── 5534f26a795c2b7607b0b24e8f5398611b0bd19b.nq.gz
│   ├── a631063221bd74f247690bde40cd8cfbea174fb5.nq.gz
│   ├── b35f49f1224175b5be0ba9e887b047a2667045d4.nq.gz
│   ├── ca6788bccb39e6a8270d204d3b7abc6d6cd379fd.nq.gz
│   ├── d601206f5bd9c9701c4c765cf581e1ec8efc2ca0.nq.gz
│   ├── daf00172a13551e60dd3690422966ff06a7743f5.nq.gz
│   └── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 531daf18cd71c59fb4690dc09d42d8ff0075a1bb.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 19 files
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

[altair-viz/altair_matplotlib](https://github.com/altair-viz/altair_matplotlib)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
