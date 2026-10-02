# proseandpigment.app

The site for Prose & Pigment, a reader for Markdown, text and code files on
iPhone and iPad. It carries the privacy policy and the support page the App
Store listing points to.

- `site/` is the whole site: static HTML and CSS, no build step, no script.
  Vercel serves this directory (`vercel.json`), with clean URLs, so
  `site/privacy.html` is served at `/privacy`.
- `site/fonts/` holds web subsets of Source Serif 4 and JetBrains Mono, both
  under the SIL Open Font License (the two `OFL-*.txt` files beside them).

To look at it locally, serve `site/` with a static server that maps `/privacy`
to `privacy.html`. Asset paths are absolute, so opening the files directly does
not work.

`vercel.json` also sends security headers. The content policy allows styles,
fonts and images from this site only, so an inline style, a script, or a file
from another host is blocked until the policy is changed to allow it.

A push to the production branch deploys the site.
