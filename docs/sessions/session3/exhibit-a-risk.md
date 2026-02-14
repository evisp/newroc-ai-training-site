# Exhibit A (Scope Exhibit)

Turn a subcontract **Exhibit A – Scope of Work** into job-ready tables (scope ownership, deliverables, schedule/safety/insurance obligations, and a risk + open-issues log) that your team can verify and reuse. 

!!! info
    Use this page when you need to translate Exhibit A language into: (1) a kickoff scope matrix, (2) a “what we owe” checklist, and (3) a risk log you can escalate early. 


## What to extract

Exhibit A usually contains far more than “trade scope”—it often pulls in other exhibits, sets schedule rules, assigns logistics responsibilities, and creates backcharge / rework risk. 

Extract these **four buckets** every time:

- **Scope**: inclusions, exclusions, and “complete system” language (anything that can expand what’s included).
- **Responsibilities**: who provides / furnishes / installs, coordination duties, permits, protection, testing.
- **Deliverables**: submittals, schedules, QA/QC plans, closeout documents, warranties, trainings.
- **Commercial risk triggers**: overtime / recovery, standby costs, backcharges, “no payment until…”, notice and approval gates.

!!! important
    The goal is not a summary; it's a set of tables your PM, field, and accounting teams can act on. 

## Non‑negotiables

!!! warning
    Golden rule: **No reference = not usable**. 

!!! warning
    If the contract does not state it, the output must say **Not stated** (or “TBD / missing input”), not “typical practice.” 

!!! note
    Keep the scope small (one exhibit / one excerpt at a time) so the output stays tight and checkable. 

!!! tip
    Verification habit: require clause/page references, then spot-check 2–3 high-impact items (time/money/risk) directly in the PDF before you rely on it. 


## Repeatable workflow

1. **Attach the Exhibit A PDF** (or paste 2–4 pages at a time if needed). 
2. **Run “Exhibit Map” first**: list incorporated exhibits/attachments and where they appear in Exhibit A. 
3. **Extract tables** (templates below) with “Proof” on every row.
4. **Flag gaps**: missing referenced documents, undefined responsibilities, ambiguous boundaries. 
5. **Escalate with questions**: generate a short, prioritized RFI/clarification list for JV/GC/Owner. 

!!! success
    What you should leave with: one reusable prompt + one verified table/checklist tied to clause/page references + a saved note linking back to the source PDF. 

## Output templates

Use these table shapes so the output is immediately usable (Excel-ready) and easy to review internally. 

### A) Scope + responsibility breakdown

| Scope line item | Included? | Excluded? | Owner (Sub/JV/Owner/TBD) | Deliverables (submittals/tests/closeout) | Dependencies / coordination | Proof (clause/page) | Notes |
|---|---:|---:|---|---|---|---|---|

**Guidelines**

- Write scope as **line items**, not paragraphs (one obligation per row). 
- Capture exclusions explicitly (if Exhibit A has a “Work Not Included” section, mirror it row-by-row). 
- If the Exhibit A references other documents (safety manual, OCIP, insurance exhibit), add a row noting “requirements live in referenced doc—missing copy.” 

### B) Schedule / safety / insurance obligations

| Topic | Requirement | Who must comply | Cost / risk if missed | Proof (clause/page) |
|---|---|---|---|---|

**Typical topics to look for**

- Working hours restrictions, weekend rules, overtime recovery language. 
- Safety meetings, PPE requirements, barricade/protection rules. 
- Insurance/OCIP obligations that are incorporated by reference. 

### C) Deliverables checklist (kickoff → closeout)

| Deliverable | When due (if stated) | Format / content | Acceptance gate (if any) | Proof (clause/page) | Notes |
|---|---|---|---|---|---|

**Deliverables to watch**

- Submittal schedule, construction schedule, SOV, site-specific safety plan, QA/QC plan. 
- Testing/inspection reports, warranties, O&M manuals, as-builts, attic stock/spares. 

### D) Risk register + open issues

| Risk / open issue | Trigger language (short) | Impact (time/money/liability) | Mitigation / question | Owner | Proof (clause/page) |
|---|---|---|---|---|---|

!!! tip
    Treat “complete system,” “best practices,” “AHJ requirements,” and “at no additional cost” language as automatic risk triggers that deserve their own rows. 

## Prompt pack (copy/paste)

