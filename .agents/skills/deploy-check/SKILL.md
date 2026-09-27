---
name: deploy-check
description: Use this after pushing to main to confirm the change is live on GitHub Pages.
---

# Deploy check

1. Push to `main`. GitHub Pages rebuilds automatically.
2. Check the build: `gh api repos/clement2471994/clement2471994.github.io/pages/builds/latest --jq .status` (wait for `built`).
3. Fetch the live page: `curl -s https://clement2471994.github.io/<path> | grep -o '<title>.*</title>'` and confirm the expected title.
4. If it still shows old content after 2 minutes, it is CDN cache; retry with `?v=<timestamp>`.
5. If the build errored, read `gh api repos/clement2471994/clement2471994.github.io/pages/builds/latest --jq .error`.
