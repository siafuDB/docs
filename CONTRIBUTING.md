# Contribute to the SiafuDB documentation

Thank you for your interest in contributing to the SiafuDB docs! This repo
holds the documentation site only — for the database engine itself, see
[`nyuchi/siafudb`](https://github.com/nyuchi/siafudb) and its own
`CONTRIBUTING.md`.

## How to contribute

### Option 1: Edit directly on GitHub

1. Navigate to the page you want to edit
2. Click the "Edit this file" button (the pencil icon)
3. Make your changes and submit a pull request

### Option 2: Local development

1. Fork and clone this repository
2. Install the Mintlify CLI: `npm i -g mint`
3. Create a branch for your changes
4. Make changes
5. Run `mint dev` (or `npm run dev`) at the repo root
6. Preview your changes at `http://localhost:11300`
7. Commit your changes and submit a pull request

See [README.md](README.md) for more on how this site is structured.

## Writing guidelines

- **Use active voice**: "Run the command" not "The command should be run"
- **Address the reader directly**: Use "you" instead of "the user"
- **Keep sentences concise**: Aim for one idea per sentence
- **Lead with the goal**: Start instructions with what the user wants to accomplish
- **Use consistent terminology**: Don't alternate between synonyms for the same concept — a SiafuDB instance is a **fragment**, not a "shard" or a "partition"
- **Include examples**: Show, don't just tell

## Code of conduct

This project follows the SiafuDB
[Code of Conduct](https://github.com/nyuchi/siafudb/blob/main/CODE_OF_CONDUCT.md).
