# Estimating Overview Page — Spec-to-Estimate Scope Matrix (STM)

This page is a reusable internal guide for building a “Spec-to-Estimate Scope Matrix” that turns contract documents into estimator-ready bid line items (scope + inclusions/exclusions + submittals/QA/testing + warranties), and makes gaps obvious early (RFIs instead of hidden assumptions).

## 1) What an STM is (and why we use it)

**STM = a one-table bridge between specs and the estimate.**  
It helps estimators, PMs, and subcontractor bidders all price the *same scope*, because it translates narrative requirements into line items and checklists.

**Best time to create it:** right after receipt of the bid set (before takeoff and before vendor RFQs), and update it with each addendum.

> !!! Rule of thumb: If it affects cost, schedule, or acceptance, it must show up in the STM row for the line item that will “carry” it.


## 2) How to build an STM (generic workflow)

### Step-by-step
1. **List your inputs** (specs, drawings, addenda, bid forms, existing conditions). Mark what’s missing.
2. **Define bid line items first** (use the project’s SOV/Unit Price/Alternates if provided; otherwise use your internal WBS).
3. **For each line item, extract requirements** from the controlling spec sections:
   - Scope included (materials, accessories, “incidental” items the spec makes mandatory)
   - Exclusions/clarifications (by others, not in contract, or ambiguous)
   - Submittals (product data, MSDS, samples, schedules, qualifications)
   - QA / testing / mock-ups (lab tests, field tests, manufacturer rep involvement, certifications)
   - Warranty (term + trigger date wording)
4. **Add a “Risk flags / RFIs” field** to each row:
   - Missing drawings, missing quantities, unclear access, conflicting warranty triggers, unknown substrate conditions, etc.
5. **De-duplicate**: if a requirement repeats, keep one entry (cite the first or most specific reference).

### STM table format (recommended)
Use one table, with consistent columns:

- **Spec Section(s)**: where the requirements come from (one row can cite multiple sections)
- **Bid line item**: what we will price (or carry as allowance/LS)
- **Unit + quantity basis**: SF/LF/EA/LS and whether it’s measured from drawings, allowance, unit price, or field-verified
- **Scope included**
- **Exclusions/clarifications**
- **Submittals**
- **QA/Testing/Mock-ups**
- **Warranty**
- **Risk flags / RFIs**
- **Page**: printed spec page ID if available; otherwise “PDF p.__”

### Quality bar (what “good” looks like)
- Div 1 requirements are treated as real cost drivers (not “overhead hand-waving”).
- Every row answers: “What do I need to carry so the work gets accepted?”
- Unknowns become RFIs (not assumptions).

## 3) Prompt #1 (generic, reusable)

Copy/paste this prompt for any project:

```text
You are creating a company estimating deliverable titled:
“Estimating Overview — Spec-to-Estimate Scope Matrix (STM)”.

CONSIDER THE ATTACHMENTS PROVIDED
- Use only the attached documents.
- List every attachment used by filename under “Inputs received”.
- If any of the input categories below are not provided, state “Not provided” and add them to “Missing inputs”.

INPUT CATEGORIES (map attachments into these buckets)
- Specs / Project Manual: <SPEC_PDF_FILENAME or “Not provided”>
- Drawings set (plans/elevations/details): <DRAWINGS_PDF_FILENAME or “Not provided”>
- Addenda/Bulletins/RFI responses: <ADDENDA_FILENAMES or “Not provided”>
- Bid forms (SOV / Unit Prices / Alternates) if separate: <BID_FORMS_FILENAMES or “Included in specs” / “Not provided”>
- Existing conditions docs (survey/photos/hazmat/FISP/probes): <EXISTING_CONDITIONS_FILENAMES or “Not provided”>

GOAL
Produce ONE Markdown page that is useful to estimators and PMs. It must include:
1) Inputs received vs Missing inputs (bullets).
2) The STM table (rows = bid line items; deduplicate repeats).
3) Estimator QA checklist (short bullets).
4) Open items / RFIs (short bullets).

STRICT RULES
- Use only information in the attachments; no outside assumptions.
- Do not guess quantities, manufacturers, or scope. If not explicit, write “Not stated”, “Not provided”, or “TBD”.
- Do not invent drawing details. If drawings are referenced but not attached, flag as a Risk + RFI.
- Capture Division 1 / administrative requirements when they create cost, schedule, submittal, QA/testing, access, or acceptance obligations. [file:2]
- If warranty triggers differ across sections, flag as “Risk” and draft an RFI.
- Cite the exact spec section(s) and page ID for each row (printed spec page ID if visible; otherwise “PDF p.__”).

STM TABLE (single Markdown table, exact columns)
Spec Section(s) | Bid line item | Unit + quantity basis | Scope included | Exclusions/clarifications | Submittals | QA/Testing/Mock-ups | Warranty | Risk flags / RFIs | Page
```

