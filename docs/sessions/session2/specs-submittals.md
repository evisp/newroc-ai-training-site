# Specifications: Overview – scope mapping & per-section extraction

**The challenge:** A typical specification is 400 - 1000+ pages.  
**The reality:** You can't paste it all into AI and expect a useful breakdown. Document size + complexity = garbled output, missing sections, token limits, and unchecked errors. 

This page explains what's realistically achievable and where caution is needed.

---

## Why big specs are risky for AI (and how to work around it)

!!! warning "The Size Problem"
    **What happens if you paste 400+ pages at once:**
    - Output gets fragmented or incomplete (missing sections, contradictions).
    - AI misses cross-references (a material requirement in one section conflicts with another).
    - Section references get confused (wrong page numbers, lost context).
    - You can't verify; you don't know what it read or skipped.

    **Safety rule:** Work on one section (or one discipline) at a time, just like you'd review a spec by hand. 

### What AI is good at on specs

- **Reading + rephrasing**: Turn a dense clause into plain language.  
- **Structuring**: Extract a list of submittals, tests, materials from one section.  
- **Mapping**: Identify which section numbers match your scope.  
- **Tabling**: Convert spec text into a job-ready table (materials, dates, roles, etc.).  
- **Extracting proof**: Pull out section references and page numbers to support each item.

### What AI struggles with on specs

- **Reading the whole book** : 400+ pages at once creates errors and blind spots.
- **Making final decisions** : Spec interpretation needs a human who knows your scope and risk tolerance.  
- **Cross-checking contradictions** : If one section says one thing and another says another, you need to catch it yourself.  
- **Understanding your internal priorities** : Only you know what's critical to your scope and means/methods.  
- **Filling gaps with "typical practice"** : If the spec is silent, AI will guess; you must force "Not stated" instead.

## The realistic two-part workflow (no shortcuts)

### Part 1: Scope → Section Mapping (Fast)
**Goal:** Identify which spec sections apply to your scope.

!!! success "Typical input"
    "Our scope is: masonry restoration, façade overcladding, window replacement, thermal insulation, and applied fireproofing."

!!! success "Typical output"
    ```
    Section Number | Title | Applies? | Notes
    04 01 20       | Masonry Restoration | YES | Full scope
    04 42 00       | Exterior Stone | NO | Not in our scope
    07 21 00       | Thermal Insulation | YES | Façade insulation
    07 27 26       | Self-Adhered Water Resistive Air Barrier | YES | Required
    07 42 51       | Porcelain Tile Wall System | YES | Overcladding
    08 51 13       | Aluminum Window | YES | Window replacement
    07 81 00       | Applied Fireproofing | YES | Full scope
    ```



### Part 2: Per-Section Deep Extraction (Repeatable)
**Goal:** For each section mapped in Part 1, extract the information fields you need for the submittal log.

!!! success "Typical input"
    "Here is Section 04 01 20 Masonry Restoration (pages 45–68). Extract the materials, manufacturers, submittals, LEED info, tests, warranties, execution, and admin requirements."

!!! success "Typical output (one section)"
    | Field | Extracted Info | Spec Ref |
    |-------|---|---|
    | **Recommended Materials** | Brick (CMU per ASTM C-90), mortar (Type N per ASTM C-270), joint sealant (polyurethane per ASTM C-920) | 04 01 20, p. 48–50 |
    | **Manufacturers** | Brick: Acme Brick Co.; Mortar: Sakrete; Sealant: Dow Corning | 04 01 20, p. 49 |
    | **Allowed Substitutes** | Brick: "Other manufacturer equivalent if approved; submit with 3 completed projects" | 04 01 20, p. 49, subsection "Substitutions" |
    | **LEED Requirements** | Not stated. | : |
    | **Tests & Inspections** | Compressive strength test (ASTM C-39) per 3000 units; bond strength per ASTM C-1006 | 04 01 20, p. 55 |
    | **Samples & Mockups** | Mortar sample (2 lbs); 4×4 ft mockup wall with full brick, mortar, and joint detail | 04 01 20, p. 60–61 |
    | **Warranty** | Contractor warranty: 5 years; Manufacturer brick warranty: 20 years | 04 01 20, p. 62 |
    | **Execution / Application** | Lay brick in running bond; joint depth 3/8″; tooled concave joint; no mortar smears after 24 hrs | 04 01 20, "Execution", p. 64–66 |
    | **Admin Requirements** | Submit samples day 1; mockup approval before production; progress photos weekly | 04 01 20, p. 50–51 |


**Repeat for each mapped section** and aggregate results into your Excel submittal log.

## Why this two-step approach works

| Aspect | Why it matters |
|--------|---|
| **Scope-first** | You only extract what applies to your work; no wasted effort on unrelated sections. 
| **One section at a time** | Output stays tight, verifiable, and section-linked (no confusion about what came from where). |
| **Proof-on-every-item** | Each extracted item includes its spec reference so you can spot-check in the PDF before using it. |
| **Repeat pattern** | Same prompt structure works across all sections; once you've done one, the second and third are faster. |
| **Aggregation step** | Collecting results into your Excel log is manual but safe; you review and own every row. |


## What to watch for (cautions)

!!! danger "Caution 1: Confident errors on details"
    AI will extract a threshold or a date wrong, and sound certain about it.  
    **Remedy:** For any spec item that affects cost, time, or risk, spot-check 2–3 examples in the PDF before using. 

!!! danger "Caution 2: Guessing when the spec is silent"
    The spec may say "Not stated" or be vague; AI will try to fill the gap with "typical practice."  
    **Remedy:** Force the output to say "Not stated" and create a "Missing inputs needed" list to escalate to the team. 

!!! danger "Caution 3: Cross-section conflicts"
    One section may say material X is allowed; another may restrict it. AI sees each section separately and won't catch the contradiction.  
    **Remedy:** Once you've extracted from all sections, do a human review pass to check for conflicts and dependencies.

!!! danger "Caution 4: Addenda and revisions"
    The spec may have addenda or revision marks. If you don't explicitly state which version/addendum to use, AI may mix old and new language.  
    **Remedy:** Always specify "Use only the current issue dated [date]" and include addenda as part of your scope. 


## Golden rules (non-negotiable)

- **No reference = not usable.** Every extracted item must point to a section/page. 
- **If it's not stated, say so.** Never let AI invent "typical practice" or assumptions. 
- **Verify before sending.** Spot-check 2–3 items per section in the PDF before logging them. 
- **One section at a time.** Do not paste multiple sections in one prompt; keep scope tight. 
- **Store the source link.** Save your final log with a link back to the spec PDF and any missing inputs. 

## Next: Use case examples

The next page shows **Part 1 (Scope Mapping)** and **Part 2 (Deep Extraction)** in action with concrete prompts you can copy/paste and test on your own specs.

Continue to: [Specification extraction – prompts & use cases](../../prompts/spec-prompts.md)


![Specs](https://i.imgur.com/ycYcb4v.png)