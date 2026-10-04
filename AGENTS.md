# Documentation project instructions

## About this project

- This is the documentation site for [SiafuDB](https://github.com/nyuchi/siafudb),
  built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` (or `npm run dev`) to preview locally, on port `11300`
- Run `mint broken-links` (or `npm run broken-links`) to check links
- The database engine itself does not live here — see
  [`nyuchi/siafudb`](https://github.com/nyuchi/siafudb)

## Terminology

- **Fragment** — a SiafuDB instance; a meaningful subset of a larger graph,
  not a shard or a partition
- **Authority** — whether a vertex is `authoritative` (source of truth here),
  `referenced` (source of truth elsewhere), or `local` (never synced)
- **Graph Sync Protocol (GSP)** — the CRDT-inspired sync protocol between
  fragments; GSPA is the transport-agnostic wire spec, GSPN is the
  network/transport layer
- **NTL** — a separate, related project ("the nervous system"); it has its
  own repo and its own Mintlify site. Don't conflate NTL docs with SiafuDB
  docs.

## Style preferences

- Use active voice and second person ("you")
- Keep sentences concise — one idea per sentence
- Use sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, and code references

## Content boundaries

- This repo documents SiafuDB (the database) and the Graph Sync Protocol.
- Don't document NTL here — it has its own site.
- `research/` and `governance/` contain some `.md` working drafts not yet
  linked from `docs.json` navigation; treat those as source material, not
  finished pages.

## Track big work in GitHub issues

Any substantial build, migration, investigation or multi-step task gets a GitHub
issue in the repo that owns it — before or as work starts — so another session,
agent or person can pick it up.

- The issue holds the goal, the owner's decisions (verbatim where given), the
  plan, acceptance criteria, owner-only steps and links.
- Every PR references its issue (`Refs #n`; `Fixes #n` only when the merge
  completes it).
- Post progress, decisions and a hand-off note (what's done, what's left, branch
  names) as issue comments — at each merge and before a session or agent
  finishes.
- Work spanning repos gets a tracking issue that links the per-repo issues.
- Never put secrets, credential status or exploitable detail in issues on public
  repos.
