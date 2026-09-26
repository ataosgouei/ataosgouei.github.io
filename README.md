# atahbar.com

Personal website of Ataollah Kalantari Osgouei. Plain HTML, CSS and a little JavaScript. No build step.

## What each file does

- `index.html`: the whole site (text, styles and scripts)
- `photo.jpg`: portrait
- `og-image.jpg`: preview image shown when the link is shared (LinkedIn, WhatsApp, email)
- `apple-touch-icon.png`, `favicon-32.png`: browser and phone icons
- `404.html`: page shown for broken links
- `CNAME`: tells GitHub Pages to serve the site at atahbar.com

## Put it online (GitHub Pages + Cloudflare)

1. Create a free GitHub account.
2. Create a new **public** repository named `YOUR-USERNAME.github.io`.
3. In the repository, click **Add file > Upload files**, drag in every file from this folder, and click **Commit changes**.
4. Open **Settings > Pages**. Under "Build and deployment", choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
5. In Cloudflare, open atahbar.com > **DNS > Records** and add these records. Set **Proxy status** to **DNS only** (grey cloud) for all of them:
   - `A` record, name `@`, value `185.199.108.153`
   - `A` record, name `@`, value `185.199.109.153`
   - `A` record, name `@`, value `185.199.110.153`
   - `A` record, name `@`, value `185.199.111.153`
   - `CNAME` record, name `www`, target `YOUR-USERNAME.github.io`
6. Back in GitHub **Settings > Pages**, check that "Custom domain" shows `atahbar.com` (type it and click Save if it doesn't).
7. When the DNS check passes, tick **Enforce HTTPS**. This can take up to 24 hours.

## Edit later

Open `index.html` on GitHub, click the pencil icon, change the text, and commit. The live site updates in a minute or two.
