# ericlu28.github.io

Personal website for Eric Lu — Jekyll (GitHub Pages stack), HTML entries, custom CSS, and Bootstrap Icons.

**Live site:** https://ericlu28.github.io

---

## Structure

```
.
├── _config.yml        # Jekyll config (permalink, markdown, etc.)
├── Gemfile            # Pins github-pages gem (Bundler)
├── index.html         # Homepage (YAML front matter + layout)
├── resume.html        # Resume page
├── blog.html          # Blog index (lists `_posts`)
├── _layouts/default.html   # Wrapper: nav, head, footer
├── _posts/            # Blog posts (`YYYY-MM-DD-title.md`)
├── css/
│   ├── style.css      # Palette, hero, resume, posts
│   └── syntax.css     # Rouge / code highlighting
├── img/
│   ├── profile.jpeg   # Hero photo (referenced in `index.html`)
│   └── life/          # Homepage photos (paths fixed in `index.html`)
│       ├── family.jpeg
│       ├── golf.jpeg
│       ├── travel.jpeg
│       └── beach-surf.jpeg
└── _site/             # Build output (`jekyll build`); gitignored locally
```

## Local development

Pages use **Layouts and YAML front matter** — do not open repo-root `*.html` in the browser as raw files (they are not standalone HTML).

**Recommended:** run Jekyll’s built-in server (processes Liquid, layouts, posts, and resolves asset paths):

```bash
bundle install          # install gems once
bundle exec jekyll serve
```

Then open **http://127.0.0.1:4000/** (or the URL Jekyll prints). Use `--livereload` if you want auto-refresh:

```bash
bundle exec jekyll serve --livereload
```

**Optional:** produce static files then serve **`_site/`** with any static HTTP server:

```bash
bundle exec jekyll build
python3 -m http.server 8080 --directory _site
# visit http://localhost:8080
```

Serving only the repo root with `python3 -m http.server` **without building** skips Jekyll—you get un-rendered Liquid/front matter instead of the real site.

## Deploying to GitHub Pages

1. Make sure the repo is named exactly `ericlu28.github.io`.
2. Push to the `main` branch:

```bash
git add .
git commit -m "Update site"
git push origin main
```

3. In the repo settings → **Pages**, set source to **Deploy from branch → main → / (root)**.
4. GitHub Pages will build the site with Jekyll when you push. Live URL: https://ericlu28.github.io within a minute or two.

## Customisation checklist

- [ ] Add or swap your hero image at `img/profile.jpeg` and keep `src` in `index.html` in sync
- [ ] Tweak About copy in `index.html` to match how you describe your Adobe work
- [ ] Add photos under `img/life/` (`family.jpeg`, `golf.jpeg`, `travel.jpeg`, `beach-surf.jpeg`) or change `src` paths in `index.html`
- [ ] Fill in Adobe role details in `resume.html`
- [ ] Keep the Resume **Download PDF** asset and path in `resume.html` aligned with the PDF in the repo root
- [ ] Add posts as `_posts/YYYY-MM-DD-my-title.md` (see existing posts for front matter)
