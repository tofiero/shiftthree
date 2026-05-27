Deployment options

1) GitHub Pages (quick)
- Push this repo to GitHub (remote `origin`) on branch `main`.
- The included GitHub Action `.github/workflows/deploy-pages.yml` will publish the repository root to the `gh-pages` branch and enable Pages.

2) Cloudflare Workers (preview + custom domain)
- Install Wrangler: `npm install -g @cloudflare/wrangler` or see https://developers.cloudflare.com/workers/cli-wrangler/installation
- Fill `wrangler.toml` with your `account_id` and optionally `route`/`zone_id`.
- Authenticate: `wrangler login` or set `CF_API_TOKEN`.
- Publish: `wrangler publish`

Notes
- GitHub Pages is the easiest: it uses the automatic `GITHUB_TOKEN` secret and requires no additional secrets.
- Cloudflare Workers requires an account and API token; the `wrangler.toml` provided is a template.
