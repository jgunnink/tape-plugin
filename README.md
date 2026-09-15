# Tape for Cursor

Record short demos in the [Tape](https://use-tape.com) browser recorder and share a link back in chat.

**Recording-first.** Tape is not a generic video host. Agents (and humans) capture in the Tape recorder at `/record`, then press **Upload & share** on the preview screen. This plugin teaches that loop. It does not add an arbitrary file-upload API.

## What you get

- Skill: `share-demo-with-tape` — triggers on demo / walkthrough / Loom-style asks
- Flow: open Tape → record → Upload & share → return `https://use-tape.com/tape/...`

## Install (local test)

1. Clone this repo (or copy the folder).
2. Symlink or copy into Cursor local plugins:

```bash
mkdir -p ~/.cursor/plugins/local
ln -s "$(pwd)" ~/.cursor/plugins/local/tape
```

3. Reload Cursor (or restart the agent window) so the skill appears.
4. Ask: "Record a 45s demo of X and share a Tape link."

## Marketplace

Submit this repository at [cursor.com/marketplace/publish](https://cursor.com/marketplace/publish) when ready for review.

## Product constraints

- Do not add MCP tools that upload arbitrary MP4/WebM outside the recorder.
- Sign-in is required for upload; recording can start without an account.
- Free hosted-video quotas apply; keep agent demos short.

## Links

- Product: https://use-tape.com
- Record: https://use-tape.com/record
- Homepage for share links: `https://use-tape.com/tape/<id>`
