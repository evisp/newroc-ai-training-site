# HR/Payroll Eligibility Checking 

HR and payroll files are dense: employee records, job roles, work locations, and state-related requirements are often spread across exports, forms, and notes.   
AI can help you structure that information into an Excel-ready eligibility view, but it only stays safe when you avoid assumptions and clearly flag missing data. 

!!! warning "Golden rule (use every time)"
    - **No reference = not usable.** If the output can’t point to the specific field/row/file it used, treat it as a draft only. 
    - If the data is missing, write **Not stated** (do not infer residence, work location, or eligibility). 
    - Verify a small sample (2–3 employees, especially edge cases) against the source file before you rely on the output. 

## Where AI helps

Use AI as a text assistant to extract and organize employee data into a consistent table (one row per employee) that HR/Finance can review quickly.   
Don’t use it as a “source of truth” for legal determinations; it can structure what’s in the files, but it can’t safely fill gaps or apply rules that aren’t provided. 

## What to look for

These are the high‑value data points to extract and validate early (before assigning work, mobilizing crews, or processing payroll across states): 

!!! success "1) Identity & role"
    - Employee ID and full name (consistent formatting; duplicates flagged). 
    - Job role / classification as stated in the files. 

!!! success "2) Location signals"
    - Work location / assigned site (as stated). 
    - State of residence (if present); if not present, mark **Not stated**. 

!!! success "3) State-specific requirements (only if present in the files)"
    - Any NJ/NY eligibility indicators in the dataset (e.g., required fields, restrictions, notes, forms). 
    - Clear flags for missing or conflicting records (example: two different states listed). 

## How to work (safe + fast)

Use the same 5-step prompting pattern as Session 1: Task, Context, Constraints, Output format, Verification.   
Keep scope small (one export or one dataset at a time), force an Excel-ready table, and require a “data source” reference per employee so HR can spot-check fast. 

!!! tip "Easy operating rhythm"
    Extract employee dataset → ask for one-row-per-employee eligibility table → flag gaps/conflicts → spot-check 2–3 edge cases → save the output with source file notes. 

## What you should produce

Aim to leave the review with reusable artifacts (not a paragraph summary): an “Eligibility Matrix” (NJ Eligible / NY Eligible with reasons) plus a “Data Gaps List” that HR can assign for follow-up.   
The next page contains short copy/paste prompts that generate these outputs from your specific HR/payroll files. 

## Templates & examples

Ready-to-copy prompts and examples live here:

- [HR/Payroll eligibility prompts](../../prompts/hr-payroll-eligibility-prompts.md)


![HR Payroll](https://i.imgur.com/QxUfKnt.png)

!!! success "Remember"
    AI drafts and organizes; you review and decide. 
