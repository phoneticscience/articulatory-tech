# Session Log: 2026-02-23

## What was done

### Custom Domain Configuration
- Added `public/CNAME` file with `articulatory.tech` to persist custom domain across deploys
- Committed and pushed to `main` (triggered GitHub Actions deploy)
- Configured Cloudflare DNS:
  - Added 4 A records for apex domain (`articulatory.tech`) → GitHub Pages IPs (`185.199.108-111.153`), all DNS only
  - Added CNAME record: `www` → `phoneticscience.github.io`, DNS only
- Enabled "Enforce HTTPS" in GitHub Pages settings
- Verified `https://articulatory.tech` is live and returning HTTP 200
- `www.articulatory.tech` still propagating at end of session

### Housekeeping
- Updated `TODO.md` with consolidated task list (domain, content, design, features)

## Status
- Site is live at https://articulatory.tech
- `www` subdomain DNS propagation pending
- TLS certificate provisioned for apex domain
