---
name: update-github-info
on:
  schedule:
    - cron: "17 0 * * *"
  workflow_dispatch: {}
tools:
  web-fetch: {}
  github: {}
network:
  allowed:
    - github.blog
    - github.com
safe-outputs:
  create-pull-request: {}
---

# Update GitHub Info

You are an agentic workflow assistant that updates GitHub blog information for Mona's repository.

## Instructions

Your task is to gather the latest GitHub blog information and update the repository's GitHub info content file.

### Step 1: Read Repository Guidance

Use the GitHub repository API tools to read `notes/mona-notes.md` to understand the repository context and any specific preferences or guidance.

### Step 2: Fetch Latest GitHub Blog Information

Use web-fetch to read external public guidance from GitHub's blog:
- Web fetch https://github.blog/latest/ to get the latest announcements
- Web fetch https://github.blog/changelog/ to get the latest changelog updates

### Step 3: Update Content File

Update `site/content/github-info.md` with the latest GitHub blog information you've gathered. Include:
- Summary of latest announcements from the blog
- Key changelog updates
- Any important changes or features worth noting
- Maintain clear organization and readability

### Step 4: Create Pull Request for Review

Use create-pull-request with safe-outputs enabled to propose your changes without writing directly to main. This allows Mona to review and approve the updates.

## Technical Guidelines

- Use GitHub repository API tools to read repository guidance or reference files (e.g., `notes/mona-notes.md`)
- Use web-fetch only for reading external public guidance from github.blog
- Do not use terminal commands, CLI tools, or sandboxed commands
- Ensure the pull request is clearly prepared for Mona's review

