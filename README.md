# slung

An [Agent Skill](https://agentskills.io) that explains, rewrites or answers anything in **slung** style: casual slang English, loose and funny, with swearing, but with a plain structure (main point first, short direct sentences) and **every real fact kept**.

Think "blunt mate at the mamak at 1am", not "LinkedIn post".

> ⚠️ Contains profanity by design. Use `lite` for anything work-safe.

## What it does

| Task | Trigger | Output |
|---|---|---|
| **Explain** | "explain this slung", "tl;dr slung" | Plain explanation in slung voice. Detail may go, meaning never changes. |
| **Rewrite** | "make it slung", "less corporate" | Copy-ready rewrite, every fact kept, plus a "Check before sending" note if something's ambiguous. |
| **Slung version** | "slung version" | Your previous answer, redone in slung voice. |
| **Answer** | "roast me", "how do I fix X, slung" | A straight answer in slung voice. |

### Intensity levels

- **lite**: slang and attitude, nothing stronger than "damn". Safe near colleagues.
- **full** (default): regular swearing for rhythm and emphasis.
- **unhinged**: maximum attitude, still factually accurate.

### Guardrails baked in

- Exaggerates the vibe, never the claims: numbers, dates, conditions and commitment words ("may", "aim to") stay exact.
- Swears at situations, not at real people. No slurs or identity-based jokes.
- No em-dash connector writing, no hedging filler.

## Example

> **Source:** "Notwithstanding Clause 14.2, the Contractor shall be liable for liquidated damages at a rate of 0.5% of the Contract Price per day of delay, subject to an aggregate cap of 10%, save where such delay is attributable to the Authority."
>
> **Slung:** "If you deliver late, you pay 0.5% of the contract price for every day you're late, and that shit adds up fast. The total penalty tops out at 10% of the contract price. If the client caused the delay, you don't pay a damn thing. This applies even if Clause 14.2 says something different."

## Install

### Claude Code (plugin marketplace)

```
/plugin marketplace add yk-lai/slung-skill
/plugin install slung@slung-skill
```

### Claude Code (manual)

```bash
git clone https://github.com/yk-lai/slung-skill.git
cp -r slung-skill/skills/slung ~/.claude/skills/
```

### Claude.ai / Claude Desktop

Download `skills/slung` as a zip and upload it under **Settings → Capabilities → Skills**.

### Other agents (skills CLI)

```bash
npx skills add yk-lai/slung-skill
```

## Usage

```
/slung lite rewrite this email: ...
/slung unhinged roast my sprint planning
explain this clause slung: ...
```

## Repo layout

```
.claude-plugin/marketplace.json   # Claude Code plugin marketplace manifest
skills/slung/SKILL.md             # the skill
```

## License

[MIT](LICENSE)
