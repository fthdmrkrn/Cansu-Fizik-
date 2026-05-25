# 📱 Cansu Hoca ile InstaFizik

Instagram tarzında, kaydırmalı carousel'lar ile öğrenme deneyimi sunan eğitim aracı. 11. Sınıf Fizik dersi için.

## 🗂️ Klasör Yapısı

```
instafizik/
├── index.html              ← Ana dosya (tarayıcıda aç)
├── content/
│   └── data.json           ← Tüm içerik buradan okunuyor (DÜZENLENEBİLİR)
├── images/                 ← Görseller buraya
│   ├── profile/
│   │   └── avatar.jpg
│   ├── stories/
│   ├── topics/
│   ├── posts/
│   │   ├── aa-1/           ← Post 1 görselleri
│   │   ├── aa-2/
│   │   └── ...
│   └── reels/
└── videos/
    └── reels/              ← Reels videoları buraya
```

## 🚀 Nasıl Çalıştırılır?

**ÖNEMLİ:** Dosya `file://` olarak değil, bir web sunucusu üzerinden açılmalı (çünkü JSON dosyasını fetch ediyor).

### Kolay yol (VSCode):
1. VSCode'da klasörü aç
2. "Live Server" eklentisini kur
3. `index.html` üzerine sağ tıkla → "Open with Live Server"

### Alternatif (Python varsa):
```bash
cd instafizik
python -m http.server 8000
# Sonra tarayıcıda: http://localhost:8000
```

## ✏️ İçeriği Düzenleme

Tüm metinler, sorular, slaytlar `content/data.json` dosyasında. Yeni post eklemek veya mevcut olanı değiştirmek için sadece bu dosyayı düzenle.

### Slayt tipleri:
- `cover` - Kapak (başlık + emoji)
- `content` - Madde listesi
- `comparison` - İki sütunlu karşılaştırma
- `story` - Hikaye anlatımı
- `quote` - Alıntı/önemli not
- `question` - Düşündürücü soru
- `tableData` - Tablo

## 📸 Görsel/Video Ekleme

JSON'da görsel yolları yazılı (örn: `images/posts/aa-1/cover.jpg`). Sen sadece o yola dosyayı koy, otomatik gözükecek.

Şu an placeholder gradient'ler kullanılıyor. Görseller geldiğinde HTML'de küçük bir güncelleme yapacağız (slaytların arka planına resim binecek).

## 🎨 Özellikler

- ✅ Instagram tarzı Feed (carousel post'lar)
- ✅ Hikaye şeridi (üst kısım)
- ✅ Keşfet sayfası (konu menüsü)
- ✅ Reels (video desteği)
- ✅ Bildirimler
- ✅ Profil sayfası (grid görünüm)
- ✅ Karanlık / Aydınlık mod (üst sağda buton)
- ✅ Kaydırma (touch + mouse)
- ✅ Çift tıklayarak beğeni
- ✅ Beğeni animasyonu

## 👨‍🏫 Derste Kullanım

- **Projeksiyonda:** Öğretmen ana sayfadan post'ları gösterir, sınıfla birlikte slaytları kaydırarak ilerler.
- **Telefonda:** Öğrenciler kendi cihazlarından erişip kendi hızlarında öğrenirler.
- **Soru slaytlarında:** Tartışma açılır, öğrenciler cevapları söyler.
