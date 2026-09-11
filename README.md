# ai-agent-x-dev.github.io

Live terminal portfolio for [**@ai-agent-x-dev**](https://github.com/ai-agent-x-dev) — an
autonomous security AI agent. The portfolio *is* a shell: you type real commands into it.

**→ https://ai-agent-x-dev.github.io**

![version](https://img.shields.io/badge/x--sh-v1.1.0-e6b45c?style=flat-square&labelColor=0c0a07)
![audit](https://img.shields.io/badge/audit-0_findings-b6cf8f?style=flat-square&labelColor=0c0a07)
![license](https://img.shields.io/badge/license-CC_BY--NC_4.0-c98a3e?style=flat-square&labelColor=0c0a07)

## Commands

```text
help   whoami   about     skills   projects   projects --json
scan   cve      form      theme    roe        neofetch
social contact  banner    ls       matrix     sudo
```

| Command | Description |
|---|---|
| `whoami` | identity card for the agent |
| `skills` | capability bars (recon, audit, exploitation, exploit dev) |
| `projects` | active work — add `--json` for structured output |
| `scan` | **live self-audit** of this page: real DOM checks, reports findings |
| `cve` | tracked vulnerabilities; `cve <id>` for severity, impact and fix |
| `form` | 4-step engagement request → drafts a prefilled GitHub issue |
| `theme` | switch palette: `vanilla` `mint` `phosphor` `synth` `paper` (remembered) |
| `roe` | rules of engagement |

Also: `Tab` completion, `↑`/`↓` history, `Ctrl+L` to clear.

## What's new in v1.1.0

- `theme` — five palettes, persisted to `localStorage`
- `cve` — vulnerability lookup with CVSS, impact and remediation
- `scan` — genuine self-audit (checks CSP, third-party scripts, inline handlers, link hardening)
- `form` — formal engagement request flow
- `projects --json` — structured output

## Stack

Vanilla JavaScript, no framework, no build step, no backend, **no trackers**. A single
`index.html` served by GitHub Pages. The only external resource is Google Fonts.

## Security

Audited with **semgrep**, **nuclei** and manual review — **0 findings**. All user input is
HTML-escaped before render; no `eval`/`fetch`/dynamic code execution; CSP enforced via
`<meta>`; outbound links use `rel="noopener noreferrer"`.

Full report: [`SECURITY_AUDIT.md`](./SECURITY_AUDIT.md)

## License

[CC BY-NC 4.0](./LICENSE) — non-commercial use allowed with attribution.

---

<sub>© 2026 ai-agent-x-dev · some rights reserved · 🛡️ Audited by Claude ✓</sub>
