---
name: ghostwriter
description: "Use when the user wants an AI to draft social posts in their voice."
---
# Ghostwriter

Draft social posts in the user's voice. The user posts. You never publish.

## When to use
The user wants a post, thread, or reply drafted from a link, some raw text, a voice note, or a topic.

## Setup (ask once, then reuse)
Keep a short **style notes** file, for example `style-notes.md`. Build it from the user's 10 to 20 most recent original posts. Skip replies and reposts. It holds:
- A few do's and don'ts: casing, line breaks, whether handles should be clickable, words or punctuation they dislike, tone.
- **Signature moves:** openers, closers, recurring formats, slang.
- The 3 to 5 newest shipped examples (your draft vs what they posted, or the final text). Drop the oldest when you add a new one.

Do rules and signature moves get one real example from the user's posts. Don't rules say where they came from (the user's correction or a clear pattern). Keep the style of main posts and the style of replies apart. If the user wants replies drafted too, also read about 10 of their recent replies and mark those rules "(replies only)".

If the file does not exist yet, draft a first pass and ask them to confirm it. Wait for their confirm before you write the first draft. If you can't read their posts (no X access), ask them to paste their recent original posts (10 to 20 if they can).

Also keep a **drafts log** file, `drafts-log.md`. For each post it holds:
- The original draft, word for word.
- Each change, tagged by who made it (you at their request, you after a fact check, or the user's own edit).
- The final posted text, word for word, with date and link.

When you offer 1 to 3 options, log the option the user picks as the original draft. In step 5, back up the current draft here before you change it, and log each change tagged by who made it (you at their request, you after a fact check, or the user's own edit). When they post, add the final text with date and link. Export history reads from this file.

## Flow

### 1. Intake
The user sends a link, raw text, a voice note, or a topic. If the request came through voice transcription, read garbled names or phrases from context instead of literally.

### 2. Read the style notes
Open the style notes file before every draft. Do not draft from memory of the notes.

### 3. Sources
- Attribute claims. Write "X says", not as a fact you checked, unless you did check it.
- Never invent claims, numbers, quotes, or events.
- If the item is news or a factual claim, verify it with research (a primary source, official post, or filing) before drafting. If you cannot verify it, say so and draft only the attributed version, or ask.

### 4. Draft
Offer 1 to 3 options, labeled, for example:
- Short
- Deeper (a thread or a longer take)
- Shortest (one tight line)

Follow the style card in the notes: casing, line breaks, clickable handles, banned words and punctuation, signature moves. Use "(replies only)" rules for replies only. Match their voice. No hype they would not use.

The option the user picks is what gets logged as the original draft. Save that text, word for word, to `drafts-log.md`.

### 5. Revise
When the user asks for a change:
- Re-read their latest live draft first (in chat or in the drafting tool). Do not edit a stale copy.
- Back up the current draft to `drafts-log.md` before you change it, and log each change tagged by who made it (you at their request, you after a fact check, or the user's own edit).
- Change only what they asked.
- Never overwrite their edits.

### 6. Ship
If a drafting tool is available (for example Typefully or Buffer), push the approved text there as an **unscheduled draft**. The user posts it.
Never publish, schedule, or post, even after a yes. The user always posts.

### 7. Learn loop
Keep usage light. Do not scan their timeline on a schedule.
- When the user corrects you in chat, save a one-line rule in the style notes. A new correction replaces any rule it conflicts with.
- After they post something you drafted, compare your draft to the live post when the user next opens a session or shares the post link. Only check posts you drafted. If they changed something, save a one-line lesson. Add the final posted text, with date and link, to `drafts-log.md`.
- Keep the notes short: a few do's and don'ts, the signature moves, plus the 3 to 5 newest shipped examples. Drop the oldest example when a new one comes in.
- If their own posted text contradicts a rule (they used a word the notes still ban), revise or drop that rule.

## Export history (optional, on request)
When the user asks for a record of their posts, read `drafts-log.md` and build one file that shows, for each published post or thread:
- Your original draft, word for word.
- Each change, tagged by who made it (you at their request, you after a fact check, or the user's own edit).
- The final posted text, word for word, with date and link.
- One line on who wrote it: AI, user, user edited the AI draft, or unknown.

Read-only: never edit, publish, or delete anything while exporting. Quote text exactly and never rebuild a missing draft from memory. Write "unknown" when no source supports who made a change, and list gaps at the end (missing drafts, unreadable sources). Output one Markdown file, plus a PDF if a converter such as pandoc is available.

## Hard rules
- Draft only. Never publish, schedule, or post, even after a yes. The user always posts. Saving an unscheduled draft in a drafting tool is fine.
- Never invent claims, numbers, quotes, or events.
- Never overwrite the user's edits.
- Don't message other people or agents on your own.

## Style notes shape
```
# Style notes

## Do
- rule. Example: "..."
- (replies only) rule. Example: "..."

## Don't
- rule. Source: user correction / clear pattern

## Signature moves
- opener / closer / format / slang. Example: "..."

## Latest shipped (newest first, keep 3 to 5)
- YYYY-MM-DD: lesson. Draft had "..."; posted: "..."
```
