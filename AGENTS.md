# AGENTS.md

Instructions for AI coding agents (Cursor, Claude Code, Codex, Copilot, etc.) working in this repo.
Humans: see `README.md`.

## Project

Clement Lab is a static personal site served by **GitHub Pages** at https://clement2471994.github.io.
There is no build step, no framework, and no server. Every file on `main` is published as-is.

## Structure

```
index.html            Home page (Clement Lab hero)
assets/css/style.css  All shared styles and design tokens
assets/js/            Optional scripts (create only when needed)
<page>/index.html     Extra pages, one folder per page (clean URLs)
.agents/skills/       Task playbooks for agents (read the relevant SKILL.md first)
.cursor/rules/        Cursor rule that points back to this file
.nojekyll             Disables Jekyll so files are served raw
llms.txt              Short machine-readable summary of the site
```

## Design system

- Dark theme only. Background `--bg: #07070c`.
- Accent colours: `--a` violet `#7c5cff`, `--b` cyan `#00e5ff`, `--c` pink `#ff3cac`.
- Font: Space Grotesk (Google Fonts), weights 300 / 600 / 700.
- Signature elements: blurred floating colour blobs, faint grid overlay, frosted-glass card, animated gradient headings.
- Reuse the tokens in `:root`; do not hard-code new colours without adding a token.

## Rules

1. Keep it static: plain HTML, CSS, and vanilla JS. No build tools or npm unless the owner asks.
2. Use absolute asset paths (`/assets/...`) so nested pages work.
3. Every page needs `<meta name="viewport">`, a `<title>`, and must link `/assets/css/style.css`.
4. This repo is **public**. Never commit secrets, tokens, or private data.
5. Keep pages accessible: semantic tags, alt text, sufficient contrast.
6. Commit with clear messages. Pushing to `main` deploys within about a minute.

## Skills

| Skill | Use when |
|---|---|
| `.agents/skills/add-page/SKILL.md` | Adding a new page or section |
| `.agents/skills/edit-style/SKILL.md` | Changing the look, colours, or animations |
| `.agents/skills/deploy-check/SKILL.md` | Verifying a change is live on GitHub Pages |

## Verify

- Local preview: `python3 -m http.server 8000` then open http://localhost:8000
- Live check: follow `deploy-check`.
