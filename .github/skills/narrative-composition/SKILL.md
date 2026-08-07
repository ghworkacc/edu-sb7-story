---
name: narrative-composition
description: "Narrative composition for customer and internal artifacts. Converts grounded evidence into an SB7-style story brief before document or visual rendering. Triggers: SB7, StoryBrand, customer story, narrative brief, executive narrative, transformation story, customer-facing deck, story-driven report, value proposition."
argument-hint: "Provide the audience, artifact type, grounded evidence, and desired decision or action"
---

# Narrative Composition

## Purpose

This is a post-synthesis, pre-rendering skill. It converts grounded evidence into a compact story brief while keeping the customer or affected audience at the center. It does not retrieve raw evidence, render files, or replace domain quality gates.

## Activation Gate

Use it for customer-facing stories, executive decision briefs, value propositions, technical-to-business translations, transformation visuals, and story-driven documents or videos.

Do not use it for:

- raw CRM, milestone, task, or Power BI tables
- schema lookups, diagnostics, write previews, or routine status reports
- technical runbooks and purely structural architecture diagrams
- spreadsheets without a requested narrative summary

Run domain retrieval and synthesis first. Keep raw CRM, M365, transcript, and PBI payloads in their owning context.

## Flow

1. Freeze the 10-15 claims that materially affect the narrative. Record source, confidence, sensitivity, assumptions, and gaps.
2. Read [story-brief.md](references/story-brief.md). Select the audience mode, compose the seven beats, choose an artifact pattern, and emit the typed story brief.
3. Keep the customer as story subject for internal artifacts; the internal team may receive the action without becoming the hero.
4. Hand only the story brief, evidence map, format constraints, and confidentiality boundary to the renderer.
5. For a control-versus-treatment experiment, also read [ab-testing.md](references/ab-testing.md) and freeze test conditions before drafting either version.

## Evidence Rules

- Every factual claim must trace to evidence; hypotheses stay labeled.
- Never invent motives, quotes, metrics, deadlines, competitive claims, or stakes.
- Omit an unsupported story beat instead of filling it with plausible prose.
- Do not cross internal, customer-safe, or public-safe boundaries.
- If a material evidence rule fails, return `status: needs-evidence` and name the gap. Do not render polished fiction.

## Output

- `status`: `ready` | `needs-evidence` | `not-applicable`
- `story_brief`: structured narrative contract
- `evidence_map`: claim-to-source references
- `renderer_handoff`: artifact type, outline, constraints, and confidentiality