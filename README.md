# Global Travel

One-file travel app (`index.html`) + installable/offline support. No build step, no server code.

## Deploy
**GitHub:** create a repo, upload everything in this folder, commit to `main`.
(`index.html` is ~8 MB — fine for GitHub, under the 25 MB Cloudflare file limit.)

**Cloudflare Pages:** Workers & Pages → Create → Pages → Connect to Git → pick the repo.
Framework preset: **None**. Build command: *(empty)*. Output directory: `/` (root). Save and deploy.

## Updating
Edit `index.html`, commit, push — Cloudflare redeploys automatically.
After changing `index.html`, bump `V` in `sw.js` (e.g. `gt-v2`) so installed copies refresh.

## Files
- `index.html` – the app
- `manifest.webmanifest`, `icon-192.png`, `icon-512.png` – "Add to Home Screen"
- `sw.js` – offline cache (only active over https)
- `_headers` – Cloudflare security/cache headers
- `DEV-NOTES.txt` – developer notes (moved out of `index.html`; not used by the app). To keep working on the app, use the CORE file `newcore-FINAL-2026-10-16_v19_merged-panorama-tips-reset.html`, not `index.html`.

## Version
Built from `newcore-FINAL-2026-10-16_v19_merged-panorama-tips-reset.html`. Service worker cache: `gt-v24`.
