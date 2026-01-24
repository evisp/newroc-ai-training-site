# JHA / Pre‑Task Plans – prompt templates

Use this page as a quick reference for “what good looks like” when prompting on JHAs / Pre‑Task Plans using method statements, sequencing notes, and layout instructions. 

These are **generic templates** you can reuse on any activity (demo, façade, concrete, interiors, etc.) as long as you paste the relevant method/sequence excerpt and ask for a table output with proof. 

For training, we use the [attached HSS install]() sequencing and tube layout MOP as an illustration input, but the prompt structure stays the same across projects. 

!!! warning "Golden rule"
    - Use only the text you paste (don’t add outside OSHA rules or “typical controls”).   
    - If the document doesn’t say it, write **Not stated** and list missing inputs.   
    - Treat outputs as drafts; a competent person must review before field use. 



## JHA / Pre‑Task prompt examples

??? example "Use case 1: Method/sequence → Activity-based JHA table (core deliverable)"
    **Goal:** Convert the method/sequencing excerpt into a job-ready hazard + mitigation table that can be copied into your standard JHA form. 

    === "Bad prompt (don’t use)"
        ```text
        Write a JHA for installing HSS tubes.
        ```

        !!! warning "Why this fails"
            - Encourages generic hazards and invented controls not tied to the method you’re actually using. 
            - You won’t get “proof” back to the source steps, so it’s hard to verify. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Turn the method/sequence text below into an activity-based JHA.
        Context: This is for a pre-task briefing; keep it field-usable and specific to the steps described.
        Constraints: Use only the pasted text; do not add outside standards; if a detail isn’t stated, write “Not stated.”
        Output: A table with columns: Activity step | Where it happens | Hazards | Controls/Mitigations | PPE/Tools noted in text | Proof (quote 3–8 words + page/section label from my excerpt).
        ```

        !!! tip "How to test on the attached files"
            - Paste 1–2 sections at a time from the MOP (e.g., “Installation Rods” + “Installation Tubes”) so the output stays tight. ]
            - Include the sequencing steps (Step 1–4) if you want the table to reflect the work flow by survey plate levels/mast climber.



??? example "Use case 2: Work areas + “what happens where” (turn steps into locations)"
    **Goal:** Extract a clear breakdown of *where* activities occur (façade, survey plate levels, mast climber position, recessed brick pocket openings) so the JHA is not generic. 

    === "Bad prompt (don’t use)"
        ```text
        Where does this work take place?
        ```

        !!! warning "Why this fails"
            - Too vague; you’ll get a one-paragraph guess instead of a usable location breakdown tied to the text. 

    === "Good prompt (copy/paste)"
        ```text
        Task: From the text below, list the distinct work areas/locations and what activities occur in each.
        Constraints: Use only the excerpt; don’t infer site logistics; mark unknowns as “Not stated.”
        Output: Table with columns: Work area/location | Activities performed there | Access/equipment mentioned | Key constraints (hours/levels/sequence) | Proof (short quote + page/section label).
        Verification: List 5 missing site inputs needed to finalize the location plan (e.g., access method, drop zones, material staging).
        ```


??? example "Use case 3: Competent-person references + sign-off roster (ready for form tool)"
    **Goal:** Produce the supporting pieces your example request calls for: competent-person role references and a crew sign-off roster concept (50 lines). 

    === "Bad prompt (don’t use)"
        ```text
        Add competent person info and sign off.
        ```

        !!! warning "Why this fails"
            - It doesn’t force role clarity, and it can lead to invented qualifications/titles. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Build the “Roles / Competent Person” section and a crew sign-off roster for this pre-task plan.
        Context: We will paste this into our standard JHA/Pre-Task form (fillable PDF will be made later).
        Constraints: Use only what’s stated in the excerpt; do not invent names or certifications; use placeholders (TBD) where needed.
        Output: (1) Table “Roles & Competent Person References” (Role | Responsibility | Trigger/When needed | Proof or Not stated), (2) Table “Pre‑Task Sign‑Off Roster” with 50 blank rows (Name | Company | Signature | Date).
        ```


??? example "Use case 4 (optional): One-page pre-task briefing script (foreman-ready)"
    **Goal:** Turn the same excerpt into a short script the foreman can read in 2–3 minutes, aligned with the JHA table. 

    === "Bad prompt (don’t use)"
        ```text
        Write a toolbox talk.
        ```

        !!! warning "Why this fails"
            - Too generic; not aligned to the actual steps/tools in the method statement. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Write a 2–3 minute pre-task briefing script based only on the excerpt below.
        Constraints: Keep it practical; include the top 5 “stop points” where we pause and re-check (if the excerpt states them); if not stated, write “Not stated.”
        Output: Title + 5 bullets (what we’re doing) + 5 bullets (main hazards & controls) + a short close (questions + sign-off reminder).
        ```


!!! success "Remember"
    - Paste one excerpt at a time and force table outputs—this keeps JHAs specific and checkable.   
    - If it isn’t stated in the method/sequence, mark it **Not stated** and ask for the missing input. 
