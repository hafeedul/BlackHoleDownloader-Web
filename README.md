# Black Hole Downloader — Website

Minimalist landing page + APK host for the Black Hole Downloader Android app.
Static site, deploys free on Vercel.

## Files

| File | Purpose |
|------|---------|
| `index.html` | The landing page (SEO-optimized, light minimalist) |
| `app.apk` | **Your APK** — replace this file to publish a new version |
| `vercel.json` | Serves the APK with the correct download headers |
| `robots.txt` / `sitemap.xml` | Search-engine crawling + indexing |
| `site.webmanifest` / `favicon.svg` | Icon + PWA metadata |

> **Note:** The APK is 25 MB+, so it is hosted via **GitHub Releases** (not committed to the repo). The download button points to `github.com/hafeedul/BlackHoleDownloader-Web/releases/latest/download/app.apk`, which always serves the newest release.

## One-time setup

1. **Push the site to GitHub.** Create a repo and upload all these files (you do NOT upload the APK here).
2. **Fill in your repo details.** In `index.html`, replace `hafeedul/BlackHoleDownloader-Web` (3 places) with your GitHub username and repo name.
3. **Create the first Release with your APK.** Repo page → **Releases** → **Create a new release** → tag `v1.0.0` → drag your APK (named `app.apk`) into "Attach binaries" → **Publish release**.
4. **Deploy on Vercel.** vercel.com → New Project → import the GitHub repo → Deploy. No build settings needed (static site).
5. **Point search engines.** After deploy, replace `blackholedownloader.vercel.app` with your real domain in `index.html` (canonical + og:url), `robots.txt`, and `sitemap.xml`. Then submit the site in [Google Search Console](https://search.google.com/search-console).

## Updating the APK (your main workflow)

1. On your repo page, go to **Releases → Draft a new release**.
2. Give it a new tag (e.g. `v1.1.0`), attach your new build named `app.apk`, and **Publish**.
3. That's it — the download button automatically serves the latest release. No site redeploy needed.

> Tip: bump the version number shown on the page by editing the spots in `index.html` that say `v1.0.0`.

## SEO already included

- Optimized `<title>`, meta description, and keywords targeting "tiktok downloader", "youtube downloader", "twitter video downloader", etc.
- Open Graph + Twitter Card tags for link previews.
- `SoftwareApplication` + `FAQPage` structured data (JSON-LD) for rich Google results.
- `sitemap.xml` + `robots.txt`.
- FAQ section with real keyword-rich questions.

## Optional: social share image

Add a `1200×630` PNG named `og-image.png` to this folder for nice link previews on social media (the meta tags already reference it).