These prompts follow the same “Task, Context, Constraints, Output format, Verification” structure used elsewhere in this playbook. 
They are written to force **deliverables (tables/checklists)** with proof references, not narrative summaries.

!!! note
    Replace bracketed fields like `[PROJECT NAME]` and `[EXHIBIT NAME]` before you run them. 

### Prompt 1: Exhibit Map (navigation first)

Goal: Build a quick navigation map of what documents Exhibit A pulls in (and where), so you don’t miss hidden requirements.   

Goal: Produce a “missing inputs” list early (safety manual, insurance exhibit, OCIP manual, etc.) before kickoff decisions get made. 

```text
Task
- Create an Exhibit Map from the attached Exhibit A.

Context
- Project: [PROJECT NAME].
- Document: [EXHIBIT NAME + DATE + REV].
- This is for PM/field kickoff so we can find key requirements fast.

Constraints
- Use only the attached Exhibit A text.
- Do not guess.
- If the Exhibit A references another document we don’t have, write “Missing—need copy.”

Output format
- Table: Referenced document | Date (if stated) | What it controls (1 line) | Where referenced (clause/page).

Verification
- List 5 referenced documents/sections we must obtain or review before kickoff.
```

### Prompt 2 — Scope + responsibility breakdown (the main table)

Goal: Turn Exhibit A into a scope matrix your PM/field team can review line-by-line (what’s included, what’s excluded, and who owns it).   
Goal: Surface coordination and “complete system” obligations that often drive extras, rework, or backcharges if missed. 

```text
Task
- Build a Scope of Work Breakdown from Exhibit A.

Context
- This is for kickoff and estimating alignment.
- We need inclusions, exclusions, responsibilities, and deliverables.

Constraints
- Use only Exhibit A text.
- Do not add typical trade scope.
- If unclear or silent, write “Not stated.”

Output format
- Table with columns:
- Scope line item | Included? | Excluded? | Owner (Sub/JV/Owner/TBD) | Deliverables | Dependencies/coordination | Proof (clause/page) | Notes.

Verification
- Flag 10 high-risk ambiguities or scope gaps we should clarify before starting.
```

---

### Prompt 3: Deliverables + gates (“no pay until…”)
Goal: Extract what must be submitted (submittals/schedules/plans/closeout) so nothing blocks procurement, mobilization, or payment.   
Goal: Identify acceptance gates (e.g., “no payment until…”) so accounting and PMs don’t learn the hard way. 

```text
Task
- Extract a Deliverables Checklist and identify acceptance/payment gates stated in Exhibit A.

Context
- This is for PM + accounting handoff (avoid missing a required submission).

Constraints
- Use only Exhibit A text.
- If timing is not stated, write “Not stated.”

Output format
- 1 table: Deliverable | Due timing | Who submits | Acceptance gate | Proof (clause/page).

Verification
- List the top 5 reasons payment/work authorization could be delayed based on Exhibit A language.
```

### Prompt 4: Risk register + clarification questions
Goal: Convert “you own it” language into a clean risk register with proof references so the team can escalate early.   
Goal: Generate a short set of clarification questions prioritized by cost/schedule exposure (missing docs, unclear boundaries, coordination traps). 

```text
Task
- Create a risk register and a clarification question list based only on Exhibit A.

Context
- We want early clarity on scope boundaries, coordination duties, schedule recovery exposure, and referenced docs we don’t have.

Constraints
- Use only Exhibit A.
- Include “Trigger language (short)” and “Proof (clause/page)” on every row.
- If it’s not stated, say so.

Output format
1) Risk table:
Risk / open issue | Trigger language (short) | Impact (time/money/liability) | Mitigation / question | Owner | Proof (clause/page).
2) 10 clarification questions, prioritized by cost/schedule risk.
```

??? example "Live demo (this project)"
    Use the prompts above on: **50 Hudson Street, Jersey City, NJ — JV Exhibit A “Scope of Work EIFS”, Project 2464JV, BP 10B, dated 01/20/2026 (Rev 00)**.   
    Exhibit A explicitly lists incorporated JV documents (e.g., Safety Logistics Plan, Exhibit 1A Safety Requirements, Exhibit D Insurance Requirements, Exhibit R OCIP Manual), which makes it a strong example for the “Exhibit Map → Missing docs → Risk log” flow.   
    It also contains schedule/working-hours language, safety requirements, a deliverables submission requirement, and trade-specific scope items like testing/compatibility and warranty language—ideal for demonstrating all four output buckets. 
