# Deployment Guide

Seven methods for deploying DataViz Studio, from the simplest single-device use
to a publicly hosted web application accessible from any device in the world.

---

## Method 1 — Direct Browser Use (No Deployment Needed)

The simplest method. No internet, no server, no setup required.

### Desktop (Windows / macOS / Linux)

1. Download `index.html` from this repository
2. Save it anywhere (Desktop, Documents, Downloads)
3. Double-click `index.html`
4. It opens in your default browser
5. Upload a CSV and start analysing

### Android Tablet (ITEL Vista Tab 30s or any Android device)

**Transfer the file:**
- USB cable: connect tablet to PC, copy file to tablet Downloads folder
- Google Drive: upload from PC, open Drive on tablet, download
- WhatsApp/Telegram: send file to yourself, tap attachment, tap Download
- Email: send as attachment, open on tablet, download

**Open the file:**
1. Open the Files app on your tablet
2. Navigate to Downloads (or wherever you saved the file)
3. Tap `index.html`
4. If prompted: select "Open with Chrome"
5. The app loads and runs fully offline

**Pin to Home Screen (recommended):**
1. Tap the three-dot menu (⋮) in Chrome
2. Tap "Add to Home Screen"
3. Tap "Add" in the confirmation dialog
4. The app now appears on your home screen as an icon
5. Opening it from the home screen launches it full-screen without the browser address bar

---

## Method 2 — GitHub Pages (Recommended — Free, Permanent URL)

Free permanent public URL. Auto-deploys every time you push to main.

### Prerequisites
- A GitHub account (free at github.com)
- Your `index.html` file

### Step-by-Step

**Step 1 — Create the repository**

1. Log in to github.com
2. Click the + icon at the top right, then "New repository"
3. Repository name: `dataviz-studio`
4. Description: `Professional browser-based data analytics platform`
5. Visibility: Public (required for free GitHub Pages)
6. Do NOT tick "Add a README file" (you have your own)
7. Click "Create repository"

**Step 2 — Upload all files**

1. In the empty repository, click "uploading an existing file"
2. Select and upload all files at once:
   - `index.html` (rename from dataviz-studio-v7.html)
   - `README.md`
   - `LICENSE`
   - `CHANGELOG.md`
   - `CONTRIBUTING.md`
   - `DEPLOYMENT.md`
   - `SAMPLE_DATA.md`
   - `SECURITY.md`
   - `CODE_OF_CONDUCT.md`
   - `.gitignore`
3. Commit message: `feat: initial release — DataViz Studio v7`
4. Click "Commit changes"

**Step 3 — Upload GitHub Actions workflow**

1. Click "Add file" then "Create new file"
2. In the name box type exactly: `.github/workflows/deploy.yml`
   (GitHub will automatically create the folder structure)
3. Paste the contents of `deploy.yml`
4. Commit message: `ci: add GitHub Actions auto-deploy workflow`
5. Click "Commit changes"

**Step 4 — Upload issue templates**

Repeat for each:
- `.github/ISSUE_TEMPLATE/bug_report.md`
- `.github/ISSUE_TEMPLATE/feature_request.md`
- `.github/PULL_REQUEST_TEMPLATE.md`

**Step 5 — Enable GitHub Pages**

1. Go to the Settings tab of your repository
2. In the left sidebar, click "Pages"
3. Under Build and deployment, set:
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
4. Click "Save"

**Step 6 — Wait and verify**

1. Wait 2-3 minutes
2. Refresh the Pages settings page
3. A green banner appears: "Your site is live at https://cssadewale.github.io/dataviz-studio/"
4. Click the link to verify it works

**Step 7 — Configure repository settings**

1. Go to repository main page
2. Click the gear icon next to "About"
3. Set:
   - Website: `https://cssadewale.github.io/dataviz-studio/`
   - Topics: `data-visualization`, `analytics`, `tableau-alternative`, `javascript`, `nigeria`, `edtech`, `open-source`
4. Click "Save changes"

### Updating After Changes

Every time you push to main, GitHub Pages redeploys automatically (2-3 minutes):

```bash
git add index.html
git commit -m "feat: add new feature"
git push origin main
# GitHub Actions deploys automatically
```

Or via the GitHub web interface:
1. Click `index.html` in the repository
2. Click the pencil (Edit) icon
3. Delete all content, paste the new version
4. Click "Commit changes"

---

## Method 3 — Netlify (Fastest — Under 60 Seconds)

**Step 1.** Go to netlify.com. Click "Sign Up", use your GitHub account (free).

