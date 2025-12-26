# Documents to Data Method (Excel + clear emails)

This page explains the **method** used in Session 2 to turn documents (PDFs, schedules, exports) into clean data and actions, such as Excel tables and short, actionable emails.   

It is designed to be repeatable across projects, even when the source documents change.   
The key idea is traceability: every table and email should be easy to verify back to the original source using a simple evidence pack (source link + prompt + version).   
Use this page for the "why" and the guardrails; use the [demos](./demos.md) and [exercises](./exercises.md) pages for the step-by-step practice.   


![Workflow](https://i.imgur.com/LRZQIai.jpeg)

## Goal (what "good" looks like)

By the end, you should have:

- A clean table in Excel that a teammate can use without rework.   
- An "evidence pack" record that shows where the data came from and what prompt was used.   
- A short status email that turns the table into actions (not confusion).   

This session focuses on repeatable habits: define the target table, extract carefully, clean consistently, spot-check against the source, then communicate clearly.   

## Workflow at a glance

### 1) Choose the source + define the table 
Start by deciding what you are extracting and what the table should look like.   

- Pick the source document type: spec table, schedule, detail index, export, etc.   
- Write down the target columns (names) and units (LF, SF, EA, dates, etc.).   
- Define the scope: page range, section range, or “only this table”.   

**Rule:** If you can't describe the table structure in one minute, extraction will be messy.   

![Mind Map](https://i.imgur.com/vcrghR1.jpeg)

### 2) Extract to a structured table 
Use a precise prompt to pull only what you need, in a spreadsheet-friendly format.   

- Request a CSV/table output for easy Excel import.   
- Tell the model the exact columns and units you want.   
- Tell it what to do when something is unclear (leave blank + flag in Notes).   

> **Rule:** Do not accept "filled in" guesses; missing data should be marked for review.   

### 3) Clean in Excel 
Cleaning turns "a table" into "usable data".   

- Standardize formats (dates, numbers, text).   
- Normalize units (don’t mix LF and FT, SF and SQFT, etc.).   
- Remove duplicates and fix obvious inconsistencies.   
- Add light structure if needed (drop-downs, validation, consistent status values).   

> **Rule:** Cleaning is where most time is saved later; do it once, do it right.   

### 4) Check against the source 
Verification builds trust and prevents downstream mistakes.   

- Spot-check 2–3 rows against the original document.   
- If something does not match, correct it and note it.   
- If the table seems incomplete, re-extract with clearer scope (pages/columns).   

> **Rule:** A quick spot-check is faster than fixing errors after the table is used.   

### 5) Write a clear email (5 minutes)
The email is not a summary of everything. It is a short action-oriented update.   

- Subject: state what changed or what is needed.   
- Body: 3 action bullets (Owner + action + due date if known).   
- Link/attach: point to the Excel table and evidence pack.   

**Rule:** If a reader cannot tell what to do next in 20 seconds, rewrite.   

## Evidence pack (traceability, not bureaucracy)

An evidence pack is a small record that makes your output auditable and reusable.   

Include:
- Source file name + where it’s stored (link/path) + page/section range used.   
- Exact prompt(s) used (copy/paste).   
- Table version/date + where the Excel file is saved.   
- Notes: assumptions, missing fields, open questions.   

![Evidence Pack](https://i.imgur.com/bV2Ao0B.jpeg)

## Quality gates (when to move to the next step)

Use these quick checks to avoid “pretty but wrong” outputs.   

- Before extracting: Columns and units are defined.   
- Before cleaning: Table has the right columns and reasonable row counts.   
- Before emailing: 2–3 rows verified against the source.   
- Before saving: Evidence pack captured (source + prompts + version).   

## Common pitfalls (and how to avoid them)

- **Pitfall:** AI invents values to "complete" the table.     
  - Fix: Require blanks for unknowns + "Notes" flags; verify sample rows.   

- **Pitfall:** Units drift (LF vs FT, SF vs SQFT, inconsistent dates).     
  - Fix: Specify units in the schema; normalize during cleaning.   

- **Pitfall:** Emails become long and vague.     
  - Fix: Use 3 action bullets; link to the table for details.   

## Close-out

> This method works when you treat the table as a shared project asset, not a one-time extract.   

Before you move on, make sure your outputs are saved where the team can find them and that the evidence pack makes the data easy to trace back to the source (source link + prompt + version).   

Next:
- For a guided walkthrough, go to [demos](./demos.md)   
- To practice end-to-end and build muscle memory, go to [exercises](./exercises.md)   
- To reuse the checklists and email scaffolds, go to [templates](./templates.md)
