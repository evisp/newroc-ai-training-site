# Who owns what (Permits / debris / safety) 


This page shows how to spot ownership language early, translate it into line items/allowances/exclusions, and issue tight bid clarifications with clause/page proof. 

!!! info
    Use this page during takeoff/bid leveling and again before you finalize inclusions/exclusions.

## Documents used for illustration

AI is most helpful here when it can quickly scan the *usual places* these requirements live and turn them into a simple ownership/pricing checklist with clause/page proof. 

For illustration on this page, we use:

- **Subcontract Scope Exhibit (Exhibit A)**: *50 Hudson Street — JV Exhibit A (EIFS)*, which is a good example of broad “provide/furnish/install” definitions and explicit responsibilities around permits/approvals and safety/protection. 

- **Division 01 / General Requirements + Conditions**: *445 E 80th Street — Project Manual* (Division 01 + conditions), which clearly assigns permit/fee responsibility and sets debris/waste disposal and cleanup expectations. 

!!! note
    Swap these examples for any active project; what matters is using the same document types so you don’t miss a cost item that’s “not in the trade spec,” but still in the bid documents. 

!!! important
    Always bring the same three sections into estimating review: the scope exhibit (Exhibit A), Division 01 (Temporary Facilities / Execution / Admin Provisions), and any safety/OCIP/logistics exhibits incorporated by reference. 


## What to price (estimating view)

Treat “who owns what” as a **pricing checklist**; every item should become (1) a line item, (2) an allowance, or (3) an exclusion/clarification.

### Permits & approvals
Common cost drivers to look for:

- Language that subcontractor/contractor must “file for and obtain all permits and approvals,” and pay filing/permit/expeditor fees (or reimburse JV/Owner if they pull them). 
- Language stating contractor “shall procure and pay” permit/utility connection fees and deliver copies of permits/certificates. 

Pricing actions:

- Decide: include as lump sum **Permit Admin** line, or break out (DOB permit, DOT, hoisting, scaffold, site safety plan filing, expeditor). 
- Add a bid clarification when the exact permit set is not listed (“List all permits assumed included; confirm which permits will be pulled by Owner/JV vs trade”). 

### Debris, waste, housekeeping

Common cost drivers to look for:

- “Contractor responsible for legally disposing of all waste” and “material must be removed daily.” 
- Daily cleanup language and “broom clean” requirements; disposal container rules may sit in conditions/Division 01. 

Pricing actions:

- Include dumpsters/containers, haul-out labor, trucking, tipping fees, manifests, and daily housekeeping labor. 
- If the project is constrained (no staging, limited access hours), carry a productivity factor and/or add a clarification for staging and haul routes. 

### Safety, protection, and temporary measures

Common cost drivers to look for:

- Broad “subcontractor shall provide … protection … safety … PPE … fire extinguishers … meetings” style scope language. 
- Requirements to provide/maintain barricades/guardrails/temporary walkways and protection against weather/water intrusion (often buried in conditions). 

Pricing actions:

- Carry costs for temporary protection (tarps, shrink wrap, dust barriers), barricades, signage, flagmen/traffic control when required, and weekend/holiday maintenance of protection if required. 
- If “standby trades” (site safety, temporary power, laborers, hoist/crane ops) can be charged to the subcontractor when working off-hours, price the risk or qualify it. 

!!! warning
    If the document says “complete job/complete system” or “better quality/greater quantity/higher cost,” assume scope expansion risk and protect your bid with clarifications tied to proof references. 


## Estimating deliverables 

### 1) Ownership → pricing matrix

| Category | Item (plain language) | Owner (Us / GC/JV / Owner / Other / TBD) | Estimating treatment (Include / Allowance / Exclude / Clarify) | Cost drivers (1 line) | Proof (clause/page) |
|---|---|---|---|---|---|

!!! tip
    “TBD” is acceptable during estimating only if you also create a clarification question and track it to close before final bid. 

### 2) Bid clarifications / inclusions-exclusions list (short and sharp)
Write them so they can be pasted into your proposal letter and used for bid leveling.

