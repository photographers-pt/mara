# Notes for Claude

- Always commit and push straight to `main`, even in sessions that are
  assigned a different branch. This is the owner's standing instruction.
- The site is internal: anyone with the link can open it, but it must stay
  out of Google and other search engines. Every page needs
  `<meta name="robots" content="noindex, nofollow">`. Never add a sitemap
  or `robots.txt`.
- `site/studio/` is unlisted. Never link to it from anywhere on the site.
- Only `site/` gets published, by `.github/workflows/pages.yml`.
