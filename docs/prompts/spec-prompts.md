# Specifications – prompts & use cases

These are **generic templates** you can reuse on any project spec. They work best when you break the spec into small excerpts/sections and force “proof” (section/page) for every extracted item. 

!!! warning "Golden rules (use every time)"
    - Do **not** paste an entire spec book at once; work section-by-section. 
    - **No reference = not usable.** Every extracted item must include a section/page label. 
    - If the spec does not say it, write: **Not stated** (do not fill gaps with “typical practice”). 


## Use case 1: Scope → Section Mapping (fast)

**Goal:** Start from a short scope statement and produce a list of relevant spec sections (Section No. + Title + Applies? + Notes).  
**Why this matters:** The spec's Table of Contents already lists Division/Section numbers and titles, so mapping can be done quickly without reading everything. 

??? example "Prompt: Scope → Section mapping from TOC (copy/paste)"
    ```text
    Task: Identify which spec sections are relevant to the scope of work and produce a section mapping list.
    Context: I'm building a submittal log / tracker. I only want sections that will drive submittals, materials, mockups/samples, testing/inspections, warranties, admin requirements, and any means/methods or execution constraints.
    Inputs:
    1) Scope of work (paste below).
    2) Spec Table of Contents (paste below – section numbers + titles only).
    Constraints:
    - Use only the TOC text I paste (do not guess sections not listed).
    - If a section might apply but scope is unclear, mark as MAYBE and ask what input is missing.
    Output format:
    A) Table with columns:
       Division | Section No. | Section Title | Applies? (YES/NO/MAYBE) | Why (1 line) | Priority (High/Med/Low) | Notes / Follow-up question
    B) “Next extraction set”: list the first 5–10 sections (highest priority) I should extract next.
    Verification:
    - For each YES/MAYBE, quote 3–10 words from the TOC line as proof (so I can confirm I pasted it correctly).
    ```

??? tip "How to run this in the real world"
    - Step 1: Copy/paste your scope (5–10 bullets).  
    - Step 2: Copy/paste only the TOC lines that include section numbers + titles (not the whole spec). 


## Use case 2: Per‑Section deep extraction → Submittal log rows (repeatable)

**Goal:** For each relevant section, extract the items your company wants (materials + manufacturers + substitutes; LEED; tests/inspections; samples/mockups; warranties; special limitations; submittal timelines; means & methods; execution/application; admin requirements).  
**Important:** Division 01 sections often define the global rules for submittals, review time, and substitutions (e.g., Submittal Procedures and Substitution Procedures), so extract those early. 

??? example "Prompt: Extract Division 01 “rules that drive the log” (copy/paste)"
    ```text
    Task: Extract the “global rules” that affect our submittal log from the spec excerpt below.
    Context: I'm building a submittal log / tracker and need the admin/timing rules that apply across trades.
    Constraints:
    - Use only the text I paste below.
    - Do not add outside standards or typical practice.
    Output format (tables):
    1) Submittal timing & review rules
       Columns: Rule / Requirement | Applies to | Timing / Duration | Notes | Spec ref (section/page label)
    2) Substitution / comparable product rules
       Columns: Requirement | Substitution type (cause/convenience/comparable product) | Required documentation | Timing limits | Spec ref
    3) Quality / testing admin rules
       Columns: Requirement | Who provides | When | Record / report required | Spec ref
    4) Sustainability / LEED admin rules (if present)
       Columns: Requirement | Documentation needed | Who signs | Spec ref
    Verification:
    - For each row, include the spec reference and a short “proof phrase” (3–10 words).
    - If the excerpt does not mention LEED/sustainability, write: Not stated.
    ```

!!! tip "Illustration input (example sections you often extract early)"
    - Section 01 33 00 “Submittal Procedures” includes review durations and submittal schedule requirements in this spec set. 
    - Section 01 25 00 “Substitution Procedures” defines what counts as a substitution and what documentation/timing is required in this spec set. 
    - Section 01 40 00 “Quality Requirements” typically frames testing/inspection reporting and responsibilities. 


??? example "Prompt: Per‑section extraction → CSV rows for Excel (copy/paste)"
    ```text
    Task: Convert the spec excerpt below into CSV rows for a submittal log / tracker.
    Context: This output will be pasted into Excel. Rows = one submittal/log item each.
    Constraints:
    - Use only the text I paste below.
    - If something is not stated, write “Not stated.”
    - Keep each CSV cell short (max ~20 words).
    Output format:
    - Return ONLY CSV (comma-separated) with this exact header row:

    Category,Section No.,Section Title,Item (material/submittal/test/mockup/sample/warranty/admin),Subcategory (materials/mockups/samples/special testing/means & methods/admin),Manufacturer / Basis-of-design,Allowed substitutes (or substitution rule ref),Required submittal type (Action/Info/Not stated),Key requirement summary,Execution/Application notes (from Execution/Part 3),Tests/Inspections,LEED/Sustainability,Warranty,Timeline (submittal/review/lead time),Spec ref (section/page label + proof phrase)

    Extraction rules:
    - Materials: list recommended materials + named manufacturers (if any).
    - Substitutes: if the section doesn't list “allowed substitutes,” capture “Not stated” AND point to the substitution procedure section if referenced.
    - Samples/Mockups: list each sample/mockup and what it must include.
    - Tests/Special inspections: list each test/inspection, who performs if stated, and required reports if stated.
    - Means & Methods: extract any explicit means/methods restrictions or required procedures.
    - Execution: under Part 3 / Execution, pull application/installation requirements as short notes.
    - Admin: include closeout submittals, record requirements, and special coordination/timing notes if stated.
    Verification:
    - Every CSV row must have “Spec ref” filled in (section/page label + 3–10 word proof phrase).
    ```

??? tip "How to keep outputs clean"
    - Paste one spec section (or 2–4 pages) at a time so the CSV stays complete and checkable. 
    - If the section is long, run it in two passes: Part 1/General & Part 2/Products first, then Part 3/Execution second.


## Aggregation: Build the master Excel log

**Goal:** Combine the per‑section CSV outputs into one master tracker and de-duplicate obvious repeats.

??? example "Prompt: Merge multiple CSV blocks into one (copy/paste)"
    ```text
    Task: Merge multiple CSV blocks into one master CSV for a submittal log.
    Context: Each CSV block below uses the same headers. I want one combined list, de-duplicated where the same “Item + Section No.” repeats.
    Constraints:
    - Do not invent new rows.
    - If two rows conflict, keep both and add a note in “Key requirement summary” starting with “CONFLICT:” (do not resolve it).
    Output:
    - Return ONLY a single combined CSV with the same header row, sorted by:
      Subcategory → Section No. → Item.
    Verification:
    - At the end (after the CSV), add a short “Missing inputs needed” list (max 10 bullets) if placeholders remain.
    ```

!!! warning "Final step (non‑negotiable)"
    Spot‑check 2–3 extracted rows per section in the PDF before you send or rely on the log (especially timelines, warranties, and testing requirements). 
