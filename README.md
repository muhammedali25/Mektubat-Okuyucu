# Mektûbât Okuyucu

İmâm-ı Rabbânî'nin Mektûbât'ı: Farsça aslı, Arapça tercümesi ve iki Türkçe tercümesiyle yan
yana, cümle cümle eşleştirilmiş olarak. Tarayıcıda çalışır, sunucusu yoktur. Metne yorum
katmaz; eşleştirir, sayar ve gösterir.

**Aç:** https://muhammedali25.github.io/Mektubat-Okuyucu/

iPhone ve iPad'de Safari ile açın; sayfa ana ekrana nasıl ekleneceğini kendisi gösterir.
Eklendikten sonra uygulama gibi açılır ve internetsiz çalışır (iOS 16.4 ve sonrası).

**Android:** [Mektubat.apk dosyasını indirin](https://github.com/muhammedali25/Mektubat-Okuyucu/releases/latest/download/Mektubat.apk)
ve açın. Her gönderimde `Android APK` iş akışı dosyayı yeniden derleyip yayımlar.

## İçinde ne var

- **Nâmehâne:** 536 mektubun alıcıları bir yazışma ağı olarak; kişiye göre mektup dizisi.
- **Mektuplar:** dört metin yan yana; bir cümleye dokununca öteki dillerdeki karşılığı yanar.
  Altını çizme, not, cümle kartı, murâkabe okuması, Akçiçek ↔ Hakikat karşılaştırması.
- **Atlas / Seyr / Tayf:** tasavvuf terimlerinin mektuplara dağılımı, makam daireleri,
  tercümelerin bir kavramı nasıl karşıladığı.
- **Kur'ân:** Farsça metindeki 788 âyet atfının sûrelere göre haritası.
- **Divan:** Akçiçek tercümesindeki 291 beyit, okunuş ve mealleriyle.

## Derleme

```bash
python3 build/derle.py     # dist/Mektubat.html (tek dosya), dist/web/ (web yayını), dist/assets/ (APK içeriği)
build/apk.sh               # dist/Mektubat.apk  (ANDROID_HOME ve JDK gerekir)
```

Yayın, `dist/web/` içeriğinin `gh-pages` dalına konmasıyla yapılır. `android/` klasörü, gömülü
sayfayı bir WebView içinde gösteren tek ekranlı uygulamadır; paylaşma, sesli okuma ve iki ana
ekran bileşeni içerir, hiçbir izin istemez. Veriyi üreten betikler ve sınamalar
`veri-araclari/` klasöründe, sonuçları `TEST-RAPORU.md` dosyasındadır.

APK imzası: depoya `MEKTUBAT_ANAHTAR_B64` (anahtar deposunun base64'ü) ve
`MEKTUBAT_ANAHTAR_PAROLA` gizli değerleri eklenirse iş akışı onlarla imzalar. Eklenmezse her
derlemede geçici bir anahtar üretilir ve yeni sürüm eskisinin üstüne kurulamaz (önce eskisi
kaldırılır).

## Kaynaklar ve haklar

| Katman | Kaynak |
|---|---|
| Farsça asıl metin | *Mektûbât-ı İmâm-ı Rabbânî*, tahkik: Nur Ahmed Amritsarî, Amritsar 1908–1915. Şamile için hazırlayan: Mücahid Sagir Ahmed (archive.org). |
| Arapça tercüme | *ed-Dürerü'l-meknûnâtü'n-nefîse*, Muhammed Murad el-Menzelevî (ö. 1934), Mektebetü'n-Nîl, Kahire. Şamile metni (archive.org). |
| Türkçe tercümeler | Abdülkadir Akçiçek tercümesi (534 mektup) ve Hakikat Kitabevi tercümesi (313 mektup), Dr. Necati Aksu'nun düzenlediği necatiaksu.net/mektubat sayfalarından. |
| Kelime açıklamaları | Bu uygulama için yazıldı; bir sözlükten alınmadı. |

Türkçe tercümelerin hakları mütercimlerine ve yayıncılarına aittir; telif süreleri dolmamıştır.
Bu depo ticari amaç taşımaz. Hak sahibi talep ederse ilgili metin kaldırılır.
