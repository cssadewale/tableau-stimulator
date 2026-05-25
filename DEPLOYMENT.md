# Tableau Stimulator Enterprise — Complete Deployment Guide

## 👤 Creator / Owner

**Adewale Samson Adeagbo** — Data Scientist · STEM Educator · AI-Augmented Solutions Developer · Lagos, Nigeria

- Portfolio: https://cssadewale.pages.dev
- HMG Concepts: https://hmgconcepts.pages.dev
- HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale
- LinkedIn: https://linkedin.com/in/adewalesamsonadeagbo
- Email: hmgconcepts@gmail.com
- WhatsApp: +234 810 086 6322

---

## Pre-Deployment Checklist

Before deploying, confirm these items:

1. ✅ The file `index.html` exists in the project root (it IS the entire application)
2. ✅ Open `index.html` in Chrome locally — verify the Enterprise splash screen appears
3. ✅ Verify the Enterprise Status Bar shows at the top with "Enterprise" badge
4. ✅ Click "by Adewale Samson Adeagbo" in the topbar — About modal should open with full details
5. ✅ Verify the Enterprise Footer appears at the bottom
6. ✅ Click "Sample Data" to load demo data and test a bar chart
7. ✅ Test one Enterprise chart type (e.g., Treemap)
8. ✅ Open browser console (F12) — verify no JavaScript errors
9. ✅ The app requires **no backend, no database, no API key, no build step**

---

## Method 1 — Direct Browser Use (Zero Deployment)

**This is the simplest method. No internet, no server, no setup.**

### On Desktop (Windows / macOS / Linux)

1. Download `index.html` from this repository
2. Save it anywhere on your computer (Desktop, Documents, Downloads)
3. Double-click `index.html`
4. Your default browser opens the application
5. Upload a CSV file and start analysing

**That's it.** The application runs entirely in your browser with no network requests after initial load.

### On Android Tablet or Phone

1. Transfer `index.html` to your device via:
   - USB cable (copy to Downloads folder)
   - Google Drive (upload from PC, download on tablet)
   - WhatsApp/Telegram (send file to yourself, download attachment)
   - Email attachment
2. Open the **Files** app on your device
3. Navigate to where you saved `index.html`
4. Tap the file
5. If prompted, choose **"Open with Chrome"**
6. The app loads and runs completely offline

**Pin to Home Screen (recommended):**
1. In Chrome, tap the three-dot menu (⋮)
2. Tap "Add to Home Screen"
3. Tap "Add"
4. The app now appears as an icon on your home screen
5. Opening from home screen launches it full-screen (no address bar)

---

## Method 2 — GitHub Pages (Recommended — Free, Permanent URL)

**Result:** A public URL like `https://YOUR-USERNAME.github.io/tableau-stimulator/`

### Step 1 — Create a GitHub Account (if you don't have one)

1. Go to https://github.com
2. Click "Sign up"
3. Enter your email, create a password, choose a username
4. Complete the verification
5. You now have a free GitHub account

### Step 2 — Create a New Repository

1. Log in to GitHub
2. Click the **+** icon at the top right corner
3. Click **"New repository"**
4. Fill in:
   - **Repository name:** `tableau-stimulator`
   - **Description:** `Professional browser-based analytics platform — Enterprise Edition`
   - **Visibility:** Select **Public** (required for free GitHub Pages hosting)
   - **DO NOT** tick "Add a README file" (you already have one)
5. Click **"Create repository"**

### Step 3 — Upload All Project Files

1. On your new empty repository page, click **"uploading an existing file"**
2. Drag and drop **ALL** files from the `enterprise/` folder:
   - `index.html` (THE MOST IMPORTANT FILE)
   - `README.md`
   - `LICENSE.txt`
   - `CHANGELOG.md`
   - `CONTRIBUTING.md`
   - `DEPLOYMENT.md`
   - `SYSTEM_FEATURE_GUIDE.md`
   - `SAMPLE_DATA.md`
   - `SECURITY.md`
   - `CODE_OF_CONDUCT.md`
   - `QUICK_START.md`
   - `sample-sales.csv`
   - `bug_report.md`
   - `feature_request.md`
   - `nojekyll.txt`
