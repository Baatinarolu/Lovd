# 💌 Love Letter — A Personal Site for Khadijat

A romantic, interactive single-page love letter built with vanilla HTML/CSS/JS. Features an animated envelope opening, floating hearts particle system, photo gallery, relationship counter, timeline, poem & promise sections, and a smooth scroll story layout.

## 🚀 Deploying to Vercel

This repo is a static site (no build step required). Vercel will auto-detect it and serve `index.html` as the entry point.

### One-click Deploy
Click the button below to deploy instantly:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Baatinarolu/Lovd)

### Manual Deploy via CLI
```bash
# 1. Install Vercel CLI
npm i -g vercel

# 2. From the project root, run:
vercel

# 3. For production:
vercel --prod
```

### Manual Deploy via Git
1. Push this repo to GitHub.
2. Go to [vercel.com/new](https://vercel.com/new).
3. Import the repository.
4. Leave **Framework Preset** as `Other` (static site).
5. No build command, no output directory needed — Vercel serves files from the root.
6. Click **Deploy**.

## 📁 Project Structure

```
.
├── index.html       # Entire single-page love letter (HTML + CSS + JS)
├── vercel.json      # Vercel config: headers, caching, clean URLs, SPA rewrites
├── images/
│   ├── classroom.jpg
│   ├── khadijat.jpg
│   ├── bracelet.jpg
│   └── sunset.jpg
└── README.md
```

## 🛠 Local Development

Since this is pure static HTML, any static file server works:

```bash
# With Python
python3 -m http.server 8080

# With Node (npx)
npx serve .

# With Vercel CLI (runs production-like locally)
vercel dev
```

Then open http://localhost:8080 in your browser.

## ⚙️ Configuration Notes

- **`cleanUrls: true`** — `/index.html` is served as `/`.
- **SPA rewrites** — every route falls back to `index.html` so that visiting any path on the deployed URL still renders the page (useful if you ever add more routes/sections with hash-like behavior).
- **Caching** — images in `/images/` are cached for 1 year with `immutable` so the page loads fast on repeat visits.
- **Security headers** — `X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy`, and a restrictive `Permissions-Policy` are set for safety.

## 💖 Customization

- **Photos** — replace the files inside `images/` (keep the same filenames or update `src` in `index.html`).
- **Names / dates** — open `index.html` and search for "Khadijat", "June 13", and the "Together Since" date to change.
- **Counter start date** — in the `<script>` block near the bottom, change:
  ```js
  const startDate = new Date('2024-06-13T00:00:00');
  ```

---

Made with love 💕
