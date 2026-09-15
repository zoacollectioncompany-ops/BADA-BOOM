# BadaBoom Techno Club — Website

Tek dosyalık (single-file) web sitesi. Tüm kod, görseller ve stiller `index.html` içinde — ayrı bir resim/CSS dosyası yok, bu yüzden GitHub Pages'e yüklemesi çok basit.

## 🚀 Yayınlama (GitHub Pages)

1. Bu repoyu GitHub'a yükle (`index.html` ve `README.md` repo'nun **kök dizininde** olmalı).
2. Repo → **Settings → Pages**.
3. **Source** kısmından `Deploy from a branch` seç.
4. **Branch**: `main`, klasör: `/ (root)` seç → **Save**.
5. 1-2 dakika içinde siten şu adreste yayına girer:
   `https://KULLANICI_ADIN.github.io/REPO_ADI/`

Her `index.html` güncellemesinde GitHub Pages siteyi otomatik yeniden yayınlar, ekstra bir işlem yapmana gerek yok.

## 📅 Upcoming Events'i güncelleme

`index.html` içinde `const EVENTS = [` satırını ara. Etkinlik eklemek için listeye yeni bir blok ekle:

```js
{
  day: "Sat, 18 Oct",
  time: "23:00",
  name: "Etkinlik Adı",
  tags: ["Techno", "Presale"],
  doors: "Doors 23:00 — 05:00"
}
```

Liste boşsa (`const EVENTS = [];`) sayfa otomatik olarak **"Coming Soon"** gösterir.

## ✏️ Sık değiştirilecek diğer yerler

| Ne | Nerede ara |
|---|---|
| Adres / konum | `id="location"` bölümü |
| House Rules maddeleri | `class="rule"` satırları |
| Instagram / sosyal medya linkleri | `footer-social` içindeki `href="#"` |
| Sayfa başlığı (tarayıcı sekmesi) | `<title>` etiketi (en üstte) |

## 🖼️ Görseller

Logo, hero fotoğrafı ve favicon dosyanın içine **base64** olarak gömülü — yani ayrı bir `images/` klasörüne gerek yok, tek dosya taşınabilir. Görseli değiştirmek istersen bana yeni görseli gönder, ben tekrar gömüp sana güncel dosyayı veririm.

## 📌 GitHub için başka ne gerekiyor / önerilir

- **Repo adı**: Kısa ve URL-dostu bir isim seç (ör. `badaboom-chiangmai`) — GitHub Pages linkine yansıyacak.
- **Sosyal medya önizlemesi (Open Graph)**: `index.html`'de `<meta property="og:image" content="REPLACE_WITH_LIVE_IMAGE_URL.jpg">` satırı var. Bu, birisi linki Instagram/WhatsApp/Facebook'ta paylaştığında çıkan önizleme görseli için. **Site yayına girdikten sonra** repo'ya küçük bir `og-image.jpg` (1200×630px önerilir) ekleyip bu satırı şu şekilde güncellemen gerekiyor:
  `https://KULLANICI_ADIN.github.io/REPO_ADI/og-image.jpg`
  (Base64 gömülü görseller bu alanda çalışmıyor, Instagram/Facebook gerçek bir link istiyor.)
- **Özel alan adı (opsiyonel)**: `badaboomchiangmai.com` gibi bir domain alırsan, Settings → Pages → Custom domain kısmına ekleyip DNS'te bir CNAME kaydı oluşturman yeterli.
- **HTTPS**: GitHub Pages otomatik sağlıyor, ekstra bir şey yapmana gerek yok.
- **Analytics (opsiyonel)**: Kaç kişi siteye giriyor görmek istersen basit bir Plausible/Google Analytics kodu ekleyebilirim — istersen söyle.

## 🛠️ Yerelde test etme

`index.html` dosyasına çift tıklayıp tarayıcıda açman yeterli — sunucu, kurulum ya da internet gerekmiyor.
