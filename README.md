# Mera App — Cloud Build

Jack ki apni apps. HTML likho, GitHub cloud pe APK banega — computer nahi chahiye.

## Kaise use karein

1. **Code badlo:** `www/index.html` kholo (GitHub app ya browser se) → Edit karo → apna HTML/CSS/JS badlo → Save/Commit karo.
2. **Build ka wait karo:** Upar **Actions** tab mein jao → "Build APK" wali run dekho → 2–5 minute mein complete ho jayegi.
3. **APK download karo:** Run kholo → neeche **Artifacts** mein "Mera-App" mile ga → download karo.
4. **Install karo:** Files > Downloads se APK pe tap karo → Install. Pehli dafa install hoga; agle version usi ke upar install honge (data safe) — kyunki har build ek hi keystore se sign hoti hai.

## Files

- `www/index.html` — tumhari app (HTML + CSS + JavaScript). Sirf ye badlo.
- `package.json` / `capacitor.config.json` — app ka setup (appId: com.jack.myapp). In ko haath na lagao.
- `.github/workflows/build-apk.yml` — cloud build ka tareeqa. Is ko haath na lagao.

## Note

- Build sirf tab chalti hai jab `www/`, `package.json` ya `capacitor.config.json` badle. Actions tab se **Run workflow** dabaa ke bhi dobara chala sakte ho.
- Signing keystore GitHub Secrets mein hai (APK_KEYSTORE_BASE64, APK_KEYSTORE_PASSWORD, APK_KEY_ALIAS, APK_KEY_PASSWORD) — kabhi repo mein mat daalna.
