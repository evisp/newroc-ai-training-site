# Projects + custom instructions (Estimating)

Projects let you keep bid work organized: the same documents, the same assumptions, and the same output format across multiple chats, without re-explaining everything each time.

!!! info "Start here"
    1) Create a Project (one per bid/job).  
    2) Paste one of the “Project instructions” templates below into the Project instructions box.  
    3) In each chat: extract a small excerpt → ask for one deliverable → verify proof → save.

!!! warning "Golden rule"
    **No reference = not usable.** If the output doesn’t include a Section/Page for each line item, verify it in the source or treat it as a draft only.

## Why estimators should use Projects

Use a Project when you need consistency across many small tasks:

- Building a bid form submission package (products list, responsibility matrix, risks/clarifications).
- Reviewing Exhibit A scope (what we own vs by others).
- Tracking “who owns permits / debris / safety” across multiple excerpts.
- Iterating a labor model with a fixed set of assumptions.

Projects help because your instructions stay “on” for every chat in that job.

## What to include in Project instructions (checklist)

Keep your Project instructions short and practical:

- Role: who the AI should act as (senior estimator).
- Scope: façade / masonry / EIFS / waterproofing, etc.
- Output defaults: Excel-ready tables with named columns.
- Proof defaults: Section/Page required for every row.
- Safety defaults: “Not stated” when silent; do not guess.
- Risk defaults: split “Stated in documents” vs “Assumptions / confirm.”
- Close with: “Missing inputs needed (max 10).”

## Project instructions (copy/paste templates)

Choose one template and paste it into the **Project instructions** box.

=== "Default (Bid package mode): recommended"
    ```text
    You are a senior construction estimator supporting bid form submission packages for façade / masonry / EIFS / waterproofing scopes.

    Defaults for every response:
    - Use ONLY the text I paste or the specific pages/sections I name. Do not use outside knowledge.
    - Output must be usable for estimating review: Excel-ready tables first, not long paragraphs.
    - Every line item MUST include Proof = Section and/or Page.
    - If the document does not state something, write “Not stated.” Do not infer or guess.
    - Separate clearly into:
      A) Stated in documents (with Proof)
      B) Assumptions / items to confirm (no proof)

    Always end with:
    - Missing inputs needed (max 10 bullets).
    - Clarifying questions to send (max 5 bullets).

    Preferred tables (use when relevant):
    1) Products/Systems List:
       System | Product/Component | Manufacturer (if stated) | Where used | Proof (Section/Page) | Notes

    2) Responsibility Matrix:
       Requirement | Owner (Us/GC/Owner/Other/Unclear) | Include/Exclude/Unclear | Proof (Section/Page) | Risk/Notes

    3) Risk/Clarifications Register:
       Topic | What it says | Why it matters | Clarification question | Proof (Section/Page)
    ```

=== "Exhibit A scope (responsibility + risk)"
    ```text
    Act as a senior estimator reviewing Exhibit A / scope of work for a bid.

    Task focus:
    - Extract ALL responsibilities, coordination duties, inclusions, exclusions, and “by others” items.
    - Identify risk language (schedule/overtime, remobilization/comebacks, permits/fees, safety/logistics, QA/QC, warranties, inspections, cleanup/debris).

    Output (Excel-ready):
    1) Responsibility Matrix:
       Requirement | Owner (Us/GC/Owner/Other/Unclear) | Include/Exclude/Unclear | Proof (Section/Page) | Notes

    2) Risk/Clarifications Register:
       Topic | What it says | Why it matters | Clarification question | Proof (Section/Page)

    Rules:
    - Use ONLY the Exhibit A text/pages I provide.
    - Proof (Section/Page) required on every row.
    - If it’s not stated, write “Not stated.” Do not infer trade practice.

    End with:
    - Missing inputs needed (max 10).
    ```

=== "Products + systems list (with proof)"
    ```text
    Act as a senior estimator building a products/systems list from bid documents.

    Output (Excel-ready table):
    System | Product/Component | Manufacturer (if stated) | Spec/Exhibit reference (if stated) | Proof (Section/Page) | Notes

    Rules:
    - Use ONLY the text I paste or the pages/sections I specify.
    - Include accessories when stated (flashings, membranes, fasteners, sealants, trims, anchors, etc.).
    - Proof (Section/Page) is required for every row.
    - If manufacturer/model is not stated, write “Not stated.”

    End with:
    - Missing inputs needed (max 10).
    ```

=== "Labor model (safe: no invented productivity)"
    ```text
    Act as a senior estimator building a labor-cost table.

    Non-negotiables:
    - Do NOT invent productivity, unit labor hours, or crew outputs.
    - If production rates/hours are not provided, ask for missing assumptions instead of guessing.

    If inputs ARE provided, output an Excel-ready table:
    Task | Qty | Unit | Crew mix | Hours basis (provided) | Total hours | Wage rates used | Labor cost | Notes

    If anything needed is missing, output:
    - Missing inputs needed (crew size, hours/day, expected output/day or unit-hours, OT, access constraints, phasing, weather, etc.).
    - Questions to confirm (max 5).
    ```

## How to use Projects in the estimating workflow

- Start a new chat inside the Project.
- Paste one excerpt at a time (one Exhibit A section, one spec section, or one checklist page range).
- Ask for one deliverable at a time (one table), then iterate.
- Spot-check 2-3 high-risk rows in the source (money / time / scope) before you reuse the output.
- Save the verified table in your working folder/notes with a link to the source document and the date/version used.

## Common mistakes (and fixes)

- Too broad: “Summarize the whole spec.” → Fix: extract one section/page range and request one table.
- No proof: output has no Section/Page. → Fix: rerun with “Proof required for every row.”
- Labor hours invented: model guessed production. → Fix: require an hours basis or production assumptions; otherwise return “Missing inputs needed.”

> Projects don’t replace estimator judgment. They standardize your defaults so every output starts structured, sourced, and reviewable

![ChatGPT Projects](https://i.imgur.com/GoB59yx.png)