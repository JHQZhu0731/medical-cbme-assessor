# 🩺 CBME Assessment Prompt Builder

A simple, static web app that turns **Competency-Based Medical Education (CBME)** guidelines into a
structured **JSON prompt** for a Large Language Model (LLM) to assess residents/fellows in real
**Graduate Medical Education (GME)** clinical settings.

## What it does

1. Pick a **framework** — ACGME Core Competencies (US) or CanMEDS Roles (international).
2. Pick a **competency domain** — the app loads the assessment guidelines for that domain.
3. Label the **input type** the LLM will assess: `transcript`, `test`, `video`, or `other`.
4. Generate a ready-to-use **JSON prompt** and copy or download it.

The generated JSON explicitly labels the evidence type and includes an output schema so the LLM
returns milestone-style levels, per-guideline evidence, feedback, and safety flags.

Every framework, competency domain, rating rubric, and evidence type is **linked to its primary
source**. Citations appear inline in the interface (numbered superscripts), in a full **References**
section, and are embedded in a `provenance` block inside the generated JSON so each assessment is
traceable back to the literature.

## Live site

Once GitHub Pages is enabled, the app is served at:

```
https://<username>.github.io/medical-cbme-assessor/
```

## Files

| File | Purpose |
|------|---------|
| `index.html` | The entire single-page app (HTML + CSS + JS). |
| `guidelines.json` | Editable dataset of frameworks, domains, and guidelines. |
| `README.md` | This file. |

## Editing guidelines

Educators can expand or replace guidelines by editing `guidelines.json` — no code changes needed.
Add new domains under a framework's `domains` object, or add whole new frameworks.

## Deploy to GitHub Pages

1. Push this repo to GitHub.
2. **Settings → Pages → Source: `main` branch, `/ (root)`**.
3. Wait ~1 minute; your site goes live at the URL above.

## Notes

Guidelines here are **curated summaries** (paraphrases) of the ACGME competencies and CanMEDS roles,
each linked to its source. For specialty-specific, verbatim ACGME Milestones 2.0 text, replace the
entries in `guidelines.json` with the official milestone language for your program. Citation metadata
lives in the `citations`, `rubric`, and per-domain `sources` fields of `guidelines.json`.

## References

The frameworks, rubric, and assessment-tool mappings summarized in this tool are drawn from the
following primary sources:

1. Swing SR. The ACGME outcome project: retrospective and prospective. *Medical Teacher.* 2007;29(7):648-654. doi:10.1080/01421590701392903
2. Accreditation Council for Graduate Medical Education (ACGME). *Common Program Requirements (Residency), Section IV.B.1 (Core Competencies).* Chicago, IL: ACGME. https://www.acgme.org/programs-and-institutions/programs/common-program-requirements/
3. Edgar L, McLean S, Hogan SO, Hamstra S, Holmboe ES. *The Milestones Guidebook (Version 2020).* Chicago, IL: ACGME; 2020. https://www.acgme.org/globalassets/MilestonesGuidebook.pdf
4. Nasca TJ, Philibert I, Brigham T, Flynn TC. The next GME accreditation system — rationale and benefits. *New England Journal of Medicine.* 2012;366(11):1051-1056. doi:10.1056/NEJMsr1200117
5. Frank JR, Snell L, Sherbino J, editors. *CanMEDS 2015 Physician Competency Framework.* Ottawa: Royal College of Physicians and Surgeons of Canada; 2015. ISBN 978-1-926588-28-5. https://canmeds.royalcollege.ca/en/framework
6. Frank JR, Snell LS, Ten Cate O, et al. Competency-based medical education: theory to practice. *Medical Teacher.* 2010;32(8):638-645. doi:10.3109/0142159X.2010.501190
7. Ten Cate O. Nuts and bolts of entrustable professional activities. *Journal of Graduate Medical Education.* 2013;5(1):157-158. doi:10.4300/JGME-D-12-00380.1
8. Norcini J, Burch V. Workplace-based assessment as an educational tool: AMEE Guide No. 31. *Medical Teacher.* 2007;29(9-10):855-871. doi:10.1080/01421590701775453
9. Norcini JJ, Blank LL, Duffy FD, Fortna GS. The mini-CEX: a method for assessing clinical skills. *Annals of Internal Medicine.* 2003;138(6):476-481. doi:10.7326/0003-4819-138-6-200303180-00012
10. Holmboe ES, Iobst WF. *Assessment Guidebook.* Chicago, IL: ACGME; 2020. https://www.acgme.org/globalassets/pdfs/milestones/guidebooks/assessmentguidebook.pdf

## Citing this tool

> Zhu JHQ. CBME Assessment Prompt Builder [software]. 2026. Available from: https://jhqzhu0731.github.io/medical-cbme-assessor/
