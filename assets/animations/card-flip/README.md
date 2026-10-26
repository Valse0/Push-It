# 🃏 Kart Çevirme Animasyonu
> 3D dönme efekti — kart kapalıyken önde, açıldığında arkaya döner

## CSS KODU — Kopyala & Kullan
```css
/* ==============================================
   ANİMASYON: Kart Çevirme
   Sınıflar: .flip-card | .flip-card-inner | .is-flipped
============================================== */

.flip-card {
  perspective: 1000px;
  width: 160px;
  height: 220px;
  cursor: pointer;
}

.flip-card-inner {
  position: relative;
  width: 100%;
  height: 100%;
  transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
  transform-style: preserve-3d;
}

.flip-card.is-flipped .flip-card-inner {
  transform: rotateY(180deg);
}

.flip-card-front,
.flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
  border-radius: 12px;
  overflow: hidden;
  /* 1'den gelen neon hava */
  border: 2px solid #00f0ff;
  box-shadow: 0 0 15px rgba(0, 240, 255, 0.3);
}

.flip-card-back {
  background-color: #0d0d1a;
  transform: rotateY(180deg);
}
