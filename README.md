# cfsopuerta.github.io — new site files

## How to deploy (replace the current site)

1. In your `cfsopuerta.github.io` repo, **delete** the old files and folders:
   `index.html`, `News_and_Events.html`, `Carlos_F._Sopuerta_Webpage_files/`,
   `News_and_Events_files/`, `Media/`, `orcid.png`.
2. Copy everything from this folder (`index.html`, `news.html`, `style.css`,
   `images/`) into the root of the repo.
3. Commit and push to `main`. GitHub Pages will rebuild automatically —
   no build step, no extra tools needed.

## One thing to finish yourself

The institutional logo strip at the bottom of the homepage currently links
directly to a file on ICE's own server:

```
https://www.ice.csic.es/templates/yootheme/cache/e7/Logos%20CSIC%20ICE%20MdM%20Max_2026-e75e1eee.jpeg
```

That works, but it depends on ICE's website never moving that file. Whenever
you have a minute: save that image yourself, drop it in `images/` (e.g.
`images/logo-ice-csic-mdm-max.jpg`), and in `index.html` change the `<img
src="https://www.ice.csic.es/...">` line under `<div class="institutions">`
to `src="images/logo-ice-csic-mdm-max.jpg"`.

## How to make routine updates

**Add a publication** — open `index.html`, find the `<div class="pub-list">`
block, and copy-paste one `<div class="pub">…</div>` entry as a template.
Each entry has: a year badge, an author line (wrap your own name in
`<span class="me">…</span>` to keep the highlight), an italic title, a venue
line, and one `arxiv`/`journal` link each. Journal buttons show whatever text
you put in them (`PRD`, `PRL`, `JCAP`, …) — match the venue.

**Add a news item** — open `news.html`, find `<div class="timeline">`, and
copy-paste one `<div class="t-item">…</div>` block. To update the five most
recent items shown on the homepage itself, do the same inside `index.html`'s
`<div class="timeline">` under the News & events section.

**Update contact info, CV link, or publication-list link** — these are plain
text/links in `index.html`; search for the section (`id="contact"`, the
`CV ↓` link in the header, or `View full publication list`).

All shared styling (colors, type, spacing) lives in `style.css` — change a
value once there and it updates both pages.
