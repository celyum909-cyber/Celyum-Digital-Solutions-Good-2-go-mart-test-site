# Good 2 Go Mart — Website

A single-page site for Good 2 Go Mart, 1005 Abbott Rd, Buffalo, NY 14220.

## What's here

- `index.html` — the entire site (HTML, CSS, and JS all in one file).
- `assets/` — all photos and images the page uses.

That's it. There's no build step, no framework, and no server-side code — it's a static site.

## Hosting it on GitHub Pages

1. Create a new repository on GitHub (or use an existing one).
2. Add these files to the repository root, keeping the folder structure as-is (`index.html` at the root, `assets/` beside it).
3. Commit and push:
   ```
   git init
   git add .
   git commit -m "Add Good 2 Go Mart site"
   git branch -M main
   git remote add origin <your-repo-url>
   git push -u origin main
   ```
4. In the repository on GitHub, go to **Settings → Pages**.
5. Under "Build and deployment", set **Source** to "Deploy from a branch", pick the `main` branch and the `/ (root)` folder, then save.
6. GitHub will give you a URL, usually `https://<your-username>.github.io/<repo-name>/`, live within a minute or two.

If you want a custom domain (like `good2gomart.com`), you can add it under the same Pages settings once the site is live — GitHub will walk you through the DNS records to add.

## The "owner" product editor

The site has a hidden admin view (reached at `yoursite.com/#admin`) protected by a password, for editing product listings. Heads up: the "Publish changes" button in that editor only works when the page is hosted as a Claude Artifact — it calls an API that doesn't exist on GitHub Pages or any other static host. On GitHub, you'd instead edit the product data directly in `index.html` (search for `id="product-data"`) and push the change, or ask Claude to make the edit and export an updated `index.html`.

## Updating content later

Since this is one HTML file, the easiest way to make changes is to edit `index.html` directly (or have Claude do it) and push the updated file. Product photos live in `assets/products/`, `assets/menu/`, etc.
