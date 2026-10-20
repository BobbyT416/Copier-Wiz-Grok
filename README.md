# Copier Wizard — Build 280

Intelligent diagnostic assistant for HP copiers/printers.

## Important: finish the Build 280 publish

`version.json` is already **280**. The full `index.html` (with the onsite-technician step filter) is large and needs one manual step:

1. Download the Build 280 package: use the zip from the chat, or the files in this repo once uploaded.
2. Open https://github.com/BobbyT416/Copier-Wiz-Grok
3. Click **Add file → Upload files**
4. Drag in **`index.html`** from the Build 280 zip (overwrite the current loader)
5. Commit to `main`

After that, enable **Settings → Pages → Deploy from branch → main → / (root)** if not already on.

Live site (after Pages is enabled): https://bobbyt416.github.io/Copier-Wiz-Grok/

## What Build 280 changes

Documented troubleshooting **starts at the onsite technician procedure**.

Customer / call-center layers (repeated power-cycles, “contact support”, “dispatch a technician”) are skipped. Example for **31.03.20** on M527:

1. Turn the printer off, and then on.
2. Verify the cables between scanner and SCB (ADF side-2 FFC)…
3. Ensure the FFC cable routing is correct…
4. Replace the document feeder assembly.
5. If the issue persists, replace the SCB.

## Files that should be in the repo root

| File | Purpose |
|------|---------|
| `index.html` | Full application (Build 280) — **upload from the zip** |
| `cw-manual-data.js` | HP error catalogs (already present) |
| `version.json` | `{"build":"280","version":"280"}` (already present) |
| `manifest.json` / icons | PWA assets (already present) |
