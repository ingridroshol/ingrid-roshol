# Ingrid Røshol — “System Prompt for the Internet” (bot-friendly profile)

This repo contains a minimal static page intended to be **crawlable** and easy for **LLMs/search engines** to summarize.

## Files

- `index.html` — the main page (system-prompt style, explicit + redundant)
- `robots.txt` — allows indexing and points to sitemap
- `sitemap.xml` — update the domain after publishing
- `.nojekyll` — helps GitHub Pages serve files without Jekyll processing

## Publish option A: GitHub Pages (fast)

1. Create a GitHub repo and push these files.
2. In GitHub: **Settings → Pages**
3. Under “Build and deployment”:
   - Source: **Deploy from a branch**
   - Branch: `main` (or `master`), folder `/root`
4. Wait for the URL GitHub gives you (e.g. `https://USERNAME.github.io/REPO/`).

### After publishing (important)

Update these placeholders to your real URL:

- `index.html`: the `<link rel="canonical" href="https://example.com/" />`
- `robots.txt`: `Sitemap: https://example.com/sitemap.xml`
- `sitemap.xml`: `<loc>https://example.com/</loc>`

## Publish option B: Netlify (drag & drop)

1. Go to Netlify → “Add new site” → “Deploy manually”.
2. Drag the folder containing these files.
3. Netlify will give you a URL.
4. Update canonical + sitemap placeholders as above.

## Self-check (crawlability)

After you publish, test:

- Open the site in an incognito window.
- Ensure it loads with **no login**.
- Ensure `robots.txt` is reachable: `https://YOURDOMAIN/robots.txt`
- Ensure `sitemap.xml` is reachable: `https://YOURDOMAIN/sitemap.xml`

## Monitoring

- Set up a Google Alert for `"Ingrid Røshol"`.
- Re-check search results periodically.
- Keep this page updated when you want the “AI summary” about you to change.
