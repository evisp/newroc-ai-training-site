# Practice & exercises (Session 1)

This page is where the session becomes practical. You will use ChatGPT to take a small piece of a large spec, ask for a clear deliverable, and then verify the result in the PDF before using it.  

The goal is not “perfect writing.” The goal is **trustworthy output** that is easy to reuse and easy to defend in a meeting.  

!!! info "Exercise files (Google Drive)"
    Full exercise handouts, templates, and the extracted spec sections are stored [here:](  
    https://docs.google.com/document/d/1rap4eOB0CuRJmiIQzj3QkEa9K7Leg70UsTMllGq7Wxc/edit?usp=drive_link) 

## Before you start

Most specification books are extremely large (often 1,000+ pages). For these exercises, we avoid “read the whole spec” and instead work section-by-section so the result is focused and checkable.  

!!! success "The workflow you will repeat"
    - **Extract:** Work from one spec section only (example: 013300 or 014339).  
    - **Prompt:** Use the 5-step pattern (Task → Context → Constraints → Output → Verification).  
    - **Verify:** Spot-check 2–3 items in the PDF using section/page references.  
    - **Correct + Save:** Fix mistakes and save the verified output with a link to the source.  

![Prompt Builder](https://i.imgur.com/418xD3w.jpeg)

!!! warning "Verification rules (non‑negotiable)"
    - Your output must include **spec reference + page label** for each bullet/row.  
    - Spot-check **2–3 items** in the PDF before relying on the output.  
    - If the section does not state something, write **Not stated** (do not guess).  

## What you will practice

These exercises are designed to build one core habit: moving faster **without guessing**.    
By the end, you should feel comfortable doing three things on your own: (1) writing a clear prompt, (2) asking for output in a useful format (table/checklist), and (3) quickly checking the result in the spec before relying on it.  

You will practice how to:

- Keep scope tight by using only one extracted spec section.  
- Produce outputs that are immediately usable (not generic summaries).  
- Mark unknowns honestly as “Not stated” or “Missing inputs needed.”  
- Create a simple paper trail: prompt + output + verification notes + source link.  

---

## Exercise 1: Submittal checklist + schedule template (Section 013300)

In this exercise you will turn Submittal Procedures into something a PM or superintendent can use during project setup.    
The output should be short, clear, and practical — something you would actually keep open while planning and sending submittals.  

### What you build
- A practical submittal **Do/Don’t checklist**.  
- A **Submittal Schedule Template** table (fields/columns required).  

### What it teaches
This exercise trains you to convert a spec section into a checklist and a table, while keeping everything tied to source references.    
It is a fast way to reduce missed requirements and rework later.  

### What your output must include
- [ ] 8–12 checklist bullets a PM/super can follow.  
- [ ] One table describing submittal schedule fields in plain language.  
- [ ] A spec reference + page label for **each** bullet and **each** table row.  
- [ ] If something is not stated in the section, write: **Not stated in Section 013300**.  

??? tip "Starter prompt (copy/paste) — Exercise 1"
    ```text
    TASK
    Turn this spec excerpt into a job-ready submittal checklist and a submittal schedule template.

    CONTEXT
    - Document: Spec Section 013300 (Submittals) excerpt
    - Audience: PM / Superintendent
    - Purpose: Project setup + planning submittals

    CONSTRAINTS
    - Use only the text I paste below (Section 013300 excerpt).
    - Do not add typical practice or outside standards.
    - If the section does not state something, write: Not stated in Section 013300.

    OUTPUT FORMAT
    1) Do/Don’t checklist (8–12 bullets). Each bullet must include spec reference + page label.
    2) Submittal Schedule Template table with columns:
       - Field name
       - What it means (plain language)
       - Where it comes from (spec reference + page label)

    VERIFICATION
    - Include spec reference + page label for every item.
    - List any “Missing inputs needed” to complete this for a real job.

    SPEC TEXT
    [Paste the Section 013300 excerpt here]
    ```  
     

---

## Exercise 2: Mockup hold points + testing matrix (Section 014339)

In this exercise you will build a simple plan that prevents work from moving forward before the right approvals and testing happen.    
Mockups often set the workmanship standard, so the goal is to make hold points and responsibilities easy to understand and hard to miss.  

### What you build
- A short list of mockup **hold points** (what must happen before work continues).  
- A **Mockup Testing Matrix** table.  
- A “Missing inputs needed” list (what the section does not tell you).  

### What it teaches
This exercise trains you to plan with clear gates (“stop points”) and to avoid inventing details that are not in the spec.    
It also builds the habit of explicitly listing what the team must confirm to finalize the plan.  

### What your output must include
- [ ] 5–8 hold points written in simple, actionable language.  
- [ ] One testing matrix table with: mockup type, test, standard, responsible party, records.  
- [ ] A spec reference + page label for **each** hold point and **each** table row.  
- [ ] A clear “Not stated / Missing inputs needed” list.  

??? tip "Starter prompt (copy/paste) — Exercise 2"
    ```text
    TASK
    Turn this spec excerpt into mockup hold points and a mockup testing matrix we can use to control work.

    CONTEXT
    - Document: Spec Section 014339 (Mockups) excerpt
    - Audience: PM / Superintendent / QA-QC
    - Purpose: Define hold points (stop points) and required testing/records

    CONSTRAINTS
    - Use only the text I paste below (Section 014339 excerpt).
    - Do not add typical practice or outside standards.
    - If the section does not state something, write: Not stated.

    OUTPUT FORMAT
    1) Hold points list (5–8 bullets). Each bullet must include spec reference + page label.
    2) Mockup Testing Matrix table with columns:
       - Mockup type
       - Test / inspection
       - Standard (as stated)
       - Responsible party
       - Records / closeout
       - Spec reference + page label
    3) Missing inputs needed / Not stated list

    VERIFICATION
    - Include spec reference + page label for every item.
    - Flag any conflicts or unclear wording inside the excerpt.

    SPEC TEXT
    [Paste the Section 014339 excerpt here]
    ```  
     

---

## What to show when you finish (for group share‑out)

Keep the report-out short and practical. You are not presenting a “perfect document” — you are demonstrating that you can produce something useful and verified.  

!!! success "Share‑out checklist (what to show)"
    1) **Your prompt** (the 5-step version).    
    2) **Your output** (checklist + table, or hold points + matrix).    
    3) **Your proof checks** (2–3 quick spot-checks in the PDF).    
    4) **One correction** you made, or one item you flagged as “Not stated”.  

> Fast answers are helpful. Verified answers are usable.    
> If you can't point to the spec page that supports the output, don't rely on it.  
