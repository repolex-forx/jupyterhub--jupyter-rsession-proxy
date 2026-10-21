# Repolex Knowledge Graph of jupyterhub/jupyter-rsession-proxy

RDF knowledge graph data for [jupyterhub/jupyter-rsession-proxy](https://github.com/jupyterhub/jupyter-rsession-proxy), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/jupyter-rsession-proxy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 2bc193994d6167f356c6878afe09b1c923b01575
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 2bc193994d6167f356c6878afe09b1c923b01575
│           └── chunk-001.nq.gz
├── blob
│   ├── 0dc89813dc10ed07777226c26d348a19ce3afb93.nq.gz
│   ├── 1aba38f67a2211cf5b09466d7b411206cb7223bf.nq.gz
│   ├── 435269a5a404ff2f8f0807029cfe2f11c42ccc4e.nq.gz
│   ├── 4f0bd70ceb4b27813576df3db7d43af2b3d225ea.nq.gz
│   ├── 5fb0eea12b7bf9510ef6eeac0f646a63b76ae5e1.nq.gz
│   ├── 7039f580a174a2e1d9eebe9f1f569f7dd427fd63.nq.gz
│   ├── 8183238ab1c7f1b7f360cd8536d5f4f75e3fe170.nq.gz
│   ├── 8d34bf0659e125f777c98cf96b58f11b755c5bef.nq.gz
│   ├── 919c332a5b20956aa32cce51ca02071ccbd6de4b.nq.gz
│   ├── a76395562314b661b2598f377b47fb2c5ab9a60a.nq.gz
│   ├── afbb405a82ee810e59585d9615641c989ec5fc30.nq.gz
│   ├── b225f13d71163050fbdcf419dbd79bfb8713ad8c.nq.gz
│   ├── b3b247639b2b6e06864f0f95931c17e03017e3c5.nq.gz
│   ├── bee8a64b79a99590d5303307144172cfe824fbf7.nq.gz
│   ├── c8334f524bcf1d2d00d41cf718cab9f05951b224.nq.gz
│   ├── d5994dae4f32ac7d59766b17e6824d0d88f08049.nq.gz
│   ├── f4657e0397d13196c6c31c0b1d2480666b6ce4ee.nq.gz
│   └── fc7d336a17be1f096f0726e472140a8a320c9fbb.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 2bc193994d6167f356c6878afe09b1c923b01575.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[jupyterhub/jupyter-rsession-proxy](https://github.com/jupyterhub/jupyter-rsession-proxy)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
