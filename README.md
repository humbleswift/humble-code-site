# Humble Code — portfolio site

Static site, no build step. Structure:

```
index.html
styles.css
learn-animals/
  privacy.html
  terms.html
learn-animals-pro/
  privacy.html
  terms.html
```

Each app has its own privacy policy and terms. App Store Connect URLs to use once live:
- Learn Animals privacy: `https://humble-code.com/learn-animals/privacy.html`
- Learn Animals Pro privacy: `https://humble-code.com/learn-animals-pro/privacy.html`

## Deploy with GitHub Pages (free)

1. Create a new GitHub repo, e.g. `humble-code-site` (public or private, both work with Pages on a paid plan; public is free).
2. Upload these 4 files to the repo root (drag-and-drop on github.com works fine, or `git push`).
3. Go to **Settings → Pages** in the repo.
4. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`. Save.
5. GitHub gives you a URL like `https://yourusername.github.io/humble-code-site/` within a minute or two.

## Use your existing domain (humble-code.com)

1. In the repo, add a file named `CNAME` (no extension) containing just:
   ```
   humble-code.com
   ```
2. At your domain registrar, add these DNS records:
   - `A` records for the apex domain (`humble-code.com`) pointing to GitHub's IPs:
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - Or a `CNAME` record for `www.humble-code.com` → `yourusername.github.io`
3. Back in Settings → Pages, enter `humble-code.com` as your custom domain and enable "Enforce HTTPS" once it's verified (can take a few hours).

## Before you publish — fill in the placeholders

- `index.html`: swap the two `apps.apple.com/app/idXXXXXXXXX` links for your real App Store URLs, and update the contact email if `contact@humble-code.com` isn't right.
- Privacy pages are done (lifted from your app bundle). The per-app `terms.html` files still have `[bracketed]` placeholders (in-app purchases, jurisdiction, date) that need filling.
- The `[date]` placeholders on both privacy pages need a real "last updated" date.
- Optional: replace the "LA" text icons with your real app icon images — just swap the `.app-icon` div for an `<img>` tag pointing to an icon file you add to the repo.

## Adding your next app later

1. Duplicate one of the app folders (e.g. copy `learn-animals-pro/` to `new-app/`), edit the privacy and terms content for the new app.
2. Duplicate one `<article class="app-card">` block in `index.html`, update the name/tagline/App Store link, and point its Privacy/Terms links at the new folder.
3. Use `https://humble-code.com/new-app/privacy.html` as the Privacy Policy URL in App Store Connect.
