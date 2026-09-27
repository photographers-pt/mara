# Mara

Website for the short film *Mara*: a public one-page site, plus an unlisted
studio page for styling and IG post generators.

Plain HTML and CSS, with no build step and no dependencies.

## Structure

```
site/                    the website: publish this folder and nothing else
  index.html             public one-page site
  assets/css/base.css    shared design tokens and reset, used by every page
  assets/css/main.css    public page styles
  studio/                unlisted page for styling and IG post generators
```

## Preview locally

```sh
python3 -m http.server 8000 --directory site
```

Then open <http://localhost:8000/> and <http://localhost:8000/studio/>.

## The studio page

`/studio/` is unlisted, not private:

- Nothing on the public site links to it, and its `noindex, nofollow` tag
  keeps it out of search results.
- Don't add it to a sitemap or `robots.txt`. `robots.txt` is public, so
  naming the path there would advertise it.
- Anyone with the URL can still open it, so don't put anything secret there.
