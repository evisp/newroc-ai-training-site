# Estimating – extracting scope, pricing inputs, and risk fast

Estimating packages are scattered: proposal language, leveling sheets, drawings/specs, addenda/RFIs, plus pricing assumptions and unit rates.   
AI can help you extract and organize these inputs quickly into estimate-ready artifacts, but it only stays safe when you keep scope tight, avoid assumptions, and verify key items back in the source. 

!!! warning "Golden rule (use every time)"
    - **No reference = not usable.** If the output can’t point back to the source (proposal page, leveling sheet line, drawing note, spec clause), treat it as a draft only. 
    - If the documents are silent, write **Not stated** (do not fill gaps with “typical scope” or “typical productivity”). 
    - Verify 2–3 critical items (scope gaps, unit assumptions, high-risk exclusions) in the PDF/doc set before relying on the output. 

## Where AI helps

Use AI as a text assistant to compare documents, extract what matters, and present it in job-ready formats (tables, checklists, structured sections) that an estimator can review fast.   
This is most effective when you feed it one excerpt at a time (proposal section, drawing note block, one spec section, one unit price ask) and require proof. 

## What to look for

These are the high-value estimating items to extract and verify early:

!!! success "1) Scope completeness (proposal vs contract documents)"
    - Confirmed included scope, stated in the proposal and aligned to the contract documents. 
    - Potential missing scope items that appear in drawings/specs but are not clearly included in the proposal. 
    - Scope overlaps or double-counted items. 
    - Exclusions that should be explicit, plus assumptions/clarifications that should be stated. 
    - Risk & exposure notes that could lead to change orders or scope disputes. 
    - Quantity/unit alignment checks (units, descriptions, and measurement basis consistency). 

!!! success "2) Unit pricing inputs (labor + material)"
    - Labor unit prices should be driven by stated assumptions: project location, labor type (open shop/union), work classification, and unit of measure. 
    - Labor unit prices should exclude material costs, overhead/profit, and items like scaffolding/protection/mobilization unless explicitly included. 
    - Material unit prices should be tied to material type/spec and unit of measure, include base material cost, and exclude labor, O&P, sales tax, and equipment/scaffolding unless stated otherwise. 

!!! success "3) Product specification summaries (estimate + proposal ready)"
    - Convert product names/data sheets/spec sections into a concise summary: manufacturer, intended use, key performance properties, installation limitations, and warranty (if available). 

## How to work (safe + fast)

Use the same 5-step prompting pattern: Task, Context, Constraints, Output format, Verification.   
Start by locking the scope first (what’s included/excluded/assumed), then support it with pricing assumptions and product spec summaries, and keep everything traceable to the source. 

!!! tip "Easy operating rhythm"
    Extract one excerpt → ask for a reusable table/sections → require references → verify 2–3 key items → save output with source links and “Not stated / missing inputs.” 

## What you should produce

Aim to leave estimating review with reusable artifacts (not a long narrative): a “Scope Leveling Summary” (included/missing/exclusions/assumptions/risks), a “Unit Price Assumptions Sheet” (labor + material basis), and short “Product Spec Cards” you can paste into an estimate narrative or proposal.   
The next page contains short copy/paste prompts that generate these outputs from your proposal, drawings/specs, and estimating inputs. 

## Templates & examples

Ready-to-copy prompts and examples live here:

- [Estimating prompts](../../prompts/estimating-prompts.md)


![Estimating](https://i.imgur.com/tmSlYqs.png)

!!! success "Remember"
    Do not revise pricing when you’re running scope completeness checks—focus on whether scope is fully accounted for and clearly stated. 
