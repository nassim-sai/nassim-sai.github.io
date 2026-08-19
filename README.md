# nassim-sai.github.io

Personal portfolio — Nassim Sai, Network & Security Engineer.
Live at **https://nassim-sai.github.io**

## What's here

```
index.html          the entire site — HTML, CSS, JS, photo and all six CVs inlined
assets/og.png       social preview card (LinkedIn / Twitter / WhatsApp link previews)
assets/favicon.svg  favicon
cv/                 the CV PDFs as standalone files, for direct linking
robots.txt          crawl policy
sitemap.xml         one-URL sitemap
.nojekyll           tells GitHub Pages to serve files as-is, no Jekyll build
```

`index.html` is fully self-contained. It has no build step, no dependencies to
install, and one external request (Google Fonts). Open it locally by
double-clicking and everything works, including the CV viewer.

## Features

- **Trilingual** — English, French and Arabic, with full RTL layout for Arabic.
  Auto-detects the visitor's browser language on first load.
- **CV viewer** — pick a region (Tunisia / Europe / GCC) and a language; the
  matching one-page CV previews inline and downloads with one click. The PDFs
  are embedded as base64 and served to the browser as blob URLs, so the viewer
  works offline and from a local file.
- **Light and dark themes**, project filters, scroll animations, animated
  counters, mobile menu.
- Respects `prefers-reduced-motion`.

## Direct CV links

Useful for pasting into emails and applications:

| Market | Link |
|---|---|
| Tunisia (EN) | `/cv/Nassim_Sai_CV_TN_EN.pdf` |
| Tunisia (FR) | `/cv/Nassim_Sai_CV_TN_FR.pdf` |
| Europe (EN) | `/cv/Nassim_Sai_CV_EU_EN.pdf` |
| Europe (FR) | `/cv/Nassim_Sai_CV_EU_FR.pdf` |
| GCC (EN) | `/cv/Nassim_Sai_CV_Gulf_EN.pdf` |
| GCC (AR) | `/cv/Nassim_Sai_CV_Gulf_AR.pdf` |
