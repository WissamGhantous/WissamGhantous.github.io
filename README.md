# wissamghantous.github.io

Plain HTML/CSS personal academic site, no build step required.

## Files
- `index.html` — Home (bio + photo)
- `research.html` — Research (publications + talks)
- `teaching.html` — Teaching & supervision
- `style.css` — shared styling

## Deploying to GitHub Pages

You already own the repo `wissamghantous.github.io`, so this is a straight replace:

```bash
# 1. Clone your existing repo (or cd into it if you already have it locally)
git clone https://github.com/wissamghantous/wissamghantous.github.io.git
cd wissamghantous.github.io

# 2. Copy in the new files (overwriting the old index.html etc.)
# Keep "Ghantous Thesis.pdf" — research.html links to it directly.
cp /path/to/downloaded/index.html .
cp /path/to/downloaded/research.html .
cp /path/to/downloaded/teaching.html .
cp /path/to/downloaded/style.css .

# 3. Commit and push
git add .
git commit -m "Redesign site as plain HTML/CSS"
git push origin main
```

GitHub Pages will redeploy automatically within a minute or two at
https://wissamghantous.github.io

## To customize later
- **Photo**: currently pulled from your old Google Sites image link. Swap in
  your own file (e.g. `portrait.jpg` placed in the repo root) and update the
  `src` in `index.html`.
- **Colors**: edit the `:root` variables at the top of `style.css`
  (`--accent` controls link/heading color).
- **New publication**: copy a `<li class="pub-item">...</li>` block in
  `research.html` and edit.
- **New talk**: add a `<li>` under the relevant `<div class="year-block">`
  in `research.html`, or add a new year block.
- **New course/student**: add a `<li>` under the relevant section in
  `teaching.html`.

No npm, no build tools — just edit the `.html`/`.css` files directly and push.
