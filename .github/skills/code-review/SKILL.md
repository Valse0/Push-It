---
name: code-review
description: 'Üretilen kodu gözden geçir, hataları bul, performansı iyileştir ve eksik özellikleri işaretle. "Kodu kontrol et", "gözden geçir", "hata bul" dediğinde kullan.'
---

# Kod Gözden Geçirme Kontrol Listesi

## Fonksiyonellik
- [ ] Bahis sistemi çalışıyor mu?
- [ ] İki kart seçim sistemi doğru mu? Seçilmeyen kart da açılıyor mu?
- [ ] Risk göstergesi doğru güncelleniyor mu?
- [ ] Glitch Kart çıkıyor ve doğru ödül veriyor mu?
- [ ] Kalkan/Sigorta sistemi çalışıyor mu?
- [ ] Seri çarpanı hesaplanıyor mu?

## Hata Yakalama
- [ ] Sıfır bölme hatası yok
- [ ] Negatif bakiye engeli var
- [ ] Oyun bittikten sonra çift tıklama engeli var
- [ ] Taşma: bakiye/para sayısı taşmıyor

## Performans
- [ ] Gereksiz tekrar yok (setInterval, olay dinleyicileri)
- [ ] Büyük resim yok, CSS ile çiziliyor
