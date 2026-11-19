# Philo Gents Salon — Concept Site

A single-page concept website for Philo Gents Salon (The Icon Casa 3, JVC), built to
show what a dedicated site — with online booking — could look like. No build step —
`index.html` is a fully self-contained static page (fonts load from Google Fonts;
every photo is embedded directly in the file).

## Run locally

Just open `index.html` in a browser — no server or install needed.

## Deploy on Netlify

**Option A — connect this GitHub repo (recommended, auto-deploys on every push):**

1. Push this repo to GitHub (see below).
2. On [netlify.com](https://app.netlify.com), click **Add new site → Import an existing project**.
3. Pick this repository. Build settings are already set via `netlify.toml`
   (publish directory `.`, no build command needed) — just click **Deploy**.

**Option B — drag and drop (fastest, no GitHub needed):**

Go to [app.netlify.com/drop](https://app.netlify.com/drop) and drag `index.html` onto
the page.

## Push this repo to GitHub

```bash
git init
git add .
git commit -m "Philo Gents Salon concept site"
git branch -M main
git remote add origin https://github.com/<your-username>/<repo-name>.git
git push -u origin main
```

(Create the empty repo on GitHub first at github.com/new — don't initialize it with a
README, since this folder already has one.)

## About the booking widget

The "Book an Appointment" section is a **front-end-only demo** — it walks through a
realistic service → date → time → details → confirmation flow entirely in the
browser, with a deterministic pattern of "taken" time slots so it looks like a live
system. **Nothing is actually submitted anywhere** — no backend, no calendar, no SMS
or email. It exists to show the salon what a working booking system would feel like.
Wiring it up to something real (a calendar, a notification, a database) would be a
follow-on project once they're on board.

## Notes

- Service names and prices come directly from the salon's own printed price list
  (photographed menu) — no reconstruction needed, should be accurate as of when the
  photos were taken.
- Address, phone, hours, and rating are from the official Google Maps listing.
- Source photos used to build the page are kept locally but excluded from git via
  `.gitignore` (already baked into `index.html` as compressed images).
