---

## 📄 Örnek Şablon 2 — Glitch Efekti: `assets/animations/glitch-effect/README.md`

```markdown
# ⚡ Glitch Efekti
> Neon bozulma, ekran titremesi — Glitch Kart yakalandığında tetiklenir

## CSS KODU
```css
/* ==============================================
   ANİMASYON: Glitch Patlaması
   Tetikleme: .glitch-burst sınıfı ekle/çıkar
============================================== */

@keyframes glitch-skew {
  0% { transform: skew(0deg); }
  20% { transform: skew(-3deg); }
  40% { transform: skew(3deg); }
  60% { transform: skew(-1deg); }
  80% { transform: skew(1deg); }
  100% { transform: skew(0deg); }
}

@keyframes glitch-flash {
  0%, 100% { opacity: 1; }
  50% { opacity: 0.8; }
}

@keyframes glitch-shift {
  0% { clip-path: inset(0 0 0 0); }
  20% { clip-path: inset(20% 0 60% 0); }
  40% { clip-path: inset(40% 0 40% 0); }
  60% { clip-path: inset(60% 0 20% 0); }
  80% { clip-path: inset(80% 0 0 0); }
  100% { clip-path: inset(0 0 0 0); }
}

.glitch-burst {
  animation: glitch-skew 0.8s ease-in-out,
             glitch-flash 0.1s ease-in-out 4,
             glitch-shift 0.6s ease-in-out;
  position: relative;
}

.glitch-burst::before,
.glitch-burst::after {
  content: '';
  position: absolute;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: inherit;
}

.glitch-burst::before {
  left: 2px;
  filter: hue-rotate(60deg) brightness(1.2);
  animation: glitch-shift 0.4s ease-in-out reverse;
  opacity: 0.5;
}

.glitch-burst::after {
  left: -2px;
  filter: hue-rotate(-60deg) brightness(1.2);
  animation: glitch-shift 0.5s ease-in-out;
  opacity: 0.5;
}
