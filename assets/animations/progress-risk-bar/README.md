---

## 📄 Örnek Şablon 3 — Risk Çubuğu: `assets/animations/progress-risk-bar/README.md`

```markdown
# 📊 Risk Çubuğu Animasyonu
> Renk değiştiren, yumuşak geçişli ilerleme çubuğu

## CSS KODU
```css
/* ==============================================
   ANİMASYON: Risk Çubuğu
   Renkler: Yeşil → Sarı → Turuncu → Kırmızı
============================================== */

.risk-bar-container {
  width: 120px;
  height: 8px;
  background: #1a1a24;
  border-radius: 4px;
  overflow: hidden;
}

.risk-bar-fill {
  height: 100%;
  width: 10%; /* JS ile güncelle */
  border-radius: 4px;
  transition: width 0.6s ease, background-color 0.6s ease;
}

/* Renk durumları */
.risk-bar-fill.level-1 { background: #00ff90; box-shadow: 0 0 8px #00ff9040; }
.risk-bar-fill.level-2 { background: #f0e620; box-shadow: 0 0 8px #f0e62040; }
.risk-bar-fill.level-3 { background: #ff9020; box-shadow: 0 0 8px #ff902040; }
.risk-bar-fill.level-4 { background: #ff2060; box-shadow: 0 0 8px #ff206040; }


// Risk değerini güncelle
function updateRiskBar(percent) {
  const bar = document.querySelector('.risk-bar-fill');
  bar.style.width = percent + '%';
  
  // Renk seviyesini belirle
  bar.classList.remove('level-1','level-2','level-3','level-4');
  if (percent <= 30) bar.classList.add('level-1');
  else if (percent <= 50) bar.classList.add('level-2');
  else if (percent <= 70) bar.classList.add('level-3');
  else bar.classList.add('level-4');
}
