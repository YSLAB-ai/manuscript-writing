---
name: manuscript-writing
description: Use when revising or reviewing scientific, technical, or academic manuscripts, proposals, abstracts, reports, or related writing for precision, concision, logical cohesion, citation support, evidence alignment, and objective scholarly tone.
---

# Manuscript Writing

## Overview

Use this skill to improve academic and scientific writing without changing unsupported claims. It has two modes: `revision`, which edits the document, and `review`, which lists suggestions without editing the document.

Always use verified facts only. Do not invent citations, data, mechanisms, numerical values, novelty claims, or literature context. If verification requires sources or figures that are not available, flag the claim instead of rewriting it as fact.

## Mode Selection

Use `revision` when the user asks to edit, revise, rewrite, polish, tighten, or improve the manuscript text directly. Return the revised text or update the supplied document, depending on the user's request and available tools.

Use `review` when the user asks for comments, feedback, suggestions, critique, audit, or review without changing the manuscript. Return a listed set of actionable suggestions and do not edit the source document.

If the user asks for both, run `review` first to identify issues, then ask before applying edits unless the user already clearly requested direct revision.

## Shared Rules

- Preserve technical meaning. Do not change the scope, certainty, mechanism, temperature range, material system, causal relationship, baseline, or numerical interpretation unless the supplied evidence supports the change.
- Separate evidence from interpretation. Data, literature claims, limitations, and implications must not be merged into stronger claims than the evidence permits.
- Keep examples as rewrite patterns only. Do not insert an example's technical content into a manuscript unless the source document or cited evidence supports it.
- Maintain the author's intended contribution while removing vague language, redundancy, inflated certainty, unsupported novelty, and logical gaps.
- When facts cannot be verified from the provided text, citations, figures, tables, or user-supplied context, mark them as requiring verification.
- Before performing either `revision` or `review`, read `references/revision-checklist.md` and use it as the governing checklist.
- Execute the checklist phases in order. If a checklist item cannot be completed because required evidence, figures, tables, citations, equations, or constraints are unavailable, flag it under `Needs Verification` instead of skipping it silently.

## Revision Mode: Edit the Document

1. Identify the target audience, venue constraints, required tone, and whether edits should be in-place, returned as revised prose, or provided as a separate revised file.
2. Read the full relevant text before editing so terminology, claims, abbreviations, figures, and equations are handled consistently.
3. Apply `references/revision-checklist.md` sequentially: scope setup, precision, concision, tone, scientific rigor, and final audit.
4. Preserve citations and factual claims unless the user provides evidence for a correction. If a claim is unsupported, keep the text conservative or insert a visible verification note rather than fabricating support.
5. Prefer objective active voice with the data, model, method, or literature as the subject.
6. Remove orphan facts, redundant modifiers, unsupported hyperbole, repeated arguments, and transition words that do not mark a clear logical relationship.
7. Check numerical consistency, percentage logic, figure/table sequencing, equation-variable definitions, and citation specificity when the required materials are available.
8. Return a concise revision log after the edited text or edited file, noting major changes to claims, structure, terminology, and evidence support.

## Review Mode: List Suggestions Only

Do not rewrite the document unless a short suggested replacement is needed to make a recommendation actionable.

Use `references/revision-checklist.md` as the review rubric. Convert checklist failures into listed suggestions rather than editing the source document.

For each issue, provide:

- Location: section, paragraph, sentence, heading, figure, table, or equation when identifiable.
- Issue: the specific problem, such as unsupported claim, vague term, overstatement, missing citation, inconsistent terminology, flawed comparison, or unclear causal logic.
- Why it matters: the precision, rigor, readability, or evidence problem created by the issue.
- Suggested action: a concrete edit, verification step, citation need, or structural move.
- Optional rewrite: one concise sentence when useful, clearly marked as suggested wording.

Prioritize high-impact issues first: unsupported novelty, incorrect certainty, data inconsistency, mathematical errors, missing citations for factual claims, and claims that exceed the evidence. Then address flow, concision, tone, and style.

## Output Expectations

For `revision`, provide the revised document content or edited file path, then a short revision log. If unresolved verification issues remain, list them separately under `Needs Verification`.

For `review`, provide grouped suggestions with clear labels such as `Scientific Rigor`, `Evidence and Citations`, `Structure and Flow`, and `Style and Clarity`. Do not present stylistic preferences as factual requirements.

For either mode, keep all feedback actionable and grounded in the supplied manuscript, data, figures, tables, citations, or user-provided context.