**Template**
- Included: …
- Excluded: …
- Assumptions: …
- Clarifications requested (RFI): …

!!! note
    If it’s not stated, say **Not stated**—don’t fill gaps with typical practice. 

### 3) Risk & allowance register (estimating)
| Risk item | Trigger language (short) | Exposure (time/cost) | Pricing approach (carry/allow/qualify) | Proof (clause/page) |
|---|---|---|---|---|


## Prompts (copy/paste)

These prompts are designed for estimating outputs: pricing matrix + clarifications + allowances/risk log, with clause/page proof. 

!!! important
    Golden rule: **No reference = not usable**. 

### Prompt 1 — Extract “who owns what” (estimating matrix)

Goal: Build a single table that tells estimating what to carry (permits, waste, safety/protection) and who owns each item. Force clause/page proof so you can defend inclusions/exclusions in bid leveling. 

```text
Task
- Create an estimating “Who owns what” matrix focused on permits/approvals, debris/waste/housekeeping, and safety/protection.

Context
- Project: [PROJECT NAME].
- Document(s): [EXHIBIT A NAME] and/or [DIV 01 / CONDITIONS SECTION].
- This is for estimating—each item must map to a pricing treatment (Include/Allowance/Exclude/Clarify).

Constraints
- Use only the provided text.
- Do not guess.
- If ownership or requirement is unclear, write “TBD / Not stated”.
- Every row must include Proof (clause/page).

Output format
Table:
Category | Item (plain language) | Owner (Us/GC-JV/Owner/Other/TBD) | Estimating treatment (Include/Allowance/Exclude/Clarify) | Cost drivers (1 line) | Proof (clause/page).

Verification
- List the 10 highest-cost / highest-risk rows and why they matter (1 line each).
```

### Prompt 2 — Turn the matrix into bid clarifications + exclusions
Goal: Produce a proposal-ready list that protects you from scope creep and makes bid leveling clean. Convert “TBD” items into specific, answerable questions tied to proof references. 

```text
Task
- Draft proposal inclusions/exclusions, assumptions, and bid clarifications from the matrix above.

Context
- Project: [PROJECT NAME].
- Audience: GC/JV/Owner estimator for bid leveling.

Constraints
- Use only items from the matrix above.
- Do not add trade “typical” items.
- Keep it to one page worth of bullets if possible.

Output format
1) Included (bullets)
2) Excluded (bullets)
3) Assumptions (bullets)
4) Clarifications requested (numbered list, each with trigger clause/page)

Verification
- For any exclusion that could be disputed, suggest an alternate: “Include as allowance of $____ subject to ___” (leave $ blank if unknown).
```

### Prompt 3 — Allowances and unit-price candidates (permits/debris/safety)
Goal: Identify which “who owns what” items are best handled as allowances or unit prices because quantities are uncertain (dumpsters/tons, daily cleanup hours, permit counts, flagmen days).  Reduce bid risk without hiding scope. 

```text
Task
- From the provided Exhibit A / Division 01 language, propose an allowances + unit-price list for permits, debris/waste, and safety/protection.

Context
- Project: [PROJECT NAME].
- We want to reduce estimating risk where quantities are unknown.

Constraints
- Use only the provided text.
- If the contract already assigns a fixed obligation, do not convert it into a unit price—flag it as a fixed-cost risk instead.
- Include Proof (clause/page) per line item.

Output format
- Table:
Line item | Recommended structure (Allowance / Unit price / Lump sum) | Suggested unit (if unit price) | What’s included | Proof (clause/page) | Notes.

Verification
- List any items that should be clarified before bid close (max 10).
```

??? example "Illustration sources"
    Exhibit A example: **50 Hudson Street — JV Exhibit A (EIFS)** includes broad responsibilities (“provide… permits… protection… insurance”), explicit safety/protection requirements, and explicit permit/approval duties with fees/reimbursements.   
    Division 01 / conditions example: **445 E 80th Street — Project Manual** includes contractor responsibility to procure/pay permit-related fees and to legally dispose of waste with daily removal/cleanup language. 
```