# Contributing

Thank you for improving `manuscript-writing`.

## What Helps

- Sharper checklist items for academic and scientific writing.
- Better examples that preserve technical meaning and avoid unsupported facts.
- Compatibility fixes for Codex, Claude Code, OpenClaw, or other `SKILL.md`-based agents.
- Documentation improvements that make installation or usage clearer.

## Contribution Rules

- Use verified facts only.
- Do not add fabricated citations, benchmarks, novelty claims, or domain claims.
- Keep examples clearly labeled as examples unless they are backed by citations.
- Preserve the two public modes: `revision` edits text; `review` lists suggestions without editing.
- Keep `SKILL.md` concise and move detailed checklist content into `references/`.

## Validation

Before opening a pull request, validate the skill:

```bash
python3 /path/to/quick_validate.py .
```

Also check that `README.md` still names the correct files in the repository layout.

## Pull Requests

In the pull request description, include:

- What changed.
- Why the change improves the skill.
- How you validated it.
- Any factual claims that still need verification.
