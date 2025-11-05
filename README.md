# ELIO — Intelligent Medical Notes

Landing page and project overview for ELIO — a portfolio project developed at Holberton School in collaboration with Asistencial Médica.

## 🚀 What is ELIO
ELIO is an application that reduces the time clinicians spend on clinical documentation by generating complete, structured medical notes in seconds. It provides a guided consultation workflow and AI‑assisted suggestions so physicians can spend more time with patients while clinical information remains standardized for later analysis.

Deployed app: https://www.asistencial-elio.tech/

## Key features highlighted on the landing page
- Speed: Generate a full clinical note in seconds.
- Accuracy: Structured notes that include history, allergies, medications and follow-up recommendations.
- Simplicity: Clean UI and workflow integration for tablets, phones and desktops.

## Repository structure
Place all public assets inside the `Public/` folder. Current repository layout:

ProyectoFinal/
- Public/
  - AlejandroArevaloQR.png
  - Alejandro_Arevalo.png
  - Asistencial-Medica-logotipo-Photoroom.jpeg
  - BrunoBarreraQR.png
  - Bruno_Barrera.png
  - Elio-image-Photoroom.jpeg
  - FernandoFalconQR.png
  - holberton-logo.jpeg
  - elio-logo.svg
  - styles.css
- README.md
- index.html

(If any filename is different in your working copy, update `index.html` paths accordingly.)

## How to run locally
1. Clone the repository:
   ```bash
   git clone https://github.com/feratholberton/ProyectoFinal.git
   cd ProyectoFinal
   ```
2. Serve the files with a simple HTTP server (recommended because some browsers block iframes from file://):
   - With Python 3:
     ```bash
     python3 -m http.server 8000
     ```
     Open: http://localhost:8000/index.html
   - With Node (http-server):
     ```bash
     npx http-server . -c-1
     # open http://127.0.0.1:8080
     ```

Verify:
- The hero, features, about, demo and CTA sections render.
- Images are loaded from `Public/`.
- The embedded YouTube demo loads (requires running over http(s) — see above).

## Deploy (recommended options)

Option A — GitHub Pages (free)
1. Ensure your landing file is named `index.html` at repo root.
2. Commit and push a branch (example):
   ```bash
   git checkout -b landingpage/publish
   git add index.html Public/
   git commit -m "Publish landing page"
   git push -u origin landingpage/publish
   ```
3. In GitHub: Repository → Settings → Pages → Select branch `landingpage/publish` (or `main`) and root `/`.
4. (Optional) To use a custom domain (e.g., `www.asistencial-elio.tech`) add a `CNAME` file in the repo containing the domain, and update your DNS provider:
   - `CNAME` contents:
     ```
     www.asistencial-elio.tech
     ```
   - Create either a CNAME (for `www`) pointing to `<your-github-username>.github.io` or A records to GitHub Pages IPs for apex domains:
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```

Option B — Netlify / Vercel
- Connect the GitHub repo and deploy. For simple static sites no build command is required; publish directory is `/`.
- Configure the custom domain in the provider's domain settings (Netlify/Vercel will show DNS records to add).

## Files to review / edit before final deploy
- `index.html`: update any placeholder links (deploy URL, social links).
- `Public/styles.css`: tweak colors, spacing or fonts if needed.
- `Public/*`: confirm all images (team photos, QR codes, logos) exist and are referenced with correct filenames.

## Holberton Portfolio Landing Page Checklist
This landing page was built to satisfy the Portfolio Project landing page requirements:
- Intro section: large hero image, project name, one-line description, nav links and CTA to the deployed app.
- Features section: 3 highlighted features with short descriptions.
- About section: inspiration/personal story (editable), team member cards with photos and social links (LinkedIn/GitHub). QR codes included in `Public/`.
- Demo section: embedded YouTube demo.
- Final CTA: buttons to the deployed app and GitHub repository (public).
- Footer: partner logos and ELIO logo.

Make sure to request a peer review before the project deadline (manual QA).

## Team & Links
- Alejandro Arévalo — Project lead • Backend  
  LinkedIn: https://www.linkedin.com/in/a-arevalo  
  GitHub: https://github.com/alearecuest

- Bruno Barrera — Backend • Integrations  
  LinkedIn: https://www.linkedin.com/in/bruno-barrera-27a7ba389/  
  GitHub: https://github.com/BrunoBarrera1

- Fernando Falcon — Design • Frontend  
  LinkedIn: https://www.linkedin.com/in/fernandofalcon/  
  GitHub: https://github.com/feratholberton

Repository: (project code) https://github.com/feratholberton/ProyectoFinal

Deployed app: https://www.asistencial-elio.tech/

Contact: aarevalo@fcien.edu.uy

## Accessibility & SEO notes
- The page uses semantic HTML (header, nav, section, footer) and should include alt text on images.
- Add meta description (already present) and consider adding Open Graph tags for social sharing.

## Troubleshooting / Tips
- If the YouTube iframe does not display when opening `index.html` directly in the browser, serve over HTTP (see "How to run locally").
- If images appear cropped (logo clipped in nav), make sure the SVG `viewBox` and CSS `object-fit` are set to `contain` (see `Public/elio-logo.svg` and `Public/styles.css`).
- To replace the Fernando avatar, add `Public/Fernando_Falcon.png` and update the `src` in the team card.

## License
This repo can be licensed as you prefer. Example (MIT):
```
MIT License
Copyright (c) 2025 ELIO
...
```
(Add an actual LICENSE file to the repo if you want to publish under a specific license.)

---

If you want I can:
- Create the `landingpage/publish` branch, commit the final files and open a Pull Request to `main` (I can do this for you if you provide the repo owner/repo and confirm the branch name), or
- Produce a Spanish version of the README, or
- Generate a short checklist for the Holberton reviewer to confirm the landing page meets all rubric points.

Which of these should I do next?  