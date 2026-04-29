# aqilmanzoor850.github.io

Hosting for Universal Links / App Links assets used by the OC mobile apps.

| File | URL | Purpose |
|------|-----|---------|
| `.well-known/apple-app-site-association` | https://aqilmanzoor850.github.io/.well-known/apple-app-site-association | iOS Universal Links — declares which app paths this domain hands off to. |
| `.well-known/assetlinks.json` | https://aqilmanzoor850.github.io/.well-known/assetlinks.json | Android App Links — declares which package + signing certificate this domain hands off to. |
| `.nojekyll` | (none) | Tells GitHub Pages NOT to run Jekyll, so the `.well-known/` folder (which starts with a dot) is served. |
| `index.html` | https://aqilmanzoor850.github.io/ | Empty placeholder so the root URL does not 404. |

## Used by

- App: `com.anonymous.scbb` (OC Onboarding mobile)
- Singpass redirect URL registered in dev portal: `https://aqilmanzoor850.github.io/singpass/callback`
- Corppass redirect URL registered in dev portal: `https://aqilmanzoor850.github.io/corppass/callback`

## Updating the AASA / assetlinks

If you rotate the Android keystore, regenerate the SHA-256 with:

    keytool -list -v -keystore android/app/release.jks -storepass <password>

...and paste the new value into `.well-known/assetlinks.json`.

If you change Apple Team ID, update `.well-known/apple-app-site-association`.
