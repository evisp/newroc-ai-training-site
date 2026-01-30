# Estimating – prompt templates (scope, pricing, products)

Use this page as a quick reference for "what good looks like" when prompting on estimating packages: proposals, leveling sheets, drawings/specs, unit pricing inputs, and product specifications.

!!! info "Where to find the full playbook"
    The complete Prompt Playbook (all use cases + full Prompt Builder template + data) lives in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link).

Below are short examples (bad prompt vs good prompt) designed to produce **usable AI** output: tables and structured sections you can save, share, and verify.  
The goal is the same as Session 1: keep scope tight, request a deliverable you can reuse, and require references so you can verify in the source documents.

!!! warning "Golden rule"
    - No reference = not usable (must point to proposal page, drawing note, spec clause).
    - If documents don't state it, write **Not stated** (don't fill gaps with "typical scope" or "typical productivity").
    - Verify 2–3 critical items (scope gaps, pricing assumptions, high-risk exclusions) before relying on the output.

---

## Estimating prompt examples

??? example "Use case 1: Scope completeness check (proposal vs contract documents)"
    **Goal:** Compare the proposal/leveling sheet against drawings, specs, addenda, and RFIs to confirm all required work is accounted for, flag missing scope, overlaps, and risk items.

    === "Bad prompt (don't use)"
        ```text
        Check if my proposal covers everything.
        ```

        !!! warning "Why this fails"
            - Too broad; you won't get a structured breakdown or traceable proof.
            - Encourages high-level summaries instead of a line-by-line scope check.
            - No clear output for what's confirmed, what's missing, and what's risky.

    === "Good prompt (copy/paste)"
        ```text
        Task: Compare the proposal/scope of work below against the contract documents (drawings, specifications, addenda, RFIs, clarifications) and confirm all required work is accounted for.

        Context:
        - This is for scope leveling before submitting a final bid or before contract signing.
        - I will paste: (a) proposal/leveling sheet, (b) relevant drawing notes/sections, (c) relevant spec excerpts.

        Constraints:
        - Use ONLY the pasted text/documents.
        - Do not revise pricing; focus only on scope completeness.
        - If documents are silent on a scope item, write "Not stated."
        - Do not infer "typical scope" or add items not explicitly shown in the documents.

        Output (structured sections):
        1) **Confirmed Included Scope** (table)
           Columns: Scope item | Where stated in proposal | Where shown in contract docs (drawing/spec ref) | Notes

        2) **Potential Missing Scope** (table)
           Columns: Scope item | Where shown in contract docs | Why it appears missing from proposal | Risk level (High/Med/Low) | Proof (drawing/spec ref + quote)

        3) **Exclusions That Should Be Explicit** (bullets)
           - Items that appear unclear or could be interpreted as included but should be explicitly excluded in the proposal.

        4) **Assumptions / Clarifications** (bullets)
           - Assumptions that should be stated explicitly in the proposal (access, hours, phasing, means & methods, coordination, etc.).

        5) **Risk & Exposure Notes** (bullets)
           - Items that may lead to change orders or scope disputes; flag where drawings/specs conflict or are vague.

        6) **Quantity/Unit Alignment Check** (table, if applicable)
           Columns: Item | Proposal qty/unit | Drawing/spec qty/unit | Match? (Yes/No/Unclear) | Notes

        Verification:
        - Every line in Potential Missing Scope and Risk & Exposure must include proof (drawing/spec reference + short quote).
        - If you cannot confirm a scope item from the pasted documents, mark "Not stated" and list it under missing inputs needed.
        ```

        !!! tip "How to run this safely"
            - Paste one trade section or one proposal line item at a time (e.g., masonry scope vs masonry drawings/specs).
            - If the document set is large, break it into passes: base building scope first, then architectural finishes, then specialty items.
            - Spot-check 2–3 "Potential Missing Scope" items in the actual drawings/specs before flagging them as gaps.

---

??? example "Use case 2: Labor unit price (productivity-based)"
    **Goal:** Generate labor unit prices for a defined scope item based on clear assumptions (location, labor type, work classification, productivity basis) without including material, O&P, or indirect costs.

    === "Bad prompt (don't use)"
        ```text
        What's the labor cost for masonry work?
        ```

        !!! warning "Why this fails"
            - Too vague; no location, no labor type (union/open shop), no unit basis.
            - You'll get generic or unreliable numbers that can't be defended.

    === "Good prompt (copy/paste)"
        ```text
        Task: Provide labor unit prices for the described scope of work based on stated assumptions.

        Context:
        - This is for estimating; I need productivity-based labor pricing I can apply to quantities.
        - I will paste: (a) scope item description, (b) project-specific assumptions below.

        Assumptions (fill in before pasting):
        - Project location: [City/State]
        - Labor type: [Open shop / Union]
        - Work classification: [Masonry / EIFS / Façade / etc.]
        - Unit of measure: [SF / LF / EA / CY / etc.]
        - Productivity basis: [typical crew size/output if known, or state "use industry average"]

        Constraints:
        - Use ONLY the pasted scope description and stated assumptions.
        - Exclude: material costs, overhead and profit, scaffolding, protection, mobilization, equipment (unless explicitly included in scope description).
        - If productivity data is not provided, state the assumed productivity rate you used and mark it "Assumed (verify)."

        Output:
        1) Labor unit price table
           Columns: Scope item | Crew type | Productivity (units/day or hrs/unit) | Labor rate ($/hr) | Unit price ($/unit) | Assumptions used | Notes

        2) Missing inputs needed (bullets)
           - What additional productivity data, wage rates, or scope clarifications are required to finalize pricing.

        Verification:
        - Present results as $/unit.
        - If you assumed a productivity rate or wage not provided in the input, clearly mark it "Assumed (verify)" and explain basis.
        ```

        !!! tip "Practical add-on"
            - If you have historical productivity data or RS Means references, paste those alongside the scope and ask AI to compare/calibrate.

