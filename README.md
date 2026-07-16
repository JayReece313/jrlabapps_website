# jrlabapps.com — JR LABS LLC

Static marketing site for JR LABS LLC (`index.html`, `privacy.html`, `terms.html`). No build step — Tailwind CSS is loaded via CDN.

## Before going live

- [x] **Formspree**: form ID `maqrqkzw` wired into the contact form's `action` attribute in [index.html](index.html), delivering to `info@jrlabapps.com`. Confirm the destination email is verified in your Formspree dashboard, and send a test submission once deployed.
- [x] **Governing law state**: [terms.html](terms.html) Governing Law section set to Michigan.
- [ ] **Legal review**: the Privacy Policy and Terms of Use are generic boilerplate covering the current site's data practices (contact form only). Have a lawyer review before this is treated as the official policy for a live app that collects user data.

## Deploying to GitHub Pages

1. Create a new GitHub repository (public or private — Pages works with both on a paid/org plan; public repos get Pages free).
2. From this directory:
   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
3. In the repo's **Settings → Pages**, set the source to the `main` branch, root folder.
4. Under **Settings → Pages → Custom domain**, enter `jrlabapps.com`. The `CNAME` file in this repo already contains that value, so GitHub should pick it up automatically.

## DNS records (at your domain registrar)

Point the apex domain at GitHub Pages with four `A` records:

| Type | Host | Value           |
|------|------|-----------------|
| A    | @    | 185.199.108.153 |
| A    | @    | 185.199.109.153 |
| A    | @    | 185.199.110.153 |
| A    | @    | 185.199.111.153 |

Optional, if you want `www.jrlabapps.com` to work too:

| Type  | Host | Value                      |
|-------|------|----------------------------|
| CNAME | www  | `<your-github-username>.github.io` |

DNS changes can take anywhere from a few minutes to 48 hours to propagate. Once GitHub reports the domain as verified, enable **"Enforce HTTPS"** in the Pages settings.

## Follow-up (separate task)

Design a logo / brand identity for JR LABS LLC and swap it into the header (currently a text wordmark) and as a favicon.
