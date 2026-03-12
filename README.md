# Ikigai Vat — PWA

A personal passion-finding funnel. Activities flow down a vat, leak into side buckets at each decision, and the survivors reach the pot of gold (money game).

## Deploy to GitHub Pages (10 min)

### Step 1 — Create a GitHub repo

1. Go to https://github.com/new
2. Name it `ikigai` (or anything you want)
3. Keep it **Public** (required for free GitHub Pages)
4. Click **Create repository**

### Step 2 — Upload the files

Option A — drag & drop (easiest):
1. On the repo page, click **uploading an existing file**
2. Drag ALL files from this folder:
   - `index.html`
   - `manifest.json`
   - `sw.js`
   - `icons/` folder (with `icon-192.png` and `icon-512.png`)
3. Click **Commit changes**

Option B — GitHub CLI (if you have it):
```bash
cd ikigai-vat
git init
git add .
git commit -m "init"
git remote add origin https://github.com/YOUR_USERNAME/ikigai.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages

1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under **Source**, select **Deploy from a branch**
3. Choose branch: `main`, folder: `/ (root)`
4. Click **Save**

Your app will be live at:
`https://YOUR_USERNAME.github.io/ikigai`

(Takes ~1 minute to deploy on first push)

### Step 4 — Install as a mobile app

**On iPhone (Safari):**
1. Open your GitHub Pages URL in Safari
2. Tap the Share button (box with arrow)
3. Scroll down → tap **Add to Home Screen**
4. Tap **Add** — done!

**On Android (Chrome):**
1. Open your GitHub Pages URL in Chrome
2. Tap the 3-dot menu → **Add to Home screen**
   OR wait for the install banner to appear in the app
3. Tap **Install**

The app will appear on your home screen with a dark icon, run full-screen with no browser chrome, and work offline.

---

## File structure

```
ikigai-vat/
├── index.html      ← the entire app
├── manifest.json   ← PWA metadata
├── sw.js           ← service worker (offline)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

## Data

All data is stored in `localStorage` on your device. Nothing leaves your phone.
To back up: open browser console and run `JSON.stringify(localStorage.getItem('ikigai_v3'))`
To restore: `localStorage.setItem('ikigai_v3', '<paste backup here>')`
