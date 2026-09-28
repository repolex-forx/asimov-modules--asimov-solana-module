# Repolex Knowledge Graph of asimov-modules/asimov-solana-module

RDF knowledge graph data for [asimov-modules/asimov-solana-module](https://github.com/asimov-modules/asimov-solana-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-solana-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5868590dfc8776b5e6729f5b3f03859802403f17
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 5868590dfc8776b5e6729f5b3f03859802403f17.nq.gz
│   └── repolex
│       └── 5868590dfc8776b5e6729f5b3f03859802403f17
│           └── chunk-001.nq.gz
├── blob
│   ├── 0ce7e79e0b4754b41a1ee28ef7687b7c0d572637.nq.gz
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 2909c66eccf5beabe5811487516cc8f17b5cc246.nq.gz
│   ├── 4b02198285c4c8ca236c0c045b9dc63595926e47.nq.gz
│   ├── 4e379d2bfeab6461d0455bf5bbb8792845d9bbea.nq.gz
│   ├── 66ec7c8820cb0bae04644a13893bb698771327be.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7a5c0437ad958635b15d5c43e768cbc46aaee38d.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── aae9bf091c6b579e543599c77a707e9338e68f2f.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── bf8ee3c1bfd42766c167fefb6d4f541935fe0e0e.nq.gz
│   ├── cc69eed9ef77a78053a05941e3e07b1911195afe.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 5868590dfc8776b5e6729f5b3f03859802403f17.nq.gz
├── filetree
│   └── 5868590dfc8776b5e6729f5b3f03859802403f17.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[asimov-modules/asimov-solana-module](https://github.com/asimov-modules/asimov-solana-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
