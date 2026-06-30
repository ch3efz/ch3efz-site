# Ch3efz

Personal site and digital asset hub for **Ch3efz** (Necho Logan).

- **FrutiTheme** — Frutiger Aero HTML/CSS theme
- Static site, no build step, free to host on Cloudflare Pages or GitHub Pages

## Local preview

```bash
cd ch3efz-site
python3 -m http.server 8080
# open http://localhost:8080
```

## Deploy to Cloudflare Pages (free)

1. Create a GitHub repo named `ch3efz-site` (or any name).
2. Push this folder:

   ```bash
   git init
   git add .
   git commit -m "Initial Ch3efz site"
   git branch -M main
   git remote add origin https://github.com/YOUR_USERNAME/ch3efz-site.git
   git push -u origin main
   ```

3. Go to [Cloudflare Dashboard](https://dash.cloudflare.com) → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
4. Select the repo. Build settings:
   - **Framework preset:** None
   - **Build command:** (leave empty)
   - **Build output directory:** `/`
5. Deploy. Your site will be live at `https://ch3efz-site.pages.dev` (or similar).

### Custom domain (optional, ~$10/year)

Buy a domain (Cloudflare Registrar, Porkbun) → Cloudflare Pages → **Custom domains** → add `ch3efz.com` or similar.

## Deploy to GitHub Pages (alternative)

1. Push to GitHub (same as above).
2. Repo → **Settings** → **Pages** → Source: **main** branch, folder **/ (root)**.
3. Live at `https://YOUR_USERNAME.github.io/ch3efz-site/`

## Shop setup

When ready to sell FrutiTheme:

1. Create a [Gumroad](https://gumroad.com) product.
2. Replace the placeholder button URL in `shop.html` with your Gumroad link.

## Structure

```
index.html    Home
about.html    Bio + social links
demo.html     FrutiTheme live preview
shop.html     Digital assets (Gumroad links)
css/          FrutiTheme + site styles
demo/         Sample themed HTML output
```