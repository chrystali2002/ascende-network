# Deploying the ASCENDE Network site (free, on GitHub Pages)

## Before you deploy — fill in the placeholders
Open `index.html` in any text editor and search for these:
- `[INSTAGRAM_HANDLE]` — your Instagram username (appears in the "Follow us" button link)
- `[WHATSAPP_OR_SIGNUP_LINK]` — your WhatsApp group invite or signup form link
- `[EMAIL]` — contact email in the footer
- `[Month 2026]` / `[Add a past session title]` — past sessions list (or delete those rows)

## Option A: GitHub Pages (recommended)
1. Sign in at github.com → **New repository**.
   - Name it `ascendenetwork.github.io` if you create an org/account named `ascendenetwork` (site lives at that exact URL), or any name like `ascende-site` (site lives at `yourusername.github.io/ascende-site`).
   - Set it to **Public**.
2. Click **uploading an existing file** and drag in `index.html` and the `assets` folder. Commit.
3. Go to **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main`, folder `/ (root)` → Save.
4. Wait ~1 minute. Your site is live at the URL shown on that Pages screen.

To update later: edit files directly on GitHub (pencil icon) and commit — the site redeploys automatically.

Or from the terminal:
```bash
cd ascende-site
git init && git add . && git commit -m "ASCENDE Network site"
git branch -M main
git remote add origin https://github.com/YOURUSERNAME/ascende-site.git
git push -u origin main
```
Then enable Pages in Settings as in step 3.

## Option B: Netlify (fastest, no account setup needed to test)
Go to app.netlify.com/drop and drag the whole `ascende-site` folder onto the page. Done — instant free URL, and you can claim it with a free account to keep it.

## Custom domain (optional, later)
Both GitHub Pages and Netlify support a custom domain (e.g. ascendenetwork.org, ~$10–12/yr from Namecheap/Porkbun) for free — you just point the DNS records and enable HTTPS in the settings.

## Updating each month
For each new edition, in `index.html` update the "Next session" section:
- swap `assets/august-flyer.png` for the new flyer image,
- update the theme, speaker, date, times, and Zoom link,
- move the old session's title into the "Recent sessions" list.
