# S01E03 review artifacts

This repository reviews the support knowledge-base export dated 2026-10-04.

- Review source: `src/routes/kb/incidents/4471-review/+page.svx`
- Rendered review: `rendered/4471-review.html` (self-contained snapshot; controls disabled)
- Full-page image: `rendered/4471-review.png`
- Issue drafts: `issue-drafts/parser.md`, `issue-drafts/hint.md`
- Reproducible report membership: `report-analysis.json`
- Proposed decision: `src/routes/kb/decisions/0002-dedupe-by-cause/+page.svx`

The table runs the exported cause logic over deduplicated reports: 379 parser, 33 hint.
Five unusual reports remain in the parser count as the classifier assigns them; their
bodies require further investigation. No third root cause is established by this export.

The original accepted decision 0001 and incident 4471 are preserved. Triage has a proposed
update. Components and their computation logic are preserved.

## Rebuild

Run `npm ci`, then `npm run build`. The Vite build produces the interactive bundle in
`rendered/`. To inspect it locally, run `npm run dev` and open
`/kb/incidents/4471-review`. The HTML snapshot and PNG were captured from the rendered
page, not inferred from the Markdown. Rebuilding clears `rendered/`, so recapture these
two review artifacts afterward. The dynamic bundle can also render the other KB routes.

The snapshot reflects the 2026-10-04 data and the 2026-10-29 review date. It is not a live
support queue. Refresh the export and regenerate views and issue counts before a new handoff.
