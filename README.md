# Fully Promoted Temecula — New Job Intake

A single-file quote/order build sheet. Fill out the form, get a live job-ticket
preview, save to a per-device Job Log, and optionally auto-email the ticket to
the team.

**Live form:** https://signarama2023.github.io/fully-promoted-intake/

## Everything lives in `index.html`

No build step, no dependencies. Open the file locally or host it anywhere static.

## Turning on team email (optional, ~2 min)

Email is off until you add a key. In `index.html`, find the `CONFIG` block near
the top of the `<script>` and edit:

1. Create a free access key at [web3forms.com](https://web3forms.com) using **your
   own email** (you'll get a copy of every job).
2. Paste it into `WEB3FORMS_ACCESS_KEY`.
3. Put your team's real addresses in `TEAM_EMAILS`, comma-separated (they're CC'd).
4. Commit & push. Use **Send test** on the page to confirm it lands.

> The page is public, so the Web3Forms key is visible in the source — that's
> expected for Web3Forms. If it's ever abused, regenerate the key or put the page
> behind a login (e.g. Cloudflare Access).

## Notes

- The Job Log is stored per-device in the browser (localStorage). It is **not**
  shared across devices — share a job by emailing or copying its ticket.
