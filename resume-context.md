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

## Resolved (2026-07-28, continued — mock-interview pass)
Ran a full mock-interview drill across every FMP bullet to test whether the CV
reads senior enough. Every story held up under pushback; the gap was narration
(leading with situation, not decision), not competence. Applied CV edits to
surface the decisions once found:
5. **Multi-brand bullet** — now names the actual decision (temporarily extended
   the schema for legacy account data rather than dropping unmapped fields, to
   guarantee zero data loss).
6. **CEP monorepo bullet** — now credits the leadership mechanism (mobbed with
   the team to establish the pattern, then reviewed migrations for consistency)
   instead of just "led."
7. **Iterable bullet** — now credits two previously-uncredited builds: in-house
   dismiss-state tracking (Iterable's own dismiss logic wasn't permanent/
   cross-device) and Zod-based schema validation with alert-on-threshold
   (Iterable allows arbitrary JSON; thresholded rather than alerting on every
   failure since engagement-team testing accounts throw expected failures).
8. **Kubernetes bullet** — now names the actual root cause found and fixed:
   `maxUnavailable` = full pod count + missing/misconfigured readiness probes
   let bad deploys register as "ready" before serving traffic. Fix was scoped
   to Kafka consumers only (switched to Recreate + real probes; brief downtime
   there was already expected/acceptable) — RollingUpdate was kept for
   client-facing services. This scoping detail didn't make the CV bullet
   (kept short) but is worth having ready verbally.
9. **New bullet added — internal A/B testing framework** (previously not on
   the CV at all). Built frontend hooks (toggle/experiment-id fetching,
   variant serving) + backend support for dynamic free-trial length; adopted
   company-wide beyond Marc's own team. Flagship experiment: refactored a
   hardcoded 14-day free trial into a dynamic, journey-based length (e.g.
   3 days for search-heavy "hardcore" users, 7 for newbies), worked with data
   science on segmentation — **~40% conversion boost, all-time monthly record
   for trial starts**. This is arguably the strongest single story from the
   whole interview drill.
10. **Earlier-tenure bullet merged, not dropped** — Marc wanted room for the
    A/B testing bullet but was firm that the e-commerce/payments-migration
    story stay (it's a strong, high-stakes story on its own — phased cutover,
    vendor-assisted bulk migration, honest about a caching hiccup post-launch).
    Resolved by merging the migration bullet and the A/B testing framework
    into one earlier-tenure bullet (chronologically sequential: migration
    was year 1, experimentation was years 2–3, CRM/Iterable is years 4–5 —
    confirmed no timeline overlap with the "last two years" Iterable claim).
    Dropped the Cypress/Selenium/Jest stack detail to make room — least
    distinctive part of the original bullet.

## Suggested next steps
- Cold re-read on a full screen with fresh eyes — **done twice** (initial pass +
  post-Innovation-Guild pass); Marc is now checking a PDF preview himself.
- Regenerate PDF once Marc confirms the preview looks right.
- Optional: a Topsort-tailored variant (surface REST/API integration + ownership
  language; likely drop the homelab section for that version).
- Consider a fresh cold read now that 5 bullets changed/were added in the
  mock-interview pass — page length/density hasn't been rechecked since.


