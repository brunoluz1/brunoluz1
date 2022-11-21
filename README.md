name: Update top issues dashboard
on:
  schedule:
    - cron: "0 0 */3 * *"

jobs:
  showAndLabelTopIssues:
    name: Update top issues Dashboard.
    runs-on: ubuntu-latest
    steps:
      - name: Run top issues action
        uses: rickstaa/top-issues-action@v1
        env:
          github_token: ${{ secrets.GITHUB_TOKEN }}
        with:
          filter: "1772"
          label: false
          dashboard: true
          dashboard_show_total_reactions: true
          top_issues: true
          top_bugs: true
          top_features: true
          top_pull_requests: true



<p dir="auto"><a target="_blank" rel="noopener noreferrer" href="https://github.com/rafaballerini/rafaballerini/blob/output/github-contribution-grid-snake.svg"><img src="https://github.com/rafaballerini/rafaballerini/raw/output/github-contribution-grid-snake.svg" alt="Snake animation" style="max-width: 100%;"></a></p>
