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

| Day | Time | Event | Status |
|---|---|---|---|
| Mon Jun 1 | 8:30am | Maersk: The Future of Supply Chain | ✅ Approved |
| Mon Jun 1 | 12:30pm | IBM Generative Computing Masterclass | ✅ Approved |
| Mon Jun 1 | 2:00pm | IBM Beyond the Spec Masterclass | ✅ Approved |
| Mon Jun 1 | 6:30pm | Tech Week Kickoff Party | ⛔ At capacity |
| Tue Jun 2 | 9:00am | Agentic Commerce: Build Day | ✅ Approved |
| Tue Jun 2 | 4:00pm | Operating MCP | 🟠 Waitlist |
| Tue Jun 2 | 6:00pm | Cloudflare + Shopify: Build for the Agent Era | ✅ Approved |
| Wed Jun 3 | 10:45am | Architecture of Failure (AI Agents Masterclass) | ✅ Approved |
| Wed Jun 3 | 1:30pm | Anthropic Founder Salon | 🟠 Pending |
| Thu Jun 4 | 9:00am | Snowflake Cafe at Verci | ✅ Approved |

## Leave-home times

Route maps in the page show exact timing sourced from MTA GTFS + OpenStreetMap routing.

| Day | Leave home | Train | GCT arrive | Subway to venue |
|---|---|---|---|---|
| Mon Jun 1 | 6:54am | dep 7:09am | 7:46am | 4/5/6 → 14th St (15 min) |
| Tue Jun 2 | 7:20am | dep 7:35am | 8:10am | 6 → Spring St (18 min) |
| Wed Jun 3 | 8:59am | dep 9:14am | 9:48am | S → Times Sq → 1 (15 min) |
| Thu Jun 4 | 7:50am | dep 8:05am | 8:38am | 4/5/6 → 23rd St (10 min) |

