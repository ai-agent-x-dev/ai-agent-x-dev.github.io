# Changelog

All notable changes to the Agent X terminal (`x-sh`) are documented here.

## v1.2.0 — 2026-09-15

### 🔒 Fully self-contained — nothing external
This release is **100% self-contained**. The page **loads nothing external, uploads
nothing, and connects to nothing**:
- **No external requests** — no CDNs, no analytics, no trackers, no third-party scripts.
- **Fonts are embedded** in the page (base64 woff2) — the previous Google Fonts links
  were removed, so there is no font CDN dependency.
- **No network egress at all** — enforced by CSP `default-src 'none'` and
  `connect-src 'none'`; there is no `fetch`, `XMLHttpRequest`, or WebSocket in the code.
- **No data collection** — no cookies, no backend. The engagement form transmits
  nothing on its own; it only drafts a GitHub issue link that *you* choose to open.
- **Works fully offline** — verified rendering with DNS blocked.
- Security re-audit for v1.2.0: **0 findings** (SAST + manual + offensive DOM-XSS review).
  See `SECURITY_AUDIT.md`.

### ✨ Added
- **`hack`** — an HTB-style box-pwning mini-game (aliases: `htb`, `pwn`). Picks a random
  target and runs the full kill-chain: recon → foothold → user flag → privesc → root flag
  → "owned". Five boxes, randomized flags/IP each run. Lab simulation only.
- **`banner`** now animates — a glow-pulse + flicker intro (respects
  `prefers-reduced-motion`).
- Footer **hover-illuminate** — footer items brighten on hover, stay subtle otherwise.
- Footer **meta row** — last-audit date, tooling, and version tag (`v1.2.0`), driven by a
  single `VERSION` constant.
- **`prefers-contrast: more`** support — brighter palette for high-contrast users.

### 🛠 Fixed
- **`matrix`** now fills the whole window — the canvas was stuck at its default 300×150
  size (rendered only in a corner); it now sizes to the terminal and rains full-screen.
  Stops on any key or click.
- **Accessibility / contrast (WCAG AA)** — the footer separator color failed AA
  (2.37:1); muted text tokens were re-tuned to pass (now ≥4.6:1).

### 🔤 Changed
- **Short display name** — the page title and copy now use **Agent X**; the terminal's
  own identity (`ai-agent-x-dev`, titlebar, aria-labels) is unchanged.
- Version bumped to **v1.2.0** across the page, `README.md`, and `SECURITY_AUDIT.md`.

---

## v1.1.0 — 2026-09-11
- Initial public release: themes, `cve`, `scan`, engagement form, `projects --json`,
  full command reference. Security audit: 0 findings.

---

_Project inspired by **andrei-quest** by C4sh$R._
