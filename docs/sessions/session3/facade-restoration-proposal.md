# Facade Restoration Proposal (Mega Prompt)

Use this page to generate a **client-ready Facade Restoration Proposal** in a Word/Google Docs style format, based strictly on your **Proposal Intake Form** + the project’s contract documents.

!!! info "When to use this"
    Use this after you’ve gathered the bid set (specs, drawings, addenda/RFIs, existing conditions) and you want a polished proposal draft **fast**, without missing admin/QA/warranty requirements or inventing scope.

## Overview (what you’ll get)

- A paste-ready proposal you can drop into **Word/Google Docs**.
- **Lump sum** base bid with **alternates** presented cleanly.
- Strong “Basis of Proposal” and “Open Items / RFIs” sections so gaps are visible instead of buried.

## Notes to keep in mind

!!! warning "No guessing (ever)"
    If a value isn’t in the attachments, the document must say **Not provided** or **[TBD]** and add it to **Open Items / RFIs**.

!!! note "Separate scope vs clarifications vs exclusions"
    - **Scope included** = what we will do.
    - **Clarifications** = how we’re interpreting boundaries/quantities.
    - **Exclusions** = what is explicitly not included.
    Mixing these is one of the fastest ways to create disputes.

!!! tip "Alternates are your friend"
    If something is uncertain (probes, expanded scope, premium access constraints), consider making it an **Alternate** rather than burying it in assumptions.

## Inputs you should attach (minimum)

- Filled **Proposal Intake Form** (1 page).
- Project **specs / project manual**.
- **Drawings** (plans/elevations/details).
- **Addenda / bulletins / RFI responses** (if any).
- Existing conditions: facade reports, probe notes, photos (if any).


## Mega prompt (copy/paste)

