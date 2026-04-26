# ceyizim-web

Çeyizim iOS uygulamasının web sayfaları:
- Marketing landing
- Privacy policy (TR + EN)
- Support / FAQ (TR + EN)
- Terms & subscription disclosure
- Universal Links AASA dosyası

Live URL: https://saevaexe.github.io/ceyizim-web/

## Yapı

```
ceyizim-web/
├── index.html             — TR landing
├── index-en.html          — EN landing
├── privacy.html / privacy-en.html
├── support.html / support-en.html
├── terms.html             — TR + EN bilingual
├── style.css              — minimal stil (soft pembe / lila / altın)
├── assets/                — logo, screenshot, app store badge'leri
└── .well-known/
    └── apple-app-site-association
```

## Deploy (GitHub Pages)

1. GitHub'da public repo: `saevaexe/ceyizim-web` (private app repo `saevaexe/ceyizim` ayrı kalır)
2. Lokal:
   ```
   cd /Users/osmanseven/ceyizim-web
   gh repo create saevaexe/ceyizim-web --public --source=. --push
   ```
3. GitHub repo Settings → Pages → Source: `main` branch, `/ (root)` folder → Save
4. ~1-2 dk sonra `https://saevaexe.github.io/ceyizim-web/` aktif

### URL doğrulama

- [ ] `https://saevaexe.github.io/ceyizim-web/` → 200, landing yüklendi
- [ ] `https://saevaexe.github.io/ceyizim-web/privacy.html` → 200
- [ ] `https://saevaexe.github.io/ceyizim-web/privacy-en.html` → 200
- [ ] `https://saevaexe.github.io/ceyizim-web/support.html` → 200
- [ ] `https://saevaexe.github.io/ceyizim-web/support-en.html` → 200
- [ ] `https://saevaexe.github.io/ceyizim-web/terms.html` → 200
- [ ] `https://saevaexe.github.io/ceyizim-web/.well-known/apple-app-site-association` → 200, **Content-Type: application/json** dönmeli (GitHub Pages otomatik veriyor)
- [ ] AASA validator: https://branch.io/resources/aasa-validator/

> **AASA notu:** Apple cache'ler — değişiklik sonrası `swcutil_show` veya cihaz reset gerekebilir. TestFlight'ta ilk kurulumda fresh fetch olur.

## Eksikler (post-deploy doldur)

- [ ] `assets/favicon.png` — 32x32 logo
- [ ] `assets/appstore-tr.svg` — App Store badge (Türkçe)
- [ ] `assets/appstore-en.svg` — App Store badge (English)
- [ ] `assets/shot-1..4.png` — TR screenshot küçük versiyonları
- [ ] `assets/shot-1..4-en.png` — EN screenshot küçük versiyonları
- [ ] `index.html` ve `index-en.html` içindeki `id0000000000` → ASC'den gelecek gerçek App Store ID ile değiştir

## Bağımlı dokümanlar

- App Store metadata: `çeyiz/docs/aso/appstore-metadata.md`
- ASC submit checklist: `çeyiz/docs/aso/asc-checklist.md`
