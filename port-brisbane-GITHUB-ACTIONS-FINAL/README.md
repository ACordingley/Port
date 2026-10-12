# Port Brisbane - Whyte Island Live Tide

## How it works (no more 1.57m stuck)
GitHub Actions fetches https://opendata.tmr.qld.gov.au/Whyte_Island.txt every 5 mins server-side (no CORS) and commits it as Whyte_Island.txt in repo root.
Dashboard reads ./Whyte_Island.txt locally -> always live.

## Deploy
1. Create repo port-brisbane-tide (public)
2. Upload all files from this zip (including .github folder)
3. Settings -> Pages -> Deploy from branch -> main / root -> Save
4. Settings -> Actions -> General -> Workflow permissions -> Read and write -> Save
5. Actions -> Update Tide Data -> Run workflow -> Wait 30s
6. Open https://YOURNAME.github.io/port-brisbane-tide/ -> Should show Source: Local Whyte_Island.txt (GitHub Actions - LIVE)

If it still shows embedded fallback, Actions hasn't run yet. Check Actions tab for green check.
