# CV — Working Context / Handoff Notes

Drop this next to `Marc_Marina_Miravitlles_CV.md` so any session can pick up the work.

## Goal
A near-senior, general backend-leaning full-stack CV. Also intended to be lightly
re-targetable for a Topsort "Software Engineer, Integrations" role (more API/
integration/customer-facing emphasis) without changing the core narrative.

## Files & workflow
- `Marc_Marina_Miravitlles_CV.md` — the working source of truth (edit this).
- The styled **PDF is not generated from the Markdown**. It's rendered from a
  separate HTML/CSS file via `wkhtmltopdf` (A4, 16mm/18mm margins). To reproduce
  the exact look, keep an HTML version and render with:
  `wkhtmltopdf --page-size A4 --margin-top 16mm --margin-bottom 16mm --margin-left 18mm --margin-right 18mm --encoding utf-8 cv.html output.pdf`
- Obsidian's built-in "Export to PDF" will work but won't match this layout.

## Voice / register
- Using **Version B (polished but de-buzzworded)** throughout. Keep strong verbs
  ("Led", "Architected", "Established"); avoid generic filler like
  "turning ambiguous problems into reliable, well-instrumented services".

## Content decisions already locked
- Iterable (CRM/messaging) = **current** work, main focus last ~2 years. Up top.
- E-commerce / subscriptions / micropayments = **earlier tenure**.
- Refer to **CEP** (the platform), not "CEP Gate". (Gate is one service within CEP;
  the monorepo rewrite was literally CEP Gate — clarify verbally if pressed.)
- **Loki removed** — not used.
- **No topologySpreadConstraints** in the Kubernetes bullet.
- **Knip** framed as facilitating the migration, not standalone cleanup.
- Two earliest roles compressed into one "Earlier experience" line.
- Homelab kept as a small, clearly self-directed section.
- Throughput / rps figure deliberately **left off**.
- "10+ workspaces" for the CEP rewrite (actual range given: 9–15).

## Resolved (2026-07-28)
1. **PostgreSQL** — kept in skills line; Marc confirmed it's defensible in interview.
2. **Title** — "Software Engineer" confirmed. At Findmypast, "Software Engineer" is
   the title used for mid-level engineers (no separate "Mid-Level Engineer" title
   exists there) — kept as-is, matches reality.
3. **London Met (2019–2020)** — was a final-year top-up (transferred in with prior
   credits, completed only the final year there). CV now reads
   "BSc Software Engineering (final year top-up)".
4. **Innovation Guild bullet added** — folded into the existing FMP bullet list
   (not a new section), sitting after the Kubernetes bullet and before the
   "(Earlier tenure)" bullet. Covers two of the three projects Marc described:
   an AI summary generator over newspaper search results with OCR-linked source
   text, and a similar summarizer for scanned historical transcripts. The third
   project (conversation → family tree) was **dropped** — least active, not
   worth the space. Marked `_(ongoing, periodic)_` since the guild work recurs
   roughly every 1–2 months for a few days at a time, not a one-off.

## Suggested next steps
- Cold re-read on a full screen with fresh eyes — **done twice** (initial pass +
  post-Innovation-Guild pass); Marc is now checking a PDF preview himself.
- Regenerate PDF once Marc confirms the preview looks right.
- Optional: a Topsort-tailored variant (surface REST/API integration + ownership
  language; likely drop the homelab section for that version).


