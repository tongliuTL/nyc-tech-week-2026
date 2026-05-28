# NYC Tech Week 2026 — Personal Agenda

Personal event tracker for [NYC Tech Week](https://www.tech-week.com/calendar/nyc) (Jun 1–7, 2026), presented by a16z.

**Live page:** https://tongliutl.github.io/nyc-tech-week-2026/

## What's in here

| File | Purpose |
|---|---|
| `index.html` | The agenda — all events, statuses, route maps |
| `.github/workflows/deploy.yml` | Auto-deploys to GitHub Pages on every push to `main` |

## Updating the agenda

Edit `index.html` locally at `~/Documents/Courses/nyc-tech-week-2026.html`, then push:

```bash
gh api repos/tongliuTL/nyc-tech-week-2026/contents/index.html \
  --method PUT \
  --field message="Update agenda" \
  --field sha="$(gh api repos/tongliuTL/nyc-tech-week-2026/contents/index.html --jq '.sha')" \
  --field content="$(base64 -i ~/Documents/Courses/nyc-tech-week-2026.html)"
```

GitHub Actions picks it up and the live page updates in ~60 seconds.

## Events tracked

| Day | Confirmed | Pending/Waitlist |
|---|---|---|
| Mon Jun 1 | Maersk, IBM Generative Computing | IBM Beyond the Spec, Kickoff Party |
| Tue Jun 2 | Agentic Commerce, Cloudflare + Shopify | Operating MCP |
| Wed Jun 3 | Architecture of Failure | Anthropic Founder Salon |
| Thu Jun 4 | Snowflake Cafe at Verci | — |
