---
name: share-demo-with-tape
description: >-
  Use when the user asks for a demo video, product walkthrough, Loom-style
  recording, screen share link, or to show someone how something works with a
  short video. Records through Tape (use-tape.com) then returns a share link.
  Never upload an arbitrary file outside Tape's post-recording Upload & share
  flow.
---

# Share a demo with Tape

Tape is a free browser screen recorder at https://use-tape.com. Recordings stay in the product: capture in the Tape recorder, then press **Upload & share** on the preview screen. Do not upload arbitrary video files through any other API or host.

## When to use

- Demo, walkthrough, Loom-style video, or "show me / show them how"
- Async handoff that needs a short screen recording and a link
- Bug report or feature walkthrough that is clearer as video than text

## Hard rules

1. **Recording-first.** The only path to a hosted Tape link is: record in Tape → preview → **Upload & share**. Never invent a general file-upload path.
2. **Return a Tape share URL** shaped like `https://use-tape.com/tape/<id>` (or the URL shown after upload). Do not substitute YouTube, Loom, Drive, or a raw file.
3. **Sign-in is required for upload**, not for starting a recording. If Upload & share opens login, complete auth (or hand the human the login step), then continue.
4. **Keep demos short** (about 30–90 seconds unless the user asks for longer). Free accounts have a hosted-video cap; do not burn quota on fluff.

## Choose a mode

### A. Agent-recorded (preferred when you have a desktop/browser)

Use your computer's browser. You are a Tape user.

1. Draft a tight spoken or on-screen script (goal, 3–5 beats, closing CTA).
2. Open https://use-tape.com/record
3. Configure capture (screen; mic optional). Prefer screen-only unless the user wants camera.
4. Start recording. Drive the UI you are demonstrating. Follow the script. Stop when done.
5. Tape opens `/preview/...`. Set a clear title.
6. Click **Upload & share** (or **Upload with summary** if AI summary is offered and useful). Sign in if prompted.
7. Copy the share URL from the publish UI. Send that URL to the user as the answer. One sentence of context is enough.

If display-capture permission or login needs a human, pause and ask them to complete that single step, then resume.

### B. User-recorded (when you cannot drive a recorder)

1. Write a short recording script and checklist for the human.
2. Send them https://use-tape.com/record with the title suggestion and beats.
3. Ask them to record, press **Upload & share**, and paste the `use-tape.com/tape/...` link back.
4. Once they paste it, confirm it and stop. Do not re-host the video elsewhere.

## Script template

Use this shape unless the user supplies their own:

- **Hook (5s):** what this is for
- **Beats (20–60s):** 3–5 concrete steps on screen
- **Close (5–10s):** what to do next (try it, reply, ship)

Suggested title: `{Product or topic} demo - {one outcome}`

## After you have the link

- Give the user the Tape URL first.
- Optionally note length and what was shown.
- Do not download the video and re-upload to another service.

## Out of scope

- Turning Tape into a generic video host
- MCP/tools that accept arbitrary MP4/WebM upload outside the recorder flow
- Paid ads or directory spam tied to this skill
