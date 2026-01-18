# Templates (Prompt examples)

Use this page as a quick reference for “what good looks like” when prompting on New Roc documents.

!!! info "Where to find the full playbook"
    The complete Prompt Playbook (all use cases + full Prompt Builder template) lives in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link)

## Session 1 examples

Below are a few examples (bad prompt vs good prompt) to model the habits from Session 1: tight scope, job-ready output, and verification.

??? example "Use case: Section 013300 - Submittal quick checklist + schedule template"
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

??? example "Use case: Section 014000 - QA/QC Plan + Tests & Inspections Tracker"
    **Goal:** Produce a job-ready QA/QC package from Section 014000, including responsibilities, logs, and a “Schedule of Tests and Inspections” table.

    === "Bad prompt (don’t use)"
        ```text
        Write a quality control plan for a construction project at 140 E. Prospect Ave., Mount Vernon, NY.
        Use Section 014000 from the specs. Include tests, logs, and stuff like that. Make it professional.
        ```

        !!! warning "Why this fails"
            - Vague deliverables (“tests, logs, and stuff”) leads to generic output.
            - Missing enforceable structure (tables/templates/checklist).
            - No built-in verification checklist to QA the result.

    === "Good prompt (copy/paste)"
        ```text
        Task: Draft a Contractor Quality-Control Plan (QCP) package for submittal that is project-ready and executable in the field.

        Context:
        - Project: 140 E. Prospect Ave., Mount Vernon, NY 10550 (PE Project 0074871).
        - Spec basis: Section 014000 “Quality Requirements” (Design Development, Oct 24, 2025).

        Constraints:
        - Do not quote the specification text; write original, construction-ready procedures that comply with the spec intent.
        - State QCP submittal timing: submit within 10 days of Notice of Award and not less than 5 days prior to the preconstruction conference.
        - Clearly define Quality Assurance vs Quality Control, and state that testing/inspection does not relieve Contractor responsibility for Contract Document compliance.
        - Include implementable procedures for:
          a) Submittal review/management (who reviews, compliance checks, resubmittals).
          b) Testing/inspection coordination, including notifying testing agencies at least 24 hours before work requiring testing/inspection.
          c) Mockups: notification, review/approval gating before related work, maintaining mockups as workmanship standard, removal when directed.
          d) Preconstruction testing: specimens/assemblies provided by Contractor, intended installers used, testing agency reports compliance/deviations.
          e) Delegated design (when required): signed/sealed statement by responsible design professional including codes/loads/factors used.
          f) Nonconformance + corrective action: logging, correction, retesting/reinspection, documentation; include repair/protection after testing/inspection activities.
        - Clearly define responsibilities/limits for Owner, Contractor, testing agency, AHJ, Architect, and Commissioning Authority, including who bears retesting/reinspection costs when work is nonconforming.
        - Use placeholders where project specifics are unknown, and list the exact missing inputs needed to finalize (e.g., scopes/trades, known special inspections, commissioning scope, schedule milestones, etc.).

        Output (deliver in this order):
        A) QCP Narrative with clear headings:
           - QA/QC approach (QA vs QC definitions and intent)
           - Organization & qualifications (QC roles; minimum experience expectations)
           - Submittal QC procedures
           - Testing/inspection coordination process
           - Mockup procedure
           - Preconstruction testing procedure
           - Delegated design procedure (if applicable)
           - Nonconformance & corrective action workflow (including retesting/reinspection)
           - Reporting & document control
           - Closeout requirements (including record submittals/log turnover)

        B) “Schedule of Tests and Inspections” table with columns:
           - Spec Section number/title | Responsible entity | Test/inspection | Standards | Method | Frequency/quantity | Timing | Sampling | Notes

        C) Appendices (templates):
           - Test & Inspection Log
           - Nonconformance Report (NCR)
           - Corrective Action Log
           - Daily QC Report

        D) One-page Responsibility Matrix:
           - Owner | Contractor | Testing Agency | AHJ | Architect | Commissioning Authority

        Verification:
        At the end, include a verification checklist with YES/NO for:
        - QCP submittal timing is stated correctly.
        - QA vs QC are defined and Contractor responsibility disclaimer is included.
        - Tests/inspections responsibilities are clearly split (Owner vs Contractor vs others) and retesting cost responsibility is stated.
        - 24-hour notification to testing agencies is included.
        - The “Schedule of Tests and Inspections” table is present with all required columns.
        - All four templates and the responsibility matrix are included.
        - A clear “Missing Inputs Needed” list is provided.

        Spec text:
        [Paste the Section 014000 excerpt here]
        ```

