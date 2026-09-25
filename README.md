# Mukhammadkodir Tokhirjonov — CV Site

A terminal-styled personal portfolio site, built as a single self-contained `index.html` (no build step needed).

## Deploy to GitHub Pages

1. Create a new repo (e.g. `enigmajon/enigmajon.github.io` for a root domain, or any repo name for a project page).
2. Push `index.html` to the repo root:
   ```bash
   git init
   git add index.html
   git commit -m "Initial CV site"
   git branch -M main
   git remote add origin https://github.com/enigmajon/YOUR-REPO.git
   git push -u origin main
   ```
3. In the repo on GitHub: **Settings → Pages → Source → Deploy from branch → main / (root)**.
4. Your site goes live at `https://enigmajon.github.io/YOUR-REPO/` (or `https://enigmajon.github.io/` if you used the special `username.github.io` repo name).

## Editing content

Everything is in `index.html`:
- Bio text → `renderAbout()`
- Education timeline → `renderEducation()` (the `socials` array style — edit the `log-entry` blocks)
- Social links → `renderConnect()`, the `socials` array near the top of that function
- Principles list → `renderPrinciples()`, the `items` array

## Adding your resume PDF

Drop a `resume.pdf` file next to `index.html`, then in `renderConnect()` replace the placeholder `.cv-block` div with:
```html
<a href="resume.pdf" download>Download résumé (PDF)</a>
```
