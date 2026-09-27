---
name: edit-style
description: Use this when changing colours, fonts, layout, or animations on the Clement Lab site.
---

# Edit style

1. All styles live in `assets/css/style.css`. Design tokens are in `:root`.
2. Change a colour by editing its token, not individual rules.
3. New colour? Add a token (`--d`, etc.) and document it in the Design system section of `AGENTS.md`.
4. Keep the dark theme and contrast readable (text at least #b8b8cc on the dark background).
5. Respect reduced motion: wrap new heavy animations in `@media (prefers-reduced-motion: no-preference)`.
6. Check the result at 1280px wide and at 375px (mobile) before pushing.