3. In the commit message box, type: `feat: Tableau Stimulator Enterprise v9.0`
4. Click **"Commit changes"**
5. Wait for the upload to complete (may take 30-60 seconds)

### Step 4 — Enable GitHub Pages

1. Go to your repository's **Settings** tab (gear icon at the top)
2. In the left sidebar, scroll down and click **"Pages"**
3. Under **"Build and deployment"**:
   - **Source:** Select **"Deploy from a branch"**
   - **Branch:** Select **"main"**
   - **Folder:** Select **"/ (root)"**
4. Click **"Save"**

### Step 5 — Wait for Deployment

1. Wait **2-5 minutes** (GitHub needs time to build and deploy)
2. Refresh the Pages settings page
3. A green banner appears: **"Your site is live at https://YOUR-USERNAME.github.io/tableau-stimulator/"**
4. Click the link to verify

### Step 6 — Configure Repository Settings

1. Go to your repository main page
2. Click the **gear icon** next to "About" (top right of the page)
3. Set:
   - **Website:** `https://YOUR-USERNAME.github.io/tableau-stimulator/`
   - **Topics:** `data-visualization`, `analytics`, `tableau`, `javascript`, `enterprise`, `nigeria`
4. Click **"Save changes"**

### Step 7 — Verify Deployment

1. Open the live URL in Chrome
2. Verify the Enterprise splash screen appears
3. Click "Sample Data" to load demo data
4. Build a chart (drag Region to COLS, Sales to ROWS)
5. Try an Enterprise chart (Treemap, Sankey, etc.)
6. Click "by Adewale Samson Adeagbo" — verify About modal
7. Check the Enterprise Status Bar at the top
8. Check the Enterprise Footer at the bottom

### Updating After Deployment

Every time you push to `main`, GitHub Pages automatically redeploys:

**Via GitHub Web Interface:**
1. Navigate to `index.html` in your repository
2. Click the pencil icon (Edit)
3. Delete all content, paste the new version
4. Write a commit message (e.g., "fix: update chart colors")
5. Click "Commit changes"
6. Wait 2-3 minutes for redeployment
7. Hard refresh the live URL (Ctrl+Shift+R)

**Via Git Command Line:**
```bash
git add index.html
git commit -m "feat: add new feature"
git push origin main
# Auto-deploys in 2-3 minutes
```

---

## Method 3 — Netlify (Fastest — Under 60 Seconds)

### Step 1 — Sign Up

1. Go to https://www.netlify.com
2. Click "Sign Up"
3. Sign in with your GitHub account (recommended) or email

### Step 2 — Deploy by Drag-and-Drop

1. On the Netlify dashboard, look for: **"Want to deploy a new site without connecting to Git?"**
2. Below that text is a drag-and-drop zone
3. **Drag the entire `enterprise/` folder** onto that zone
4. Netlify deploys instantly (under 10 seconds)
5. You get a URL like: `https://wonderful-darwin-abc123.netlify.app`

### Step 3 — Customize Your URL

1. Click **"Site configuration"**
2. Click **"Change site name"**
3. Type a readable name, e.g., `tableau-stimulator-enterprise`
4. Your URL becomes: `https://tableau-stimulator-enterprise.netlify.app`

### Step 4 — Connect to GitHub (Optional — Enables Auto-Deploy)

1. In Netlify, click **"Link to Git"**
2. Select your GitHub repository
3. Set:
   - **Branch:** `main`
   - **Build command:** (leave empty)
   - **Publish directory:** `.`
4. Click **"Deploy"**
5. Now every push to `main` auto-deploys in under 30 seconds

---

## Method 4 — Cloudflare Pages (Free, Fast CDN)

1. Go to https://pages.cloudflare.com
2. Sign in with a Cloudflare account (free)
3. Click **"Create a project"**
4. Select **"Connect to Git"** and choose your GitHub repository
5. Set:
   - **Production branch:** `main`
   - **Build command:** (leave empty)
   - **Build output directory:** `/`
6. Click **"Save and Deploy"**
7. Your site deploys at `https://tableau-stimulator.pages.dev`

