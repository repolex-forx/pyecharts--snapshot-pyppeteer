# Repolex Knowledge Graph of pyecharts/snapshot-pyppeteer

RDF knowledge graph data for [pyecharts/snapshot-pyppeteer](https://github.com/pyecharts/snapshot-pyppeteer), parsed by [repolex](https://repolex.ai).

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
rlex download pyecharts/snapshot-pyppeteer
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c8548d598a6288ac62bf48395eac95b1ca70d49e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c8548d598a6288ac62bf48395eac95b1ca70d49e
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ef128ad438a1fff5c5e6ebadc34b29874edf1f9.nq.gz
│   ├── 0f20b95c086eb09c8e10dd0a5a1388858cef9057.nq.gz
│   ├── 15762a07145bd47abb7950c05ded814b59f9528b.nq.gz
│   ├── 19d2c12b0b10275d1a840a806159c701d7e8576e.nq.gz
│   ├── 290e6269e3e809b37eae61b1ebbc34f9f03bb1e2.nq.gz
│   ├── 29148b46e779daaeadf978ee96011d6e627b661a.nq.gz
│   ├── 3e5eab01a6997e32c181e8e5f774d28ac1b7c321.nq.gz
│   ├── 90f6b5f0f53e73309d4041c1a6bef87504469660.nq.gz
│   ├── acffef63c216d01ccedcf99f163a07d9e6237dae.nq.gz
│   ├── b49747e31f180bfcfdf43f52e85abf2538ea3677.nq.gz
│   ├── c1a09918eae938f84c8e36ec71565f4a2b0678bc.nq.gz
│   ├── ce3ef3db2396ab8d9b9ce2c6949b090b9f74ac22.nq.gz
│   ├── e67a9e01c56cff5c0d6ed7b5c729ff82c60042d5.nq.gz
│   └── f2b8f9b14027623c694c7eb36a00d47676c169a5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c8548d598a6288ac62bf48395eac95b1ca70d49e.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 21 files
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

[pyecharts/snapshot-pyppeteer](https://github.com/pyecharts/snapshot-pyppeteer)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
