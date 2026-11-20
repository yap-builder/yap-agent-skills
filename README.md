# yap-agent-skills

Free, plain-text skills for AI agents doing research, daily digests, and ghostwriting. Works in Claude Code, Cursor, Codex, and Grok Bot.

Each skill is a folder with a `SKILL.md` file (YAML frontmatter with `name` and `description`, then instructions). Your agent reads the description and loads the skill when it fits the task.

## Skills

| Skill | What it does |
| --- | --- |
| [dig-contract](skills/dig-contract/SKILL.md) | Research a lead or claim: quick check first, primary sources, own read-only on-chain read, and a 500-word findings brief with labeled facts, a required self-challenge, Details in the same file, and no verdict. |
| [scout-digest](skills/scout-digest/SKILL.md) | Turn a list of trusted sources into a short daily digest (what happened, why it matters, links), with a silent-unless-big alert mode. |
| [ghostwriter](skills/ghostwriter/SKILL.md) | Draft social posts in your voice from a link, text, or voice note. Reads style notes first, offers 1 to 3 options, and learns from your edits and posts. Can export a draft vs posted history. Never publishes. |

## Install

For Claude Code, Cursor, and Codex: clone the repo, then copy (or symlink) the skill folders you want into your tool's skills folder.

```bash
git clone https://github.com/yap-builder/yap-agent-skills.git
cd yap-agent-skills
```

### Claude Code
- Personal (all projects): `~/.claude/skills/`
- One project: `.claude/skills/` in the project root

```bash
mkdir -p ~/.claude/skills
cp -r skills/* ~/.claude/skills/
```

### Cursor
- Personal: `~/.cursor/skills/` (or `~/.agents/skills/`)
- One project: `.cursor/skills/` (or `.agents/skills/`) in the project root
- Cursor also reads `.claude/skills/`, `~/.claude/skills/`, `.codex/skills/`, and `~/.codex/skills/`, so a Claude Code or Codex install works in Cursor too.

```bash
mkdir -p ~/.cursor/skills
cp -r skills/* ~/.cursor/skills/
```

### Codex
- Personal: `~/.agents/skills/`
- One project: `.agents/skills/` in the repo (Codex scans from where you launch it up to the repo root)

```bash
mkdir -p ~/.agents/skills
cp -r skills/* ~/.agents/skills/
```

**One folder for Cursor and Codex:** both read `~/.agents/skills/`, so installing there covers both.

Restart your tool after installing so it picks up new skills. Folder names must match the `name` in each `SKILL.md`.

### Grok Bot
Send a bot the repo link and ask it to save the skills.

## Tested
- Claude Code with Claude Opus 5.5 (November 2026): all three skills were picked up from their descriptions alone and followed their steps.
- Grok Bot (November 2026): all three skills ran end to end.
- Cursor (model: Auto, November 2026): research, digest and ghostwriting requests loaded the skills on their own. One short "is it true…" question was answered without the skill.
- Codex: install path follows its docs, not tested live yet.

Tried a skill on another model or tool? Open an issue and say what worked and what didn't: https://github.com/yap-builder/yap-agent-skills/issues

## Tools the skills expect
The skills are tool-agnostic. They work best when your agent has:
- Web search and page fetch
- A block explorer or public RPC for on-chain reads in dig-contract
- A drafting tool (for example Typefully or Buffer) if you want ghostwriter to save unscheduled drafts

None of these skills post, trade, or move funds. The ghostwriter skill may save an unscheduled draft in a drafting tool if you have one; you still publish it yourself. The other skills are read-only.

## Contributing
Issues and pull requests welcome. Keep skills short, practical, and tool-agnostic.

## License
[MIT](LICENSE)

Built by [@Yap452](https://x.com/Yap452).
