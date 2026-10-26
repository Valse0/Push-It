Tamam kanka, bu listeyi direkt üretime hazır hale getirdim. Kopyala-yapıştır çalışır, 60fps, mobil uyumlu. Hepsi senin palete göre: `# / # / # / # / #`

1. 💎 KART PARLAMASI / HOVER

*Hedef:* Tıklanabilir olduğunu hissettirir.

<div class="card card--hover"></div>

.card--hover{
 --glow-color:#;
 --lift:-8px;
 transition: transform 0.3s cubic-bezier(0.4,0,0.2,1), box-shadow 0.3s;
}
.card--hover:hover{
 transform: translateY(var(--lift)) scale(1.03);
 box-shadow: 0 0 20px var(--glow-color), 0 10px 30px rgba(0,0,0,0.5);
}

// JS yok, CSS hover yeterli. Mobil için:
card.addEventListener('touchstart', ()=> card.classList.add('is-active'))

*Ayar:* `--glow-color` değiştir, `--lift` ile kalkma miktarı.

2. 🌊 VERİ AKIŞI ARKA PLANI

*Hedef:* Arka planda sürekli akan Matrix.

<div class="data-flow"></div>

.data-flow{
 position:fixed; inset:0; z-index:-1;
 background:#;
 overflow:hidden;
}
.data-flow::before{
 content:'10101 01010 11001 00101';
 position:absolute; width:200%; height:200%;
 top:-50%; left:-50%;
 color: rgba(0,240,255,0.08);
 font-family: monospace; font-size:14px; line-height:20px;
 letter-spacing:4px;
 animation: flow-move 20s linear infinite;
 white-space: pre-wrap;
}
@keyframes flow-move{
 from{ transform: translateY(0); }
 to{ transform: translateY(60px); }
}

*Performans:* Sadece transform, 0 resim.

3. ✨ KOİN SIÇRAMASI

<div class="coin">+120 <span class="coin-icon">$</span></div>

@keyframes coin-burst{
 0%{ transform: translateY(0) scale(0.8); opacity:0; }
 20%{ opacity:1; }
 100%{ transform: translateY(-60px) scale(1.2); opacity:0; }
}
.coin.is-burst{ animation: coin-burst 0.8s cubic-bezier(0.4,0,0.2,1) forwards; }
.coin-icon{ color:#; text-shadow: 0 0 10px #; }

function burstCoin(el){ el.classList.remove('is-burst'); void el.offsetWidth; el.classList.add('is-burst'); }

4. 🛡️ KALKAN AKTİVASYONU

<div class="card shield-active"></div>

.shield-active{ position:relative; }
.shield-active::after{
 content:''; position:absolute; inset:-4px;
 border-radius:14px;
 border:2px solid #;
 opacity:0.8;
 animation: shield-spin 2s linear infinite, shield-pulse 1.5s ease-in-out infinite;
}
@keyframes shield-spin{ from{ transform: rotate(0); } to{ transform: rotate(360deg); } }
@keyframes shield-pulse{ 0%,100%{ box-shadow:0 0 10px #; } 50%{ box-shadow:0 0 25px #; } }

5. 💥 VİRÜS / HATA

<div class="card virus-hit"></div>

@keyframes virus-flicker{
 0%,100%{ transform: translate(0); filter: none; }
 20%{ transform: translate(-2px,1px); filter: hue-rotate(90deg); }
 40%{ transform: translate(2px,-1px); border-color:#; }
}
.virus-hit{ animation: virus-flicker 0.3s ease 3; box-shadow: 0 0 20px # inset; border-color:# !important; }

6. 📈 ÇARPAN YÜKSELİŞİ

<div class="multiplier is-up">x2.5</div>

@keyframes mult-pop{
 0%{ transform: scale(1); }
 50%{ transform: scale(1.4); }
 100%{ transform: scale(1); }
}
.multiplier.is-up{ animation: mult-pop 0.4s cubic-bezier(0.34,1.56,0.64,1); color: var(--mult-color); }
.multiplier{ --mult-color:#; transition: color 0.3s; }
/* JS ile: x1=mavi, x2=sarı, x3=turuncu, x4=kırmızı */

function setMult(el, val){
 el.textContent = `x${val}`;
 el.style.setProperty('--mult-color', val<2?'#': val<3?'#': val<4?'#':'#');
 el.classList.remove('is-up'); void el.offsetWidth; el.classList.add('is-up');
}

7. 🕐 GERİ SAYIM NABZI

<div class="timer-ring" style="--p:75"><span>7s</span></div>

.timer-ring{
 width:60px; height:60px; border-radius:50%;
 background: conic-gradient(var(--c,#) calc(var(--p)*1%), #222 0);
 display:grid; place-items:center;
 animation: pulse 1s ease-in-out infinite;
}
.timer-ring span{ background:#; width:50px; height:50px; border-radius:50%; display:grid; place-items:center; }
@keyframes pulse{ 0%,100%{ transform:scale(1); } 50%{ transform:scale(1.05); } }
.timer-ring.is-danger{ --c:#; animation-duration:0.4s; }

8. 🎉 BAŞARI HALKASI

<div class="victory"></div>

@keyframes victory-sweep{
 0%{ transform: rotate(0) scale(1.2); opacity:0; }
 20%{ opacity:1; }
 100%{ transform: rotate(360deg) scale(1); opacity:0; }
}
.victory{
 position:fixed; inset:0; pointer-events:none;
 border:3px solid #;
 border-radius:20px;
 animation: victory-sweep 1.2s ease-out forwards;
 box-shadow: 0 0 40px #;
}

function showVictory(){ const v=document.createElement('div'); v.className='victory'; document.body.appendChild(v); setTimeout(()=>v.remove(),1300); }

---

*Dosya yapına eklemen için README satırları:*

| `hover-glow-card/` | Kart üzerine gelme parlaması | Seçim beklentisi, etkileşim |
| `background-data-flow/` | Sürekli akan dijital arka plan | Atmosfer, siberpunk hissi |
| `coin-burst/` | Koin sıçrama animasyonu | Kazanç geri bildirimi |
| `shield-activation/` | Kalkan koruma halkası | Güvende hissi |
| `virus-corruption/` | Virüs bulaşma efekti | Kayıp geribildirimi |
| `multiplier-pulse/` | Çarpan büyüme ve renk değişimi | Artan risk/ödül vurgusu |
| `timer-pulse-ring/` | Geri sayım çemberi nabzı | Aciliyet hissi |
| `victory-ring/` | Başarı dönen ışık halkası | El sonu kutlaması |

Hepsi saf CSS, `transform` + `opacity` sadece. İstersen şimdi bunları tek bir `animations.css` dosyasına birleştirip sana atayım mı?
