# Labor model (safe estimating prompt)

AI can help you draft a clean, review-ready labor model faster (hours by scope item + assumptions list), so you can spend time on the decisions instead of reformatting notes.  
This is meant to support your estimating workflow—not replace it. 

!!! info "Use this when…"
    You have a scope excerpt + your takeoff, and you want AI to turn it into a **verifiable** labor-hour table you can adjust. 

!!! warning "Non‑negotiables"
    - Keep scope small (one section / one excerpt at a time). 
    - Require references (section/page) for anything you might reuse. 
    - If the document doesn’t say it, the output must say **Not stated**. 
    

## What you’ll get (outputs)

- A labor-hour table by scope line item (with “stated vs assumed” called out). 
- A short assumptions + risk flags list (what could move labor, and what to verify/ask). 


## What to paste (inputs)

Paste inputs in this order to keep the output tight and checkable. 

1. **Scope excerpt(s)** (trade scope, exhibit, spec section, or bid item descriptions).  
2. **Constraints excerpt(s)** that drive labor (Division 01 / conditions: access rules, housekeeping, daily debris removal, protection, working hours, etc.). 
3. **Your quantities** (table is fine: item | qty | unit | notes).  
4. Optional: **your crew plan / productivity assumptions** (only if you want the model to calculate hours from them).

!!! tip "Shortcut"
    If the exhibit/spec is long, paste it in chunks (2–4 pages at a time) and ask AI to **append** to the same table. 

## Which documents to start with

Use the document types that usually control “how we do it,” then align to how the job is priced/measured. 

- **Scope exhibit / trade scope (Exhibit A / scope sheet):** inclusions, responsibilities, schedule/shift expectations, and anything that implies extra handling/protection or coordination. 
- **Division 01 / General Requirements + Conditions:** labor-driving constraints (occupied building rules, protection, cleanup, waste removal, access limits). 
- **Unit Prices / SOV / bid forms:** make sure your labor model structure matches what you’ll price and how it’s measured, and avoid double-counting what’s already included in unit prices. 

!!! info "Unit price reminder (avoid double-counting)"
    Some bid forms state that unit prices include all necessary labor, scaffolding, material, overhead, profit, and taxes—treat that as the baseline when you’re deciding what belongs “inside” the unit price item vs. separate labor lines. 

## Copy/paste prompt (safe version)

```text
Task: Build a labor-hour model from the excerpts and quantities I paste.

Context:
- Project: [name]
- Trade: [trade]
- Why: I want a first-pass labor model (hours by scope item) + an assumptions list for estimate review.

Constraints:
- Use ONLY the text and quantities I paste.
- Do not assume crew size, productivity, access method, overtime, working hours, cleanup frequency, or sequencing unless stated.
- If something is missing, write “Not stated” and list it under Assumptions to confirm.
- Every requirement/constraint must include a proof reference (section/page or exhibit/page).
- Keep the output in tables (no long paragraphs).

Inputs I will paste:
1) Scope excerpt(s)
2) Division 01 / conditions excerpt(s) (if applicable)
3) My quantity takeoff table

Output format:

A) Table: Labor Model
Columns:
- Scope line item
- Qty
- Unit
- Labor drivers found in text (access, cleanup, protection, constraints)
- Crew size (Stated / Not stated)
- Production rate (Stated / Not stated)
- Calculated labor hours (show the math in plain text)
- Proof (section/page)
- Notes / dependencies

B) Table: Assumptions + risk flags
Columns:
- Assumption / risk
- Why it changes labor
- What to verify / who to ask
- Proof (section/page or “Not stated”)

Verification:
List 5 items I should spot-check in the PDF before I use these hours in pricing.
```


## What “good output” looks like

!!! success "Labor Model (example structure)"
    | Scope line item | Qty | Unit | Labor drivers found in text | Crew size (Stated/Not) | Production (Stated/Not) | Hours (math shown) | Proof (sec/page) | Notes |
    |---|---:|---|---|---|---|---:|---|---|

!!! success "Assumptions + risk flags (example structure)"
    | Assumption / risk | Why it changes labor | What to verify / who to ask | Proof |
    |---|---|---|---|


## What to watch for (cautions)

!!! danger "Caution 1: Confident guesses"
    AI will try to fill gaps with “typical practice” unless you force **Not stated**. 
    Remedy: Keep the constraints strict and require proof on every row. 

!!! danger "Caution 2: Too much text at once"
    Pasting huge sections at once can lead to missing items, mixed references, and output you can’t verify. 
    Remedy: One section / one excerpt at a time; append results. 

!!! danger "Caution 3: Hidden labor drivers in Division 01"
    Cleanup, waste removal frequency, protection, access restrictions, and occupied-building rules can move labor even when the trade scope looks simple. 
    Remedy: Always paste the relevant Division 01/conditions excerpt alongside the scope. 


## Golden rules (non‑negotiable)

- **No reference = not usable.** 
- **If it’s not stated, say so.** 
- **Verify before pricing:** spot-check 2–3 high-impact items (cost/time/risk) in the PDF. 
- **Keep scope tight:** one excerpt at a time. 
