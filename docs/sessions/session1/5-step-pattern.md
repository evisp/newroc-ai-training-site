# The 5-step prompting pattern

This is the main pattern we’ll use in all sessions. It turns talking to AI into a simple checklist you can reuse on any project.

![AI Prompting Pattern](https://i.imgur.com/rCzisdL.png)

!!! info "Use this when…"
    You need a **verifiable** answer from a spec, contract, email thread, or meeting notes — and you want the output in a usable format (bullets/table), not a long paragraph.

!!! warning "Non‑negotiables"
    - Keep scope small (one section / one excerpt at a time).
    - Require references (section/page) for anything you might reuse.
    - If the document doesn’t say it, the output must say **Not stated**.

## 1) Task — what do you want?

Start by asking for one clear action.

Good task words: **Summarise**, **List**, **Extract**, **Find**, **Explain**.

Examples:

- “Summarise the key requirements in this section.”
- “List the masonry submittals in this spec extract.”
- “Explain this clause in simple language for our team.”

Keep it to one main task at a time. If you need more, ask again in a second prompt.

## 2) Context — what are you working with?

Tell AI what the document is and why you care.

Useful context details:

- Project name or type.
- Document type (spec, contract, email thread, meeting notes).
- Relevant sections, pages, or dates.
- What you need this for (submittals, change notice, weekly update, etc.).

Example:

- “This is the masonry spec section for Project X, pages 120–140. I need this for submittal planning.”

Good context helps AI stay focused on your real situation, not a generic answer.

## 3) Constraints — what should it focus on (or ignore)?

Add a few simple limits so the answer stays tight and checkable.

Helpful constraints:

- Which sections/pages/paragraphs to use.
- What to leave out (old revisions, general boilerplate, unrelated trades).
- Time bounds (e.g., construction phase only; ignore design options not selected).

Examples:

- “Focus only on masonry submittal requirements, not other trades.”
- “Use only pages 120–130 and ignore earlier drafts or notes.”

Constraints keep the answer small, specific, and easier to check.

## 4) Output format — how should the answer look?

Say how you want the answer presented so it’s ready to use.

Common formats for New Roc:

- Short bullet list.
- One or two short paragraphs.
- A table (e.g., Item / Section / Notes).

Examples:

- “Give the answer as a short bullet list.”
- “Create a table with columns: Item, Section, Notes.”
- “Write 3–5 bullets I can paste into an email update.”

If you don’t ask for a format, you may get a long, hard-to-use block of text.

## 5) Verification — what will you double-check?

Finish by planning how you will check the answer.

Simple verification moves:

- Ask for section/page references in the output.
- Spot-check 2–3 items directly in the PDF/system.
- Save a note of what you checked (so the output is defendable later).

Examples:

- “Include the section or page number for every item so I can check it.”
- “List any parts where the spec is unclear or conflicts with itself.”

In the live training, we will practise this by comparing AI answers to real spec and contract pages.

??? tip "Copy/paste verification add‑on (append to most prompts)"
    - Use only the text I provide below.
    - For each requirement, include the section/page reference.
    - Quote short phrases only when needed to verify wording.
    - If the document does not state something, write: **Not stated**.
    - Do not add outside standards, typical practice, or assumptions.

## Putting it together (template)

```text
Task: [Summarise / List / Extract / Find / Explain] …
Context: [Project, document type, section/pages, why you need it]
Constraints: [What to focus on, what to ignore]
Output format: [Bullets, short paragraph, or table with named columns]
Verification: [Ask for references and note how you will check]
```

!!! danger "Common prompt mistakes (and fixes)"
    - Too broad: “Read the whole spec” → Fix: use one section/excerpt.
    - No output shape: “Tell me everything” → Fix: request bullets or a table with columns.
    - No proof: “What does it require?” → Fix: require section/page references.
    - Guessing: “What’s typical?” → Fix: force **Not stated** + Missing inputs needed.

## Next steps

In the next pages, we’ll use this pattern in live demos and group exercises:

- See it applied: [Live demos](demos.md)
- Try it yourself: [Practice & exercises](exercises.md)

> Clear prompts are just clear thinking written down. AI simply makes that thinking faster to use on real projects.

![AI Good Prompts](https://i.imgur.com/3b71ENR.png)
