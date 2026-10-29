# booking-v3 date hint contradicts day-first tenant parsing

Reports covered: **33** unique reports from merged ticket #4471 in the 2026-10-04 export.

booking-v3 prints MM/DD/YYYY for day-first tenants, while the form interprets input in tenant order. Affected form tenants: alder.physio, copper.studio, pale.harbour. R-41230: 6 January became 1 June. Align displayed hint and input parsing; test the hint and resulting stored date together.

Classification: deduplicate IDs, filter mergedInto=4471, join tenant configuration, then run causeOf in src/lib/kb/causes.ts. Browser locale and intakeTag are not authoritative.

Seen: 2026-04-17 to 2026-09-22. This is an export snapshot; refresh before a new count.

See src/routes/kb/incidents/4471-review/+page.svx and its rendered page for the full review.

Report IDs:

R-41230, R-41241, R-41251, R-41259, R-41262, R-41275, R-41294, R-41305, R-41308, R-41366, R-41372, R-41384, R-41387, R-41396, R-41400, R-41406, R-41415, R-41416, R-41418, R-41428, R-41439, R-41441, R-41449, R-41453, R-41456, R-41460, R-41472, R-41485, R-41493, R-41539, R-41572, R-41582, R-41584

## Final disposition

Engineering update on the course Challenge page: #4471 closed 2026-10-05. Hint disposition: won't fix; booking-v3 form retired. Closing as not planned because the affected form was retired rather than the hint repaired.

Source: https://hq.mega.dev/challenges/what-it-shows
