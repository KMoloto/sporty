# Via Sport JBM FC — Matchday Checklist

A single-page checklist (`index.html`) that two or more people can tick off live.

## 1. Create the free Firebase backend (5 min)
1. Go to https://console.firebase.google.com and create a project (no Analytics needed).
2. **Build > Firestore Database > Create database** (production mode, any region).
3. Open the **Rules** tab, paste the contents of `firestore.rules`, click **Publish**.
4. **Project settings (gear) > General > Your apps > Web (`</>`)**. Register an app and copy the config object.
5. Open `index.html`, find `FIREBASE_CONFIG` near the top of the script, and paste in `apiKey`, `authDomain`, `projectId` and `appId`.

## 2. Put it on GitHub Pages
1. Create a GitHub repository and upload `index.html` (plus this README and `firestore.rules` if you like).
2. **Settings > Pages > Build and deployment**: Source = *Deploy from a branch*, Branch = `main`, folder = `/ (root)`, Save.
3. After a minute your site is live at `https://<your-username>.github.io/<repo-name>/`.

## 3. Use it
- On first open, each person enters the same **team code** (6+ letters/numbers, e.g. `viasport-k29x-fc`). Use a hard-to-guess code.
- Shortcut: share the link with the code on the end, e.g. `.../#viasport-k29x-fc`, and it signs in automatically.
- Ticks and notes now sync live between everyone using that code.

## Good to know
- The Firebase config is meant to be public in a web page; the team code is what keeps your data private.
  Anyone who learns the code can edit the checklist, so change it if it leaks.
- Leave `FIREBASE_CONFIG` empty and the page still works, saving ticks on that device only.
