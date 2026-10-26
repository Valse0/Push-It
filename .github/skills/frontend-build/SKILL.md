---
name: frontend-build
description: 'Tek dosya HTML/CSS/JS olarak çalışan, dış bağımsızlığı olmayan, mobil uyumlu oyun kodu üret. "Kodu yaz", "uygula", "geliştir" dediğinde kullan.'
---

# Frontend Geliştirme — Kodlama Standartları

## Teknik Kısıtlamalar
- Tek dosya: HTML + `<style>` + `<script>` aynı dosyada
- Sadece saf JavaScript — framework yok
- CSS: CSS değişkenleri kullan, inline stil yazma
- Animasyonlar: CSS transitions/animations, requestAnimationFrame

## Kod Yapısı Kuralı
```javascript
// 1. SABİTLER (en başta)
const RISK_TABLE = [/* ... */];

// 2. DURUM (tek nesne içinde)
const gameState = {
  balance: 1000,
  currentBet: 0,
  // ...
};

// 3. FONKSİYONLAR (gruplandırılmış)
function initGame() {}
function selectCard(side) {}
// ...

// 4. BAŞLATMA
document.addEventListener('DOMContentLoaded', initGame);

Hata Ayıklama

• console.log ile aşırı kalabalık etme

• Hata mesajlarını kullanıcıya göster: showMessage("Hata: ...", "error")

• Değişken adları anlaşılır olsun: remainingRisk → kalanRisk değil, İngilizce kullan

Doğrulama

Kodu yazdıktan sonra şunları kontrol et:

□ Hiç harici <script> veya <link> yok

□ Tüm butonlar çalışıyor

□ Sayfa kaydırılmıyor, taşma yok

□ Mobilde tıklama alanları yeterince büyük (en az 44×44px)
