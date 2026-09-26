# Yusuf O. Tijani — academic website

Plain static site: hand-written HTML + one stylesheet. No build step, no framework,
no JavaScript beyond a two-line script that prints the current year. Push the folder
to GitHub and enable GitHub Pages — nothing to compile.

## Files

| File | Page |
|---|---|
| `index.html` | About — bio, research interests, news, academic background |
| `publication.html` | Publications (numbered, grouped by year) |
| `talks.html` | Talks & presentations |
| `Teachings.html` | Teaching & mentorship |
| `portfolio.html` | Portfolio |
| `blog-post.html` | News & notes |
| `assets/style.css` | The entire design |

Images (`*.jpg`, `*.PNG`) and PDFs (CV, slides) sit in the root and are referenced
relative to it.

## Editing

**Add a publication** — copy one `<li class="entry">` block in `publication.html`,
change the number, title, URL and journal line. Numbers run descending, newest first;
renumber the block above if you add to the top.

**Add a talk or news item** — same pattern in `talks.html` / `blog-post.html`, with
a date in `entry__date` instead of a number.

**Change colours or spacing** — everything lives in the `:root` block at the top of
`assets/style.css`. `--accent` is the link colour; `--rule` is the hairline grey.

**Change the sidebar** — the profile block is repeated at the top of every page's
`<div class="shell">`. Edit it in each file, or keep one page as the reference and
copy across.

## Notes

- Tailwind, Alpine.js and `node_modules` were removed; they are no longer needed.
- Font Awesome and Google Fonts load from CDNs; the layout degrades gracefully
  without them.
- The layout is a two-column grid that collapses to a single column under 900px.
