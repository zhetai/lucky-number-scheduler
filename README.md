# LuckyNumber Scheduler

This public repository triggers the private LuckyNumber repository's daily pipeline workflow via repository_dispatch.

## Purpose

GitHub Actions scheduled workflows don't reliably run on private repositories. This public repository acts as a reliable scheduler that triggers the private repository's workflow daily at UTC 00:05.

## Setup

1. Create a Personal Access Token (PAT) with `repo` scope at https://github.com/settings/tokens
2. Add the PAT as a repository secret named `PAT_FOR_PRIVATE_REPO` in this repository's Settings → Secrets and variables → Actions
3. The workflow will automatically run daily at UTC 00:05

## Manual Trigger

You can also manually trigger the workflow from the Actions tab.