## 4) Prompt #2 (specific to our current documents: 445 E 80th St)

### Inputs we currently have
- `445-E80th-St-Project-Manual-01.23.2026.pdf` (Facade Repairs Project Manual). 
- The manual’s Table of Contents lists bid forms and key sections including 00003 Proposal/SOV, 00005 Unit Prices, Div 1 sections, 040120.91 Masonry Restoration, 079200 Joint Sealants, and 098700 Coatings. 
- The manual lists a drawing index (T-001.00, A-101.00, A-201.00, A-202.00, A-203.00, A-501.00, A-901.00), but the drawing sheets themselves are not confirmed as included in the current attachment. 

Copy/paste this prompt to generate the STM overview page for this bid set:

```text
You are creating a company estimating deliverable titled:
“Estimating Overview — Spec-to-Estimate Scope Matrix (STM)”.

PROJECT
445 East 80th Street, New York, NY — Facade Repairs

CONSIDER THE ATTACHMENTS PROVIDED
- Review all attached files and list them under “Inputs received”.
- Identify and list “Missing inputs” that typically block a complete estimate (e.g., drawings, addenda/RFIs, existing-conditions reports), but only if they are not attached.

GOAL
Produce ONE Markdown page our estimators/PMs can use immediately:
1) Inputs received vs Missing inputs.
2) A Spec-to-Estimate Scope Matrix (STM) table aligned to the bid structure found in the documents (SOV/Unit Prices if present).
3) Estimator QA checklist (short bullets).
4) Open items / RFIs (short bullets).

STRICT RULES
- Use only information in the attachments; do not add outside assumptions.
- Do not guess quantities or manufacturers. Use “Not stated”, “Not provided”, or “TBD”.
- Use printed spec page IDs when visible (e.g., 040120-7). If not visible, use “PDF p.__”.
- De-duplicate repeats; cite the first or most specific occurrence.
- If drawings are referenced but not attached, flag as a Risk + RFI.
- If warranty trigger language conflicts across sections, flag as a Risk + RFI.

STM TABLE (single Markdown table, exact columns)
Spec Section(s) | Bid line item | Unit + quantity basis | Scope included | Exclusions/clarifications | Submittals | QA/Testing/Mock-ups | Warranty | Risk flags / RFIs | Page
```

## General notes

!!! STM is the “source of truth”  
If it affects cost, schedule, or acceptance, it must appear in the STM (either as its own line item or explicitly included under the right line item).

### Writing strong STM rows
- One row = one priceable bid line item (avoid “everything” rows).
- Use spec language; do not add “typical” assumptions.
- De-duplicate repeated requirements; keep the clearest/most controlling reference.

### Risk + RFI discipline
- Missing drawings/locations/quantities/access/existing-conditions info → mark “TBD” and write an RFI (don’t bury assumptions).
- Acceptance requirements (mock-ups, tests, manufacturer rep, certifications) are common cost misses—capture them explicitly.
- Conflicting warranty terms/triggers → flag as Risk + RFI; don’t choose silently.

### Consistency standard
- Always list attachments by filename; clearly separate “Inputs received” vs “Missing inputs.”
- Always cite a printed spec page ID when visible; otherwise use “PDF p.__” consistently.