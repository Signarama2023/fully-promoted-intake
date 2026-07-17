# Fully Promoted Temecula — New Job Intake

A single-file quote/order build sheet. Fill out the form, get a live job-ticket
preview, save to a per-device Job Log, and optionally auto-email the ticket to
the team.

**Live form:** https://signarama2023.github.io/fully-promoted-intake/

## Everything lives in `index.html`

No build step, no dependencies. Open the file locally or host it anywhere static.

## Team email — via FormSubmit.co (free)

Jobs are emailed to the team through [FormSubmit.co](https://formsubmit.co) —
free, no account, and supports multiple recipients. To change who gets jobs,
edit the `RECIPIENTS` list in the `CONFIG` block near the top of the `<script>`
(comma-separated), then commit & push.

- The **first** address in `RECIPIENTS` is the primary; the rest are CC'd.
- **One-time activation:** the first send triggers a "Confirm your email" link
  from FormSubmit to the first address. Someone at that inbox clicks it once;
  after that every send goes through automatically. Use **Send test** on the
  page to confirm.
- No API key is stored in the page. If you change recipients, the new first
  address must confirm once again.

## The "view / edit online" link

Each job email includes a link that opens a read-only view of the whole job,
with an **Edit** button that reopens it as a pre-filled form. The job data
rides in the link's query string (`?job=…`) — no backend. Anyone with the link
can view that job, so treat it like the email itself (not secret).

## Notes

- The Job Log is stored per-device in the browser (localStorage). It is **not**
  shared across devices — share a job by emailing or copying its ticket/link.