**Step 2.** On the Netlify dashboard, find:
*"Want to deploy a new site without connecting to Git?"*
There is a drag-and-drop zone below it.

**Step 3.** Drag your `index.html` file onto that zone.

**Step 4.** Netlify deploys instantly and gives you a URL like:
`https://wonderful-darwin-abc123.netlify.app`

**Step 5.** Customise the URL:
- Click "Site configuration" then "Change site name"
- Type e.g. `dataviz-adewale`
- Your URL becomes: `https://dataviz-adewale.netlify.app`

**Step 6 (Optional — Connect GitHub for auto-deploy):**
1. In Netlify, click "Link to Git"
2. Select your GitHub repository
3. Set: Branch = main, Build command = (empty), Publish directory = `.`
4. Click "Deploy"

Now every push to main automatically redeploys in under 30 seconds.

---

## Method 4 — Vercel

```bash
npm install -g vercel
cd dataviz-studio
vercel --prod

# Prompts:
# Scope: your username
# Link to existing project? No
# Project name: dataviz-studio
# Directory: ./
# Override settings? No
```

Your site deploys at `https://dataviz-studio.vercel.app`

---

## Method 5 — Traditional Web Hosting (cPanel / Shared Hosting)

Works with any hosting provider: Namecheap, GoDaddy, Bluehost, etc.

1. Log in to your hosting control panel (cPanel or equivalent)
2. Open the File Manager
3. Navigate to the `public_html` folder (your website root)
4. Click "Upload" and upload `index.html`
5. For root domain (yourdomain.com): ensure file is named `index.html` in `public_html`
6. For subdirectory (yourdomain.com/analytics):
   - Create a folder called `analytics` inside `public_html`
   - Upload `index.html` into that folder
7. Visit your domain to verify

---

## Method 6 — Local Network Sharing (Classroom / Office)

Share across all devices on your local WiFi — for classroom demonstrations without internet.

**Using Python (built into macOS and Linux, available on Windows):**

```bash
# In the folder containing index.html
python3 -m http.server 8080

# Find your local IP address:
# macOS/Linux:
ifconfig | grep "inet " | grep -v 127.0.0.1
# Windows:
ipconfig | findstr "IPv4"
```

On any device connected to the same WiFi, open:
`http://[your-ip-address]:8080`

Example: `http://192.168.1.105:8080`

Every student or colleague on the same network can access DataViz Studio in their browser.

---

## Method 7 — USB Drive Distribution

1. Copy `index.html` to a USB drive
2. Recipients plug in the USB drive
3. Open their file manager and double-click `index.html`
4. The browser opens and DataViz Studio runs completely offline from the USB drive

---

## Custom Domain Setup

### With GitHub Pages

1. At your domain registrar (Namecheap, GoDaddy, etc.), open DNS settings
2. Add a CNAME record: Name = `analytics` (or `@` for root), Value = `cssadewale.github.io`
3. In your GitHub repository: Settings → Pages → Custom domain → enter your domain
4. Click "Save". GitHub verifies DNS and enables HTTPS automatically (up to 24 hours)

### With Netlify

1. In Netlify: Domain management → Add custom domain
2. Enter your domain. Netlify provides DNS instructions.
3. At your domain registrar, update nameservers to Netlify's nameservers
4. Netlify provisions a free HTTPS certificate automatically

---

## Performance Notes

| Dataset Size | Load Time | Recommendation |
|---|---|---|
| < 1,000 rows | Instant | Use any chart type |
| 1,000 - 10,000 rows | < 1 second | All features work normally |
| 10,000 - 50,000 rows | 1-3 seconds | Enable Sampling (1K-5K rows) |
| 50,000+ rows | 3-10 seconds | Enable Sampling (500-1K rows) |

Enable **Data Sampling** in the shelf controls bar to limit rendering rows.
The full dataset is still used for CSV export, statistics, and the data cleaner.

---

## Troubleshooting

| Problem | Solution |
|---|---|
| Site shows 404 | Ensure the file is named exactly `index.html` in the repository root |
| GitHub Pages not updating | Wait 5 minutes and hard-refresh (Ctrl+Shift+R) |
| Chart not rendering | Check browser console (F12) for errors; try a different browser |
| CSV not loading on mobile | Ensure UTF-8 encoding; avoid special characters in column headers |
| Fonts not loading offline | App works without fonts; Sora/DM Mono load from Google Fonts when online |
| Slow on large files | Enable Data Sampling (500-1K rows) in the shelf controls |
| All buttons not working | Check the browser console for a JavaScript syntax error |
