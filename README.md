# allfloridapodiatry.com

Website for All Florida Podiatry. Static site on GitHub + Cloudflare Pages — no build step, no framework. Cloudflare Pages serves `public/` as-is.

Currently a **coming-soon placeholder** (`noindex`). Remove the `noindex` meta tag when the real site goes up.

## Deploy (Cloudflare Pages)

Pages → Create → Connect to Git → `bluemoonco/allfloridapodiatry.com`

| Setting | Value |
|---|---|
| Framework preset | None |
| Build command | (leave empty) |
| Build output directory | `public` |
| Root directory | `/` |

Every push to `main` deploys.

- **Custom domains:** `www.allfloridapodiatry.com` and `allfloridapodiatry.com`. Canonical is www.
- **Redirect Rule** (Rules → Redirect Rules): `allfloridapodiatry.com/*` → `https://www.allfloridapodiatry.com/${1}`, 301, keep query string.
- **Let the bots in** (once the real site is live): Security → Bots / AI Crawl Control → turn off "Block AI bots" and Cloudflare's managed robots.txt. Leave Bot Fight Mode off.

## Files

```
public/
  index.html   coming-soon page (noindex)
  404.html
  robots.txt
  _headers     Cloudflare Pages security headers
```

Preview locally: `python3 -m http.server 8765 --directory public`
