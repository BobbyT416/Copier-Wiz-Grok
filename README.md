# Copier Wizard — Build 280

Intelligent diagnostic assistant for HP copiers/printers.

## Change in this build

Documented troubleshooting now **starts at the onsite-technician procedure**.

Customer and call-center layers (repeated power-cycles, “contact support”, “dispatch a technician”) are skipped. The first step shown is the power-cycle that belongs with the real onsite work, followed by cable/FFC checks, replacements, etc.

Example for **31.03.20** on M527:

1. Turn the printer off, and then on.
2. Verify the cables between scanner and SCB (ADF side-2 FFC)…
3. Ensure the FFC cable routing is correct…
4. Replace the document feeder assembly.
5. If the issue persists, replace the SCB.

## Files

| File | Purpose |
|------|---------|
| `index.html` | Full application (Build 280) |
| `cw-manual-data.js` | HP error catalogs, parts, procedures |
| `version.json` | `{"build":"280","version":"280"}` |
| `manifest.json` / icons | PWA assets |

## Publish to a new GitHub repo

1. Create an empty repository.
2. Upload every file from this folder to the root.
3. Settings → Pages → Deploy from branch → main → / (root).
4. Live URL: `https://YOUR-USERNAME.github.io/YOUR-REPO-NAME/`

Open `index.html` locally for a quick check (keep `cw-manual-data.js` beside it).
