# Live demos (Session 1)

This page shows how we use ChatGPT on real project documents **without guessing** and without reading a 1,000+ page spec from start to finish.

The key idea is simple: **break big specs into small sections**, ask focused questions, and always verify the answer in the original PDF.

---

## The demo method (use every time)

Working with huge documents means being smart about scope. We extract one section at a time, ask for something we can actually use (a checklist, a table, a plan), and then spot-check the answer in the PDF before trusting it.

![Demo Method](https://i.imgur.com/418xD3w.jpeg)

### 1) Break the document into a small piece
- Do **not** paste a full spec book into ChatGPT.
- Extract one section (example: **013300**, **014000**, **014339**) and work only on that.
- If you are unsure what to extract, start with one section that matches your scope.

### 2) Ask for a useful output, not a generic summary
ChatGPT works best when you ask for something concrete and structured. Good demo outputs are things you can actually use on a job:
- A checklist
- A table you can copy into Excel
- A short plan with clear steps and responsibilities
- A tracker / log template

### 3) Require proof and do a quick spot-check
Before using the output, make sure you can trust it. This is the step that separates good practice from risky guessing:
- Ask ChatGPT to include **section references + page labels** for each item.
- Spot-check **2–3 items** in the PDF to confirm they are real.
- If something is not written in the section, it must say: **"Not stated."**

### 4) Save it where work lives
Once verified, treat it like any other project document—store it with context:
- Save the verified result in your shared notes/wiki folder.
- Add a link back to the source PDF and note any "missing inputs."

---

## What we demo in Session 1 (high level)

We use the same method on three common spec sections:

- **Submittals (013300):** Turn requirements into a practical checklist + schedule template.
- **Quality (014000):** Turn requirements into a QA/QC plan + tests/inspections tracker.
- **Mockups (014339):** Turn requirements into a mockup execution plan + hold points + testing matrix.

Full examples (bad prompts + good prompts + outputs) are kept in our internal [Google Drive](https://drive.google.com/drive/folders/1BzornliazSVh5qxljQ-vz22KFNmRFed9?usp=drive_link)

---

## Quick "universal add-on" to any prompt

Copy/paste this block at the end of any prompt to force verification:

- Use only the text I paste below.
- For each requirement, include the spec reference and the page label.
- If the section does not state something, write: **Not stated**.
- Do not add outside standards, typical practices, or assumptions.

---

## Prompt Builder (short version)

Sometimes people start with a rough request like:
> "Summarize this spec section and tell me what to do."

This "Prompt Builder" helps convert rough requests into a clear, repeatable prompt that ChatGPT can follow.

### What it does
It turns a plain request into a structured prompt with:
**Task → Context → Constraints → Output format → Verification**

### When to use it
- When the request is vague and the output must be consistent.
- When you need tables/templates (not paragraphs).
- When you want a built-in QA checklist before using the result.

![Prompt Builder](https://i.imgur.com/jJL1yjn.jpeg)

### Concise Prompt Builder (copy/paste)

**READY PROMPT**

**TASK**  
Convert the request below into a practical, job-ready deliverable.

**CONTEXT**  
- Project: <TBD>  
- Spec/standard basis: <Section / date>  
- Stakeholders: <Owner / Architect / CM / AHJ / testing agency>  
- Assumptions/placeholders: <List what is missing>

**CONSTRAINTS**  
- Use only the document text I provide.  
- Do not invent project facts; use placeholders like <TBD>.  
- Do not quote spec text verbatim; write original, field-ready instructions.  
- Keep it practical and executable (steps, roles, timing, templates).  

**OUTPUT FORMAT (IN THIS ORDER)**  
A) <Deliverable 1>  
B) <Deliverable 2>  
C) <Tables/templates with required column headers>  

**VERIFICATION**  
- YES/NO checklist confirming the output meets the request.  
- Missing Inputs Needed (who must provide what).

**EMPLOYEE REQUEST (RAW)**  
<<<  
Paste the employee request here.  
>>>

For the full "Prompt Builder" version (with stricter rules and formatting), use the internal [Google Drive link](https://drive.google.com/drive/folders/1BzornliazSVh5qxljQ-vz22KFNmRFed9?usp=drive_link)

---

## Demo safety notes (always follow)

- Do not paste sensitive client information unless approved.
- If a document contains private details, redact or extract only what's needed.
- Never treat ChatGPT output as final; verify in the PDF before using or sending.

> Build small AI habits: clear questions, strict scope, and quick verification. 

They add up to major time savings on every project. *Use ChatGPT to move faster, but always anchor decisions to the source document.*
