# Repolex Knowledge Graph of tiangolo/pydantic-sqlalchemy

RDF knowledge graph data for [tiangolo/pydantic-sqlalchemy](https://github.com/tiangolo/pydantic-sqlalchemy), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/pydantic-sqlalchemy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3632b4131723a1899c507654ff56d168e82dd284
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3632b4131723a1899c507654ff56d168e82dd284
│           └── chunk-001.nq.gz
├── blob
│   ├── 0304a29c93f131110fc34b63411962c3fed409fe.nq.gz
│   ├── 0cabf52a9fdf21914814f854f6890bbed6f58c94.nq.gz
│   ├── 1616166966172c49de04a478b4271d86b58c244e.nq.gz
│   ├── 30701a556ba844409e400b69fe6e27ebb3e789b6.nq.gz
│   ├── 31ed1d669e50ea14373bcb00625ba985f911ea81.nq.gz
│   ├── 3aab3e8e9f593ea25b8314d254e04f92577ea350.nq.gz
│   ├── 46960438c51583cda655448b20a3308820823f56.nq.gz
│   ├── 4b595def3556165d0ee048cdeabe45e04bcde579.nq.gz
│   ├── 5369970585dd4ec7bbe506062ebcdfe41834e4b0.nq.gz
│   ├── 5fc5f542be61a8ec27f104a4685be273a6350ebd.nq.gz
│   ├── 65021901413a897bc25e1bfd5de217bce5c7946f.nq.gz
│   ├── 708a5edb956ee39b1e35dfdfa0506f746f297c0a.nq.gz
│   ├── 9018b0c5eec27a9c9e8aed80eb11a10f79626b0d.nq.gz
│   ├── a74e5d218fe186bb274d846f5f37ad4b537cbea8.nq.gz
│   ├── c3b82124b425109d299592400be1fe778529ce3e.nq.gz
│   ├── c94d562277a586c63f96f5e08e85cef15d9b1a4f.nq.gz
│   ├── cd9c10c80eacda37d027a1ebecbc0ff43324541c.nq.gz
│   ├── cf3d68be26ea764d61e205055ef8b7987ee26310.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e911d46056833156059d377937d5f086c0d941cf.nq.gz
│   ├── f5acc59efceb72e47b2fecb093f32cf8a451d896.nq.gz
│   └── ff4b114b186342c2380e790aa54ac24eb506b217.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3632b4131723a1899c507654ff56d168e82dd284.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 30 files
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

[tiangolo/pydantic-sqlalchemy](https://github.com/tiangolo/pydantic-sqlalchemy)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