---

??? example "Use case 3: Material unit price (market conditions)"
    **Goal:** Generate material unit prices for specified materials based on current market conditions, tied to location and material spec, excluding labor/O&P/tax/equipment.

    === "Bad prompt (don't use)"
        ```text
        How much does brick cost?
        ```

        !!! warning "Why this fails"
            - No location, no material spec (type, finish, size), no unit basis.
            - You'll get a wide range or generic number that's not usable for an estimate.

    === "Good prompt (copy/paste)"
        ```text
        Task: Provide material unit prices for the specified materials based on current market conditions.

        Context:
        - This is for estimating; I need base material cost I can apply to quantities.
        - I will paste: (a) material type and specification, (b) project-specific inputs below.

        Inputs (fill in before pasting):
        - Project location: [City/State]
        - Material type and specification: [e.g., "Standard modular brick, smooth finish, ASTM C216 Grade SW"]
        - Unit of measure: [SF / LF / EA / Ton / etc.]

        Constraints:
        - Use ONLY the pasted material spec and stated location.
        - Include: base material cost (delivered to site if typical for this material type).
        - Exclude: labor, overhead and profit, sales tax, equipment, scaffolding (unless explicitly part of material package).
        - If current market pricing is not available in your data, state the source/basis you used and mark it "Estimated (verify with supplier)."

        Output:
        1) Material unit price table
           Columns: Material description | Unit | Base cost ($/unit) | Source/basis (market data year or "Estimated") | Lead time (if known) | Notes

        2) Missing inputs needed (bullets)
           - What supplier quotes, spec clarifications, or market data updates are required to finalize pricing.

        Verification:
        - Present pricing as $/unit.
        - If pricing is estimated or not current, clearly mark "Estimated (verify with supplier)" and note the basis used.
        ```

        !!! tip "Practical add-on"
            - If you have recent supplier quotes or material data sheets, paste them alongside and ask AI to extract/compare pricing.

---

??? example "Use case 4: Product specification summary (estimate + proposal ready)"
    **Goal:** Convert a product name, data sheet, or spec section into a concise specification summary suitable for estimate narratives and proposals.

    === "Bad prompt (don't use)"
        ```text
        Summarize this product spec.
        ```

        !!! warning "Why this fails"
            - Too open-ended; you'll get a paragraph instead of structured fields.
            - Misses key estimate-relevant details (installation requirements, warranty, limitations).

    === "Good prompt (copy/paste)"
        ```text
        Task: Based on the product name, data sheet, or specification section I paste below, generate a concise product specification summary suitable for an estimate and proposal.

        Context:
        - This will be used in estimate narratives and proposal documents; keep it clear and professional.

        Constraints:
        - Use ONLY the pasted product information.
        - Do not add "typical" product features not stated in the source.
        - If a field is not mentioned (e.g., warranty), write "Not stated."

        Output (structured format):
        **Product Name:** [Manufacturer + product line]  
        **Intended Use / Application:** [Brief description]  
        **Key Performance Properties:**  
        - [Strength, thickness, finish, fire rating, acoustic rating, durability, etc. as stated]  
        **Installation Requirements / Limitations:**  
        - [Surface prep, temperature limits, curing time, special equipment, etc. if stated]  
        **Warranty Information:**  
        - [Warranty period, coverage, conditions if available; otherwise "Not stated"]  
        **Source Reference:**  
        - [Data sheet title, spec section, page number]

        Verification:
        - If the pasted information is incomplete, list missing inputs needed (e.g., "Installation temp range not stated," "Warranty terms not provided").
        ```

        !!! tip "Practical add-on"
            - Use this for key products that appear in multiple estimate line items (EIFS, waterproofing, sealants, anchors, etc.).
            - Save the output as a reusable "Product Spec Card" you can reference across estimates and proposals.

---

!!! success "Remember"
    These prompts work best when you paste one scope section, one pricing input, or one product spec at a time and force structured outputs with proof.  
    Do not revise pricing during scope checks—focus on completeness and clarity first.  
    AI drafts and organizes; you review and decide.
