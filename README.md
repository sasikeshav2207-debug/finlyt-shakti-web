# finlyt-shakti-web

Marketing landing site for **FinLytTech Shakti** — the women's financial inclusion vertical of FinLytTech.

**Live at:** [shakti.finlyt.net](https://shakti.finlyt.net)

## What this repo serves

- `index.html` — the Shakti landing page (hero, 3-layer problem, 3 products, journey, founders, waitlist)
- `terms.html` — Terms of Service (Shakti-specific, MUDRA disclosure, AI content warning)
- `privacy.html` — Privacy Policy (DPDP Act 2023 aligned, includes Samuh SHG-specific data handling)
- `CNAME` — `shakti.finlyt.net` (GitHub Pages custom domain)

## Brand palette (locked)

| Role | Hex | Where |
|---|---|---|
| Primary | `#1E3A5F` Coastal indigo | Buttons, section headers, MUDRA-Ready Score bar |
| **Wordmark accent** | **`#C24E2E` Terracotta** | The "lyt" letters in `finlyttech` |
| Secondary | `#D87A6A` Coral | Tagline accent, secondary CTAs |
| Accent | `#C9A961` Brass gold | MUDRA-Ready callouts, "Shakti" pill, highlights |
| Surface | `#F8F1E3` Off-white shell | Page background |
| Ink | `#1A2332` Slate | Body text |

## Wiring

- **Waitlist form** posts to `https://finlyt-backend.onrender.com/api/enquiry` with
  `source: "Shakti Web — waitlist"` so the admin /admin/enquiries view tags these distinctly.
- **Trial signups** route to `https://dashboard.finlyt.net/signup` (the main app). Backend
  detects the `journey=shakti` cookie / referer and renders the Shakti shell after auth.
  (Backend wiring lands separately in the `finlyt-app` repo.)

## Deploy

GitHub Pages auto-deploys on push to `main`. Custom domain `shakti.finlyt.net` set in repo
Settings → Pages.

## Repo siblings

- `finlyt-web` — main marketing site (finlyt.net)
- `finlyt-app` — React app (dashboard.finlyt.net)
- `finlyt-shakti-web` — this repo (shakti.finlyt.net)
