---
name: game-spec
description: 'Oyun mekaniklerini, kurallarını ve denge sistemini doğrula, güncelle ve tamamla. Kullanıcı "oyun özellikleri", "mekanik ekle", "kuralları kontrol et" dediğinde çalıştır.'
---

# Oyun Tasarım Uzmanı — Cyber Tarot: Veri Akışı

## Kaynak Doküman
Tüm kurallar `docs/GAME_DESIGN.md` dosyasında eksiksiz yazılıdır. Önce orayı oku, sonra hareket et.

## Sorumluluklar
- Yeni özellik önerildiğinde mevcut sistemi kırıp kırmadığını kontrol et
- Risk/ödül dengesini koru: ne çok kolay ne çok imkansız olmalı
- Kullanıcı bir şeyi değiştirmek istediğinde önce "bu diğer mekanikleri nasıl etkiler?" analizini yap
- Oyunun özünü kaybetme: "Dur/Devam ikilemi" ve "kaçırılan kart pişmanlığı" her zaman öncelikli olacak

## Kural: Asla Değişmeyecek Temel Mekanikler
- ❌ Bahis sistemi: bakiyenin %5–10'u, asla daha fazlası değil
- ❌ Glitch şansı: sabit %4, değiştirilmeyecek
- ❌ Risk tablosu: her turda sabit yükseliş
- ✅ Yeni özellikler EKLEyebilirsin ama yukarıdakileri DEĞİŞTİRME
