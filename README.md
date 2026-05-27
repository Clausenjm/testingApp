# Grounded PWA – Deployment Guide

## Your files
```
grounded-pwa/
├── index.html       ← The full app
├── manifest.json    ← Makes it installable
├── sw.js            ← Enables offline use
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    └── icon-512.png
```

---

## Deploy to GitHub Pages (free, ~5 minutes)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up (free).

### Step 2 — Create a new repository
1. Click the **+** button → "New repository"
2. Name it: `grounded`
3. Set it to **Public**
4. Click "Create repository"

### Step 3 — Upload your files
1. Click **"uploading an existing file"** on the repo page
2. Drag ALL the files from this folder (including the `icons` subfolder)
3. Make sure the folder structure is preserved:
   - `index.html` at the root
   - `manifest.json` at the root
   - `sw.js` at the root
   - `icons/icon-192.png` etc. inside the `icons` folder
4. Click **"Commit changes"**

### Step 4 — Enable GitHub Pages
1. Go to your repo → **Settings** → **Pages** (left sidebar)
2. Under "Source" select **"Deploy from a branch"**
3. Choose **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait ~60 seconds, then your URL appears:
   `https://YOUR-USERNAME.github.io/grounded`

---

## Install on Samsung Phone

1. Open **Chrome** on your Samsung phone
2. Go to your GitHub Pages URL
3. Wait for the page to fully load
4. Tap the **three-dot menu** (⋮) in Chrome
5. Tap **"Add to Home screen"**
6. Tap **"Add"** on the confirmation
7. Find the Grounded icon on your home screen — tap it

✅ It now opens fullscreen with no browser bar, just like a real app.
✅ It works offline after the first load.
✅ Your data is saved locally on the device.

---

## Troubleshooting

**"Add to Home screen" option doesn't appear?**
- Make sure you're using Chrome (not Samsung Internet)
- The site must be served over HTTPS — GitHub Pages handles this automatically

**Icons look blurry?**
- This is fine during first install; they sharpen after Android caches them

**Want to update the app later?**
- Just re-upload `index.html` to GitHub and the update deploys automatically
- Users get the new version next time they open the app with internet

---

## Next step: Real Android APK (optional)

If you want to submit to the Google Play Store later, use Capacitor:
https://capacitorjs.com/docs/getting-started

The HTML/JS code in `index.html` works as-is with Capacitor —
no rewriting needed.
