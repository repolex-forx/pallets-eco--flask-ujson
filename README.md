# Repolex Knowledge Graph of pallets-eco/flask-ujson

RDF knowledge graph data for [pallets-eco/flask-ujson](https://github.com/pallets-eco/flask-ujson), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-ujson
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1ee3a6489ec0b2ca569a7207aa524e29a7938282
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1ee3a6489ec0b2ca569a7207aa524e29a7938282
│           └── chunk-001.nq.gz
├── blob
│   ├── 0f433a047c73565c67a1eb48cb93c3879215e9a4.nq.gz
│   ├── 1f47f125e5c06e827ba4df75cffd838547a4163a.nq.gz
│   ├── 2ff985a67af35fdfd1076354b771c425867cdab4.nq.gz
│   ├── 35e705c5abf566a1ae72137eeb3fab13e89629b3.nq.gz
│   ├── 39136dbe0f9afd740e4d6073d42ff3e6a6ab16e4.nq.gz
│   ├── 451f557a80df1de5eeac73b599065bc6ade4bf13.nq.gz
│   ├── 4a00a4f8fde1d3c61c9b7a6277c070fca8338264.nq.gz
│   ├── 5c81841587ec3c2bf2610ef89d74105cc29db2fa.nq.gz
│   ├── 5f522c22204b689033f69e581c007bc1e1d73774.nq.gz
│   ├── 670cf591b9921a08138e3ff1d6e2ddbeb702435d.nq.gz
│   ├── 6b79eaa1d6e754caa0986f1f206799c325b95b4c.nq.gz
│   ├── 6d73a0057afd46d520a1e11f19ad5ed9573a60e4.nq.gz
│   ├── 7c303df2bca06f3173492a4eeccaf60b236f5f77.nq.gz
│   ├── 7c6c0f60f131b3fbb31f4cb24691480b7bd3328f.nq.gz
│   ├── 9955160b49d93fee57b3d82637f85e093cdf033c.nq.gz
│   ├── 9f4f26da118ddfd12f5d01ddee79217e378ecb53.nq.gz
│   ├── a2f2a6a06a38b2a6bee8d89345d52531211685ec.nq.gz
│   ├── a6844bd2f2f71d97bc5528276bbc9f58faca2cdd.nq.gz
│   ├── b1079b987d380fd2abd1b2a632a12d91c39bdf3d.nq.gz
│   ├── ca8724c2b000a8f10ed6226311b563fa41bc8673.nq.gz
│   ├── e4d8146b20f9dcc29d566165cce7758710dd775d.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e733308c609f8ff275befd81e36f1385f71cf395.nq.gz
│   └── f5f16af674111ad9786c741979c8d344ff9cb8b2.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1ee3a6489ec0b2ca569a7207aa524e29a7938282.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 31 files
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

[pallets-eco/flask-ujson](https://github.com/pallets-eco/flask-ujson)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
