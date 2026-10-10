# Repolex Knowledge Graph of marshmallow-code/flask-marshmallow

RDF knowledge graph data for [marshmallow-code/flask-marshmallow](https://github.com/marshmallow-code/flask-marshmallow), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/flask-marshmallow
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 9a83bbc1372f4b49b251cfff75a91d65d7a551c8
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 9a83bbc1372f4b49b251cfff75a91d65d7a551c8
│           └── chunk-001.nq.gz
├── blob
│   ├── 0e9383073bf197c83abf5e07857165b0f60c5dba.nq.gz
│   ├── 1005e265973ba976766d336b6c043d066e663d6e.nq.gz
│   ├── 17ec4274c4b3c8cde62ce5d4bfce5e91d6ff4ecd.nq.gz
│   ├── 18c720f804c6f034cdb1ee02a616cc1e271a4007.nq.gz
│   ├── 1b6c53b23633cb43ab6f045e6ed2c5893246975f.nq.gz
│   ├── 1c7845966f7fe345360c02410483dd7841c4e61a.nq.gz
│   ├── 1cd51f4c0ef30378fe02e43e8b730eb14c8af26f.nq.gz
│   ├── 2b4476477fe314cdf9e221f94cecc0727f32d8c9.nq.gz
│   ├── 30e82e4854f44bfab3194e814673e92c167afb5c.nq.gz
│   ├── 47fda2cbbd070ca3bc8e0e412535a70958d8c3d0.nq.gz
│   ├── 4aa3a5892f8c5af4965e8c21d4ab2184e43a7222.nq.gz
│   ├── 5156479c46c663fccbec2f5786eab962de684449.nq.gz
│   ├── 5906e751b7a9c21a5c295e3779b0fbe7541c02cb.nq.gz
│   ├── 60e27a7399e070d37c9377ea22c710da9455d3b8.nq.gz
│   ├── 64e249963b3af1a2c7db7c323f7add378b188fe8.nq.gz
│   ├── 696259b1e382706e3d1f53b3771ebad1f4696014.nq.gz
│   ├── 69c068035ca206709aab74d5c3ea3b8cdd2fbcef.nq.gz
│   ├── 76888fe1bf10912f9575845efabb510921743065.nq.gz
│   ├── 80345496491686b874f0403a0d176b162d3c8ddf.nq.gz
│   ├── 8daab7ee6efe3b6f3c2a2594b711e7a9026eb5e2.nq.gz
│   ├── 9d94833aa36a2e19b89cfb9dd57d7843247ade5c.nq.gz
│   ├── 9e8f8744746829c9d90a52643b11f25cc2759da8.nq.gz
│   ├── a7da623e512495136eca4e76935337024e43e597.nq.gz
│   ├── b20df7cab259cfce3d02bd8da515ce65870612b7.nq.gz
│   ├── b3292bdff8ed5429eedd7f409839979d408beb6a.nq.gz
│   ├── b7841a3e1b42a709e4940e6dda07d1d46b8cdba8.nq.gz
│   ├── bb70d93ec8266a9e4eb9adf5dc3ff6d7d7ea332f.nq.gz
│   ├── d54a2081fac6efd5df17a3fd7e3a11a8a03a03c5.nq.gz
│   ├── e399a02bb5165d0b2c0410214d1c7aed7e187f63.nq.gz
│   ├── e5c9481ec503da8131d75cafd3d8b90936433977.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f40ce91be5fa3ae6afbf5457462f0d87000e4f1b.nq.gz
│   ├── f726d829e6318faa7835d08487b3908ce42e038a.nq.gz
│   ├── f93993586eae95df3a8fc4a9e97b5755087e6316.nq.gz
│   ├── f9dde0b4e75cbd5d19f499ff8631d42a96715d5b.nq.gz
│   ├── fa07e9e9a0a642238290e1e531c015e7134401fa.nq.gz
│   └── fa9759a4bd3a4aec03ab589b54511917f4400c8a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 9a83bbc1372f4b49b251cfff75a91d65d7a551c8.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 45 files
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

[marshmallow-code/flask-marshmallow](https://github.com/marshmallow-code/flask-marshmallow)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
