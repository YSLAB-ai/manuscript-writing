# manuscript-writing

Installable `SKILL.md` skill for revising and reviewing scientific, technical, and academic writing.

## Modes

- `revision`: edits the manuscript or supplied text directly.
- `review`: lists actionable suggestions without editing the source document.

Both modes read `references/revision-checklist.md` before acting and follow the checklist sequentially. The skill uses verified facts only and flags unavailable evidence under `Needs Verification`.

## Install

### Codex

```bash
python3 /path/to/install-skill-from-github.py \
  --repo YSLAB-ai/manuscript-writing \
  --path . \
  --name manuscript-writing \
  --method git
```

### Claude Code

Personal skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git ~/.claude/skills/manuscript-writing
```

Project skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git .claude/skills/manuscript-writing
```

Invoke explicitly with `/manuscript-writing`, or let Claude load it when the request matches the skill description.

### OpenClaw

Global skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git ~/.openclaw/skills/manuscript-writing
openclaw skills check
```

Workspace skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git skills/manuscript-writing
openclaw skills check
```

If OpenClaw does not detect the updated skill, restart the gateway.
