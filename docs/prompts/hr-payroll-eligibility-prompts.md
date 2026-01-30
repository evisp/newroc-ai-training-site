# HR/Payroll – prompt templates (NJ/NY eligibility)

Use this page as a quick reference for “what good looks like” when prompting on employee eligibility checks across state jurisdictions (NJ, NY, or other multi-state scenarios).

!!! info "Where to find the full playbook"
    The complete Prompt Playbook (all use cases + full Prompt Builder template + data) lives in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link).

Below are short examples (bad prompt vs good prompt) designed to produce **usable AI** output: tables you can save, share, and verify.  
The goal is the same as Session 1: keep scope tight, request a deliverable you can reuse, and require references so you can verify in the source file.

!!! warning "Golden rule"
    - No reference = not usable (must point to file/field/row used).
    - If the data doesn’t state it, the output must say **Not stated**.
    - Verify 2–3 edge-case employees in the source file before relying on the output.


## HR/Payroll prompt examples

??? example "Use case 1: Data cleanup + “ready for eligibility” (before the decision)"
    **Goal:** Normalize employee records and flag gaps (missing work location, missing residence state, inconsistent IDs) so the eligibility analysis is not built on bad inputs.

    === "Bad prompt (don’t use)"
        ```text
        Clean this employee list.
        ```

        !!! warning "Why this fails"
            - Too vague; you won’t get a clear gap list or a usable output table.
            - Encourages “fixing” data by guessing instead of flagging missing fields.

    === "Good prompt (copy/paste)"
        ```text
        Task: Audit the employee data below for completeness and consistency so it can be used for NJ/NY eligibility review.

        Context: This is an HR/payroll dataset export. We need to identify missing/unclear fields before making any eligibility determinations.

        Constraints:
        - Use only the pasted data.
        - Do not infer missing values; write “Not stated.”
        - Do not merge people unless Employee ID clearly matches.

        Output:
        1) Table (Excel-ready): Employee ID | Full Name | Work location | State of residence | Job role | Data quality status (OK/Missing/Conflict) | Issue summary | Data source (file + row/field)
        2) Missing inputs needed (max 10 bullets): what fields HR must fill in to complete eligibility review.

        Verification: For every “Missing/Conflict” row, include Data source so HR can spot-check.
        ```

---

??? example "Use case 2: NJ/NY eligibility matrix (Finance request)"
    **Goal:** Determine which employees are eligible and compliant to work in New Jersey and New York based only on the attached HR/payroll files, with clear reasons and gaps flagged.

    === "Bad prompt (don’t use)"
        ```text
        Who can work in NJ and NY?
        ```

        !!! warning "Why this fails"
            - Too open-ended; you’ll get assumptions or generic rules.
            - No forced structure for Excel review or auditing.

    === "Good prompt (copy/paste)"
        ```text
        Act as an HR and payroll analyst.

        Using the data from the attached files, analyze all employees and determine which employees are eligible and compliant to work in: New Jersey and New York.

        For each employee, review the available information such as:
        - Work location
        - State of residence (if available)
        - Job role
        - Any state-specific requirements in the data

        Output requirements:
        - Create a table
        - One row per employee
        - Include the following columns:
          - Employee ID
          - Full Name
          - NJ Eligible (Yes / No)
          - NY Eligible (Yes / No)
          - Reason / Notes (explain why or why not, include the file + field/row used)

        Rules:
        - Base your determination ONLY on the information provided in the attached files
        - Do not assume missing data (write “Not stated” when needed)
        - Clearly flag any compliance or data gaps (use “Unclear” in Reason / Notes when a Yes/No cannot be supported)

        Output format:
        - Excel-compatible table
        ```

        !!! tip "How to run it safely"
            - Start with a small sample first (5–10 employees) to confirm the fields map correctly.
            - Spot-check 2–3 edge cases (multi-state, missing residence, unusual roles) back in the source before using the results.

---

!!! success "Remember"
    These prompts work best when you keep inputs controlled (one export/version at a time) and force an Excel-ready table with traceable proof (file + field/row).  
    AI drafts and organizes; you review and decide.
