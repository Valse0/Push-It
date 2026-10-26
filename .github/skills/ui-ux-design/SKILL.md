---

## 🎨 Skill 3: ui-ux-design — Görsel Tasarım Uzmanı

`.github/skills/ui-ux-design/SKILL.md`

```yaml
---
name: ui-ux-design
description: 'Siberpunk temalı arayüz, animasyonlar, glitch efektleri ve renkler üret. "Tasarım yap", "görseli iyileştir", "animasyon ekle" dediğinde kullan.'
---

# UI/UX Tasarım Rehberi

## Renk Paleti (Kesinlikle Aynen Kullan)
```css
:root {
  --bg-main: #08080c;
  --neon-blue: #00f0ff;
  --neon-purple: #b000ff;
  --neon-green: #00ff90;
  --danger: #ff2060;
  --text-primary: #e0e0e0;
  --text-dim: #888888;
}

Kart Stili

• 3D görünüm: perspective + transform-style: preserve-3d

• Hover: hafif yukarı kalkma + parlaklık

• Açılma animasyonu: 0.6s dönme + solma

Glitch Efekti

• Sadece Glitch Kart çıktığında tetiklenir

• 0.8s süreyle ekran titrer, renkler kayar

• Sonra yavaşça normale dön

Prensip

• Minimalizm: çok az yazı, çok görsel

• Okunabilirlik her zaman öncelikli

• Hareketli arka plan yazıların okunmasını engellemesin
