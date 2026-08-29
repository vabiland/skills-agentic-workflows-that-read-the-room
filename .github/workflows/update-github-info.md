---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site.
on:
  workflow_dispatch:
safe-outputs:
  create-pull-request:
    title-prefix: "[mona] "
    draft: true
    fallback-as-issue: false
---

# Update Mona's GitHub Info website

Read `notes/mona-notes.md` before making changes.

Update `site/content/github-info.md` with concise, practical updates for readers based on the information available in `notes/mona-notes.md`.

Open a pull request for Mona to review. 
Use a pull request title that mentions Mona or GitHub Info. 
Do not write directly to `main`; rely on `safe-outputs` with `create-pull-request`.
