# Cedar Drilling — draft website

Single-page static site for Cedar Drilling Company (Pty) Ltd. No build step: `index.html` is the whole site (logo is embedded inline).

## Deploy to Netlify via GitHub

1. Create a new GitHub repository (e.g. `cedar-drilling-site`) and push these files:
   ```
   git init
   git add .
   git commit -m "Draft Cedar Drilling website"
   git branch -M main
   git remote add origin https://github.com/<your-account>/cedar-drilling-site.git
   git push -u origin main
   ```
2. In Netlify: **Add new site → Import an existing project → GitHub**, pick the repo.
3. Leave the build command empty and set the publish directory to `.` (already set in `netlify.toml`). Deploy.
4. Netlify gives you a `*.netlify.app` URL to share as the draft. Rename it under **Site configuration → Site details → Change site name**.

Every push to `main` redeploys automatically.

## Before going live

- Delete `robots.txt` (it currently blocks search engines because this is a draft).
- Point `cedardrilling.com` at Netlify under **Domain management**.
- Replace the placeholder hero graphic with project photography if available.

## Editing

All content and styling lives in `index.html`. Colours are CSS variables at the top of the `<style>` block.
