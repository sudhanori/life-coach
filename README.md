# Life Coach

A personal workbook app with three original coaching personas (The Visionary, The Corporate Strategist, The Founder), a journaling space with prompts and a vision board, and a curated shelf of real books.

## Live demo
Once GitHub Pages is enabled (see below), this will be live at:
`https://sudhanori.github.io/personal-projects-of-sudha/`

## ⚠️ Important: the Coaches chat needs a live Anthropic API key to work outside Claude.ai
This file calls `https://api.anthropic.com/v1/messages` directly from the browser with no embedded key — that only works inside Claude.ai's own sandbox. Once hosted here on GitHub Pages:
- **Journal, Vision Board, and Shelf** will work perfectly for anyone who opens the link (they only use local browser storage).
- **The Coaches chat will not work** for visitors, since there's no API key wired in.

To make chat work for visitors, you'd need to either:
1. Add your own Anthropic API key directly in the `fetch` call in `index.html` — **not recommended** for a public repo/link, since anyone viewing the page source or network tab could copy and use your key.
2. Set up a small backend (e.g. a Vercel or Cloudflare serverless function) that holds your API key server-side and proxies requests — the correct way to do this securely, but requires extra setup beyond this static file.

## How to publish this on GitHub Pages
1. Go to your repo: https://github.com/sudhanori/personal-projects-of-sudha
2. Click **Add file → Upload files**
3. Drag in `index.html` (and this `README.md` if you'd like)
4. Commit the changes
5. Go to **Settings → Pages**
6. Under "Source", choose the branch you committed to (likely `main`) and folder `/ (root)`
7. Save — GitHub will give you a live URL, typically `https://sudhanori.github.io/personal-projects-of-sudha/`

That link is what you can share.
