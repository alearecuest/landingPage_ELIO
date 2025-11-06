# ELIO — Landing Page

Static portfolio landing page for ELIO — "Intelligent medical notes".  
This repository contains a simple static site with a header, features section, team, demo (YouTube embed), and footer with partner logos.

---

## Current status / Summary of recent fixes
I applied several fixes and layout adjustments to make the site look consistent and responsive across viewports. Key changes already applied in the repository:

- Logos
  - The main ELIO logo is stored as `Public/elio-logo.svg` with a tightened viewBox to remove large transparent margins.
  - Partner logos (Asistencial, Holberton) are included and sized consistently in the footer and nav.
  - Footer and nav logos have been normalized so they align and don't push other content.

- CSS (file: `Public/styles.css`)
  - Prevented images from overflowing the layout with `img { max-width: 100% }` and added targeted rules for avatar sizes.
  - Restored a modest hero/logo size to prevent the hero image from becoming too large on wide screens.
  - Constrained the demo video to the same max width as the content (`--container`) and kept a sensible aspect ratio (16:9) with caps on height to avoid an oversized player.
  - Converted the bottom black band (final call-to-action) into a contained centered box: the black background is applied to `.final-cta .wrap` and limited to `--container` so it no longer bleeds full-width outside the margins.
  - Footer logos centered and consistent spacing/gap.

- HTML (file: `index.html`)
  - Structure preserved and minor adjustments applied to footer and nav to match the updated CSS.
  - Accessibility attributes (alt text, ARIA labels where appropriate) retained.

- SVG
  - `Public/elio-logo.svg` cleaned so it no longer contains excessive whitespace that caused layout shifts.

---

## Files changed (high level)
- `index.html`
- `Public/styles.css`
- `Public/elio-logo.svg`

(See the repo for file contents and commit history.)

---

## Quick local test
1. Clone the repository (if not already local)
   - git clone git@github.com:alearecuest/landingPage_ELIO.git
   - cd landingPage_ELIO

2. Serve the static files with Python:
   - python3 -m http.server 8000
   - Open: http://localhost:8000/  
   - Use Ctrl+F5 to bypass cache after making CSS/HTML changes.

3. Alternatively, use any static server (e.g., `npx serve Public` if you prefer to serve the Public folder directly).

---

## Recommended Git workflow for changes
- Create a branch for edits:
  - git checkout -b fix/style-adjustments
  - git add index.html Public/styles.css Public/elio-logo.svg
  - git commit -m "Fix: adjust hero, video sizing and final-cta containment"
  - git push -u origin fix/style-adjustments

---

## Deployment options (recommended)
Pick one depending on how you want to manage deployment:

- GitHub Pages (fast, free)
  - Option 1 (gh-pages branch, keeps main untouched):
    - git checkout --orphan gh-pages
    - git reset --hard
    - git rm -rf .
    - cp -r Public/* .
    - git add .
    - git commit -m "Deploy site to gh-pages"
    - git push -u origin gh-pages --force
    - git checkout main
    - Then enable Pages: Settings → Pages → Branch: gh-pages / Folder: root

  - Option 2 (use /docs folder in main):
    - cp -r Public/ docs/
    - git add docs && git commit -m "Deploy site to docs" && git push
    - Settings → Pages → Branch: main / Folder: /docs

- Netlify (recommended for CI previews and easy DNS/SSL)
  - Connect the GitHub repo in Netlify, set the publish directory to `Public` and deploy.
  - Netlify automatically provides previews for pull requests.

- Vercel (good for frontend frameworks and previews)
  - Connect repo in Vercel, set the output directory to `Public`.

If you'd like, I can push a `gh-pages` branch for you with the current `Public` content and configure the Pages branch (I will do that if you confirm the repo and branch name).

---

## Visual tweaks you can change quickly
- Hero image/logo size: edit `.hero .cover { width: 220px; }` in `Public/styles.css`.
- Footer logo sizing: edit `--footer-partner-height` and `--footer-elio-height` in `:root`.
- Video sizing: change `--video-max-height` and `--video-min-height` in `:root`.
- Final CTA width/gap: edit `--container` or the `.final-cta .wrap` padding and border-radius.

---

## Accessibility & SEO notes
- All meaningful images include `alt` attributes. If a decorative image exists, set `alt=""`.
- The logo link should include an accessible label (e.g., `aria-label="Go to home"`).
- Headings are structured for screen-readers; consider adding a `<main>` wrapper for stronger landmark semantics.

---

## Troubleshooting tips
- If images appear too large: clear cache (Ctrl+F5) and inspect CSS for overriding rules.
- If the black CTA still bleeds full-width: ensure your `Public/styles.css` version contains the `.final-cta .wrap { max-width: var(--container); background: #0e0e0f; }` rules.
- If the SVG logo has whitespace: open `Public/elio-logo.svg` and verify the `viewBox` is tight around the graphic.

---

## Next steps I can help with
- Create and push a `gh-pages` branch for GitHub Pages deployment (or configure `docs/` on `main`).
- Connect and deploy the site on Netlify or Vercel with automatic previews.
- Tweak final visual details (hero size, footer spacing, video height) — tell me exact pixel values if you want a specific look.

---

## Credits
Project: ELIO — Portfolio project (Holberton School)  
Authors / contacts: see the team section on the landing page (links to GitHub / LinkedIn).

---

## License
If you want a license file, tell me which one (MIT, Apache-2.0, etc.) and I'll add `LICENSE` to the repo.