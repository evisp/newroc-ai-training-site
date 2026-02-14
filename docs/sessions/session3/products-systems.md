# Products & Systems (with Proof)

This guideline helps you build a **defensible products/systems list** from any construction document set by extracting only what is explicitly specified and tagging each line with **Section + Page proof**.  


!!! note
    This page is **generic and reusable across projects**. It includes a worked example using *445 E 80th St – Facade Repairs*.


## Goal

A products/systems list is not a “scope narrative.”  
It is a short table you can point to later (precon, buyout, change management) and say: *“This is what we carried, and here’s where it is in the documents.”*


## Before you run prompts

### What to attach
Attach the **specific spec section / exhibit / schedule** you want to mine (not the whole project if you can avoid it).  
When you must attach the full manual, tell ChatGPT exactly which **section number** to use.

### What “proof” means
- Preferred: **Printed spec page id** (e.g., `040120-7`, `09870-4`, `079200-1`). 
- If no printed id exists: use **PDF page number** and label it `PDF p.__`.

!!! warning
    Do not accept outputs without proof (**Section + Page**). If there’s no proof, it becomes opinion; not documentation.

## Session reminder: Custom Instructions

Paste this once at the start of your chat (or set as Custom Instructions for the session).

!!! important
    **Session Custom Instructions (copy/paste):**

    - Output as a **table only** (no narrative) unless asked. 
    - Every row must include: **System**, **Product/Component**, **Manufacturer (if stated)**, **Spec Section**, **Page**. 
    - Do not guess. If not explicit, write **“Not stated.”** 
    - Use the document’s **printed page id** when available; otherwise use **PDF p.__**. 
    - This page is **products/systems only**; exclude temporary works / general conditions (we cover those elsewhere). 

## Table format (standard)

Use this table shape in every project:

| System | Product/Component | Manufacturer (if stated) | Spec Section | Page |
|---|---|---|---|---|

---

## Example project (445 E 80th St)

In the 445 E 80th Street Project Manual, the Table of Contents shows these relevant sections: **040120.91 Masonry Restoration**, **079200 Joint Sealants**, **098700 Coatings**, and **00005 Unit Prices**. 

!!! note
    You can repeat the same process on other projects by swapping: (1) the document name, (2) the target section number, and (3) the number of rows requested. 


## Output 1 — Masonry Restoration (3 rows)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `040120.91 / 040120 — Masonry Restoration` (focus on **Part 2 PRODUCTS**) 

**Prompt (copy/paste):**
```text
You are extracting a products/systems list WITH PROOF.

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 040120 (Masonry Restoration) — focus on Part 2 PRODUCTS only.

Task:
- Extract ALL distinct products/components explicitly listed in Part 2 (Products/Materials) of Section 040120.
- Output a single spredsheet table with these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Rules:
- Do not guess. If manufacturer is not explicitly stated, write “Not stated”.
- Use the printed spec page id (e.g., 040120-7). If not visible, use “PDF p.__”.
- Keep each row “one product/component” (e.g., brick unit, mortar, patching compound, anchors/ties, cleaners, etc.) exactly as written.
- De-duplicate repeats: if the same product/component appears multiple times, keep one row and cite the first occurrence (or the most specific listing).

If the output is long:
- Output in batches of up to 25 rows per message.
- At the end, write: “CONTINUE? (Yes/No). Next row would be #__.”
- When I say “Yes”, continue with the next batch (do not repeat prior rows).

Exclusions:
- Do not include temporary works or general conditions.
- Do not include installation steps (means/methods) or Part 3 execution requirements.
- Use only Section 040120, Part 2 content (no other sections unless explicitly cross-referenced inside Part 2).
```

## Output 2 — Coatings (3 rows)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `098700 / 09870 — Coatings` 

