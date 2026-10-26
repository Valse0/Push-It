# OYUN TANIMI: CYBER TAROT — VERİ AKIŞI
## Genel Konsept
Siberpunk/Tarot temalı, şansa dayalı ama karar mekanikleriyle derinlik kazanan bir "Push-Your-Luck" (çekil/devam et) kart oyunu. Tek el 30–90 saniye sürer; temel soru her zaman: "Şu an durup cebimdekini mi alayım, yoksa bir kart daha çekip her şeyi riske atayım mı?" Gerçek para içermez; sadece oyun içi koin ve deneyim odaklıdır.

## Görsel & Estetik Tanımı
- Tema: Siberpunk / Dark Hacker / Dijital Tarot
- Arka plan: Derin siyah, koyu gri tonlar; yukarı doğru yavaşça akan yeşil/mavi dijital harfler (Matrix tarzı)
- Ana renkler: Neon mavi (#00f0ff), Neon mor (#b000ff), Parlak yeşil (#00ff90), Koyu Siyah (#08080c)
- Kart tasarımı: Parlayan neon çerçeveli, ortasında şifreli siber semboller bulunan kapalı kartlar; açılınca 3D dönme animasyonu
- Glitch efekti: Ekran titrer, renkler ters döner, parazit sesi, beyaz parlamalar
- Arayüz: Minimal, temiz, büyük yazılar, gereksiz detay yok; tüm odak kartlarda ve risk göstergesinde

---

## ÇEKİRDEK OYUN AKIŞI
1. **Başla & Bahis:** Oyuncu elindeki bakiyeden %5–10 arası miktarı "Veri Girişi" olarak yatırır. Minimum: 10 koin.
2. **Seçim:** Ekranda iki adet kapalı kart belirir: ← SOL | SAĞ →
3. **Seç & Gör:** Oyuncu bir kart seçer → seçtiği 3D animasyonla açılır → sonucu görür → SONRA seçmediği kart da açılır, içinde ne olduğu gösterilir.
4. **Karar:** Ekranda soru çıkar: "🔻 AKIŞI DURDUR & ÇEK  —  BİR KART DAHA ÇEK  🔺"
   - DUR: Biriktirilen pot kazanılır, el biter, bakiye güncellenir
   - DEVAM: Yeni ikili kart gelir, risk artar, çarpan yükselir
5. **Tekrarla:** Oyuncu durana veya Virüs yiyene kadar 2–4 adımları tekrarlar.

---

## KART TÜRLERİ
| Kart | Açıklama |
|------|----------|
| 💎 Veri Koini | 10–100 arası rastgele değer × geçerli çarpan pota eklenir |
| ⚡ Glitch Kart | %4 şans; değer × çarpan × 10; ekran glitch efektiyle patlar, özel ses efekti |
| 💣 Virüs | El biter; yatırılan bahis + o elde biriktirilen tüm miktar kaybedilir; eğer Kalkan varsa kırılır, el devam eder |
| 🛡️ Güvenlik Duvarı | Biriktirilen kazancın %25'i feda edilerek satın alınabilir; 1 kez Virüsü engeller; aynı anda sadece 1 adet taşınabilir |

---

## RİSK & ÇARPAN SİSTEMİ
| Tur Sırası | Virüs Riski | Çarpan | Risk Göstergesi Rengi |
|------------|-------------|--------|----------------------|
| 1 | %10 | ×1,0 | 🟢 Yeşil |
| 2 | %18 | ×1,3 | 🟢 Yeşil |
| 3 | %30 | ×1,6 | 🟡 Sarı |
| 4 | %45 | ×2,0 | 🟠 Turuncu |
| 5 | %62 | ×2,8 | 🔴 Kırmızı |
| 6 | %78 | ×4,0 | 🔴 Kırmızı |

- Risk göstergesi sol köşede sürekli görünür: "🛡️ Sızma Riski: %XX"
- Her turda risk otomatik yükselir

---

## EKSTRA OYNANIŞ ÖZELLİKLERİ (HEPSİ DAHİL)

### 🔄 1. Son Saniye Düzeltme
- Kart açılırken son anda küçük buton belirir: "🔄 FİKRİMİ DEĞİŞTİR (Kalan: 1)"
- Tıklanırsa diğer kartla yer değiştirir
- Her elde sadece 1 kez kullanılabilir

### 🔍 2. Veri Sızıntısı — Gizli İpuçları
- Bazen iki kartın altında ipucu belirir (örn: "Sağ kart daha güvenli görünüyor...")
- İpuçları %65 doğruluk oranlıdır; her zaman doğru değil

### 🎭 3. Görüntü Aldatmacası
- Bazen bir kart daha parlak/çerçeveli görünebilir
- Görünüş içeriği yansıtmak zorunda değildir — gösterişli olandan Virüs, sade olandan Glitch çıkabilir

### ⏱️ 4. Panik Zamanlayıcısı
- %8 şansla seçim ekranında 10 saniyelik geri sayım başlar
- Süre biterse otomatik olarak güvenli çıkış yapılır

### 🔥 5. Seri Çarpanı
- Aynı taraftan art arda seçim:
  - 3 kez: +%20 ekstra kazanç
  - 4 kez: ×2,0 çarpan
  - 5+ kez: ×3,0 çarpan
- Seri kırılırsa sıfırlanır

### 🎲 6. İkiye Katla Seçeneği
- "DUR" seçeneğiyle birlikte görünür:
  - ✅ GÜVENLİ ÇEK: Kazanç alınır
  - ⚠️ İKİYE KATLA (%50): Kazanılırsa ×2; kaybedersen bahsin %50'si geri gelir

### ⚡ 7. Çifti Al — Özel Fırsat
- Çok nadir her iki kart da değerli olduğunda seçenek çıkar:
  - ✅ Her ikisini de al
  - ⚠️ Bir sonraki tur riski +%50 artar

### 📋 8. El Özeti — Sonuç Ekranı
- El bittiğinde gösterilir:
  - Doğru seçim oranı: %XX
  - Kaçırılan en büyük kazanç: +XXX koin
  - En iyi/en kötü seçim analizleri
  - O el son bakiye durumu

---

## OYUN BAŞI YETENEKLERİ
Her el başında 3 rastgele seçenekten 1 tanesi aktif olur:
- 🛡️ Güvenli Başlangıç: İlk Virüs hasarı olmaz
- 💎 Değer Akışı: Tüm koin değerleri +%25
- ⚡ Glitch Yolu: Glitch şansı %4 → %7
- 🔍 Net İpucu: İpucu doğruluğu %65 → %80
- ⏱️ Sakin Akış: Bu elde Panik Zamanlayıcısı çıkmaz

---

## KALICILIK & İLERLEME
### 📅 Günlük Giriş
- Her gün ilk girişte ücretsiz Şans Çarkı çevirme hakkı
- Örnek ödüller: ekstra kalkan, başlangıç koini, ilave düzeltme hakkı
- Günlük görevler: 3 el oyna, 1 Glitch yakala, 500 koin topla → küçük bonuslar

### 🏆 Koleksiyon & Kilit Açma
- Koinlerle satın alınabilenler:
  - 🎨 Arka planlar: Neon Şehir, Derin Ağ, Uzay İstasyonu, Kırmızı Alarm
  - 🃏 Kart görünümleri: Holografik, Mat Siyah, Altın Çerçeve, Glitch
  - 📈 Başarımlar: En yüksek seri, en büyük Glitch, toplam kazanç istatistikleri

---

## DENGE & KORUMA KURALLARI
- Tek el bahsi: bakiyenin maksimum %10'u
- İkiye Katla'da tam kayıp yok; en az %50 geri ödenir
- Düzeltme hakkı: maksimum 1/el
- İpuçları: asla %100 doğru değil
- Zaman aşımı: otomatik güvenli çıkış, ceza yok
- Oyun tamamen şansa dayalıdır; adil, hile yok; gerçek para içermez
- Başlangıç bakiyesi: 1.000 koin; kaybedenler için yedekleme sistemi: günde 1 kez ücretsiz 500 koin

---

## OYUNUN AMACI & HİSSELER
Oyunun temel gücü şu duygularda yatar:
- Seçim yapma sorumluluğu → "Hangisini seçmeliyim?"
- Kaçırdığını görme → "Keşke diğerini seçseydim!"
- Duramama hissi → "Bir tane daha, kesin bu gelecek!"
- Glitch anı → Beklenmedik büyük ödül ve görsel şölen
- Güvenlik hissi → Kalkanla risk alabilme cesareti

Oyun karmaşık değil, basit ama her kararın ağırlığı var. Hızlı oyna, hızlı karar ver, durmasını bil.
