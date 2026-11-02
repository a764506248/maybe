---
name: novel-review-loop
description: Review serialized fiction against its written canon, identify continuity and narrative problems, apply minimal logical revisions when authorized, and maintain append-only review history. Use for chapter review, reviewer-issue resolution, cross-chapter consistency checks, or recurring fiction revision loops.
---

# Novel Review Loop

Use the manuscript as the reader's evidence and the world framework as a contradiction boundary. A framework may reveal an inconsistency, but must never supply an explanation absent from the prose.

## Locate the project sources

Identify, rather than assume, the project's equivalents of:

- formal numbered chapters;
- the world/canon ledger;
- the reviewer rubric and historical review log;
- alternate drafts or backup material.

In this project, prefer `rg --files` and Chinese filenames such as `第*.md`, `小说世界框架.md`, and `小说审视者.md`. Exclude `skill/`, clearly marked alternate material, and archived drafts from the formal chapter sequence.

Read the changed chapter, the preceding chapter, the latest relevant review record, and only the framework sections needed to check it. When checking a longer arc, also inspect chapter openings/endings and explicit dates across the whole range.

## Respect the authority hierarchy

1. Preserve the user's explicit choices and confirmed canon.
2. Treat confirmed framework entries as constraints.
3. Treat “待确认” and candidate entries as possibilities, never facts.
4. Judge what readers can know from the prose itself.
5. Preserve existing manuscript changes unless the task directly requires modifying them.

Do not invent a name, relationship, rank, institution, outcome, or major plot event merely to improve a score. If a fix requires choosing among pending canon options, record the blocker and ask the user rather than deciding silently.

## Choose the operating mode

- For review/report requests, diagnose and record concrete issues without editing prose.
- For requests to solve or revise reviewer issues, apply the smallest change that resolves the reading consequence.
- Do not write a new chapter solely because a review assigns a task to a future chapter, unless the user also asked to continue the manuscript. Record the constraint for the next chapter instead.

Read [references/review-criteria.md](references/review-criteria.md) when scoring a chapter, conducting a cross-chapter review, or deciding whether a proposed fix actually closes an issue.

## Review before editing

Determine what the chapter changes: circumstances, relationships, knowledge, available choices, risk, or irreversible cost. Then identify at most three highest-impact issues, each with:

- the exact scene or sentence;
- the reader-visible consequence;
- the smallest revision target.

Distinguish current defects from historical observations already resolved in later records. Do not re-open an old issue merely because its original description remains in the append-only log.

Pay special attention to:

- explicit dates and elapsed time across chapters;
- what each character could know at that moment;
- cause preceding effect;
- repeated chapter functions, endings, reports, dashboards, or explanatory summaries;
- a scene already demonstrating a theme that narration then explains again;
- dual-protagonist cadence required by the canon;
- duplicate chapter numbers or alternate drafts accidentally entering the formal sequence.

## Apply minimal, logical revisions

Prefer changes that preserve events and character choices:

- delete a thematic explanation when action or dialogue already carries it;
- repair a date, duration, or transition when the event order is otherwise sound;
- move an abstract classification onto the document or institution that would plausibly use it;
- clarify one causal link instead of adding a new subplot;
- mark a competing draft as alternate material rather than deleting it when its status is ambiguous.

Do not weaken a real dilemma by making one side foolish or malicious. “Darkness” should arise from reasonable choices, limited resources, incentives, responsibility, or competing goods—not from ominous wording alone.

When another process is editing concurrently, re-read the target immediately before patching. If the intended fix has already landed, do not duplicate it; update only the review status if needed.

## Maintain the review history

Treat historical scores and prior diagnoses as append-only evidence:

- never overwrite an old score to make the project look cleaner;
- append a re-review or problem-resolution note after the original record;
- state exactly what changed and which future obligations remain;
- distinguish the score's original scope from later chapters added afterward;
- do not claim an issue is resolved until the prose or file status confirms it.

If a competing draft is preserved, make its non-canonical status explicit in the file itself and note the resolution in the review log.

## Verify the result

After editing, check:

- only one formal file exists for each chapter number;
- chapter dates and elapsed durations can coexist;
- no pending framework item was promoted to confirmed canon;
- the revised passage no longer repeats its own meaning;
- the fix did not create a knowledge, motivation, or causal gap;
- reviewer records describe the current file state while preserving historical context.

Use focused searches and direct excerpts as evidence. A high review score is not the objective; a coherent, restrained manuscript is.
