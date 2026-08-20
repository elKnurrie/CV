# dentoom.info

Personal portfolio site for Jurjen den Toom — IT Architect Infrastructure & Cloud.
Static single page (HTML/CSS, no framework), hosted on GitHub Pages.

## Local preview

Open `index.html` in a browser, or:

```powershell
python -m http.server 8080   # if python is available
```

## Deploy

1. Create a **public** GitHub repo (any name, e.g. `dentoom.info`) and push:
   ```powershell
   git remote add origin https://github.com/<you>/dentoom.info.git
   git push -u origin main
   ```
2. Repo **Settings → Pages → Source: GitHub Actions** (the included workflow deploys on push to `main`).
3. Point DNS at GitHub Pages (registrar of dentoom.info):
   - Apex `dentoom.info`: A records `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `www.dentoom.info`: CNAME to `<you>.github.io`
4. In Settings → Pages, add custom domain `dentoom.info` (the `CNAME` file is already in the repo) and enable **Enforce HTTPS** once the certificate is issued.
