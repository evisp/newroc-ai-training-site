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
- Output a table with exactly 3 rows and these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Selection rules:
- Choose 3 distinct products/components explicitly listed in Part 2 (Materials/Products).
- If manufacturer is not stated, write “Not stated” (do not infer brands).
- Use the printed page id (e.g., 040120-7). If not visible, use PDF p.__.

Exclusions:
- Do not include temporary works or general conditions.
- Do not include installation steps (means/methods).
```

## Output 2 — Coatings (3 rows)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `098700 / 09870 — Coatings` 

**Prompt (copy/paste):**
```text
You are extracting a products/systems list WITH PROOF.

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 09870 (Coatings).

Task:
- Output a table with exactly 3 rows and these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Selection rules:
- Pick the first 3 manufacturer-named coating products/series that are explicitly listed in the materials/products portion of Section 09870.
- Use the printed page id (e.g., 09870-4). If not visible, use PDF p.__.
- Do not guess; if something isn’t explicit, omit it.
```


## Output 3 — Joint Sealants (3 rows)

**Document to attach:** `445-E80th-St-Project-Manual-01.23.2026.pdf`   
**Section:** `079200 — Joint Sealants` 

**Prompt (copy/paste):**
```text
You are extracting a products/systems list WITH PROOF.

Attached document: 445-E80th-St-Project-Manual-01.23.2026.pdf
Target spec section: 079200 (Joint Sealants).

Task:
- Output a table with exactly 3 rows and these columns:
  System | Product/Component | Manufacturer (if stated) | Spec Section | Page

Selection rules:
- Identify 3 distinct sealant-system components explicitly required (examples: sealant, primer, joint backing/backer rod, bond breaker, etc.).
- If manufacturer is not stated, write “Not stated”.
- Use the printed page id (e.g., 079200-1). If not visible, use PDF p.__.

Exclusions:
- Do not include surface prep steps or installation procedures.
- Do not invent performance properties not stated in the text.
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
1) Find the sentence that explains what unit prices include beyond the base work (the line that lists included concomitants).
2) Output a Markdown table with exactly 1 row and these columns:
   Topic | Exact included concomitants (quote exactly) | Spec Section | Page

Rules:
- Copy the list exactly as written (no paraphrase).
- Do not add anything not in that sentence.
- Use the printed page id if available; otherwise use PDF p.__.
```

!!! warning
    If this “scope adders” line includes items like sealant/primer/fasteners/flashings, your estimate and clarifications must treat them as included unless you explicitly qualify otherwise.
