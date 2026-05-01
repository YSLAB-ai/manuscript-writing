# manuscript-writing

![License: MIT](https://img.shields.io/badge/license-MIT-green.svg)
![Skill format](https://img.shields.io/badge/skill-SKILL.md-blue.svg)
![Agents](https://img.shields.io/badge/agents-Codex%20%7C%20Claude%20Code%20%7C%20OpenClaw-purple.svg)

![manuscript-writing hero](assets/hero.png)

`manuscript-writing` is an installable `SKILL.md` skill for revising and reviewing scientific, technical, and academic writing.

A few years ago, dissertation polishing meant a committee comment, a reference manager, and a 2 a.m. argument with Track Changes. This repo gives Claude, Codex, and OpenClaw a stricter manuscript checklist so they stop majoring in "sounds academic" and start dressing their claims in evidence, boundaries, and citations.

## What It Does

This skill has two modes:

- `revision`: edits the manuscript or supplied text directly.
- `review`: lists actionable suggestions without editing the source document.

Both modes read `references/revision-checklist.md` before acting and follow the checklist sequentially. The skill uses verified facts only and flags unavailable evidence under `Needs Verification`.

## Example

The image below demonstrates `review` mode: the source text remains unchanged while the skill marks weak spots and explains why they need attention.

![manuscript-writing review demo](assets/demo-review.png)

The paragraph below is a user-provided example of AI-written prose. The revised version demonstrates `revision` mode under the current checklist: preserve technical meaning, remove hyperbole, hedge unsupported causality, permit logical transitions, and flag claims that require citations. Citation placeholders mark unresolved verification needs; they do not add evidence.

### Before

> Memory formation in the human brain is one of the most remarkable and intricate processes in biology, transforming fleeting moments of experience into lasting knowledge, emotions, and skills that define who we are. It begins the instant we perceive the world through our senses--sights, sounds, smells, and touches are rapidly converted into electrical and chemical signals that travel along neural pathways. These signals first enter short-term or working memory, a temporary "holding area" supported by the prefrontal cortex. For information to endure, it must undergo encoding and consolidation, a process heavily orchestrated by the hippocampus, which acts as a kind of "memory librarian," indexing new experiences and linking them to existing knowledge.
>
> At the cellular level, memory formation relies on synaptic plasticity--the brain's ability to strengthen or weaken connections between neurons. When we repeat an experience or pay close attention to it, synapses fire more efficiently through a mechanism called long-term potentiation (LTP), essentially "hard-wiring" the memory into neural circuits. Emotional events receive extra reinforcement from the amygdala, which is why we vividly remember where we were during major life moments. Over hours and days (especially during deep sleep), these fragile traces are stabilized and distributed across the cortex for long-term storage.
>
> In short, every memory we form is the result of billions of neurons communicating, adapting, and reorganizing themselves--an elegant biological symphony that turns the chaos of daily life into the coherent story of our lives.

### Review Mode Comments

- **Strip hyperbole**
  - Flagged text: "remarkable", "intricate", "elegant biological symphony"
  - Suggested action: Replace subjective praise with specific mechanisms.

- **Explain or remove metaphors**
  - Flagged text: "memory librarian", "hard-wiring"
  - Suggested action: Use mechanistic terms or define the analogy briefly.

- **Calibrate certainty**
  - Flagged text: "which is why we vividly remember"
  - Suggested action: Hedge unless cited evidence supports the causal claim.

- **Verify numerical claims**
  - Flagged text: "billions of neurons"
  - Suggested action: Cite the magnitude or remove it.

- **Use transitions logically**
  - Flagged text: "In short"
  - Suggested action: Keep the transition only if the sentence accurately summarizes the preceding evidence; revise the overgeneralized claim.

- **Verify citation coverage**
  - Flagged text: claims about working memory, hippocampus, LTP, amygdala, sleep, and cortical distribution
  - Suggested action: Add citations or mark these claims as needing verification.

### Revision Mode Output

> Memory formation transforms sensory experience into knowledge, emotional associations, and skills. Sensory inputs are converted into electrical and chemical neural signals. Some information can be maintained briefly in short-term or working memory, a process associated with the prefrontal cortex [citation needed]. For information to persist, it must undergo encoding and consolidation. The hippocampus supports these processes by indexing new experiences and linking them to existing knowledge [citation needed].
>
> At the cellular level, memory formation relies on synaptic plasticity, the capacity of synaptic connections to strengthen or weaken over time. Repeated experience or attention can increase synaptic efficacy through mechanisms such as long-term potentiation (LTP) [citation needed]. Emotional events can receive additional reinforcement from the amygdala, which may help explain stronger recall of major life events [citation needed]. Over hours to days, especially during deep sleep, initially fragile memory traces can stabilize and become distributed across the cortex [citation needed].
>
> In short, memory formation depends on neural communication, synaptic adaptation, and systems-level reorganization. These processes convert sensory experience into information that can be maintained, consolidated, and later recalled.

### Revision Log

- Removed subjective intensifiers and metaphor-heavy phrasing.
- Replaced broad identity-focused language with evidence-bounded descriptions drawn from the source paragraph.
- Hedged causal statements about emotional salience and recall.
- Kept a logical summary transition where it accurately connects the conclusion to the preceding paragraph.
- Added citation placeholders instead of inventing support.

### Needs Verification

- Add citations for the roles of working memory, the prefrontal cortex, hippocampal consolidation, synaptic plasticity, LTP, amygdala modulation, and sleep-dependent consolidation.
- Confirm whether the paragraph should remain general or be narrowed to a specific memory type, organism, method, or evidence base.
- Verify whether the intended audience needs simplified definitions for LTP, consolidation, and cortical distribution.

## Compatibility

| Agent | Install target | Invocation style |
| --- | --- | --- |
| Codex | `${CODEX_HOME:-$HOME/.codex}/skills/manuscript-writing` | `Use $manuscript-writing ...` |
| Claude Code | `~/.claude/skills/manuscript-writing` or `.claude/skills/manuscript-writing` | `/manuscript-writing ...` |
| OpenClaw | `~/.openclaw/skills/manuscript-writing` or `skills/manuscript-writing` | Use when the request matches the skill description |

## Install

### Codex

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git "${CODEX_HOME:-$HOME/.codex}/skills/manuscript-writing"
```

Restart Codex after installing.

### Claude Code

Personal skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git ~/.claude/skills/manuscript-writing
```

Project skill:

```bash
git clone https://github.com/YSLAB-ai/manuscript-writing.git .claude/skills/manuscript-writing
```

Claude Code can invoke skills directly with `/skill-name`, and personal skills live under `~/.claude/skills/<skill-name>/SKILL.md`. See the [Claude Code skills documentation](https://code.claude.com/docs/en/skills).

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

OpenClaw loads skills from directories containing `SKILL.md`, including `~/.openclaw/skills/<skill-name>/SKILL.md` and `<workspace>/skills/<skill-name>/SKILL.md`. See the [OpenClaw skills documentation](https://openclawcn.com/en/docs/agent/skills/).

## Use

### Revision Mode

Use this when you want the document edited.

```text
Use $manuscript-writing in revision mode on this manuscript section.
Edit the text directly, preserve technical meaning, and return a revision log plus any Needs Verification items.
```

For Claude Code:

```text
/manuscript-writing revision mode: edit this paragraph for academic precision and concision.
```

### Review Mode

Use this when you want comments only.

```text
Use $manuscript-writing in review mode on this draft.
Do not edit the document. List issues, why they matter, and specific suggested actions.
```

For Claude Code:

```text
/manuscript-writing review mode: critique this introduction without editing it.
```

## Repository Layout

```text
LICENSE
CONTRIBUTING.md
CONTRIBUTORS.md
SKILL.md
README.md
.gitignore
.github/ISSUE_TEMPLATE/skill-feedback.md
.github/pull_request_template.md
assets/hero.png
assets/demo-review.png
agents/openai.yaml
references/revision-checklist.md
```

## Contributing

Checklist improvements, clearer examples, and install fixes are welcome. Please see [CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request.

## Contributors

See [CONTRIBUTORS.md](CONTRIBUTORS.md). Current contributors are derived from git history.

## License

MIT. See [LICENSE](LICENSE).
