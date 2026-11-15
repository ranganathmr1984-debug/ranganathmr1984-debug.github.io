# M.R. Ranganath portfolio

Responsive, static portfolio website and two-page resume PDF. No build step or paid hosting is required.

## Preview locally

Open `index.html` in a browser. The resume is at `assets/MR-Ranganath-Resume.pdf`.

## Free GitHub Pages preview

The linked GitHub account is `ranganathmr1984-debug`. Create a **public** repository named `ranganathmr1984-debug.github.io`, then upload the site files from this folder to the repository root (including `index.html`, `styles.css`, `script.js`, `assets/`, `.nojekyll`, `robots.txt`, and `sitemap.xml`). A public repository makes the source files and resume publicly downloadable, which matches the portfolio's public purpose.

In the repository, open **Settings → Pages**. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/(root)`, then save. Once the Pages deployment completes, the preview address will be `https://ranganathmr1984-debug.github.io/`. Verify it opens and that the resume downloads before sharing it.

## Connect `ranganathmr.com`

First register the domain with a registrar (availability was not confirmed in this environment). In the repository's **Settings → Pages → Custom domain**, enter `ranganathmr.com` and save. Then, at the registrar's DNS page, set these records:

| Type | Host | Value |
|---|---|---|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| CNAME | `www` | `ranganathmr1984-debug.github.io` |

Remove conflicting A/AAAA records for `@` and conflicting CNAME records for `www`. After DNS has propagated and GitHub Pages reports the certificate is ready, turn on **Enforce HTTPS** in Pages settings. GitHub notes DNS changes can take up to 24 hours. Do not add a wildcard DNS record.

## Content maintenance

Edit `index.html` for portfolio copy, `styles.css` for visual styles, and `script.js` for navigation behavior. Regenerate the PDF with the reportlab script in `work/generate_resume.py` when resume details change. The displayed contact links and career figures are based on the supplied LinkedIn profile and confirmed instructions.
