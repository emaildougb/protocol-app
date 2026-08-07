# HANDOFF — protocol-app (Quick Protocols)

## What it does

Clark County EMS protocol quick reference for NCEMS crews — the "Quick Protocols" button on the Apps Hub. Single-file web app (`protocol-app.html`, ~58 KB), no build step, hosted on GitHub Pages.

21 protocols in six categories (Cardiac, Respiratory, Airway, Neuro, Toxicology, Other): anaphylaxis, asthma, COPD, CHF, VFib, asystole, PEA, ROSC, bradycardia, stable/unstable tachycardia, ACS, DSI, AMS, seizure, stroke, sepsis, shock, pain, hyperkalemia, poisoning, and more. Each protocol is an expandable card with four tabs: Signs/Sx, Meds (drug/dose/route/when/notes), Actions (step list), and Red Flags. Live text search plus category filter buttons.

- Live: <https://emaildougb.github.io/protocol-app/>
- Repo: <https://github.com/emaildougb/protocol-app>

## Where the data lives

Nowhere external — **everything is baked into the HTML.** All protocol content lives in one big `const P = [...]` array at the top of the script. No localStorage, no fetch calls, no network dependency of any kind; it works fully offline once loaded. To change a dose or add a protocol, you edit the `P` array and redeploy.

## Structure

- `index.html` — the entire app (renamed from `protocol-app.html` on 2026-08-07 so the repo root URL works). Data array `P`, category map `CAT`, then rendering (search/filter → card list → tab switching) all in one inline script.
- `protocol-app.html` — redirect stub to `index.html`, kept so old bookmarks and links don't break.
- `HANDOFF.md` — this file.
- That's it. No README, no icons, no manifest.

## Anything odd

- **The repo is named `protocol-app`, not `Protocols`.** The migration status doc and some earlier links used `Protocols`, which 404s. Keep this in mind anywhere the app gets linked.
- No home-screen icon, no apple-touch-icon, no web-app meta tags — unlike Intubation and the hub, this one hasn't been dressed up for iOS install yet.
- Protocol content is based on the Clark County EMS protocols. Same caveat as the Intubation guide: reference tool, verify against current protocol book, doesn't supersede clinical judgment.
- One git commit ("Add files via upload") — uploaded through the GitHub web UI during the migration, now cloned locally for the GitHub Desktop workflow like the other apps.
