# Privacy Site — BJJ Round Timer

Standalone HTML site for the Privacy Policy. Ready to host on:

- **GitHub Pages** (recommended, free)
- `digiras.com/bjj-timer/privacy/` (self-hosted)
- Any static host (Netlify, Vercel, Cloudflare Pages)

## Files

| File | Purpose |
|---|---|
| `index.html` | Self-contained privacy policy page. Inline CSS, brand-styled (dark + Crimson + Sora-like system fonts), MarkA logo SVG embedded. No external dependencies. |
| `README.md` | This file (deploy instructions). |

## Deploy: GitHub Pages (fastest, 3 minutes)

```bash
# 1. Create new public repo
cd /tmp
mkdir bjj-timer-privacy && cd bjj-timer-privacy
cp "/Users/Orhun/Desktop/BJJ Pluging/01_Projects/digiras-utility-apps/bjj-round-timer/store-assets/privacy-site/index.html" .
git init
git add index.html
git commit -m "Initial privacy policy"

# 2. Create the repo on github.com first (digirasplus/bjj-timer-privacy, public)
# Then push:
git remote add origin git@github.com:digirasplus/bjj-timer-privacy.git
git branch -M main
git push -u origin main

# 3. On github.com → Settings → Pages → Source: "Deploy from branch" → main / root → Save
# Wait ~1 minute, URL goes live at:
#   https://digirasplus.github.io/bjj-timer-privacy/
```

This URL is what goes in Play Console → Store listing → Privacy policy field.

## Deploy: digiras.com self-host

Drop `index.html` into your web root at `/bjj-timer/privacy/index.html`, accessible at `https://digiras.com/bjj-timer/privacy`.

## Verify after publish

- Visit URL in browser — dark page, Crimson logo, "Privacy Policy" heading
- Click email link — opens mail client to bjj-timer@digiras.com
- Confirm public access (incognito window)
- Update `full-description.md` and Play Console privacy field with the final URL

## Update procedure (future versions)

When the policy changes (e.g., v1.1 adds AdMob):
1. Edit `index.html` in this repo
2. Update both "Effective Date" and "Last Updated" at top
3. Modify Section 2 (Information We Collect) and Section 4 (Third-Party Services) accordingly
4. Commit + push → GH Pages auto-deploys in ~1 min
5. Update Play Store "What's New" changelog mentioning the policy update
