# Tape

Grok Bot Marketplace plugin for [Tape](https://use-tape.com): record short demos in the browser recorder and share a link in chat.

**Recording-first.** Agents capture at `/record`, land on preview, then press **Upload & share**. This is not a generic video host and not a Cursor IDE local-plugin pack.

## Package

- Skill: `share-demo-with-tape`
- Layout: Agent Plugins root `plugin.json` plus `.cursor-plugin/plugin.json`
- Source: https://github.com/jgunnink/tape-plugin (private until Marketplace submit)

## Install

Once listed: install **Tape** from the Grok Bot Marketplace.

Marketplace listing needs a public repo and a submit at https://cursor.com/marketplace/publish. Keep this repo private until you are ready.

## Verified agent flow

1. Open https://use-tape.com/record (screen-only preferred)
2. Record the demo (30–90s)
3. On `/preview/...`, title the clip
4. Click **Upload & share**
5. If signed out: email magic link → user pastes the Firebase sign-in URL → finish auth → upload
6. Return `https://use-tape.com/tape/<id>`

## Links

- Product: https://use-tape.com
- Record: https://use-tape.com/record
