# ibrahimhroob.github.io

Personal site of Dr Ibrahim Hroob: production autonomy work, first-author research, CV.

| File | Purpose |
|------|---------|
| `index.html` | The site (single page, no build step) |
| `cv.html` | Print-ready A4 CV; source for `cv.pdf` |
| `cv.pdf` | Downloadable CV linked from the site |
| `LINKEDIN.md` | Copy for the LinkedIn profile (not linked from the site) |

## Publish

```bash
cd ~/ibrahimhroob.github.io
git init -b main && git add . && git commit -m "Initial site"
gh repo create ibrahimhroob.github.io --public --source=. --push
```

GitHub serves a repo named `<username>.github.io` at `https://ibrahimhroob.github.io` automatically. If it doesn't appear, check Settings → Pages → Deploy from branch → `main` / root.

## Regenerate the PDF after editing `cv.html`

```bash
"/Applications/Google Chrome.app/Contents/MacOS/Google Chrome" --headless=new \
  --no-pdf-header-footer --virtual-time-budget=8000 --print-to-pdf=cv.pdf cv.html
```
