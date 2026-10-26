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
