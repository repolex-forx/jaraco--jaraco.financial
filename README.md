# Repolex Knowledge Graph of jaraco/jaraco.financial

RDF knowledge graph data for [jaraco/jaraco.financial](https://github.com/jaraco/jaraco.financial), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.financial
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 59615a2747a7d5405aadef5b380e397051f67ef6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 59615a2747a7d5405aadef5b380e397051f67ef6
│           └── chunk-001.nq.gz
├── blob
│   ├── 0731ebaf01ee257a969e9cac6fd02a44b09f8f46.nq.gz
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 1f2aa7533b0423a8eb943f6f4ec02498e39581a0.nq.gz
│   ├── 21bf77dc0f2babc5ed28cbf80244831308f9b301.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2429dbfada1c104c3a33a6f1d3364b5dd7383db4.nq.gz
│   ├── 2582b35365155dd37b06f3ee4a740a6cbd2f6001.nq.gz
│   ├── 2d571130b05f42a2b6fc71a92866ef734bbad83b.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 32dd9c9c65848f9182da82f7abd030266e4fdcf6.nq.gz
│   ├── 3bc6d6eb2c074c861eddefd23e291e96c314e338.nq.gz
│   ├── 3be1ae3e14d94f4b39a4de80ab0385280fb6b94b.nq.gz
│   ├── 44d1bb84bf101bbbefec84ae60b77fea8ff30884.nq.gz
│   ├── 4d5f29c82f746fa930142bf2dacaff405ea46500.nq.gz
│   ├── 4fb96c368ef8b9caacf853d269c5af1a4b7207bc.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 629bc7cf99cb54187b31833e6fbc66803e3e07c4.nq.gz
│   ├── 6b59fa6464c9cfe705c7fa71c762d2ab2626c430.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 77cae9d7e21baff20033b0254f19cdcc9e6ba92f.nq.gz
│   ├── 881d91702fe4b2953d50f8f0d06e3b0f1addf60b.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── b9e372c8b9fd354ade983e7e7d0176798ec5ab7f.nq.gz
│   ├── cd2373854f5e5e63045f9706fe44d3c1df75a55f.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── efcb8cbc2043faa7caf4f92fc7488bd6914c934c.nq.gz
│   └── f0e31d95c345d228993066374a23345268ff3e5b.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 59615a2747a7d5405aadef5b380e397051f67ef6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
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

[jaraco/jaraco.financial](https://github.com/jaraco/jaraco.financial)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
