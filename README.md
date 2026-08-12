# Natalie Hodges — Website

A static, locally-hosted replica of nataliehodges.com, rebuilt from the original
Squarespace site as plain HTML/CSS so it can be hosted for free on GitHub Pages.

## Structure

```
natalie_website/
├── index.html              Home
├── uncommon-measure.html   The book
├── news.html               News & Events
├── about.html              Biography
├── contact.html            Contact
├── css/
│   └── style.css           Shared styles
├── images/                 (drop local photos here when ready)
└── README.md
```

## Viewing locally

Just open `index.html` in a browser. Or, for a local server (so paths behave
exactly as they will online):

```bash
cd natalie_website
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploying to GitHub Pages

1. Create a new repository on GitHub (e.g. `natalie-website`).
2. From this folder, push the files:

   ```bash
   git init
   git add .
   git commit -m "Initial site"
   git branch -M main
   git remote add origin https://github.com/<your-username>/natalie-website.git
   git push -u origin main
   ```

3. On GitHub: **Settings → Pages → Build and deployment**.
   Set **Source** to `Deploy from a branch`, branch `main`, folder `/ (root)`, then **Save**.
4. The site goes live at `https://<your-username>.github.io/natalie-website/`
   within a minute or two.

### Using a custom domain (nataliehodges.com)

If you want to point the existing domain here, add a file named `CNAME`
(no extension) to the root containing just:

```
nataliehodges.com
```

Then set the domain in **Settings → Pages → Custom domain**, and update the
DNS records at your domain registrar to point to GitHub Pages. GitHub's docs
walk through the exact A / CNAME records.

## Notes on the design

The original site uses Squarespace's proprietary template and fonts, which
can't be copied exactly. This rebuild matches the look — minimal black-on-white,
centered name header, uppercase nav, and refined serif type — using the free
Google Fonts **Cormorant Garamond** (display) and **EB Garamond** (body).

## Images

Photos and the book cover currently load from the original Squarespace CDN so
the site looks right immediately. When you have local copies, drop them into
`images/` and update the `src` attributes (search for `squarespace-cdn.com`
across the `.html` files). The three images in use are:

- Book cover (home + book page)
- Author portrait (about page)
