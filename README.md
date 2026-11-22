# Repolex Knowledge Graph of rust-lang-nursery/pin-utils

RDF knowledge graph data for [rust-lang-nursery/pin-utils](https://github.com/rust-lang-nursery/pin-utils), parsed by [repolex](https://repolex.ai).

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
rlex download rust-lang-nursery/pin-utils
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cddb4e490757830eff709310b32376420d7f5e93
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── cddb4e490757830eff709310b32376420d7f5e93.nq.gz
│   └── repolex
│       └── cddb4e490757830eff709310b32376420d7f5e93
│           └── chunk-001.nq.gz
├── blob
│   ├── 06e51c428316389d4bc49d2d27b4f1dedd98b6d9.nq.gz
│   ├── 4308d822046df995d72605f3497d02ae5ae307d8.nq.gz
│   ├── 492c26d9a8de5b85af24ab92c99991101967324e.nq.gz
│   ├── 4b6758dc123827bf24c99002e8ee90bb32f41d2f.nq.gz
│   ├── 4c0617def7a183a5f0407c1720d887dc17338239.nq.gz
│   ├── 6198e9823ae683ed35450ba3bd9f4a39a9963ad8.nq.gz
│   ├── 66ccceda5e2ea70a8eca0de32994828458938129.nq.gz
│   ├── 6af90c56be4a8703e8fa2c00d2b6f090b29587c2.nq.gz
│   ├── 8a1ed2c5af774eef6daad1e74d0667c18c80aa71.nq.gz
│   ├── 93fdeb6fae15d50513c6a548b7af2fef76d9c9e6.nq.gz
│   ├── ba0eb0de0bafd458c10d991f0db9ea355241fcd3.nq.gz
│   └── f25bd51883eda9913a4ba46f60d4d8cabc3fe33c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── cddb4e490757830eff709310b32376420d7f5e93.nq.gz
├── filetree
│   └── cddb4e490757830eff709310b32376420d7f5e93.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 22 files
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

[rust-lang-nursery/pin-utils](https://github.com/rust-lang-nursery/pin-utils)

---
*Parsed on 2026-11-22 by [repolex](https://repolex.ai)*
