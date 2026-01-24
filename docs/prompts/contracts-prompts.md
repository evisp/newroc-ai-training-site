# Contracts – prompt templates

Use this page as a quick reference for “what good looks like” when prompting on New Roc contracts and subcontracts. 

!!! info "Where to find the full playbook"
    The complete Prompt Playbook (all use cases + full Prompt Builder template + data) lives in [Google Drive](https://docs.google.com/document/d/1Yb-2WvCVzolVvYIPCQPl_bWH8yYfs_62r8xMiSMoH8Y/edit?usp=drive_link). 

Below are short examples (bad prompt vs good prompt) designed to produce **usable AI** output: tables/checklists you can save, share, and verify.
The goal is the same as Session 1: keep scope tight, request a deliverable you can reuse, and require references so you can verify in the contract PDF. 

!!! warning "Golden rule"
    - No reference = not usable. 
    - If the contract doesn’t state it, the output must say **Not stated**.
    - Verify 2–3 critical items (cost/time/risk) in the PDF before relying on the output. 


## Contract prompt examples

??? example "Use case 1: Contract map (articles + exhibits + where to find what)"
    **Goal:** Build a quick “contract navigation map” so the team knows where scope, payment, schedule, changes, insurance, lien waivers, and special requirements live. 

    === "Bad prompt (don’t use)"
        ```text
        Summarize this contract.
        ```

        !!! warning "Why this fails"
            - Too broad, so you get a generic summary instead of a usable map. <!-- [file:2] -->
            - No structure = hard to verify and hard to reuse. <!-- [file:7] -->

    === "Good prompt (copy/paste)"
        ```text
        Task: Create a “Contract Map” from the text I paste/attach (subcontract + exhibit list/table of contents).
        Context: This is for PM + accounting + field handoff; we need to find key terms fast.
        Constraints: Use only the pasted text; don’t guess; if missing, write “Not stated.”
        Output format: 2 tables—(1) Articles/Sections map, (2) Exhibits/Attachments map; include clause/page refs for every row.
        Verification: List 5 items we must verify in the PDF before kickoff (time, money, risk, forms, notice).
        ```

        !!! tip "How to use this in the session"
            - Paste the contract’s table of contents + exhibit list first, then run deeper prompts per exhibit. 
            - Save the “Contract Map” with a link to the PDF so it’s defendable later. 


??? example "Use case 2: Scope of Work breakdown (scope exhibit / exhibit A)"
    **Goal:** Turn the scope exhibit into a clean scope table: line items, inclusions, exclusions, responsibilities, and required deliverables. 

    === "Bad prompt (don’t use)"
        ```text
        What is our scope in this contract?
        ```

        !!! warning "Why this fails"
            - The question is too open-ended; you’ll miss responsibilities, exclusions, and deliverables buried in the exhibit. 
            - No output format = you won’t get something you can track or review internally. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Build a “Scope of Work Breakdown” from the scope exhibit text below.
        Context: This is for kickoff; we need responsibilities/ownership and deliverables (submittals, schedules, safety, closeout).
        Constraints: Use only the pasted exhibit text; do not add “typical trade scope”; mark unclear items as “TBD / Not stated.”
        Output format: Table with columns: Scope line item | Included? | Excluded? | Owner (New Roc / GC-JV / Other / TBD) | Proof (clause/page) | Notes/Dependencies.
        Verification: Flag 10 high-risk scope gaps/assumptions to confirm before starting.
        ```

        !!! tip "Shortcut"
            - If the exhibit is long, paste it in chunks (2–4 pages at a time) and ask AI to append to the same table. 


??? example "Use case 3: Payment, retainage, and billing checklist (pay apps)"
    **Goal:** Extract the rules the PM + accounting team must follow to get paid: SOV requirements, pay app timing, retainage, and required backup (payroll, waivers, affidavits, insurance). 

    === "Bad prompt (don’t use)"
        ```text
        What are the payment terms?
        ```

        !!! warning "Why this fails"
            - “Payment terms” is bigger than one clause; you’ll miss conditions precedent, required attachments, and retainage rules. 
            - You won’t get a checklist the team can actually use each month. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Extract a “Billing Checklist” from the payment terms text I paste below.
        Context: This is for monthly pay apps; we need the exact required documents and timing.
        Constraints: Use only the pasted text; do not infer pay app forms or timelines; if not stated, say “Not stated.”
        Output format: (1) Table “Pay App Requirements” (Requirement | Who provides it | When due | Proof clause/page), (2) bullets “Retainage + release rules”.
        Verification: List the 5 most common reasons payment could be withheld based on this text.
        ```

        !!! tip "Practical add-on"
            - Append: “Write the checklist so it can be pasted into a monthly invoice email.” 


??? example "Use case 4: Change Orders + Unit Rates (how to price and get approval)"
    **Goal:** Pull out how changes must be submitted/approved, which backup is required, and how unit prices/markups apply. 

    === "Bad prompt (don’t use)"
        ```text
        Explain the change order process.
        ```

        !!! warning "Why this fails"
            - “Explain” usually returns a paragraph, not a process you can follow under time pressure. 
            - Missing structure makes it hard to confirm you met notice/backup requirements. 

    === "Good prompt (copy/paste)"
        ```text
        Task: Turn the change order + unit price text I paste below into a step-by-step “CO Playbook”.
        Context: This is for PMs; we need to submit changes correctly and avoid rejected backup.
        Constraints: Use only the pasted text; if approval/notice timing is not stated, write “Not stated.”
        Output format: (1) Numbered CO workflow (max 10 steps), (2) table “Required Backup” (Backup item | Applies when | Proof clause/page), (3) table “Markups/Unit Rates” (Rule | Cap/rate | Applies to | Proof).
        Verification: List 3 things we must confirm with the GC/Owner because they’re outside this excerpt.
        ```

!!! success "Remember"
    These prompts work best when you paste one section/exhibit at a time and force a table/checklist output with proof.  
    AI drafts and organizes; you review and decide. 
