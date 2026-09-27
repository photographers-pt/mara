# Mara

Website for the short film *Mara*: a one-page site, plus an unlisted studio
page for styling and IG post generators.

Plain HTML and CSS, with no build step and no dependencies.

## Structure

```
site/                    the website: publish this folder and nothing else
  index.html             the one-page site
  assets/css/base.css    shared design tokens and reset, used by every page
  assets/css/main.css    main page styles
  studio/                unlisted page for styling and IG post generators
```

## Preview locally

```sh
python3 -m http.server 8000 --directory site
```

Then open <http://localhost:8000/> and <http://localhost:8000/studio/>.

## Publishing

Every push to `main` publishes `site/` to
<https://photographers-pt.github.io/mara/> via
`.github/workflows/pages.yml`. In Settings → Pages, the source must be
**GitHub Actions**. "Deploy from a branch" would publish the whole repo,
this README included.

## Keeping it off search engines

The site is internal: anyone with the link can open it, but it shouldn't
turn up on Google.

- Every page has `<meta name="robots" content="noindex, nofollow">`. New
  pages need it too.
- Don't add a sitemap or `robots.txt`. A `robots.txt` block stops search
  engines from seeing the noindex tag, so a linked page could still get
  listed.

## The studio page

`/studio/` is also unlisted: nothing on the site links to it. Keep it that
way, and don't put anything secret there, since anyone with the URL can
open it.
