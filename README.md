# Repolex Knowledge Graph of NousResearch/nousflash-agents

RDF knowledge graph data for [NousResearch/nousflash-agents](https://github.com/NousResearch/nousflash-agents), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/nousflash-agents
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 3ea552f8edbbd2d2d04239db1869538974bf167b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 3ea552f8edbbd2d2d04239db1869538974bf167b
│           └── chunk-001.nq.gz
├── blob
│   ├── 114546a70519dec0f4b04c3bf76390e7ddc8a960.nq.gz
│   ├── 167bbead7c2221e7ac60951e65b2df112da70695.nq.gz
│   ├── 2c0733315e415bfb5e5b353f9996ecd964d395b2.nq.gz
│   ├── 395c2845c56f32159e618347b0ca257c0feeb880.nq.gz
│   ├── 3db7da85d518a63e84be0be6db1575217b032b8d.nq.gz
│   ├── 3eb6d6fdd6a260ef7e1bc610bea315f876473fa0.nq.gz
│   ├── 47b599c2110276fe3aface16c0b7d3501adaa0ac.nq.gz
│   ├── 536e99e55495c0176b689ce13bd9e7262fe4db8f.nq.gz
│   ├── 614e1a16059788a6644ad7ef7d832d9d5d957de1.nq.gz
│   ├── 655b42a06ff3764b2506ea6b45bebb801004fdf5.nq.gz
│   ├── 6897791026465dd30f19248998fe34a7e575fb9d.nq.gz
│   ├── 6fe514dbc0158489e41cbfffd94ed12596d3ffee.nq.gz
│   ├── 736d56620419d2d65300c12efed3e090ed75f9f2.nq.gz
│   ├── 76d8d7bafd74c7b71293b016a4401ca43cc68e53.nq.gz
│   ├── 78bd5bfb781058956dc82b6c6582425b7d9fd7df.nq.gz
│   ├── 8556f77785ba66c6742c95ebdbc3d426626edf99.nq.gz
│   ├── 8ba1b8fcae8d3bdc0695eb91ce6d59e5ea3af483.nq.gz
│   ├── 8d6c93435b2715f0780ee38720126801af40c68b.nq.gz
│   ├── 923eeaf788624bbf9ac12f6ef549ef34f620b604.nq.gz
│   ├── a875f2a73230b0178929ae9d92c1c62ca2774065.nq.gz
│   ├── adef6a24144f2a48c2210ef69ce2ba0097895e44.nq.gz
│   ├── b42a2f36a90503737a97674905a4cf1341e16217.nq.gz
│   ├── b58edffc70572d25c41facb095009b685fd835ab.nq.gz
│   ├── b87d92756049f643b6d25fc57659b4afe0ef68e7.nq.gz
│   ├── bfd2503f958c6cbffc4c6790095722d96190bcd7.nq.gz
│   ├── c845ad7c5414cc618dc286ee3e5808099c9bd249.nq.gz
│   ├── cc1e6d99f4e53866cca52aa860a4b43d243fcbd9.nq.gz
│   ├── d00046bc39756db7434f66d08c1b94cacf4126da.nq.gz
│   ├── e12e265db484221963c2aef77b14043b4e668c30.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f598bf6aa28a6981b758a69d9885dbf560627432.nq.gz
│   ├── fb4ece994023c6a882a436dc2a448084bbda1851.nq.gz
│   └── fc1d4bbcb5164a7c4dcc8d36920086c08f62cee4.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 3ea552f8edbbd2d2d04239db1869538974bf167b.nq.gz
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

[NousResearch/nousflash-agents](https://github.com/NousResearch/nousflash-agents)

---
*Parsed on 2026-10-09 by [repolex](https://repolex.ai)*
