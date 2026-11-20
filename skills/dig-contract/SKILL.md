---
name: dig-contract
description: "Use when the user drops a lead, claim, project, raise, product, or link and wants to know what is real, or asks whether something is true."
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
2. **Quick check first (about 2 minutes, a guide, not a cutoff).** Test the core claim before a full dig: does the thing exist, is the headline number or date real, is there any verifiable data at all. If the claim is false or there is nothing verifiable, stop and send a short note in chat only, with no file: what the claim said, what is true, and the sources with links. Time-stamp your own reads. An item with no real data gets one line ("nothing verifiable found") and is never padded into a longer dig. If the quick check can't settle the claim, go on to the full dig.
3. **Research.** Use your web search tool, plus an X/Twitter search tool if you have one. Prefer primary sources (the project site, docs, filings, founder posts, code repos) over recaps and news rewrites.
4. **Own on-chain read.** When a claim involves funds, wallets, a token, or a protocol, check the chain or the protocol's public API yourself before writing: balances, pool state, debts, transfers. Use a block explorer, a public RPC, or the protocol's API. Read-only. Label it as an own chain read with the time and time zone. If you skip a chain read that this step calls for, say why in the brief (for example: no public contract, the explorer or API was down, the claim was only about a team or a document).
5. **Spot-check.** Confirm key claims across more than one source. If sources conflict, say so. Say what you did **not** check. Add the time and time zone to anything you read yourself. That is a time stamp, not a new label: each fact still gets one of the four labels below.
6. **Sentiment** (only when public opinion matters). Read several posts from different sides and weight by reach. One viral take is not sentiment.
7. **Self-challenge (required, every dig).** Before sending, reread the findings as a hostile critic. What is the weakest fact? What would make the bottom line wrong? Do two of your own facts contradict each other? Fix it or flag it. Check that every number you compare to the claim measures the same thing over the same period (visitors vs visits, one month vs three months, gross vs net). Quote the source's own label for the number. If the units or period don't match the claim, say so in the brief. Put the self-challenge in the brief. Never skip this section on a full dig.
8. **Deliver.** For a full dig, always write a file with the brief (500 words or less, hard cap) on top and a **Details** section below it in the same file. Before writing the file, count the brief's words. If it is over 500, move recaps into Details until it fits. Then share the path and paste the brief into chat exactly as it is in the file. Don't rewrite it. If the quick check ended the dig (the claim is false or nothing is verifiable), send the short note in chat only. Do not write a file.

## Brief shape (same every time, 500 words or less, hard cap)
On a full dig, the brief is the top of the file and the text you send in chat. It is 500 words or less. That is a cap, not a goal. Aim for about 450 words, so a rough count still lands under 500. Anything that does not fit goes under **Details** in the same file, never into a longer brief. If the quick check ended the dig, there is no file and no brief; the short note stays in chat only.

- **One line:** what it is, or what the claim says.
- **Key facts**, each with a real source link. Label every fact as one of:
  - from a page (quote or cite it)
  - someone else's measurement (any number from a third party, such as Similarweb, a dashboard, or a report, even when you read it yourself)
  - own calculation (show the inputs)
  - own chain read (with time and time zone)

  Use these four labels exactly as written. Don't invent new ones. A search result is not a page read: use "from a page" only for a page you opened yourself. If you only saw a fact in search results, open the page, or move the fact to Not found / not checked.
- **Sentiment**, reach-weighted, if relevant.
- **Bottom line:** what the evidence shows, and what it depends on.
- **Self-challenge:** the weakest fact, or what would make the bottom line wrong. Required in every full-dig brief.
- **Not found / not checked:** be explicit. If you skipped a chain read that the claim called for, say why here.
- **Don'ts:** easy mistakes, lookalike tokens, similarly named projects, if any.
- **So what** (one line): where this could be useful, such as a content hook, a product or tool idea, or "not actionable." This is not a verdict.

### Trimming rule
When cutting down to 500 words, keep your own original findings first (own chain reads, own calculations, facts nobody else reported). Cut recaps of other people's work first. Move the cut material into **Details**; do not delete it.

### File layout
Use this layout for every full dig. Do not write a file when the quick check ended the dig.
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
