# CascaraEdmonds.com

Marketing website for **Cascara Townhomes**, a six-townhome development opportunity at 9516 Edmonds Way, Edmonds, WA 98026.
Listed by Adam Cobb, Windermere Real Estate GH LLC · 206-854-9454 · adamcobb@windermere.com · adamcobb.com

This is a static, single-page site: one self-contained `index.html` (styles, scripts and images inside it) with no build step. Fonts load from Google Fonts.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole site (styles and scripts are inside it) |
| `og-image.jpg` | Preview image shown when the link is shared (all other images are built into `index.html`) |
| `favicon.svg` | Browser-tab icon |
| `CNAME` | Custom domain for GitHub Pages (`cascaraedmonds.com`) |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is |
| `robots.txt`, `sitemap.xml` | Search-engine basics |

## Publish on GitHub Pages

1. Create a new repository on GitHub (for example `cascara-edmonds-site`).
2. Click **Add file → Upload files**, drag in **the files inside this folder** (`index.html`, `og-image.jpg`, `favicon.svg`, `CNAME`, `robots.txt`, `sitemap.xml`, `.nojekyll`). Upload the files themselves, not the zip and not the folder, and commit.
   - `.nojekyll` is a hidden file; if your computer hides it, the site still works without it.
3. Go to **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. The site will appear at `https://<your-username>.github.io/<repo-name>/` within a minute or two.

### Point cascaraedmonds.com at it

1. At the domain registrar, add DNS records:
   - `A` records for `@` pointing to `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - a `CNAME` record for `www` pointing to `<your-username>.github.io`
2. In **Settings → Pages → Custom domain**, enter `cascaraedmonds.com`, save, and tick **Enforce HTTPS** once it becomes available.

Not using the custom domain yet? Delete the `CNAME` file so GitHub doesn't try to redirect to it.

## Common edits (all in `index.html`)

- **Price:** search for `Contact agent for pricing`.
- **Permit status:** search for `Permit Submitted` (hero badge) and `Current permit status` (timeline).
- **Contact details:** search for `206-854-9454` and `adamcobb@windermere.com`.
- **Photos:** the images are embedded in `index.html` so they cannot go missing. Ask Claude to swap or add photos and rebuild the file.

## Notes

- The tour-request form does not submit to a server. It drafts an email to Adam that the visitor sends from their own email app. To collect submissions automatically, connect a form service (for example Formspree or Netlify Forms).
- The site plan is a schematic, not the CODA Architecture site plan; unit positions are illustrative.
- Renderings are conceptual. Figures come from the CODA Architecture building-permit set dated 05/13/2025 (BLD2025-0585).
