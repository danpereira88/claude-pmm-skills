# Claude skills for product marketing

Two [Claude skills](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) that turn well-known product-marketing methods into step-by-step working guides Claude follows. Positioning comes first, then copy built on top of it.

| Skill | What it does | Method by |
| --- | --- | --- |
| [`april-dunford-positioning`](april-dunford-positioning/SKILL.md) | Positions or repositions a product: competitive alternatives, differentiated value, best-fit customers, market category. Produces a positioning canvas and turns it into a sales pitch ([`references/sales-pitch.md`](april-dunford-positioning/references/sales-pitch.md)). | April Dunford |
| [`joanna-wiebe-copywriting`](joanna-wiebe-copywriting/SKILL.md) | Writes conversion copy (landing pages, hero sections, emails, CTAs) from voice-of-customer research rather than from a blank page. Includes message-mining steps ([`references/message-mining.md`](joanna-wiebe-copywriting/references/message-mining.md)) and swipeable formulas ([`references/formulas.md`](joanna-wiebe-copywriting/references/formulas.md)). | Joanna Wiebe / Copyhackers |

## How they work together

1. **Position first.** Run `april-dunford-positioning` to settle who the product is for, what it is up against, and why it wins.
2. **Then write.** Run `joanna-wiebe-copywriting`, mining real customer language and matching the copy to the buyer's awareness stage. The positioning skill won't write messaging or a pitch until a positioning canvas exists.

Both skills trigger on plain requests ("how should we position this?", "this landing page isn't converting"), so you don't have to name the method.

## Install

Claude Code: copy a skill folder into `~/.claude/skills/` (all projects) or `.claude/skills/` (one project).

```bash
cp -R april-dunford-positioning joanna-wiebe-copywriting ~/.claude/skills/
```

Claude apps: zip a skill folder and upload it under **Settings → Capabilities → Skills**.

## Credits

The methods belong to their authors. These skills are my own summaries and working guides, written in my own words, and are no substitute for the originals:

- **April Dunford**: *Obviously Awesome* (2019) and *Sales Pitch* (2023). [aprildunford.com](https://www.aprildunford.com)
- **Joanna Wiebe / Copyhackers**: conversion copywriting and message mining. [copyhackers.com](https://copyhackers.com)
- **Eugene Schwartz**: the five stages of awareness, from *Breakthrough Advertising* (1966)

No affiliation with or endorsement by any of the above.

## License

The skill text is MIT licensed (see [LICENSE](LICENSE)). The underlying methods remain the work of their authors.
