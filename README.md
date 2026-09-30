# momen — event photo-sharing validation landing

Live (once DNS resolves): **[momen.nino.id](https://momen.nino.id/)**

Single-file static landing page for the "Momen" concept — QR photo
pooling + AI curation + per-person albums for events (weddings,
birthdays, family gatherings, open trips, corporate). This page is a
**product-validation asset**, not a launched product:

- backs the X/Threads smoke-test and organizer outreach run by the
  NinoGenio vault (`kb/reference/trip-photo-sharing-validation-plan.md`)
- waitlist form hands off to the company WhatsApp — no backend
- no pricing is shown anywhere on the page (deliberate)

## Deploy

GitHub Pages, **deploy from branch** (`main` / root). No build step.

- `CNAME` file pins the custom domain `momen.nino.id`
- DNS (one-time, done by founder at the nino.id DNS provider):
  `CNAME momen → ninogenio.github.io`
- HTTPS: GitHub provisions the certificate automatically once DNS
  resolves; enforce-HTTPS should then be enabled in repo Settings →
  Pages (or `gh api -X PATCH repos/NinoGenio/momen/pages -f https_enforced=true`)

## Editing

Edit `index.html` and push to `main` — live in ~1 minute. The internal
source-of-truth pointer and validation context live in the vault:
`kb/website/momen.md`.

Open items: og:image (1200×630) for rich X/Threads previews; replace
placeholder brand "Momen" (find & replace) once named; verify the
WhatsApp number in the three `wa.me/62819797967675` occurrences.