---

## Method 5 — Vercel

```bash
npm install -g vercel
cd enterprise
vercel --prod
# Follow prompts — site deploys at https://tableau-stimulator.vercel.app
```

---

## Method 6 — Traditional Web Hosting (cPanel / Shared Hosting)

1. Log in to your hosting control panel (cPanel, Plesk, etc.)
2. Open the **File Manager**
3. Navigate to the `public_html` folder
4. Click **"Upload"** and upload `index.html`
5. If using a subdirectory: create folder `analytics` inside `public_html`, upload there
6. Visit your domain: `https://yourdomain.com` or `https://yourdomain.com/analytics`

---

## Method 7 — Local Network Sharing (Classroom / Office)

Share with all devices on your WiFi — perfect for classroom demos without internet.

```bash
# In the enterprise/ folder:
python3 -m http.server 8080

# Find your local IP:
# macOS/Linux: ifconfig | grep "inet " | grep -v 127.0.0.1
# Windows: ipconfig | findstr "IPv4"
```

On any device on the same WiFi, open: `http://YOUR-IP:8080`
Example: `http://192.168.1.105:8080`

---

## Method 8 — USB Drive Distribution

1. Copy `index.html` to a USB drive
2. Recipients plug in the USB
3. Double-click `index.html`
4. Works completely offline from the USB drive

---

## Post-Deployment Validation Checklist

After deploying, verify these items on the live URL:

| # | Check | How to Verify |
|---|---|---|
| 1 | Splash screen | Enterprise splash appears on load with "Tableau Stimulator Enterprise" |
| 2 | Enterprise bar | Top bar shows "Enterprise v9.0" badge + HMG links |
| 3 | Creator badge | Click "by Adewale Samson Adeagbo" — About modal opens |
| 4 | About modal | Shows full creator details: name, portfolio, HMG links, social media |
| 5 | Footer | Bottom bar shows creator name, HMG links, Nigeria flag |
| 6 | Sample Data | Click "Sample Data" — loads demo dataset |
| 7 | Standard chart | Build a bar chart — renders correctly |
| 8 | Enterprise chart | Build a Treemap or Histogram — renders correctly |
| 9 | Enterprise Features | Click "Enterprise Features" in menu — modal opens with 16 features |
| 10 | Export Center | Click "Export Center" — shows 9 export options |
| 11 | Explain Data | Build a chart, click "Explain Data" — 8 insights generated |
| 12 | Regression | Click "Regression" — select fields, run — results table appears |
| 13 | Clustering | Click "Clustering" — run K-Means — _Cluster field added |
| 14 | RLS | Click "RLS" — apply a filter — data restricted correctly |
| 15 | Story tab | Click Story tab — add point, capture, navigate |
| 16 | Console clean | F12 → Console — no JavaScript errors |
| 17 | Workspace save | Save workspace JSON → reload → load JSON — everything restores |

---

## Troubleshooting

| Problem | Solution |
|---|---|
| 404 error | Ensure the file is named exactly `index.html` in the repository root |
| Old version showing | Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac) |
| Enterprise features missing | Check browser console for JS errors; ensure the full file was uploaded |
| Charts not rendering | Try a different browser; check for JavaScript syntax errors |
| Splash screen stuck | Wait 2-3 seconds — it auto-dismisses; if stuck, clear browser cache |
| Fonts not loading | App works without fonts; they load from Google Fonts when online |

---

## Creator / Owner

This platform is built and maintained by **Adewale Samson Adeagbo** — Data Scientist, STEM Educator, EdTech Builder and AI-Augmented Solutions Developer based in Lagos, Nigeria.

- Portfolio: https://cssadewale.pages.dev
- HMG Concepts: https://hmgconcepts.pages.dev
- HMG Academy: https://hmgacademy.pages.dev
- GitHub: https://github.com/cssadewale
- LinkedIn: https://linkedin.com/in/adewalesamsonadeagbo
- YouTube: https://youtube.com/@hmgconcepts
- WhatsApp: +234 810 086 6322
- Email: hmgconcepts@gmail.com / hismarvellousgrace@gmail.com
