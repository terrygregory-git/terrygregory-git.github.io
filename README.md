# terrygregory.eu

Personal academic website of Terry Gregory, served via **GitHub Pages** at
https://terrygregory.eu (GitHub fallback: https://terrygregory-git.github.io).

## Structure

| File | Purpose |
|---|---|
| `index.html` | Home: bio, positions, news, contact |
| `research.html` | Publications, working papers, work in progress, policy writing |
| `teaching.html` | Courses and PhD supervision |
| `press.html` | Media coverage by year |
| `css/style.css` | Single shared stylesheet (colors/fonts at the top in `:root`) |
| `assets/` | Portrait, CV PDF (`Gregory_CV.pdf`), favicon |
| `CNAME` | Custom domain (`terrygregory.eu`) — do not delete |

Plain HTML/CSS, no build step. Edit a file, commit, push — the site updates
automatically within a minute or two.

## Updating content

- **New paper:** add a `<div class="pub">…</div>` block in `research.html`
  (copy an existing block) and, if notable, a line in the News list in `index.html`.
- **New press item:** add a `<div class="media-item">…</div>` under the right year in `press.html`.
- **New CV:** recompile `Gregory_CV.tex` (Overleaf/Dropbox CV folder) and overwrite
  `assets/Gregory_CV.pdf`.

Or simply ask Claude Code: *"Füge auf meiner Webseite das neue Paper X hinzu"*.

## One-time DNS setup for terrygregory.eu

At the domain registrar where terrygregory.eu was purchased, set:

1. **Four A records** for the apex domain (`@` / terrygregory.eu):
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. **One CNAME record**: host `www` → `terrygregory-git.github.io`

Then in the GitHub repo: *Settings → Pages → Custom domain* = `terrygregory.eu`,
and tick **Enforce HTTPS** once the certificate is issued (can take up to a day).
