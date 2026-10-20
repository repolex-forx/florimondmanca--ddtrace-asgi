# Repolex Knowledge Graph of florimondmanca/ddtrace-asgi

RDF knowledge graph data for [florimondmanca/ddtrace-asgi](https://github.com/florimondmanca/ddtrace-asgi), parsed by [repolex](https://repolex.ai).

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
rlex download florimondmanca/ddtrace-asgi
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 78936f2556dc3df906d40fcf78a2e64907eb301f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 78936f2556dc3df906d40fcf78a2e64907eb301f
│           └── chunk-001.nq.gz
├── blob
│   ├── 087d0f409e021114791dbcd3a41af8fc85ae6197.nq.gz
│   ├── 0b403d45910a57275ad800c75cb0a536379e8953.nq.gz
│   ├── 1fad16c84df706c0ad25c4d588cc36ab9e4cc39d.nq.gz
│   ├── 20a518d0fb82b72435a59bbda31d039bb77c9e1d.nq.gz
│   ├── 2330fabe983b0741a74e32b97fd0f09fb71363a0.nq.gz
│   ├── 274f6896b36e6a88d0c3435fae777e5c901dcd15.nq.gz
│   ├── 2804cd087a54901865c3f48385ad0655f482fbf3.nq.gz
│   ├── 2a0fa6f263f1aa0934c9a9b454979fdf991c0d71.nq.gz
│   ├── 2cc5bd783fb9f0d7e15c5d69ec1abd3338f287c4.nq.gz
│   ├── 2d0fca20057f7115f2f80c1133e8eab7403c3a90.nq.gz
│   ├── 2e57062ba819754b672dbda363d781bbfda70c45.nq.gz
│   ├── 3ea4282d3fe5aaff3c84522dad3c6eb9125333c6.nq.gz
│   ├── 48fe2425c2dbdaabb947c52ded210db7c5046779.nq.gz
│   ├── 493f7415d73d5d2a0875222a1c7296000935cccc.nq.gz
│   ├── 4c83a27d20d001fdfa6b43396e13636e8497e067.nq.gz
│   ├── 58b49e22f79ad9316b3719a376ee208c62a2944d.nq.gz
│   ├── 5acb967006c2d1fbb938c136c4a20ad1e027c1c6.nq.gz
│   ├── 679176148946b7b762884670a4e97c1e5e4436a6.nq.gz
│   ├── 6f781f7bd511af69a73819eb93ac74c831685106.nq.gz
│   ├── 77631041cd7f4aa35c9459432f36f0a541b794d6.nq.gz
│   ├── 7a9170392a5b78140984de1b7cb90bdd7fb472db.nq.gz
│   ├── 7bcc099c55f98c7c1395e8eb5e4c3e40153da225.nq.gz
│   ├── 7fa5dc1189412370630926b2f87535ae796936df.nq.gz
│   ├── 7fce5120081391676164e6efd478d7c2dcf01875.nq.gz
│   ├── 824653fbda4999bc7f58b8686c0410c3098a0ace.nq.gz
│   ├── a0fd7e63c0fe45a23833743cbb9a873e738f7656.nq.gz
│   ├── a99e571269f0ea376871f43f3c9663bd22051531.nq.gz
│   ├── ad5d51c65386aa018a9e240df941aa9a8671ec4b.nq.gz
│   ├── b3ad1650abaf52fd272b3b2ca346ffe2422c539d.nq.gz
│   ├── bb605f2a37e630b910454c333f5f2011bfbb430a.nq.gz
│   ├── e5e9170f81aa0b213a434f80fd5fefc315f3af36.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ee460848d7010070a5da0a12d06a0e0808a66bb1.nq.gz
│   └── fc4312483e18393484878b597566f1eb28e1b3f8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 78936f2556dc3df906d40fcf78a2e64907eb301f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 42 files
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

[florimondmanca/ddtrace-asgi](https://github.com/florimondmanca/ddtrace-asgi)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
