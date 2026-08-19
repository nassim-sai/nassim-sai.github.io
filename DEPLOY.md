# Deploying to GitHub Pages

Target URL: **https://nassim-sai.github.io**

To get that root URL, the repository must be named exactly `nassim-sai.github.io`
— matching your username. Any other name gives you
`nassim-sai.github.io/<repo-name>/` instead, which also works but is uglier.

---

## Option A — no git, browser only (5 minutes)

1. Go to **https://github.com/new**
2. Repository name: `nassim-sai.github.io`
   Visibility: **Public** (Pages needs public on the free plan)
   Do **not** tick "Add a README" — this folder already has one.
   Click **Create repository**.
3. On the empty repo page click **uploading an existing file**.
4. Open this folder on your machine, select **everything inside it** —
   `index.html`, `README.md`, `DEPLOY.md`, `robots.txt`, `sitemap.xml`,
   `.nojekyll`, and the `assets` and `cv` folders — and drag them into the
   browser window. Drag the *contents*, not the folder itself, or your site
   ends up one directory too deep.
5. Commit message: `Initial portfolio site`. Click **Commit changes**.
6. Go to **Settings → Pages**. Source should already say
   *Deploy from a branch* / `main` / `/ (root)`. If not, set it and Save.
7. Wait 1–2 minutes, then open **https://nassim-sai.github.io**.

If Windows hides `.nojekyll` and it doesn't upload, don't worry — this site
doesn't need it. It's only there as insurance.

---

## Option B — git command line

From inside this folder:

```bash
git init -b main
git add .
git commit -m "Initial portfolio site"
git remote add origin https://github.com/nassim-sai/nassim-sai.github.io.git
git push -u origin main
```

Create the empty repo on github.com first (step 2 above), then run these.
GitHub will ask for a **personal access token**, not your password — generate
one at Settings → Developer settings → Personal access tokens, with `repo` scope.

Then check **Settings → Pages** as in step 6.

---

## Updating the site later

```bash
git add .
git commit -m "Update CV / projects"
git push
```

Changes go live in about a minute. Hard-refresh (Ctrl+Shift+R) if you still
see the old version — GitHub Pages caches aggressively.

---

## After it's live

- Add the URL to your **LinkedIn profile** — Contact info → Website, and in the
  Featured section.
- Add it to every CV. The LaTeX sources have a `\cvsite`-style contact line;
  put `nassim-sai.github.io` there and rebuild all six PDFs.
- Paste the link into a LinkedIn post once to check the preview card renders —
  it should show the dark banner from `assets/og.png` with your photo.
  If LinkedIn shows a stale or blank preview, run the URL through
  https://www.linkedin.com/post-inspector/ to force a re-crawl.

## Custom domain (optional, later)

If you buy something like `nassimsai.com`:

1. Create a file called `CNAME` in the repo root containing just the domain.
2. At your registrar, add a `CNAME` record for `www` pointing to
   `nassim-sai.github.io`, and four `A` records for the apex pointing to
   `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
3. Settings → Pages → Custom domain → enter it → tick **Enforce HTTPS**.

Verify those GitHub IPs against the current GitHub Pages documentation before
using them — they change rarely, but they do change.
