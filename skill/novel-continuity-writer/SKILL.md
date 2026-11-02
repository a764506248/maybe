---
name: novel-continuity-writer
description: Continue and maintain the serialized novel in this workspace when asked to advance time, write the next chapter, connect its two protagonists, review continuity, or resolve competing chapter drafts.
---

# Novel Continuity Writer

Advance the novel through finished scene-level prose, not through planning notes alone. Preserve confirmed world rules while making each new chapter change a character's situation, relationship, knowledge, available choices, risk, or irreversible cost.

## Load the project state

Before writing or restructuring:

1. Re-list the workspace Markdown files. Concurrent review or automation may have changed them since the previous turn.
2. Read `小说世界框架.md` completely enough to identify confirmed rules, the current story phase, unresolved character details, and the next causal step.
3. Read all recent formal chapters needed for continuity. Formal chapters use `第…章_….md`; files beginning with `备选素材_` are not canonical.
4. If `小说审视者.md` exists, read its latest review entries. Apply concrete continuity or repetition findings, but never let a review override confirmed world settings.
5. Read [references/project-invariants.md](references/project-invariants.md) when working in this novel workspace.

Do not infer the current plot solely from filenames or the world outline. The prose already written is authoritative for what readers know.

## Continue the story

- When the user says to advance or continue, create or extend actual chapter prose. Do not respond by adding another rule or timeline summary unless they explicitly ask for planning.
- Continue from the latest canonical stopping point and causal pressure. Avoid time jumps that skip the household, service-sector, debt, institutional, or military consequences needed by the world model.
- Prefer one coherent chapter per continuation run. Give it one dominant conflict and a natural ending rather than packing several outline beats into a summary.
- Show the world through prices, permissions, work arrangements, queues, contracts, spaces, bodily action, and relationships. Avoid explaining the theme immediately after the scene already demonstrates it.
- Let systems work correctly when that creates the sharper conflict. The central darkness comes from reasonable human choices, definitions, incentives, and priorities—not from making AI secretly evil or arbitrarily defective.
- Do not invent a pending protagonist name, family structure, military rank, or private history merely to make a scene easier. Use established role descriptions until the user confirms those details.
- Minor functional characters may enter a scene when necessary, but do not silently promote them into confirmed world-setting roles.

## Maintain both protagonists

The programmer line remains the economic and social spine; the special-forces line carries order, obedience, mission, and later war.

- A chapter can use one dominant viewpoint, but every major time phase must advance both protagonists.
- Do not let either protagonist disappear for a long run of chapters. After roughly three to four consecutive chapters on one line, check whether the other line needs a contemporaneous chapter or a causal bridge.
- Connect the lines through shared institutions, events, technologies, consequences, or mirrored choices before deciding whether the characters personally meet.
- Do not settle whether they know each other unless the framework or user has confirmed it.

## Review before saving

Check the draft against these gates:

- The chapter changes at least one story state.
- Its main function is not a repeat of the previous two chapters.
- Character decisions follow from visible motives and constraints.
- Macro change reaches a concrete person without turning a whole group into villains or fools.
- The ending leaves an image, action, choice, or consequence rather than a paragraph explaining what the reader should conclude.
- Dates, elapsed time, job status, permissions, and earlier promises remain consistent.

If a small revision solves the problem, revise the draft before finalizing. Do not rewrite already strong chapters merely to vary wording.

## Save and reconcile

- Save canonical prose as `第N章_标题.md` in the workspace root unless the project already uses another convention.
- Preserve user and reviewer edits. Re-read a target file immediately before modifying it when concurrent automation is active.
- When two drafts claim the same chapter number and function, compare them by continuity, scene focus, character pressure, and thematic restraint. Keep the stronger version canonical and move the other intact to a clearly named `备选素材_…` file when the choice is well supported and recoverable. Ask the user only when the alternatives imply materially different future plots.
- Update `小说世界框架.md` only after a major time-state change or confirmed setting decision. Do not mark new prose details as confirmed without user confirmation.
- Report the new chapter title and the story-state change concisely.
