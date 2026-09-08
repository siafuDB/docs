# SiafuDB — Documentation

Mintlify documentation site for [SiafuDB](https://github.com/nyuchi/siafudb) — the embedded graph database for device, edge, and Web3.

This repo holds the docs site only. The database engine itself — the Rust
crates, the sync protocol implementation, the build — lives in
[`nyuchi/siafudb`](https://github.com/nyuchi/siafudb).

---

## The system

**AI is the brain. SiafuDB is the memory. NTL is the nervous system.**

| Component           | Role                                          | Repo                              |
| -------------------- | ---------------------------------------------- | ----------------------------------- |
| AI Agents           | The brain — reason, decide, learn             | Application layer                 |
| SiafuDB             | The memory — hold context everywhere          | `nyuchi/siafudb`                  |
| Graph Sync Protocol | Memory coherence — keep fragments consistent  | `nyuchi/siafudb` (coupled to DB)  |
| NTL                 | The nervous system — neural signal transfer   | `nyuchi/ntl` (separate repo)      |

This site documents SiafuDB and the Graph Sync Protocol. NTL has its own repo
and its own Mintlify site (`http://localhost:11200` in dev).

---

## Structure

The Mintlify manifest is `docs.json`. Four tabs:

- **Documentation** — narrative: Introduction, Core Concepts, Guides, Sync, Governance.
- **Specification** — normative wire-format and transport contracts.
- **API Reference** — Rust crate surface.
- **Research** — the research documents that back the architecture.

Page-level content sits in `introduction.mdx`, `why-siafudb.mdx`,
`architecture.mdx`, `concepts/*.mdx`, `guides/*.mdx`, `sync/*.mdx`,
`spec/*.mdx`, `api-reference/*.mdx`, `governance/*.mdx`, and
`research/*.mdx`.

`research/` and `governance/` also carry a handful of `.md` working drafts
(manifesto, path-forward, decision log addenda) that haven't been curated
into `.mdx` pages yet — they aren't linked from `docs.json` navigation.

---

## Research documents

The core research documents that seeded the architecture live under
[`research/`](./research/):

1. [01 — Architecture](./research/01-architecture.mdx) — Read this first.
2. [02 — Graph Sync Protocol](./research/02-graph-sync-protocol.mdx)
3. [03 — Decision Log](./research/03-decision-log.mdx)
4. [04 — First Steps](./research/04-first-steps.mdx)

---

## Run locally

This site runs on [Mintlify](https://mintlify.com). The dev server is pinned
to port **11300** so it can coexist with the NTL docs site (pinned to port
**11200**).

```bash
npm run install:mint   # once — global install
npm run dev            # http://localhost:11300
```

`npm run build` and `npm run broken-links` are also wired up in
`package.json`.

## Publishing changes

Install the Mintlify GitHub app from your
[dashboard](https://dashboard.mintlify.com/settings/organization/github-app)
to propagate changes from this repo to the deployment. Changes deploy to
production automatically after pushing to the default branch.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for how to propose changes.

---

_Nyuchi Africa_
