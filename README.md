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

Guidelines here are **curated summaries** of the ACGME competencies and CanMEDS roles. For
specialty-specific, verbatim ACGME Milestones 2.0 text, replace the entries in `guidelines.json`
with the official milestone language for your program.
