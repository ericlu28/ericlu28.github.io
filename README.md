# ericlu28.github.io

Personal website for Eric Lu — built with plain HTML/CSS and Bootstrap Icons.

**Live site:** https://ericlu28.github.io

---

## Structure

```
.
├── index.html       # Landing page (hero, about, projects)
├── resume.html      # Resume (experience, education, skills)
├── blog.html        # Blog listing
├── css/
│   └── style.css    # All styles — earthy palette, custom components
└── img/
    └── profile.jpg  # Drop your photo here (140×140 or larger, square crop)
```

## Local development

No build step required. Open any HTML file directly in your browser:

```bash
open index.html
```

Or use a simple local server (avoids font/CORS issues):

```bash
python3 -m http.server 8080
# then visit http://localhost:8080
```

## Deploying to GitHub Pages

1. Make sure the repo is named exactly `ericlu28.github.io`.
2. Push to the `main` branch:

```bash
git add .
git commit -m "initial site"
git push origin main
```

3. In the repo settings → **Pages**, set source to **Deploy from branch → main → / (root)**.
4. Your site will be live at `https://ericlu28.github.io` within ~1 minute.

## Customisation checklist

- [ ] Add your photo to `img/profile.jpg`
- [ ] Fill in the About blurb in `index.html`
- [ ] Fill in Adobe role bullet points in `resume.html`
- [ ] Update the "Download PDF" link in `resume.html` once you export a PDF
- [ ] Add blog posts in `blog.html` when ready
