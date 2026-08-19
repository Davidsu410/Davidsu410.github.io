# David Su — Personal Academic Website

A lightweight, static site (HTML/CSS/JS only — no build step) for David Su, PhD candidate in Sociology at UC Berkeley. Domain: **davidsu.org**.

## Files

```
index.html            Home / About
research.html         Research statement + conference presentations
publications.html     Publications and working papers
teaching.html         Teaching experience & professional service
awards.html            Full list of fellowships & paper awards
css/style.css          All styling
js/main.js             Tiny script (auto-updates footer year)
assets/headshot.jpg    Homepage headshot
assets/CV_David_Su.pdf Downloadable CV (public version)
robots.txt              Tells search engines they can crawl the site
sitemap.xml              Lists pages for search engines
CNAME                    Tells GitHub Pages to serve the site at davidsu.org
```

## 1. Publish it for free with GitHub Pages

1. Create a GitHub account if you don't have one (github.com).
2. Create a new **public** repository — the name doesn't matter as much now since you'll use a custom domain, but `davidsu.org` or `personal-site` both work fine. (If you'd rather use the free `username.github.io` address instead of the custom domain, name the repo exactly `username.github.io` and skip step 4 below / delete the `CNAME` file.)
3. Upload all the files in this folder to that repository (drag-and-drop on github.com works fine, or use `git push` if you're comfortable with git).
4. In the repo, go to **Settings → Pages**, and under "Source" choose the `main` branch, `/ (root)` folder. Save.
5. Still in Settings → Pages, under "Custom domain" enter `davidsu.org` and save — GitHub will pick up the `CNAME` file already included in this folder. Check "Enforce HTTPS" once it becomes available (can take a few minutes to an hour after DNS propagates).

This costs **$0** for hosting — GitHub Pages is free indefinitely for public repos. Your only cost is the domain itself, which you've already paid for.

## 2. Point davidsu.org at GitHub Pages

In your domain registrar's DNS settings for davidsu.org, add:

- Four **A records** for the apex domain (`@`), pointing to GitHub Pages' IPs:
  `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
- One **CNAME record** for `www` pointing to `<your-github-username>.github.io`

DNS changes can take anywhere from a few minutes to ~24 hours to fully propagate. Once it does, `https://davidsu.org` will resolve straight to your site.

## 3. Getting it to rank on Google

Ranking #1 for your own name is very achievable for an academic site with almost no competition; broader terms are harder, so focus on name-based searches.

1. **Submit to Google Search Console** (search.google.com/search-console, free). Verify ownership of `davidsu.org` (DNS TXT record or HTML file method), then submit `sitemap.xml` and request indexing for the homepage. This is the single highest-leverage step — it can get you indexed within days instead of weeks.
2. **Get backlinks from authoritative sites** — this matters more than anything on the page itself:
   - Ask to have your UC Berkeley Sociology department profile page link to davidsu.org.
   - Add the URL to your Google Scholar profile, ORCID, LinkedIn, and ASA member directory.
   - List it in any conference program bios or grant/fellowship pages that mention you.
3. **Keep metadata accurate** — title tags, meta descriptions, and the embedded JSON-LD `Person` schema (in `index.html`) are already set up for davidsu.org; update them if your title or affiliation changes.
4. **Update content periodically.** Search engines favor sites that change; add new publications/talks/awards as they happen and Google will re-crawl faster.
5. **Page speed & mobile-friendliness** are already handled — the site is plain HTML/CSS with no heavy frameworks, so it loads fast and passes Core Web Vitals by default.
6. The headshot is already compressed to a reasonable web size (~75KB) so it won't slow the page down.

## 4. Updating content

Everything is plain HTML — open any `.html` file in a text editor, find the relevant `<div class="entry">` block (or, on the Research page, `<div class="project">`), and copy/adapt it for new items (a new paper, award, or talk). Remember to add new pages to `sitemap.xml` if you create any.
