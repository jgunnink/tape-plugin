# Tape

Record short demos in the [Tape](https://use-tape.com) browser recorder and share a link back in chat.

**For Grok Bot Marketplace.** Install from the Marketplace once listed. This plugin teaches agents the recording-first Tape loop. It is not a Cursor IDE local-plugin pack, and it is not a generic video host.

## What you get

- Skill: `share-demo-with-tape` — triggers on demo / walkthrough / Loom-style asks
- Flow: open https://use-tape.com/record → record → **Upload & share** → return `https://use-tape.com/tape/...`

## Install

Once published: open Grok Bot Marketplace, find **Tape**, install.

Until then (maintainers only): the source lives in this repo. Marketplace listing requires a public repo and submission at https://cursor.com/marketplace/publish

## Product constraints

- Recording-first only. Do not add MCP tools that upload arbitrary MP4/WebM outside the Tape recorder.
- Sign-in is required for upload; recording can start without an account.
- Free hosted-video quotas apply; keep agent demos short.

## Links

- Product: https://use-tape.com
- Record: https://use-tape.com/record
- Share links: `https://use-tape.com/tape/<id>`
