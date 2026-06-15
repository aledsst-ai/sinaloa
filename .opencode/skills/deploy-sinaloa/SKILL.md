---
name: deploy-sinaloa
description: Build, commit, push and deploy the Sinaloa project to Cloudflare Workers
---

## Steps
1. Run `build.ps1` in the project root to rebuild `index.html` from section partials
2. Check `git status` and `git diff` to see what changed
3. Stage all changes with `git add -A`
4. Commit with a concise message describing the changes (present tense, no period)
5. Push to `origin/main`
6. Verify the deploy by fetching `https://sinaloa.aledsst.workers.dev` and checking for the expected changes
7. If deploy seems stale, ask the user to check the Cloudflare Workers dashboard

## Context
- Repo: https://github.com/aledsst-ai/sinaloa.git
- Workers URL: https://sinaloa.aledsst.workers.dev
- Firebase project: sinaloa-mtp
- Logo: `assets/img/logo.png`
