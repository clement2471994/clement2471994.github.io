---
name: add-page
description: Use this when adding a new page (e.g. /projects, /about) to the Clement Lab site.
---

# Add a page

1. Create `<slug>/index.html` (lowercase, hyphenated slug) so the URL is `/<slug>/`.
2. Copy the `<head>` from the root `index.html` (charset, viewport, fonts, `/assets/css/style.css`) and set a unique `<title>` like `Projects · Clement Lab`.
3. Keep the background layers (`.blob` x3 and `.grid`) so the page matches the home page.
4. Put content inside `<main>`; reuse `.card`, `.tag`, `h1`, `.line` before inventing new classes.
5. Add page-specific styles to `assets/css/style.css` under a comment `/* page: <slug> */`.
6. Link the new page from the home page if the owner wants it discoverable.
7. Add the page to `llms.txt`.
8. Preview locally, commit, push, then run the `deploy-check` skill.
