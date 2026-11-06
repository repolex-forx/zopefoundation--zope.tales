# Repolex Knowledge Graph of zopefoundation/zope.tales

RDF knowledge graph data for [zopefoundation/zope.tales](https://github.com/zopefoundation/zope.tales), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.tales
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 24559529fabec400b984f1c2dfe0cf9cb4ec9a86
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 24559529fabec400b984f1c2dfe0cf9cb4ec9a86
│           └── chunk-001.nq.gz
├── blob
│   ├── 0a43f5b335cf664cb26b98c15b0a2fea95587a25.nq.gz
│   ├── 22b6ee69cbd371e43a9c87e1f874de479cb255dc.nq.gz
│   ├── 2596a596db536ea35996d5d7cabb3da57d8bb7d0.nq.gz
│   ├── 3072dbbd819b29f8e9e224aa0ddd835544f476ad.nq.gz
│   ├── 3441583325e24756102a9f491840d121faa57b3f.nq.gz
│   ├── 40f247ee0f818f66e4ada7dd40a27554a79c9a99.nq.gz
│   ├── 41e755f0ddcd0a089e9e8d4c303c6c72477a1b71.nq.gz
│   ├── 42814686e6d8116896f4bf6d4d0dd63e6d06dd7f.nq.gz
│   ├── 47e4068cb6b319aea4ccc380d8d2fa30581ae88d.nq.gz
│   ├── 4fceededc076d99e16426f0d4707c9234ea622a2.nq.gz
│   ├── 500c4d55d6236996f2e063c48ca87fc7cc327670.nq.gz
│   ├── 56fecdb72a75c4118ba880431beb7a936ff2cef0.nq.gz
│   ├── 6a80713284949c320ae23f32703e1018ecbc7e20.nq.gz
│   ├── 6d6a34893eae9f3fd68eec42dee844757db3a505.nq.gz
│   ├── 6ed54955d2cef0130db6605a1486cbe799a037fc.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 84119779b56ab0ccef344b199ef27abc637d2ae0.nq.gz
│   ├── 8a1cde635fcfe005cc4438d504940505395236a7.nq.gz
│   ├── 90a9269b242fae451d7d6b4445f27eb573d1b599.nq.gz
│   ├── 98bbd297ebe7a3e97a0b59bb0608aaee0f7eef37.nq.gz
│   ├── 99b105bc0b3d45188942c09d34aa8e3c362873be.nq.gz
│   ├── a04a3b47ba0b57f3f79d85b821ae919451145c0a.nq.gz
│   ├── abece1152df97fbd8a18fb78e03143bfd4582344.nq.gz
│   ├── ac22f4a4fa277989bf4b0df47786b8f609443cb9.nq.gz
│   ├── b10b7874b96711d8810ef881d09b72d63b255c8c.nq.gz
│   ├── b46b7751426a044cf26954c3f9a1c2d1423fa345.nq.gz
│   ├── bae6ac8642bd75d899a12116673962cfe428548b.nq.gz
│   ├── ca517f4eb0cec1c691c0c2b54cd5eb85e906f11b.nq.gz
│   ├── cc7999d0808a0f52d8c5796d11c1ed39ca15fb3d.nq.gz
│   ├── ccf848bb4e419680f4bf9ab9647596f2135ebe70.nq.gz
│   ├── d1256c9bc91630da4e80bfe8efbfe03d9da8518d.nq.gz
│   ├── d9e113ec685b92b018297dd2f200341d1fba01f9.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e4b867329e05886a4818f86b117fca2102bc84bf.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb4f53b6e4eaaa1d4062bf1b40c4100d4afb388b.nq.gz
│   ├── f3c95fd768dac9192940ce1cee6790d7b326db4a.nq.gz
│   ├── f81cabf053fb4487bb3496afbc276556076bc3f2.nq.gz
│   └── fea8ebb371a8008f598ad99a1fccf55a06cafa88.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 24559529fabec400b984f1c2dfe0cf9cb4ec9a86.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[zopefoundation/zope.tales](https://github.com/zopefoundation/zope.tales)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
