# TikTok Developer App Registration — Fill-In Sheet
## App: TikTok Empire Autopilot

---

## BASIC INFORMATION

### App Icon
- Size: 1024 × 1024 px, max 5 MB, PNG preferred
- **Free option**: Go to https://www.canva.com → create 1024×1024 design
  → use a dark blue background (#1a1a2e) + a rocket emoji or lightning bolt icon
  → export as PNG

### App Name
```
TikTok Empire Autopilot
```

### Category
```
Business
```

### Description  (copy exactly — 113 chars)
```
AI tool that helps TikTok Shop sellers research products and post videos automatically using the Content Posting API.
```

### Terms of Service URL
```
https://theviralvaultshop26.github.io/tiktok-empire-autopilot/terms.html
```

### Privacy Policy URL
```
https://theviralvaultshop26.github.io/tiktok-empire-autopilot/privacy.html
```
> See "How to Host" section below to publish these pages for free.

### Platforms
✅ Check: **Desktop**
(The app runs locally on a Mac — it is a desktop application.)

---

## APP REVIEW

### Products & Scopes to Add
Add these two products in your app before submitting:
1. **Login Kit** — with scopes: `user.info.basic`
2. **Content Posting API** — with scopes: `video.upload`, `video.publish`, `video.list`

### Redirect URI (add under Login Kit)
```
https://www.tiktok.com/auth/callback/
```

### App Review Explanation  (copy exactly — 841 chars, fits in 1000)
```
Desktop tool for TikTok Shop sellers. Runs locally on Mac, uses Content Posting API to publish product videos to the seller's own account.

Login Kit / user.info.basic: Verifies the connected TikTok account and shows username and connection status in the app dashboard. The seller initiates OAuth manually via the Settings page.

Content Posting API / video.upload + video.publish: After AI generates a product script and the seller creates a video with Creatify.ai, the app submits the video via PULL_FROM_URL. The seller reviews caption, privacy level, and product tags before submission. draft_mode saves to inbox first for review.

video.list: Displays posting history in the dashboard so the seller can track published content.

All tokens stored locally in a .env file. No user data sent to any external server beyond TikTok's own API.
```

---

## DEMO VIDEO — What to Record

Record a screen recording (QuickTime → File → New Screen Recording) showing:

1. **Open the App** — run `streamlit run dashboard.py` in Terminal, browser opens
2. **Settings page** — show the TikTok section with Client Key filled in
3. **Click "Generate Auth URL"** — show the URL appearing
4. **Open the URL** — show TikTok's login/authorization page loading
5. **Paste auth code** — show the code being pasted into the "Step 2" field
6. **Click "Exchange Code"** — show the success message with open_id and scopes
7. **Run the pipeline** — show the dashboard Pipeline page, click "Run Now"
8. **Show outputs** — show the Scripts or Platform Packages page with generated content
9. **Show the TikTok API payload** — open an output JSON file, show the post_info block
10. **Back to Settings** — click "Test Connection" → show the green connected badge

**Tips:**
- Keep it under 5 minutes
- No need for audio, but captions help
- Export as MP4, keep under 50 MB (use HandBrake to compress if needed)

---

## HOW TO HOST THE LEGAL PAGES (Free — 5 minutes)

### Option A: GitHub Pages (recommended)

1. Go to https://github.com → sign in (or create free account)
2. Click **New repository**
   - Repository name: `tiktok-empire-autopilot`
   - Set to **Public**
   - Click **Create repository**
3. Click **Add file → Upload files**
4. Upload `legal/terms.html` and `legal/privacy.html` from this project folder
5. Go to **Settings → Pages**
   - Source: **Deploy from a branch**
   - Branch: **main** / **root**
   - Click **Save**
6. Wait ~1 minute. Your pages will be live at:
   - `https://YOUR-GITHUB-USERNAME.github.io/tiktok-empire-autopilot/terms.html`
   - `https://YOUR-GITHUB-USERNAME.github.io/tiktok-empire-autopilot/privacy.html`
7. Replace `YOUR-GITHUB-USERNAME` in the URLs above with your actual GitHub username
   and paste those URLs into the TikTok registration form.

### Option B: Netlify Drop (even faster)

1. Go to https://app.netlify.com/drop
2. Drag the entire `legal/` folder onto the page
3. Netlify gives you a URL like `https://amazing-name-123.netlify.app`
4. Your pages are at `.../terms.html` and `.../privacy.html`

---

## CHECKLIST BEFORE SUBMITTING

- [ ] App icon uploaded (1024×1024 PNG)
- [ ] Description filled (113 chars, copied from above)
- [ ] Terms of Service URL live and accessible
- [ ] Privacy Policy URL live and accessible
- [ ] Platform: Desktop checked
- [ ] Login Kit product added with `user.info.basic` scope
- [ ] Content Posting API product added with `video.upload`, `video.publish`, `video.list`
- [ ] Redirect URI added: `https://www.tiktok.com/auth/callback/`
- [ ] App review explanation filled (copied from above)
- [ ] Demo video uploaded (MP4, under 50 MB)
