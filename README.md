# WDD Survey Operations Portal

A single-file web app (`index.html`). No server, no build step.
**Your data is never stored in this repository** - it lives in your own browser (see "Where your data lives").

Package built from portal **v3.01 (Build 20261117.1402)**.

---

## 1. First-time setup (about 5 minutes)

**Before you start - save your current data**
1. Open the portal the way you use it today.
2. Click the **Backup chip** at the top (e.g. "Backup: today") → **Download full backup now**.
3. Keep that `.JSON` file somewhere safe. You will restore it in step 3.

**Create the repository**
1. On github.com click **New repository**. Name it e.g. `wdd-portal`.
2. Choose **Private** if you want the source hidden (note: a private repo needs a paid plan to publish with GitHub Pages - see "Public or private" below).
3. Click **Create repository**, then **uploading an existing file**.
4. Drag in these three files from the package: `index.html`, `README.md`, `.gitignore`.
   **Do not upload any backup (`.JSON`) or export file.**
5. Click **Commit changes**.

**Turn on GitHub Pages**
1. Repository → **Settings → Pages**.
2. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, then **Save**.
3. Wait 1-2 minutes. Your address appears at the top of that page:
   `https://<your-github-name>.github.io/wdd-portal/`

## 2. Move your data to the new address

The browser treats the GitHub address as a different site, so it starts **empty**.

1. Open the new address.
2. Use the **Backup chip → Check a backup file** and pick the file you downloaded in step 1 - it shows what is inside (this changes nothing).
3. Restore it with the portal's normal restore (**Export & Print → Import & Backup → Restore Full Backup**).
4. Set up the automatic **backup folder** again (the browser asks for folder permission once per address).
5. Check your record counts, then bookmark the new address.

Keep using the **same browser and the same profile** every time.

## 3. Updating the portal

Each time you get a new version of the file:
1. Rename it to `index.html`.
2. On github.com open the repository → **Add file → Upload files** → drop it in (it replaces the old one) → **Commit changes**.
3. Wait 1-2 minutes (Settings → Pages / the *Actions* tab shows progress).
4. Open the portal and press **Ctrl + F5** so the browser loads the new version.
5. Check the build number at the bottom of the left sidebar.

Updating never touches your data.

## Where your data lives

* In **your browser, on your laptop** (local storage plus a small IndexedDB vault), for the exact address you open.
* **Not** on GitHub. GitHub only holds the app file.
* Backups go to your Downloads folder and to the backup folder you choose.
* Use the same browser profile. A different browser, profile, private window or address shows an empty portal.
* Clearing the browser's site data for this address deletes the data - your backups are the protection.
* Keep one backup copy **away from the laptop** (OneDrive / network folder / USB drive).

## Public or private

* **Public repository:** anyone can read the source. The file contains company email addresses and the Client Submission Form template.
* **Private repository:** GitHub Pages from a private repo requires a paid GitHub plan, and the published site is still reachable by anyone who has the link.
* The portal has **no login**. Anyone with the link can open the screens, but cannot see your records (they exist only in your browser).
* If you host other apps at `<your-github-name>.github.io`, they share the same browser storage origin as this one. Use a separate GitHub account or a custom domain for this portal if that matters to you.

## Never commit data

The included `.gitignore` blocks backups and exports (`*.json`, `*.JSON`, `*.xlsx`, `*.csv`, `*.docx`, `*.pdf`, `*backup*` ...) when you use git or GitHub Desktop.
The github.com **Upload files** button ignores `.gitignore`, so only ever upload `index.html`, `README.md` and `.gitignore`.

## Troubleshooting

| Problem | What to do |
|---|---|
| Page shows 404 | Wait a couple of minutes; check Settings → Pages shows branch `main` / root and that the file is named `index.html`. |
| Still the old version after an update | Press Ctrl + F5; check the build number in the sidebar. |
| Portal is empty | Wrong address, browser or profile - or the data was cleared. Restore your latest backup. |
| Folder backup asks for permission again | Normal after changing address or browser; choose the folder again. |
| Libraries/fonts do not load | The portal loads a few libraries and fonts from the internet (jsDelivr, Google Fonts); check the connection. |