??? example "Use case: Section 014339 - Mockup Execution Plan + Submittal Package"
    **Goal:** Create a step-by-step plan for exterior and room mockups with hold points so production work doesn’t move forward before approvals/testing are complete.

    === "Bad prompt (don’t use)"
        ```text
        We need mockups for this project. Write a mockup plan for the exterior and a room mockup.
        Include shop drawings, testing, and approvals. Keep it simple and professional.
        Also include the test standards.
        ```

        !!! warning "Why this fails"
            - Unclear scope (which mockups, which workflow, which deliverables).
            - Encourages invented details (standards, processes) if not in the excerpt.
            - No hold-point logic or verification checklist required.

    === "Good prompt (copy/paste)"
        ```text
        Task:
        Create a “Mockup Execution Plan + Submittal Package” that the GC can issue to subs and submit for review.
        The package must cover integrated exterior mockups and room mockups, including meetings, submittals, coordination, testing, approvals, and documentation.

        Context:
        - Project: 140 E. Prospect Ave., Mount Vernon, NY 10550 (PE Project 0074871).
        - Spec basis: SECTION 014339 – MOCKUPS (Design Development, Oct 24, 2025).
        - Related coordination (mention where relevant): Section 014000 (quality/acceptance baseline), Section 012100 (allowances), and enclosure commissioning coordination where mockup testing overlaps.

        Constraints:
        - Do not quote the specification text; write original, construction-ready procedures that comply with the spec intent.
        - Separate workflows for: (1) Integrated exterior mockups, (2) Room mockups, and (3) Preconstruction laboratory mockups (if applicable).
        - Include required submittals as distinct items: mockup shop drawings + delegated design for temporary structural supports + room mockup coordination drawings + testing agency qualifications + preconstruction test reports.
        - Include notification/review logic and “hold points” so that fabrication/production work cannot proceed until mockup approval/testing is complete.
        - Use placeholders where project details are unknown, and list the exact missing inputs needed to finalize (mockup location, dimensions, which façade/assemblies, room type/finish schedule, responsible testing agency, target dates, etc.).

        Output (deliver in this order):
        A) Mockup Execution Plan (headings: scope, roles, preinstall meeting agenda, logistics, sequencing, approvals/hold points, documentation, corrective actions).
        B) Submittal register entries (each with: spec ref, description, who prepares, who reviews, when due).
        C) Mockup Schedule (milestones + hold points + review durations).
        D) Mockup Testing Matrix table with columns:
           - Mockup type | Test | Standard | Purpose | Responsible party | Prerequisites | Frequency | Pass/Fail intent | Record required
        E) Templates (appendices):
           1. Preinstallation Conference agenda/minutes form
           2. Mockup inspection checklist (aesthetic/workmanship + interface coordination)
           3. Mockup test observation form
           4. Mockup issue / corrective action log
        F) “Open Items / Decisions Needed” list (what the team must confirm to finalize).

        Verification:
        At the end, include a verification checklist that answers YES/NO to:
        - Separate procedures provided for integrated exterior vs room mockups.
        - All required submittal types listed as distinct deliverables.
        - Hold points defined before corresponding work proceeds.
        - Testing matrix includes standard, responsibility, prerequisites, and records.
        - Templates included and usable without additional editing.
        - Missing inputs list is explicit (who must provide what by when).

        Spec text:
        [Paste the Section 014339 excerpt here]
        ```

??? tip "Prompt Builder Template (turn rough requests into good prompts)"
    **Goal:** Convert an employee’s plain-language request into a structured, ready-to-run prompt:
    **Task → Context → Constraints → Output format → Verification**.

    **Use this when:** someone asks “Can AI help with this?” but the request is vague, and you need a consistent, job-ready output (tables/templates + a quick QA checklist).

    === "Copy/paste (Prompt Builder)"
        ```text
        PROMPT BUILDER ROLE
        You are a “Prompt Builder” for construction specification and contract workflows.
        Convert the employee request below into a final, ready-to-run AI prompt that follows this structure exactly:
        Task → Context → Constraints → Output format → Verification.

        CONTEXT (WHAT YOU CAN ASSUME)
        The employee may provide:
        - Their goal in simple words
        - Any known project / spec section references (optional)
        - Any required stakeholders (Owner / Architect / CM / AHJ / testing agency) (optional)
        - Any must-follow rules or timing (optional)

        If details are missing, ask only the minimum clarifying questions OR use placeholders and list the missing inputs explicitly.

        CONSTRAINTS (FOR YOU, THE PROMPT BUILDER)
        - Output ONLY the final structured prompt (no extra commentary).
        - Keep it practical and jobsite-usable (not academic).
        - Avoid quoting any spec text verbatim; write original instructions.
        - Do not invent project facts; use placeholders like <TBD> or <Insert…>.
        - Make constraints enforceable (use clear “must/shall/include” language).
        - Ensure the Output format section forces tables/templates when the task implies them.
        - Ensure Verification contains a YES/NO checklist to QA the downstream output.

        OUTPUT (WHAT YOU MUST PRODUCE)
        Produce a single block titled “READY PROMPT” with these sections, in this order:

        READY PROMPT

        TASK
        (One short paragraph describing exactly what the downstream AI must produce.)

        CONTEXT
        - Project:
        - Document type:
        - Spec/contract basis (section/date):
        - Stakeholders:
        - Assumptions/placeholders:

        CONSTRAINTS
        - (Bullet list: timing, responsibilities, process requirements, do/don’t rules.)
        - Use only the text provided (no outside standards/assumptions) if document text will be pasted.

        OUTPUT FORMAT (IN THIS ORDER)
        A) ...
        B) ...
        C) ...
        (Include specific tables with required column headers, plus templates as appendices if needed.)

        VERIFICATION
        - YES/NO checklist items confirming the output meets requirements.
        - Missing Inputs Needed (who must provide what).

        EMPLOYEE REQUEST (RAW)
        <<<
        Paste the employee’s plain-language request here verbatim.
        >>>
        ```

    !!! warning "Reminder"
        This template improves consistency, but the downstream output is still a draft-verify against the source document before relying on it.


## Want the full Prompt Playbook?

??? info "More examples + full Prompt Builder (Google Drive)"
    All use cases and the full Prompt Builder template are here:  
    https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link