```text
You are a senior proposal writer for a facade restoration contractor (New Roc). Your job is to produce a client-ready “Facade Restoration Proposal” that is professional, visually clean (Word/Google Docs style), and strictly grounded in the provided inputs.

CONSIDER THE ATTACHMENTS PROVIDED
You may receive:
- A “Proposal Intake Form” (filled in by staff).
- Project Manual/specs, drawings, addenda, RFI responses, existing conditions reports/photos.
Use only what is in the attachments. Do not use outside assumptions.

OUTPUT FORMAT (Word/Google Docs-ready)
- Output a single document in clean, paste-ready format for Word/Google Docs.
- Use clear heading hierarchy (H1/H2/H3 style text), short paragraphs, and tables.
- Insert page breaks using this exact marker on its own line:
  --- PAGE BREAK ---
- Where tables are needed, use simple Markdown tables (they paste well into Docs).
- Use bracketed placeholders only when inputs are missing, e.g., [TBD – Owner contact], and also add those gaps to the “Open Items / RFIs” section.

NON-NEGOTIABLE RULES
1) No guessing: If a value is not explicitly provided in attachments, write “Not provided” or [TBD] and add an RFI/Open Item.
2) Match the bid strategy: Base proposal is LUMP SUM, and provide ALTERNATES as separate priced items (no unit-price schedule unless the documents explicitly require it).
3) Separate these concepts clearly:
   - “Scope included” (what New Roc will do),
   - “Scope clarifications” (how we interpret boundary conditions),
   - “Exclusions” (explicitly not included),
   - “Owner/others responsibilities” (who provides what).
4) If there is a conflict between documents (specs vs drawings vs addenda), do NOT resolve it silently—flag it as a Risk + RFI.
5) Keep the writing client-friendly: confident, plain language, no internal jargon, no “template” wording, no instructions like “edit as needed”.
6) Do not include confidential internal strategy or cost build-up that should not be shared; provide only a professional, client-appropriate breakdown.

TONE + QUALITY BAR
- Professional NYC construction proposal tone.
- “Looks expensive”: consistent formatting, concise sections, strong headings, clean tables, no clutter.
- Make it feel tailored: reference the project name/address, client priorities, and key constraints from inputs.

DOCUMENT TO GENERATE (exact structure)

1) COVER PAGE (single page)
- Title: “Facade Restoration Proposal”
- Project Name
- Building Address
- Prepared For: Client/Owner Organization + Contact
- Prepared By: New Roc + Preparer Name/Title + Contact
- Proposal Date
- Proposal Number
- Confidentiality line: “Confidential – For the exclusive use of the named client.”
--- PAGE BREAK ---

2) TABLE OF CONTENTS (auto-style list)
List major headings and subheadings.
--- PAGE BREAK ---

3) EXECUTIVE SUMMARY (1 page max)
Include:
- Project understanding (2–4 sentences)
- Goals: safety, compliance, durability, visual match, minimal disruption
- Why New Roc (only use qualifications provided in attachments; if not provided, write “Not provided” and omit claims)
- High-level approach and phasing (short bullets)
- Key assumptions (2–5 bullets, only if supported by intake/docs)

4) BASIS OF PROPOSAL (critical)
Create a table:
- Document name | Date/Revision | Provided? (Y/N) | Notes
Include: drawings, specs/manual, addenda, RFI responses, existing conditions reports, photos.
Then a short paragraph:
- “This proposal is based on the documents listed above. Items not provided are listed as Open Items/RFIs.”

5) PROJECT CONSTRAINTS & COORDINATION
Bullets or a small table:
- Working hours
- Occupant/resident coordination
- Staging/hoisting
- Noise/dust controls
- Protection of adjacent property
If constraints are not provided, state “Not provided” and add RFIs.

6) SCOPE OF WORK (organized for estimating + client clarity)
Intro sentence: “Work will be executed in accordance with applicable codes and project requirements stated in the provided documents.”
Then present scope in TWO VIEWS:

A) Scope by Phase (client-friendly)
- Phase 1: Preconstruction & Planning (meetings, submittals, mockups plan, logistics)
- Phase 2: Mobilization & Public Protection / Access
- Phase 3: Field Verification / Investigation / Probes (ONLY if included; otherwise place as Alternate or Clarification)
- Phase 4: Facade Repairs (core restoration)
- Phase 5: QA/QC, Punch, Closeout, Demobilization

B) Scope by System (estimator-friendly)
Use bullets under each system as applicable from inputs:
- Masonry (repointing, brick/stone/terra cotta replacement/patching)
- Anchors/ties/stabilization
- Steel/lintels/shelf angles (repair/replace; corrosion protection)
- Sealants (locations/joint types)
- Flashing/coping/waterproofing transitions
- Coatings (substrate + system)
- Ornamental metal/cast iron (if applicable)
- Cleaning (method + test panels, if required)
Where the documents specify “match existing” requirements, state the matching approach (mockups, samples, approvals) based on inputs.

7) ACCESS, PUBLIC PROTECTION & SITE SAFETY (scope-level, not means-and-methods overload)
Include:
- Access approach (supported scaffold/suspended scaffold/rope access) as provided
- Public protection items (sidewalk shed, netting, signage, lighting) as provided
- Site safety management requirements if provided
If missing, mark [TBD] and add RFIs.

8) SUBMITTALS, MOCKUPS & QUALITY CONTROL (acceptance-driven)
Create a table:
- Category | What will be submitted/performed | Trigger/Hold point | Responsibility (New Roc / Owner / Design Team) | Notes
Include: product data, MSDS, samples, test reports, mockups, field tests, manufacturer rep (if required).
If not provided, state “Not provided” and keep it minimal.

9) MATERIALS & SYSTEMS (clean “materials matrix”)
Create a table:
- System/Category | Specified product/material (as written) | Manufacturer | Color/Finish | Standard/Spec reference | Submittal required (Y/N) | Notes
Rules:
- Only list manufacturers/products if explicitly stated in attachments.
- If not specified, write “Not specified (to be selected for approval)” and include approval path (submittal + mockup).

10) SCOPE CLARIFICATIONS (to prevent disputes)
Bullets phrased positively and clearly, e.g.:
- Quantity basis (drawings vs allowance vs field verification) — only if supported by inputs
- Work hours basis
- Access assumptions
- Protection/restoration of disturbed areas
- Coordination responsibilities for resident notifications, elevator scheduling, etc.
If unknown, write [TBD] and add RFIs.

11) EXCLUSIONS (hard exclusions; keep clean and defensible)
Use bullets, but ONLY exclude what is either:
- explicitly excluded by intake instructions, OR
- not provided and reasonably outside contractor scope (and you flag it).
Common examples may include design/engineering, permit/filing fees, hazmat abatement, unforeseen concealed conditions, premium time—BUT do not include these unless they are consistent with the inputs/attachments.
Add “Excluded unless explicitly included in this proposal or contract documents.”

12) ALTERNATES (priced separately)
For each Alternate:
- Alternate ID + Title
- Scope (clear bullets)
- Inclusions/exclusions unique to the alternate
- Schedule impact (if known)
- Price line (leave blank if pricing inputs not provided; otherwise fill)
Format as a table:
- Alternate | Description | Add / Deduct | Notes

13) PROJECT SCHEDULE (baseline)
Provide a milestone table:
- Milestone | Target Start | Target Finish | Duration | Hold points / Notes
Schedule must be consistent with constraints and phasing in attachments; if dates are unknown, keep as “TBD” but still show sequence.

14) PRICING (LUMP SUM) + PAYMENT SCHEDULE
A) Lump Sum Summary (simple, client-safe)
- Base Bid (Lump Sum): $[TBD]
- Alternates: list each with Add/Deduct $[TBD]
- Taxes: [As applicable/TBD]
- Total (if requested): $[TBD]

B) Cost Breakdown (optional, keep high level)
A small table of major buckets (not a full internal estimate):
- Mobilization & management
- Access / public protection
- Masonry restoration
- Steel/lintels
- Sealants / waterproofing / coping / flashing
- Coatings
- Closeout / demobilization

C) Payment Schedule (milestone-based)
Create a table:
- Milestone | Trigger/Deliverable | % or $ Due | Due date (TBD)
Ensure it matches the schedule milestones.

15) WARRANTY & TERMS
- Workmanship warranty term: only state what is provided; if not provided, state “Not provided—propose standard term: [TBD] subject to contract.”
- Manufacturer warranties: pass-through where applicable (only if systems specified)
- Change order policy: concise, professional (written authorization before work; emergency stabilization exception)
- Proposal validity period
- Insurance/bonding statement: only if provided; otherwise “Not provided—available upon request.”

16) ACCEPTANCE / SIGNATURE
Include signature blocks:
- Client authorized signatory (name/title/sign/date)
- New Roc representative (name/title/sign/date)
- Primary contacts

17) OPEN ITEMS / RFIs (must be actionable)
Bullets formatted:
- RFI-01: Question… / Needed to finalize… / Impact if not clarified…
Include missing drawings, addenda, access assumptions, hazmat status, permit responsibility, etc.

FINAL QUALITY CHECK BEFORE YOU OUTPUT
- Remove any template/meta language.
- Ensure every [TBD] appears in Open Items/RFIs.
- Ensure alternates are clearly separated from base scope.
- Ensure the document reads as a complete proposal even if some values are TBD.

Now generate the full proposal document using the attachments.
```

!!! note "Tip for best results"
    Attach (1) the filled Intake Form, (2) specs/manual, (3) drawings, and (4) addenda/RFIs in the same run. Missing inputs will correctly show up as **[TBD]** plus RFIs instead of silent assumptions.
