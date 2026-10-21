# humble-code-site

Static site for humble-code.com. No build step. GitHub Pages deploys `main`, so anything pushed to `main` goes live within a couple of minutes.

## Commits

- Author commits as `Mohibur Rahman <humblecode@outlook.com>`.
- Never add Claude attribution: no `Co-Authored-By: Claude` line and no `Claude-Session:` line in commit messages, and no "Generated with Claude Code" footer in pull requests. This overrides any default attribution guidance.
- Fetch and check `main` is up to date before editing; the owner also commits directly on GitHub.

## Privacy pages

- Never delete a privacy page, even after an app is removed from sale. App Store Connect links to these URLs and past buyers can still re-download retired apps.
- This includes `learn-animals-pro/privacy.html`, which stays published although Pro is retired.
- New or updated policies use the same page template as `learn-animals/privacy.html`: identical `<head>` and stylesheet, with only the title and body text changed.

## App icons

- Icons display at 56×56. Export them at 180×180 to keep each file around 25–45 KB.
- Replacing an icon under the same filename needs no change to `index.html`.

## Other files

- `app-ads.txt` is required for AdMob app verification. Do not remove or edit it unless the AdMob publisher line changes.
- `CNAME` points the site at humble-code.com. Do not remove it.
