# Deployment & Sharing — Quick Guide

This package contains:
- `index.html` — single-page portfolio site (ready-to-deploy)
- `Prince_ml__Profile.pdf` — your uploaded resume (linked from the page)

## Quick ways to get a shareable link (pick one)

### Option A — GitHub Pages (recommended, free)
1. Create a GitHub repository. If you want the link to be `https://<your-github-username>.github.io/` name the repo exactly `<your-github-username>.github.io`.
2. Push these files to that repository (index.html + PDF) on the default branch (`main` or `master`).
   Example commands:
   ```
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-github-username>/<repo>.git
   git push -u origin main
   ```
3. GitHub Pages usually publishes automatically for a repo named `username.github.io`. Otherwise go to repo -> Settings -> Pages and set the source to the main branch root.
4. Your shareable link will be `https://<your-github-username>.github.io/` (or `https://<your-github-username>.github.io/<repo>/` for project pages).

### Option B — Netlify (easiest GUI, drag & drop)
1. Go to https://app.netlify.com/drop and drag the contents of this ZIP (extract first).
2. Netlify will deploy and give you a random `https://something.netlify.app` link instantly.
3. You can change the site name in settings for a nicer subdomain.

### Option C — Use a custom domain (thevanshgarg.com)
1. Buy the domain from any registrar (Namecheap/GoDaddy).
2. For Netlify: add domain in site settings -> Domains -> Add custom domain. Netlify will give you the DNS record (CNAME or A) to add in your registrar.
3. For GitHub Pages: create `CNAME` file with your domain and add A records pointing to GitHub Pages IPs:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```
   Also add a DNS `CNAME` for the apex or `www` subdomain as instructed by GitHub Docs.

## Notes
- The HTML file links to the attached PDF `Prince_ml__Profile.pdf`. Keep both files at the repo root.
- If you want, I can:
  - Prepare a ready-to-push Git repo (I have created this ZIP for you).
  - Help write the GitHub repo description / meta tags.
  - Customize the text, images, or add more pages (projects, blog).