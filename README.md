# LuckyNumber Scheduler

This public repository triggers the private LuckyNumber repository's workflows via repository_dispatch.

## Purpose

GitHub Actions scheduled workflows don't reliably run on private repositories. This public repository acts as a reliable scheduler that triggers the private repository's workflows.

## Workflows

### Automated Schedule

- **Theather (Weather Video)**: Daily at UTC 17:00

### Manual Trigger

You can manually trigger any workflow from the Actions tab with the following options:
- `theather` - Weather video generation
- `trendviz` - Trend visualization videos
- `ai-insight` - AI insight cards
- `daily-short` - Daily short videos
- `all` - Trigger all workflows

## Setup

1. Create a Personal Access Token (PAT) with `repo` scope at https://github.com/settings/tokens
2. Add the PAT as a repository secret named `PAT_FOR_PRIVATE_REPO` in this repository's Settings → Secrets and variables → Actions
3. The workflow will automatically run daily at the scheduled time

## Workflows Triggered

This scheduler triggers the following workflows in the private `zhetai/LuckyNumber` repository:
- `process-weather-request.yml` - Theather/Weather Video
- `trendviz_pipeline.yml` - Trend Visualization
- `daily_pipeline.yml` - AI Insight Cards
- `_daily_render_requirements.yml` - Daily Short Videos
