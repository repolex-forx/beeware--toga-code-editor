# Repolex Knowledge Graph of beeware/toga-code-editor

RDF knowledge graph data for [beeware/toga-code-editor](https://github.com/beeware/toga-code-editor), parsed by [repolex](https://repolex.ai).

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
rlex download beeware/toga-code-editor
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── d5bd0d2bbeb691b1ef6ca11f76b31b2ec29c0549
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── d5bd0d2bbeb691b1ef6ca11f76b31b2ec29c0549
│           └── chunk-001.nq.gz
├── blob
│   ├── 04b4603c9f90a65a2f18a2533262b8e4592fa334.nq.gz
│   ├── 260ae8939294cf7b1d67248711ee1460f7910ece.nq.gz
│   ├── 31d356468c0d1a6e37fa7965da103fe84fb5eb66.nq.gz
│   ├── 33fa3a57009daf340a5ddbf476cd6478fc28e0a5.nq.gz
│   ├── 35903290642b75459ef3f839c08f336e06810440.nq.gz
│   ├── 36c24e050c84eb596d773eb96564fca34a80b7ce.nq.gz
│   ├── 381bbda87debd272f19babb8267681cb792ea273.nq.gz
│   ├── 3b3e7df7864281be7e3703c929373642d4b8b4fb.nq.gz
│   ├── 3c178d36b49c29b7ed456dd1280e1dbd2c122a62.nq.gz
│   ├── 3cecf91bcf8db72561261a65ae0570b4ef75ee67.nq.gz
│   ├── 4a09c81e23ca735b7d235c71f9ed7feca8081af3.nq.gz
│   ├── 4d2e0ef8c18b578c92e1028f96f3abd00338b367.nq.gz
│   ├── 606e5970fdc32ba7366b86165bea5e7ba72a9a1b.nq.gz
│   ├── 6ad9d3df36fd51b5ebbb9aa8cebfa3f0c6da8cb4.nq.gz
│   ├── 73cfa57a72cbbf57120c8c0e19901105e811b262.nq.gz
│   ├── 819433657150aac87e7b599b1a0a2a564af1161d.nq.gz
│   ├── 85b9269631ae91558dedfb932f9cdf7702efa180.nq.gz
│   ├── 89ac4aa81c09cfcfd426932148bb32927ec1c8bd.nq.gz
│   ├── 8a47800c21efa1c0d03ffd07b7085563d6704a8e.nq.gz
│   ├── 8d8607106aab9bfd0dc041d778a940e777ad9c74.nq.gz
│   ├── 9ae7908414f69646e3f7b9f5d45f1c6fa6a700f8.nq.gz
│   ├── a56ea99557123a2c34bac495b4c4a7b08924575a.nq.gz
│   ├── a7dc0fb9043100d19977c8e42ae8b0e4e6378294.nq.gz
│   ├── a95bb95a6684b3e141616cc072e22d7561e7cdb3.nq.gz
│   ├── aa1886a880a071d0eb6cd93cea0f92f0a10ada4a.nq.gz
│   ├── b834affdddcf5014398ca9c16aafe3ea7f2d0422.nq.gz
│   ├── bf2778c4e05ff0e45f0391c4762dadc349420f00.nq.gz
│   ├── c4d88e8173e484996f9c1fe716bd0fb7e4c8a73b.nq.gz
│   ├── c687e8280ca40008e565760e2e2637ac2d248308.nq.gz
│   ├── ca58e9938a776d3dabc4299a25c0c22a53002fd9.nq.gz
│   ├── d19b03b9eec5c154173258432f98824b593cb01a.nq.gz
│   ├── d1b4cfbe378cc00af0322e621868b844a55c3077.nq.gz
│   ├── d758d206c12385b948269df13985fa534d6586f2.nq.gz
│   ├── da21578e6b85de515321013a098567d94405f6db.nq.gz
│   ├── df9b521321f90f3bd035abae45695dff60f50018.nq.gz
│   ├── e2102679a0ad2deab70a67a85f0aad7b6662aaed.nq.gz
│   ├── e4663db6bd4a014fb99e45923f7d32e0ba687c49.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f6bfb68df22c214658ccfff546f752052c6682ed.nq.gz
│   ├── f9444e78baca03399ff7d45202e01becd21360ce.nq.gz
│   └── fd0cbd6b27e9cb75a47100df2b372370126d0d5f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── d5bd0d2bbeb691b1ef6ca11f76b31b2ec29c0549.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[beeware/toga-code-editor](https://github.com/beeware/toga-code-editor)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
