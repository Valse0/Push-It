# CYBER TAROT: VERİ AKIŞI — Agent Talimatları

## 🎯 Proje Özeti
Siberpunk/Tarot temalı, Push-Your-Luck tarzı bir kart oyunu. Tek dosya HTML/CSS/JS olarak çalışacak, dış bağımlılıksız, mobil uyumlu olacak. Gerçek para içermez, sadece oyun içi koin sistemi.

## 🛠️ Teknik Kısıtlamalar
- Tek HTML dosyası içinde her şey çalışacak — dış kütüphane YOK
- Sadece saf HTML5, CSS3 ve Vanilla JavaScript kullanılacak
- Mobil öncelikli tasarım, responsive
- Performans: 60fps animasyonlar, hafif çalışacak
- Hiçbir dış API çağrısı olmayacak

## 📌 Dosya Sorumlulukları
- `project/index.html.template` → Ana yapı, arayüz elemanları
- `project/styles.css.template` → Görsel tasarım, animasyonlar, renkler
- `project/app.js.template` → Oyun mantığı, durum yönetimi, kart sistemi

## ⚡ Kullanılacak Renk Paleti
- Neon Mavi: `#00f0ff`
- Neon Mor: `#b000ff`
- Parlak Yeşil: `#00ff90`
- Koyu Arka Plan: `#08080c`
- Kırmızı Uyarı: `#ff2060`

## 🚫 YASAKLAR
- Dış CSS/JS kütüphaneleri kullanmak (Bootstrap, jQuery vb.)
- Gerçek para, ödeme sistemi eklemek
- Kullanıcı verisi toplamak, harici sunucuya veri göndermek
- Oyun mekaniklerini değiştirmek — GAME_DESIGN.md'deki her şey aynen uygulanacak

## ✅ Doğrulama Kontrol Listesi
- [ ] Tek dosya olarak tarayıcıda sorunsuz açılıyor
- [ ] Mobilde tüm butonlar tıklanabilir
- [ ] Hiçbir harici bağlantı yok
- [ ] Tüm oyun özellikleri çalışıyor
- [ ] Renkler ve temalar tanımlandığı gibi
