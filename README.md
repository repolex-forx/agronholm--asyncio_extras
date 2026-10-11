# Repolex Knowledge Graph of agronholm/asyncio_extras

RDF knowledge graph data for [agronholm/asyncio_extras](https://github.com/agronholm/asyncio_extras), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/asyncio_extras
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 6ac3aa38e219bef6eeb6752f0ff7f0d3417bd8d6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 6ac3aa38e219bef6eeb6752f0ff7f0d3417bd8d6
│           └── chunk-001.nq.gz
├── blob
│   ├── 07806f8af9dd3253ebdb5710b67e73124aea4941.nq.gz
│   ├── 1b94c9fedb96872a98436178f46fa0fe2af2dbcd.nq.gz
│   ├── 1c231e1dc130969c2795a5f3360b783bc73c2327.nq.gz
│   ├── 204a1ecc7ad1cca528965174c9585b19b0fe16ea.nq.gz
│   ├── 256347fac50dcd160b068987907f54e8b65e5880.nq.gz
│   ├── 375782a3f771b4b1cb6184d73070c246cd0f8483.nq.gz
│   ├── 3ac073faba2a4a6ff24f47ccb03c556dc1f81ff3.nq.gz
│   ├── 4822290dd6228b8f202c58b760b39b825cf8112b.nq.gz
│   ├── 4924268239da102dac49d47ae1941a787b3a8923.nq.gz
│   ├── 4a976d8edf53beaa5010b92b9b41f5d757f9b806.nq.gz
│   ├── 5118260222e08f374592759a3684504e5ce32117.nq.gz
│   ├── 580159d717392dfd0fb497f4433ae7d3ac466c16.nq.gz
│   ├── 5ca06cfd7bd53ac46d5a0bc80fe064d4916a6bf7.nq.gz
│   ├── 64f5d9ae87cb55ed30a573d6e4578aab89145360.nq.gz
│   ├── 7e9522afbff90a7f584eba474d127457f7f01c8c.nq.gz
│   ├── 90957e85026b3f9f173a52df84d9f8a7f85ca3e0.nq.gz
│   ├── 95b48accaf6ab7cca1bf1eb6f729f62708e4d0ee.nq.gz
│   ├── a3cd2aeced9fba1fd834cae2cf8bf443510b0ea5.nq.gz
│   ├── b86efb6d45ea70a21e24d66092f236be839696cb.nq.gz
│   ├── dc85a5bddc12cda76824c7fc09b9c2f38c6fa911.nq.gz
│   ├── e2603d5011e3739d68172c7adaf1e19725e033f4.nq.gz
│   ├── e4118d029b5c28b4334b7ef29f305bb88f381bba.nq.gz
│   ├── e74a48674080a71887b7ca55dc2075d5e13ace8a.nq.gz
│   ├── edcf44f39deaef9a05f3c1826da69ac2a3444270.nq.gz
│   ├── f0e710daf401e7cc39a24814534c4ac74634d363.nq.gz
│   └── f537bbaeef7774dfe88f4f269dc776e051eca234.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 6ac3aa38e219bef6eeb6752f0ff7f0d3417bd8d6.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 33 files
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

[agronholm/asyncio_extras](https://github.com/agronholm/asyncio_extras)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
