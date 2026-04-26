# Assets — eksik dosyalar (post-deploy doldur)

Bu klasör web sayfalarının ihtiyaç duyduğu varlıkları içerir. Lansman öncesi şunları ekle:

| Dosya | İçerik | Kaynak |
|---|---|---|
| `favicon.png` | 32×32 Çeyizim logo, soft pink bg | `çeyiz/Assets.xcassets/AppIcon.appiconset` küçültülmüş |
| `appstore-tr.svg` | Apple App Store TR badge | https://developer.apple.com/app-store/marketing/guidelines/#downloaded |
| `appstore-en.svg` | Apple App Store EN badge | aynı |
| `shot-1.png` … `shot-4.png` | TR ekran görüntüleri 320×694 (web küçük) | `çeyiz/docs/screenshots/` PNG'lerinden Preview ile resize |
| `shot-1-en.png` … `shot-4-en.png` | EN ekran görüntüleri | aynı |

Apple App Store badge'lerini sadece Apple sağlanan SVG/PNG'lerden kullan — Apple Identity Guidelines kuralı.
