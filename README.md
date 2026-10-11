# Repolex Knowledge Graph of pytest-dev/pytest-snap

RDF knowledge graph data for [pytest-dev/pytest-snap](https://github.com/pytest-dev/pytest-snap), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-snap
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 08ec8a95bf188cfe9abd699a58c1a830f4db0f6b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 08ec8a95bf188cfe9abd699a58c1a830f4db0f6b
│           └── chunk-001.nq.gz
├── blob
│   ├── 00abefb75a19e2d68faa25f6e9602c38f0b30471.nq.gz
│   ├── 1cb2e8deb55f5a5a7c63a5acc519d23f6727d961.nq.gz
│   ├── 2f4811caafb888420cc2ee9b30b1e445673007d2.nq.gz
│   ├── 36c01418ac9fe47865629d093ab05c311f27f63c.nq.gz
│   ├── 385e48e26968306691f5bdd0bb5c346c018d76fd.nq.gz
│   ├── 3af011c1fd175bfa55a95f5046cc853bf4252eb9.nq.gz
│   ├── 41b3c07eafaef873ce3d0e848695d52cab2d402b.nq.gz
│   ├── 467d65e56eebd99c0aafbfb8a4e5aae94b86dbfb.nq.gz
│   ├── 4f9c4ae0a95587326ca7b3ceafe8c5edd8d77cfb.nq.gz
│   ├── 65d5c165c38c6155155e91a924b5a4833fd8a8f0.nq.gz
│   ├── 814974035ed72ca66efd19e996c13f92686421aa.nq.gz
│   ├── 88979ea0c98701a163582d9f566ddc8f711c31fc.nq.gz
│   ├── 89ce2ca14b8feeef15c2cfb47b266dd0c608a5e7.nq.gz
│   ├── 8bab5bcf2c20149d99377c5ef602cda0b7fb567b.nq.gz
│   ├── 9867bb90701b24cad633aa613929dd9d98a1d6e4.nq.gz
│   ├── 9b673f0bb4d6b95f9e972805e4157a08e1d9effe.nq.gz
│   ├── a86b6c596ccb2a7ffbe16eb1dede334acea68e79.nq.gz
│   ├── ba53f2d2619f708e8976738c064b284c7c57d9ba.nq.gz
│   ├── c0bc1d5f4fe8aa8ad8f052220df33743d23a1356.nq.gz
│   ├── d0e07edbdae0db2f6b3c909c0e45edde27ec140c.nq.gz
│   ├── dc177a831300e21b37aab538ad484cbdc792b27e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ecddd16570ee3874c97ff30c477460ee459dc1f2.nq.gz
│   ├── eea2c180278f7b2bc64449bc2dce8d07e3856af1.nq.gz
│   └── fcacee83e21edbecd5e463742adf552328a3260f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 08ec8a95bf188cfe9abd699a58c1a830f4db0f6b.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 32 files
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

[pytest-dev/pytest-snap](https://github.com/pytest-dev/pytest-snap)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