**Prompt (copy/paste):**
```text
You are extracting a products/systems list WITH PROOF.

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 09870 (Coatings) — focus on the Materials/Products portion only.

Task:
- Extract ALL manufacturer-named coating products/series explicitly listed in the Materials/Products portion of Section 09870.
- Output a single spreadsheet table with these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Rules:
- Do not guess. If a manufacturer or product/series name is not explicit, do not include it.
- Treat “System” as the substrate/use case stated in the spec (e.g., steel lintels, concrete, etc.). If not stated, write “Not stated”.
- Use the printed spec page id (e.g., 09870-4). If not visible, use “PDF p.__”.
- Keep each row “one product/component” (e.g., primer, intermediate coat, finish coat, rust inhibitor, etc.) exactly as written.
- De-duplicate repeats: if the same product/series appears multiple times, keep one row and cite the first occurrence (or the most specific listing).

If the output is long:
- Output in batches of up to 25 rows per message.
- At the end, write: “CONTINUE? (Yes/No). Next row would be #__.”
- When I say “Yes”, continue with the next batch (do not repeat prior rows).

Exclusions:
- Do not include temporary works or general conditions.
- Do not include installation steps (means/methods) or Part 3 execution requirements.
- Use only Section 09870 materials/products text (no other sections unless explicitly cross-referenced inside the materials/products portion).
```


## Output 3 — Joint Sealants (3 rows)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `079200 — Joint Sealants` 

**Prompt (copy/paste):**
```text
You are extracting a products/systems list WITH PROOF.

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 079200 (Joint Sealants) — focus on Part 2 PRODUCTS only.

Task:
- Extract ALL distinct sealant-system products/components explicitly required in Part 2 of Section 079200.
- Output a single Spreadsheet table with these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Rules:
- Do not guess. If manufacturer is not explicitly stated, write “Not stated”.
- Include both “named manufacturers” (if listed) and “required components” even when not brand-named (e.g., sealant, primer, joint backing/backer rod, bond breaker, cleaners/solvents, masking tape, accessories) as long as they are explicitly required in Part 2.
- Use the printed spec page id (e.g., 079200-1). If not visible, use “PDF p.__”.
- Keep each row “one component/product” exactly as written.
- De-duplicate repeats: if the same component is required in multiple places, keep one row and cite the first occurrence (or the most specific listing).

If the output is long:
- Output in batches of up to 25 rows per message.
- At the end, write: “CONTINUE? (Yes/No). Next row would be #__.”
- When I say “Yes”, continue with the next batch (do not repeat prior rows).

Exclusions:
- Do not include surface prep steps or installation procedures (Part 3 execution).
- Do not invent performance properties or requirements not stated in the text.
- Use only Section 079200, Part 2 content (no other sections unless explicitly cross-referenced inside Part 2).
```

## Output 4 — Cross-check “scope adders” (Unit Prices)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `00005 — Proposal Supplement – Unit Prices` 

This step prevents “silent misses” by capturing what the documents say is **included inside unit price work** (often listed as “concomitants”). 

**Prompt (copy/paste):**
```text
You are extracting scope adders WITH PROOF (not pricing).

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 00005 (Proposal Supplement – Unit Prices).

Task:
1) In Section 00005, find the sentence that states what unit prices include beyond base labor/material/overhead/profit/taxes (the sentence that lists “concomitants”).
2) Output a spreadsheet table with exactly 1 row and these columns:
   Topic | Exact included concomitants (quote exactly) | Spec Section | Page

Rules:
- Quote the concomitants list exactly as written (copy/paste the wording; no paraphrase).
- Do not add or remove any items from that sentence.
- Use the printed spec page id (e.g., 00005-1). If not visible, use “PDF p.__”.
- If you cannot find a concomitants list in Section 00005, output the table anyway with:
  Topic = “Unit price inclusions (concomitants)”
  Exact included concomitants = “Not stated”
  and still provide the closest relevant page reference.

Exclusions:
- Do not discuss pricing, markups, or how to apply the unit price—only extract the inclusion language with proof.

```

!!! warning
    If this “scope adders” line includes items like sealant/primer/fasteners/flashings, your estimate and clarifications must treat them as included unless you explicitly qualify otherwise.
