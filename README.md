# Oral History Workflow
**Prototype — treat all content as unverified and check it against authoritative sources before relying on it.**
A standalone, tier-adaptive workflow tool for sensitive interview research. It walks a researcher through the full project lifecycle — from planning to closure — and adapts every recommendation to the project's **data sensitivity tier (1–5)**.

It is a practical companion to the SEC-HUM *Sensitive Research Data Guide*, developed for oral history at the University of Zurich and applicable to interview-based research more broadly.

## What it does

Pick a sensitivity tier and the whole playbook reshapes itself. For each of the eight lifecycle stages, the tool shows:

- **Which tools to use** — recorders, transcription, encryption, storage, repositories — each marked allowed or blocked at the chosen tier, with a plain description of what it does and where the data lives.
- **The security steps** that apply at that tier.
- **The documents** the stage triggers (consent forms, DPAs, deposit agreements, and so on).
- **A checklist** you can tick off; progress is saved in your browser.

The eight stages: Plan & Set Up → Contact & Consent → Record → Transcribe → Anonymise → Store & Secure → Archive & Access → Close Out.

The guiding principle throughout is *as open as possible, as closed as necessary*.

## Deploy on GitHub Pages

This is a single static file with no build step.

1. Put `index.html` in the repository root and commit it.
2. Go to **Settings → Pages**.
3. Under **Source**, choose **Deploy from a branch**, select `main` and the `/ (root)` folder, and save.

The site goes live at `https://<username>.github.io/<repo>/` within a minute. Because Pages serves over HTTPS, the tier selection and checklist progress persist between visits.

## Self-contained

The file makes **no external requests**. The interface font is embedded directly, so nothing is fetched from a CDN and no visitor data leaves the browser — appropriate for a data-protection resource. It works offline if opened directly in a browser, and includes a dark mode and a print/PDF view.

## Fonts

The interface uses **Source Sans 3** (Latin subset, weights 400/600/700 and 400-italic), embedded in the HTML.

> Source Sans 3 © 2010–2020 Adobe, with Reserved Font Name "Source".
> Licensed under the SIL Open Font License, Version 1.1: <https://openfontlicense.org>
> Font files sourced from [Fontsource](https://fontsource.org) (`@fontsource/source-sans-3`, v5.2.9).

If you redistribute the font more formally, add the full OFL license text as `OFL.txt` alongside the file.

## Integrating into MkDocs

To embed this inside the main SEC-HUM MkDocs site rather than hosting it standalone, drop the embedded `@font-face` block from `index.html` first — MkDocs already loads Source Sans, so this avoids shipping the font twice.

## Disclaimer

This tool offers **practical guidance, not legal advice**. It reflects Swiss federal law (nFADP), Zurich cantonal law (IDG), and international oral history standards, but project-specific questions should go to the UZH Delegate for Data Protection (datenschutz@dsd.uzh.ch) or your faculty's ethics committee.

SEC-HUM is funded by swissuniversities (Open Science).
