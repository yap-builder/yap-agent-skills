---
name: dig-contract
description: >-
  Use when the user drops a lead, claim, project, raise, product, or link and
  wants to know what is real. Runs a quick claim check first, then a sourced
  research dig, and returns a findings brief of 500 words or less with labeled
  facts, a required self-challenge, Details below in the same file, and no
  verdict label.
---
# Dig contract

A repeatable way to research a lead and hand back findings, not opinions.

## Sources
- **Works with no setup:** web search, project sites, docs, filings, news, block explorers, public RPCs and protocol APIs.
- **Optional:** an X/Twitter API key or X connector for live posts and sentiment. Without it, skip or shorten the sentiment step and say so.

## When to use
The user shares a link, a claim, a project, a funding raise, a product, or asks "is this real?"

## Flow
1. **Quick ack.** One short line, then do the work. Don't narrate every step.
2. **Quick check first (about 2 minutes).** Test the core claim before a full dig: does the thing exist, is the headline number or date real, is there any verifiable data at all. If the claim is false or there is nothing verifiable, stop and send a short note: what the claim said, what is actually true, and the sources. An item with no real data gets one line ("nothing verifiable found") and is never padded into a longer dig.
3. **Research.** Use your web search tool, plus an X/Twitter search tool if you have one. Prefer primary sources (the project site, docs, filings, founder posts, code repos) over recaps and news rewrites.
4. **Own on-chain read.** When a claim involves funds, wallets, a token, or a protocol, check the chain or the protocol's public API yourself before writing: balances, pool state, debts, transfers. Use a block explorer, a public RPC, or the protocol's API. Read-only. Label it as your own read with the time and time zone. If you skip a chain read that this step calls for, say why in the brief (for example: no public contract, the explorer or API was down, the claim was only about a team or a document).
5. **Spot-check.** Confirm key claims across more than one source. If sources conflict, say so. Say what you did **not** check. Time-stamp your own reads and first-party checks with the time and time zone.
6. **Sentiment** (only when public opinion matters). Read several posts from different sides and weight by reach. One viral take is not sentiment.
7. **Self-challenge (required, every dig).** Before sending, reread the findings as a hostile critic. What is the weakest fact? What would make the bottom line wrong? Do two of your own facts contradict each other? Fix it or flag it. Put the self-challenge in the brief. Never skip this section on a full dig.
8. **Deliver.** Send the brief in chat (500 words or less, hard cap). If the write-up needs more room, put the brief at the top of a file and a **Details** section below it in the same file, then share the path. The chat brief stays at 500 words or less.

## Brief shape (same every time, 500 words or less, hard cap)
The brief is the top of the file and the text you send in chat. It is 500 words or less. That is a cap, not a goal. Anything that does not fit goes under **Details** in the same file, never into a longer brief.

- **One line:** what it is, or what the claim says.
- **Key facts**, each with a real source link. Label every fact as one of:
  - from a page (quote or cite it)
  - someone else's measurement
  - own calculation (show the inputs)
  - own chain read (with time and time zone)
- **Sentiment**, reach-weighted, if relevant.
- **Bottom line:** what the evidence shows, and what it depends on.
- **Self-challenge:** the weakest fact, or what would make the bottom line wrong. Required in every full-dig brief.
- **Not found / not checked:** be explicit. If you skipped a chain read that the claim called for, say why here.
- **Don'ts:** easy mistakes, lookalike tokens, similarly named projects, if any.
- **So what** (one line): where this could be useful, such as a content hook, a product or tool idea, or "not actionable." This is not a verdict.

### Trimming rule
When cutting down to 500 words, keep your own original findings first (own chain reads, own calculations, facts nobody else reported). Cut recaps of other people's work first. Move the cut material into **Details**; do not delete it.

### File layout
```
# <title>

## Brief
<the 500-word-or-less brief>

## Details
<full chain read, extra sources, checks, tables, longer quotes>
```

## Batch wrap-up (optional)
If the user wants several digs delivered together (for example a daily set), send one wrap-up plus a path to each file. The wrap-up includes each dig's one-line So what. Do not drop So what lines from the wrap-up even when you are shortening it.

## No verdict labels
Never lead with or include "Worth it", "Skip", "Watch", "Buy", "Avoid", or any rating. Findings only; the user decides. The so-what line points to a use; it never rates the lead.

## Hard rules
- Never invent numbers, quotes, raises, users, or traction. No source means "not found", not an estimate.
- Never trade, sign transactions, connect a wallet, or move funds. Chain reads are read-only.
- Sharp and plain. No hype words.
- Research only. Don't draft posts or replies unless the user asks.
- Don't message other people or agents on your own. You can offer to save notes or hand off a brief; wait for a yes.

## Example skeleton
```
**What:** <one line>

**Facts**
- <fact> [page](link)
- <fact> (own chain read, 14:05 PT) [explorer](link)
- <fact> (own calc: A / B = C)

**Sentiment:** <reach-weighted summary, or skip>
**Bottom line:** <what it shows, what it depends on>
**Self-challenge:** <weakest fact, or what would make this wrong>
**Not found:** <list, including why a chain read was skipped if it was>
**Don'ts:** <lookalikes, traps>
**So what:** <one line>
```
