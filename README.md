# Copier Wizard — Build 279

Intelligent diagnostic assistant for HP copiers/printers.

## Files included

| File | Purpose |
|------|---------|
| `index.html` | Full application (single-page) |
| `cw-manual-data.js` | Extracted HP error catalogs, parts, and procedures |
| `version.json` | Build marker (`{"build":"279","version":"279"}`) |
| `manifest.json` | PWA manifest |
| `icon-192.png` / `icon-512.png` / `apple-touch-icon.png` | Icons |

## How to publish to a new GitHub repository

1. Create a new empty repository on GitHub (e.g. `YourName/Copier-Wizard`).
2. Upload **all** files from this folder to the root of the repository (or to a `docs/` / `gh-pages` folder if you prefer).
3. Enable **GitHub Pages** from the repository settings → Pages → Source = Deploy from a branch → main (or the branch you pushed to) → / (root).
4. After a minute or two the live site will be at:  
   `https://YourName.github.io/Copier-Wizard/`

## Local testing

Open `index.html` directly in a modern browser, or serve the folder with any static server:

```bash
npx serve .
# or
python -m http.server 8000
```

## Notes / known status (2026-10-20)

- Build **279** restores numerical error-code prefix search (typing + Enter), removes the 8-result cap, uses `desc` for descriptions, and correctly includes the full M527 31-series list.
- Automated browser suite on the original development branch had not yet gone fully green at packaging time (last failure was in Playwright smoke tests after a state-reset fix). Static validation (HTML/JS parse + build marker) passed.
- Production root of the original repo was still at Build 257 and was **not** modified.
- Do **not** invent part numbers or procedures. All diagnostic content comes from the supplied HP source data in `cw-manual-data.js`.

## Recommended next steps after you publish

1. Open the live site and confirm the build label shows **279**.
2. Test product-number-only entry with `T3U55A` (M776dn) and `F2A81A` (M527c).
3. On an M527 machine, open Numerical Error Code and type `31` — you should see the full list including `31.01.47` and `31.03.30`.
4. If anything looks wrong, keep this folder as the baseline and iterate from there.

