# Templates (Prompt examples)

Use this page as a quick reference for “what good looks like” when prompting on New Roc documents.

!!! info "Where to find the full playbook"
    The complete Prompt Playbook (all use cases + full Prompt Builder template) lives in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link)
    


## One example (Session 1)

Below is one full example (bad prompt vs good prompt) to model the habits from Session 1: tight scope, job-ready output, and verification.  


??? example "Use case: Section 013300 — Submittal quick checklist + schedule template"
    **Goal:** Turn Section 013300 into a practical checklist and a “submittal schedule” table that PMs/supers can use during project setup.

    === "Bad prompt (don’t use)"
        ```text
        Read this document and tell me what it says about submittals.
        Also, summarize any important requirements.
        ```

        !!! warning "Why this fails"
            - Too broad (“read this document”) and encourages generic summaries.
            - No required output format (hard to reuse).
            - No proof requirement (not verifiable).

    === "Good prompt (copy/paste)"
        ```text
        Task: Build a “Submittal Procedures – quick checklist + schedule template” from Section 013300.

        Context: This is for New Roc’s day-to-day project setup so PMs and supers can submit correctly and on time.

        Constraints:
        - Use only the attached Section 013300 content.
        - Do not add outside standards, assumptions, or typical industry practices.
        - Keep it practical and concise.

        Output format:
        1) A table titled “Submittal Schedule Template (Fields Required)” with one row per required field/column.
           - Columns: Field/Column name | What it means (plain language) | When it matters | Notes/Dependencies

        2) A bullet list titled “Submittal Rules (Do/Don’t)” covering:
           - What must be included in each submittal package
           - Electronic/PDF packaging and naming expectations
           - Coordination/concurrent submission expectations
           - Review time allowances and what they imply for planning
           - Resubmittal requirements
           - Distribution requirements and “use for construction” rules

        Verification:
        - After every table row and every bullet, add:
          - The exact spec reference (e.g., 1.3.A, 1.4.A, 1.5.C, etc.), and
          - The page label shown in the footer (e.g., 013300-3).
        - If the document does not explicitly state something, write: Not stated in Section 013300.

        Spec text:
        [Paste the Section 013300 excerpt here]
        ```

        !!! tip "How to use this in the session"
            - Paste only the extracted Section 013300 text (not the full spec book).
            - After you get the output, spot-check 2–3 items in the PDF using the references.
            - Save the verified result with a link back to the source file.

## Want more examples?

??? info "More use cases (Google Drive)"
    Additional examples (Section 014000 QA/QC plan, Section 014339 mockup plan, and the full Prompt Builder) are in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link)
