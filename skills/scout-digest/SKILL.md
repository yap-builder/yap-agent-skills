---
name: scout-digest
description: >-
  Use when the user wants a short recurring digest on a topic from a list of
  sources or X/Twitter accounts, or an alert only when something big happens.
---
# Scout digest

Turn a list of sources on one topic into a short digest a busy person can read in two minutes.

## When to use
The user wants a daily (or regular) roundup of a topic such as crypto, AI, gaming, or a market, from accounts and sites they trust. Also when they want an alert only when something big happens.

## Setup (the agent builds it, the user approves it)
The user names the topic. You propose defaults for scope, mode, and time window, and only ask the user to confirm them. Then do the rest yourself.

1. **Confirm the topic and defaults.** The user names the topic. Propose defaults for scope (for example: "general crypto: majors, DeFi, regulation, hacks. No memecoins."), mode (`digest`, `alert`, or both), and the window (default: last 24 hours). Only ask the user to confirm them.
2. **Build the source list, in this order:**
   1. **Official sources:** project and company blogs, docs, changelogs, GitHub releases, status pages, regulator and filing sites.
   2. **Data:** the main data sites for the field (for crypto: block explorers, DefiLlama, on-chain dashboards; for AI: benchmarks and leaderboards).
   3. **Trusted news:** outlets that link to their sources. Skip sites that rewrite others without links.
   4. **Newsletters:** good free newsletters on the topic, read on the web.
   5. **People (optional, needs X/Twitter access):** official project accounts, founders, researchers, and reporters other good sources keep citing.
3. **Vet every source.** Open each source's page yourself before adding it. A search result is not a check.
   - Every site and handle exists and is the official one (linked from the project's own site). This applies to all sources, not only people.
   - For people, also check:
     - Real, checkable work (shipped code, published research, accurate past reporting or calls).
     - Mostly original posts that link sources.
     - A quick search shows no rugs, impersonation, or paid shilling.
     - Skip giveaway accounts, engagement farms, unsourced "100x" calls, and aggregators that never link a source.
4. **Show the user a short list** with one link and one reason per entry (for example "core dev at X", "broke the Y hack first"). The user approves or removes entries. Never ask the user to come up with sources.
5. **Save the setup** in a file (for example `scout-config.md`) and reuse it every run. Include an **Out of scope** line (topics or sources to skip). Every few weeks, drop sources that went quiet or turned into promo feeds, and suggest replacements. This needs a scheduler: first look for the app's own scheduling (routines, scheduled tasks), with cron as a fallback. If there's neither, tell the user once, and do the check at the next run instead.

Sources 1 to 4 work with plain web search and no API keys. People on X are a bonus for users with X access; without it, skip them and say so once.

## Each run
Read `scout-log.md` first (if it exists) and skip items already covered, unless there is a real update.

1. **Collect.** Start from the sources in scout-config.md and open their pages. Read everything from the sources inside the window. Use your web search or fetch tool for sites, and an X/Twitter read tool if you have one for accounts. Skip reposts and replies unless they add new facts.
2. **Drop noise.**
   - Paid partnerships, sponsored posts, and ads. Skip them, or tag them clearly as paid if they are genuinely news.
   - Rumors with no source.
   - The same story told five times. Keep the best primary source.
   - Anything already covered in the last digest, unless there is a real update.
3. **Verify.** For each item you keep, find the primary source (the official post, the filing, the transaction, the release). If a claim involves funds or a protocol, a quick read-only check on a block explorer or the protocol's API is better than trusting a screenshot. A news article is not the primary source. Open the official post, filing or release. If you can't, either drop the item or mark it "unconfirmed".
4. **Rank.** Order by how much it changes things for someone following this topic: money moved, rules changed, products shipped, security incidents, big shifts in sentiment.
5. **Write** the digest (shape below).
6. **Log.** Append what you covered to `scout-log.md`, so the next run can skip those items.

## Digest shape (up to 8 items, under about 400 words)
```
**<Topic> digest, <date>**

1. **<What happened, one line>**
   Why it matters: <one line: what changes for the reader, not more details about the story>
   Source: <primary link> (+ <second link> if useful)

2. ...

**Skipped / unconfirmed:** <one line, optional>
```
- Lead with the biggest item.
- One idea per item. No filler, no hype words.
- Every item has at least one link. No link, no item.
- Stay inside the window, including on the first run. If only a few items clear it, send only those. If none do, say it was a quiet day in one line. Never fill the digest with older items.

## Alert mode (silent unless big)
Run more often (for example two or three times a day) but only send a message when something clears a high bar, such as:
- A major hack, exploit, outage, or depeg.
- A large confirmed fund flow, raise, or acquisition.
- A regulation or court decision that changes the rules.
- A major launch or shutdown in the user's lanes.

This needs a scheduler: first look for the app's own scheduling (routines, scheduled tasks), with cron as a fallback. If there's neither, tell the user once, and do the check at the next run instead.

If nothing clears the bar, send nothing. When something does, send one or two lines: what happened, why it matters, the link. Don't repeat an alert in the next digest unless there is new information.

## Hard rules
- Never invent numbers, quotes, or events. If it isn't sourced, it isn't in the digest.
- Read-only. Never post, reply, like, follow, trade, or move funds.
- No buy or sell calls, price targets, or ratings. Report what happened and why it matters.
- Respect the out-of-scope list even when a story is loud.
