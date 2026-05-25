<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>ดวงเทพพิทักษ์ ✨ โหราศาสตร์ไทย</title>
<link href="https://fonts.googleapis.com/css2?family=Pixelify+Sans:wght@400;500;600;700&family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════════════════════
   ROOT & RESET
═══════════════════════════════════════════════════════ */
:root {
  --pink:#FFB6D9;--pink2:#FF7EC8;--purple:#C084FC;--purple2:#9333EA;
  --blue:#93C5FD;--blue2:#3B82F6;--yellow:#FDE68A;--yellow2:#F59E0B;
  --gold:#FFD700;--orange:#FDBA74;--green:#86EFAC;--green2:#16A34A;
  --sky:#BAE6FD;--teal:#5EEAD4;--red:#FCA5A5;--red2:#DC2626;
  --bg-deep:#1A0A2E;--bg-mid:#2D1B4E;--bg-card:#3D2460;
  --bg-card2:#4A2E6E;--border:#6B3FA0;--text:#F0E6FF;--text2:#C4A8E0;
  --pixel:2px;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
  font-family:'Sarabun',sans-serif;
  background:var(--bg-deep);
  color:var(--text);
  min-height:100vh;
  overflow-x:hidden;
  cursor:url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='20' height='20'%3E%3Ctext y='16' font-size='16'%3E✨%3C/text%3E%3C/svg%3E"),auto;
}
.pixel-font{font-family:'Pixelify Sans',monospace}

/* ═══════════════════════════════════════════════════════
   PIXEL ART UTILITIES
═══════════════════════════════════════════════════════ */
.pixel-border{
  image-rendering:pixelated;
  box-shadow:
    4px 0 0 var(--border),
    -4px 0 0 var(--border),
    0 4px 0 var(--border),
    0 -4px 0 var(--border),
    4px 4px 0 var(--border),
    -4px -4px 0 var(--border),
    4px -4px 0 var(--border),
    -4px 4px 0 var(--border);
}
.pixel-box{
  border:3px solid;
  image-rendering:pixelated;
  position:relative;
}
.pixel-box::before{
  content:'';position:absolute;
  top:-6px;left:-6px;right:-6px;bottom:-6px;
  border:3px solid rgba(255,255,255,.15);
  pointer-events:none;
}

/* ═══════════════════════════════════════════════════════
   STARFIELD BG
═══════════════════════════════════════════════════════ */
.stars-bg{
  position:fixed;inset:0;z-index:0;overflow:hidden;pointer-events:none;
}
.star{
  position:absolute;background:#fff;
  animation:twinkle 2s infinite alternate;
  image-rendering:pixelated;
}
@keyframes twinkle{
  0%{opacity:.2;transform:scale(1)}
  100%{opacity:1;transform:scale(1.5)}
}
.pixel-cloud{
  position:absolute;
  image-rendering:pixelated;
  animation:floatCloud 20s linear infinite;
  opacity:.5;
}
@keyframes floatCloud{
  0%{transform:translateX(-200px)}
  100%{transform:translateX(calc(100vw + 200px))}
}

/* ═══════════════════════════════════════════════════════
   LAYOUT
═══════════════════════════════════════════════════════ */
.app{position:relative;z-index:1;max-width:480px;margin:0 auto;padding:0 0 120px}

/* ═══════════════════════════════════════════════════════
   HEADER
═══════════════════════════════════════════════════════ */
.header{
  text-align:center;padding:28px 16px 20px;
  background:linear-gradient(180deg,rgba(45,27,78,.98) 0%,transparent 100%);
  position:sticky;top:0;z-index:50;
}
.header-logo{
  font-size:13px;letter-spacing:3px;color:var(--gold);
  text-transform:uppercase;margin-bottom:4px;
  text-shadow:0 0 10px var(--gold);
}
.header-title{
  font-size:26px;font-weight:700;
  background:linear-gradient(135deg,var(--gold),var(--pink2),var(--purple));
  -webkit-background-clip:text;-webkit-text-fill-color:transparent;
  text-shadow:none;line-height:1.2;margin-bottom:2px;
}
.header-sub{font-size:11px;color:var(--text2);letter-spacing:2px}

/* ═══════════════════════════════════════════════════════
   SECTION SYSTEM
═══════════════════════════════════════════════════════ */
.section{
  padding:16px;margin:12px 16px;
  background:var(--bg-card);
  border:3px solid var(--border);
  position:relative;
  display:none;
}
.section.active{display:block}
.section-title{
  font-size:14px;font-weight:700;letter-spacing:2px;
  color:var(--gold);text-transform:uppercase;
  margin-bottom:14px;display:flex;align-items:center;gap:8px;
}
.section-title::after{
  content:'';flex:1;height:2px;
  background:linear-gradient(90deg,var(--gold),transparent);
}

/* ═══════════════════════════════════════════════════════
   STEP 1: BIRTHDAY INPUT
═══════════════════════════════════════════════════════ */
.birth-form{display:flex;flex-direction:column;gap:14px}
.form-row{display:grid;grid-template-columns:1fr 1fr 1fr;gap:8px}
.form-group{display:flex;flex-direction:column;gap:4px}
.form-label{
  font-size:10px;font-weight:700;letter-spacing:1px;
  color:var(--purple);text-transform:uppercase;
}
.pixel-input,.pixel-select{
  background:var(--bg-deep);
  border:3px solid var(--purple2);
  color:var(--text);
  padding:8px 10px;
  font-family:'Pixelify Sans',monospace;
  font-size:14px;
  outline:none;
  transition:border-color .15s,box-shadow .15s;
  -webkit-appearance:none;
  appearance:none;
}
.pixel-input:focus,.pixel-select:focus{
  border-color:var(--gold);
  box-shadow:0 0 12px rgba(255,215,0,.4);
}
.pixel-select option{background:var(--bg-mid)}

/* Pixel character display */
.birth-char{
  display:flex;align-items:center;justify-content:center;
  gap:12px;padding:14px;
  background:var(--bg-deep);border:3px solid var(--purple2);
  min-height:80px;
}
.char-sprite{font-size:40px;animation:float 2s ease-in-out infinite}
@keyframes float{
  0%,100%{transform:translateY(0)}
  50%{transform:translateY(-6px)}
}
.char-info{font-size:12px;color:var(--text2);line-height:1.8}
.char-name{font-size:16px;font-weight:700;color:var(--gold)}

.btn-main{
  background:linear-gradient(135deg,var(--purple2),var(--pink2));
  border:3px solid var(--gold);
  color:#fff;
  padding:14px 24px;
  font-family:'Pixelify Sans',monospace;
  font-size:16px;
  font-weight:700;
  letter-spacing:2px;
  cursor:pointer;
  width:100%;
  transition:all .15s;
  text-transform:uppercase;
  position:relative;
  overflow:hidden;
}
.btn-main::before{
  content:'✨';position:absolute;left:-30px;top:50%;transform:translateY(-50%);
  transition:left .3s;
}
.btn-main:hover::before{left:8px}
.btn-main:hover{
  box-shadow:0 0 20px rgba(147,51,234,.7),0 0 40px rgba(255,126,200,.4);
  transform:translateY(-2px);
}
.btn-main:active{transform:translateY(0)}

/* ═══════════════════════════════════════════════════════
   STEP 2: FORTUNE RESULT
═══════════════════════════════════════════════════════ */
.fortune-header{
  background:var(--bg-deep);border:3px solid var(--gold);
  padding:16px;margin-bottom:14px;text-align:center;
}
.fortune-day-name{
  font-size:22px;font-weight:700;color:var(--gold);
  text-shadow:0 0 15px var(--gold);
}
.fortune-stars{font-size:20px;margin:4px 0}
.fortune-desc{font-size:13px;color:var(--text2);line-height:1.7}

.fortune-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px;margin-bottom:14px}
.fortune-card{
  background:var(--bg-deep);border:3px solid;
  padding:12px 10px;text-align:center;
}
.fortune-card-icon{font-size:22px;margin-bottom:4px}
.fortune-card-label{font-size:9px;color:var(--text2);letter-spacing:1px;text-transform:uppercase}
.fortune-card-val{font-size:13px;font-weight:700;margin-top:2px;line-height:1.3}
.fortune-takfak{
  background:linear-gradient(135deg,rgba(255,215,0,.1),rgba(192,132,252,.1));
  border:3px solid var(--gold);
  padding:14px;margin-bottom:14px;
}
.takfak-title{font-size:12px;letter-spacing:2px;color:var(--gold);margin-bottom:8px;text-transform:uppercase}
.takfak-date{font-size:20px;font-weight:700;color:var(--text)}
.takfak-desc{font-size:12px;color:var(--text2);margin-top:6px;line-height:1.6}

/* ═══════════════════════════════════════════════════════
   STEP 3: CARD DRAW
═══════════════════════════════════════════════════════ */
.cards-instruction{
  text-align:center;font-size:13px;color:var(--text2);margin-bottom:14px;
}
.cards-grid{
  display:grid;grid-template-columns:repeat(5,1fr);gap:6px;margin-bottom:14px;
}
.card-item{
  aspect-ratio:.7;background:var(--bg-deep);
  border:2px solid var(--purple2);
  cursor:pointer;display:flex;flex-direction:column;align-items:center;
  justify-content:center;font-size:18px;position:relative;
  transition:all .15s;
  overflow:hidden;
}
.card-item::before{
  content:'';position:absolute;inset:0;
  background:linear-gradient(135deg,rgba(255,255,255,.05),transparent);
}
.card-item:hover:not(.selected):not(.revealed){
  border-color:var(--gold);
  transform:translateY(-4px);
  box-shadow:0 8px 20px rgba(255,215,0,.3);
}
.card-item.selected{
  border-color:var(--gold);border-width:3px;
  background:linear-gradient(135deg,rgba(255,215,0,.2),rgba(192,132,252,.2));
  animation:pulse 1s infinite;
}
@keyframes pulse{
  0%,100%{box-shadow:0 0 8px rgba(255,215,0,.5)}
  50%{box-shadow:0 0 20px rgba(255,215,0,.9)}
}
.card-item.revealed{
  border-color:var(--teal);
  cursor:default;
}
.card-back{font-size:16px}
.card-num{
  position:absolute;bottom:2px;right:3px;
  font-size:8px;color:var(--text2);font-family:'Pixelify Sans',monospace;
}

.drawn-cards{display:flex;flex-direction:column;gap:10px;margin-top:4px}
.drawn-card{
  background:var(--bg-deep);border:3px solid;
  padding:12px 14px;display:flex;align-items:flex-start;gap:12px;
}
.drawn-icon{font-size:32px;flex-shrink:0}
.drawn-info{flex:1}
.drawn-name{font-size:14px;font-weight:700;margin-bottom:3px}
.drawn-element{font-size:10px;letter-spacing:1px;text-transform:uppercase;margin-bottom:4px;opacity:.7}
.drawn-meaning{font-size:12px;color:var(--text2);line-height:1.6}

/* ═══════════════════════════════════════════════════════
   STEP 4: DEITY PRAYER
═══════════════════════════════════════════════════════ */
.deity-scroller{
  display:flex;gap:12px;overflow-x:auto;padding-bottom:10px;
  scroll-snap-type:x mandatory;
  -webkit-overflow-scrolling:touch;
}
.deity-scroller::-webkit-scrollbar{height:4px}
.deity-scroller::-webkit-scrollbar-track{background:var(--bg-deep)}
.deity-scroller::-webkit-scrollbar-thumb{background:var(--purple2)}

.deity-card{
  min-width:140px;scroll-snap-align:start;
  background:var(--bg-deep);border:3px solid var(--border);
  padding:14px 10px;text-align:center;cursor:pointer;
  transition:all .2s;flex-shrink:0;position:relative;
}
.deity-card:hover,.deity-card.active{
  border-color:var(--gold);
  background:linear-gradient(135deg,rgba(255,215,0,.12),rgba(192,132,252,.08));
}
.deity-card.lit .incense{animation:incenseBurn 1s ease-in-out infinite}
.deity-sprite{font-size:36px;margin-bottom:6px;display:block}
.deity-name{font-size:11px;font-weight:700;color:var(--gold);letter-spacing:1px;margin-bottom:2px}
.deity-domain{font-size:10px;color:var(--text2)}
.incense-indicator{
  position:absolute;top:6px;right:6px;font-size:14px;
  opacity:0;transition:opacity .3s;
}
.deity-card.lit .incense-indicator{opacity:1;animation:smoke .8s infinite}
@keyframes smoke{0%,100%{transform:translateY(0) rotate(0deg)}50%{transform:translateY(-3px) rotate(5deg)}}

.prayer-area{
  background:var(--bg-deep);border:3px solid var(--purple2);
  margin-top:12px;padding:14px;
}
.prayer-deity-name{
  font-size:14px;font-weight:700;color:var(--gold);margin-bottom:8px;
  display:flex;align-items:center;gap:8px;
}
.prayer-textarea{
  width:100%;background:transparent;border:none;
  color:var(--text);font-family:'Sarabun',sans-serif;font-size:13px;
  resize:none;outline:none;line-height:1.7;min-height:80px;
  placeholder-color:var(--text2);
}
.prayer-textarea::placeholder{color:var(--text2);opacity:.6}
.btn-light-incense{
  background:linear-gradient(135deg,#FF4444,#FF8800);
  border:3px solid var(--gold);
  color:#fff;padding:10px 20px;
  font-family:'Pixelify Sans',monospace;font-size:13px;
  font-weight:700;cursor:pointer;letter-spacing:1px;
  transition:all .15s;margin-top:10px;width:100%;
  text-transform:uppercase;
}
.btn-light-incense:hover{
  box-shadow:0 0 20px rgba(255,100,0,.7);transform:translateY(-1px);
}
.incense-count{
  display:flex;gap:4px;margin-top:10px;justify-content:center;
}
.stick{width:4px;height:24px;background:var(--text2);transition:background .3s}
.stick.burning{
  background:linear-gradient(180deg,#ff4444 0%,#ff8800 40%,#666 100%);
  box-shadow:0 0 6px rgba(255,100,0,.6);
}
.prayer-done-list{display:flex;flex-direction:column;gap:8px;margin-top:12px}
.prayer-done-item{
  background:rgba(255,215,0,.08);border:2px solid rgba(255,215,0,.3);
  padding:8px 12px;display:flex;align-items:center;gap:8px;font-size:12px;
}

/* ═══════════════════════════════════════════════════════
   NAV BAR (bottom tabs)
═══════════════════════════════════════════════════════ */
.bottom-nav{
  position:fixed;bottom:0;left:50%;transform:translateX(-50%);
  width:480px;max-width:100%;
  background:var(--bg-mid);border-top:3px solid var(--purple2);
  display:flex;z-index:50;
}
.nav-tab{
  flex:1;display:flex;flex-direction:column;align-items:center;
  padding:8px 0;cursor:pointer;transition:all .15s;gap:2px;
  border-right:2px solid var(--border);
}
.nav-tab:last-child{border-right:none}
.nav-tab:hover,.nav-tab.active{background:rgba(192,132,252,.15)}
.nav-tab.active .nav-icon{filter:drop-shadow(0 0 4px var(--gold))}
.nav-icon{font-size:18px}
.nav-label{font-size:9px;color:var(--text2);letter-spacing:.5px;font-family:'Pixelify Sans',monospace}
.nav-tab.active .nav-label{color:var(--gold)}

/* ═══════════════════════════════════════════════════════
   PIXEL PARTICLES
═══════════════════════════════════════════════════════ */
.particle{
  position:fixed;pointer-events:none;z-index:999;
  font-size:14px;animation:particleFly 1.5s ease-out forwards;
}
@keyframes particleFly{
  0%{opacity:1;transform:translateY(0) scale(1)}
  100%{opacity:0;transform:translateY(-80px) scale(0)}
}

/* ═══════════════════════════════════════════════════════
   MISC DECORATIONS
═══════════════════════════════════════════════════════ */
.sparkle-row{
  display:flex;justify-content:center;gap:8px;
  font-size:16px;margin:10px 0;animation:sparkleAll 2s infinite;
}
@keyframes sparkleAll{
  0%,100%{opacity:.6}50%{opacity:1}
}
.divider{
  height:2px;margin:12px 0;
  background:linear-gradient(90deg,transparent,var(--purple2),transparent);
}
.result-badge{
  display:inline-block;padding:3px 10px;
  font-size:10px;font-weight:700;letter-spacing:1px;
  text-transform:uppercase;
  border:2px solid;
}

/* loading */
.loading-screen{
  display:flex;flex-direction:column;align-items:center;justify-content:center;
  min-height:200px;gap:12px;
}
.loading-text{font-size:14px;color:var(--text2);letter-spacing:2px;animation:blink 1s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.3}}

/* pixel moon decoration */
.moon-pixel{
  position:fixed;top:20px;right:20px;font-size:40px;z-index:0;
  animation:moonGlow 3s ease-in-out infinite;filter:drop-shadow(0 0 15px rgba(255,220,100,.6));
}
@keyframes moonGlow{0%,100%{filter:drop-shadow(0 0 15px rgba(255,220,100,.6))}50%{filter:drop-shadow(0 0 30px rgba(255,220,100,.9))}}

/* greeting pixel characters floating */
.float-chars{
  display:flex;justify-content:center;gap:16px;padding:14px 0;
  overflow:hidden;
}
.float-char{
  font-size:28px;
  animation:charFloat 3s ease-in-out infinite;
  filter:drop-shadow(0 0 6px rgba(255,126,200,.6));
}
.float-char:nth-child(2){animation-delay:.4s}
.float-char:nth-child(3){animation-delay:.8s}
.float-char:nth-child(4){animation-delay:1.2s}
@keyframes charFloat{0%,100%{transform:translateY(0)}50%{transform:translateY(-8px)}}

/* shrine glow effect */
.shrine-glow{animation:shrineGlow 2s ease-in-out infinite}
@keyframes shrineGlow{
  0%,100%{text-shadow:0 0 10px var(--gold),0 0 20px rgba(255,215,0,.5)}
  50%{text-shadow:0 0 20px var(--gold),0 0 40px rgba(255,215,0,.8),0 0 60px rgba(255,215,0,.3)}
}
</style>
</head>
<body>

<!-- Stars BG -->
<div class="stars-bg" id="stars"></div>
<div class="moon-pixel">🌕</div>

<!-- App -->
<div class="app">

  <!-- Header -->
  <div class="header">
    <div class="header-logo pixel-font">✦ โหราศาสตร์ไทย ✦</div>
    <div class="header-title pixel-font">ดวงเทพพิทักษ์</div>
    <div class="header-sub">Thai Mystic Fortune · พิกเซลอาร์ต</div>
    <div class="float-chars">
      <span class="float-char">🌸</span>
      <span class="float-char">⭐</span>
      <span class="float-char">🌙</span>
      <span class="float-char">🌟</span>
      <span class="float-char">🌺</span>
    </div>
  </div>

  <!-- SECTION 1: BIRTH DATE -->
  <div class="section active" id="sec-birth">
    <div class="section-title pixel-font">กรอกวันเกิด</div>

    <div class="birth-form">
      <div class="form-row">
        <div class="form-group">
          <div class="form-label">วัน</div>
          <select class="pixel-select" id="inp-day">
            <option value="">-- วัน --</option>
          </select>
        </div>
        <div class="form-group">
          <div class="form-label">เดือน</div>
          <select class="pixel-select" id="inp-month">
            <option value="">-- เดือน --</option>
          </select>
        </div>
        <div class="form-group">
          <div class="form-label">ปี (พ.ศ.)</div>
          <input class="pixel-input" type="number" id="inp-year" placeholder="2540" min="2480" max="2590">
        </div>
      </div>

      <div class="birth-char" id="birth-preview">
        <span class="char-sprite">🔮</span>
        <div class="char-info">
          <div style="font-size:11px;color:var(--text2)">กรุณาเลือกวันเกิด</div>
          <div style="font-size:11px;color:var(--text2)">เพื่อดูดวงชะตา</div>
        </div>
      </div>

      <button class="btn-main pixel-font" onclick="calcFortune()">🔮 ดูดวง ✨</button>
    </div>
  </div>

  <!-- SECTION 2: FORTUNE RESULT -->
  <div class="section" id="sec-fortune">
    <div class="section-title pixel-font">ดวงชะตา</div>

    <div class="fortune-header" id="fortune-header"></div>

    <div class="fortune-grid" id="fortune-grid"></div>

    <div class="fortune-takfak" id="fortune-takfak"></div>

    <div class="sparkle-row">✨ 🌟 ⭐ 🌟 ✨</div>

    <div id="fortune-detail"></div>

    <button class="btn-main pixel-font" onclick="goToCards()" style="margin-top:14px">
      🃏 จั่วไพ่ดวงชะตา ✨
    </button>
  </div>

  <!-- SECTION 3: CARD DRAW -->
  <div class="section" id="sec-cards">
    <div class="section-title pixel-font">ไพ่ธาตุไทย 31 ใบ</div>

    <div class="cards-instruction" id="cards-instruction">
      🌟 เลือกไพ่ที่ดึงดูดใจ 3 ใบ<br>
      <span style="font-size:11px;color:var(--text2)">จำนวนไพ่ที่เลือก: <span id="selected-count" style="color:var(--gold);font-weight:700">0</span>/3</span>
    </div>

    <div class="cards-grid" id="cards-grid"></div>

    <div id="drawn-results"></div>

    <button class="btn-main pixel-font" id="btn-reveal-cards" onclick="revealCards()" style="display:none;margin-bottom:10px">
      ✨ เปิดไพ่ ✨
    </button>

    <button class="btn-main pixel-font" id="btn-go-pray" onclick="goToPray()" style="display:none;background:linear-gradient(135deg,#FFD700,#FF8800)">
      🙏 ไปบวงสรวงเทพ ✨
    </button>
  </div>

  <!-- SECTION 4: DEITY PRAYER -->
  <div class="section" id="sec-pray">
    <div class="section-title pixel-font shrine-glow">🙏 ศาลเทพพิทักษ์</div>

    <div style="text-align:center;font-size:12px;color:var(--text2);margin-bottom:12px">
      ปัดเลือกเทพที่ต้องการบวงสรวง · จุดธูปได้สูงสุด 5 เทพ
    </div>

    <div class="deity-scroller" id="deity-scroller"></div>

    <div class="prayer-area" id="prayer-area" style="display:none">
      <div class="prayer-deity-name" id="prayer-deity-name"></div>
      <div style="font-size:11px;color:var(--text2);margin-bottom:8px">เขียนคำอธิษฐาน:</div>
      <textarea class="prayer-textarea" id="prayer-text"
        placeholder="ข้าพเจ้าขอกราบไหว้บวงสรวง..."></textarea>
      <div class="incense-count" id="incense-sticks"></div>
      <button class="btn-light-incense pixel-font" onclick="lightIncense()">🪔 จุดธูปบวงสรวง</button>
    </div>

    <div class="prayer-done-list" id="prayer-done-list"></div>
  </div>

</div><!-- /app -->

<!-- Bottom Nav -->
<div class="bottom-nav">
  <div class="nav-tab active" id="tab-birth" onclick="switchTab('birth')">
    <span class="nav-icon">🔮</span>
    <span class="nav-label pixel-font">วันเกิด</span>
  </div>
  <div class="nav-tab" id="tab-fortune" onclick="switchTab('fortune')">
    <span class="nav-icon">⭐</span>
    <span class="nav-label pixel-font">ดวง</span>
  </div>
  <div class="nav-tab" id="tab-cards" onclick="switchTab('cards')">
    <span class="nav-icon">🃏</span>
    <span class="nav-label pixel-font">ไพ่</span>
  </div>
  <div class="nav-tab" id="tab-pray" onclick="switchTab('pray')">
    <span class="nav-icon">🙏</span>
    <span class="nav-label pixel-font">บวงสรวง</span>
  </div>
</div>

<script>
// ═══════════════════════════════════════════════════════
//  STARS GENERATION
// ═══════════════════════════════════════════════════════
const starsEl = document.getElementById('stars');
for(let i=0;i<80;i++){
  const s = document.createElement('div');
  s.className='star';
  s.style.cssText=`
    width:${Math.random()<.3?4:2}px;height:${Math.random()<.3?4:2}px;
    left:${Math.random()*100}%;top:${Math.random()*100}%;
    animation-delay:${Math.random()*3}s;
    animation-duration:${1.5+Math.random()*2}s;
  `;
  starsEl.appendChild(s);
}

// ═══════════════════════════════════════════════════════
//  DATA
// ═══════════════════════════════════════════════════════
const MONTHS_TH = ['มกราคม','กุมภาพันธ์','มีนาคม','เมษายน','พฤษภาคม','มิถุนายน',
                   'กรกฎาคม','สิงหาคม','กันยายน','ตุลาคม','พฤศจิกายน','ธันวาคม'];
const DAYS_OF_WEEK = ['อาทิตย์','จันทร์','อังคาร','พุธ','พฤหัสบดี','ศุกร์','เสาร์'];
const DAY_COLORS = ['#FF6B35','#FFD700','#FF4466','#44BB44','#FF8800','#66AAFF','#8844AA'];
const DAY_EMOJI = ['☀️','🌙','🔥','💚','⚡','🌊','🟣'];
const DAY_ELEMENT = ['ไฟ','น้ำ','ดิน','ต้นไม้','สายฟ้า','ทะเล','จักรวาล'];

// 31-card deck based on Thai elements
const CARDS = [
  {id:1,name:'ดอกบัวทอง',element:'น้ำ',emoji:'🌸',color:'#FFB6D9',meaning:'ความบริสุทธิ์และปัญญา ชีวิตจะรุ่งเรืองจากความดีงาม',power:'มงคล'},
  {id:2,name:'เพลิงศักดิ์สิทธิ์',element:'ไฟ',emoji:'🔥',color:'#FF6B35',meaning:'พลังแห่งการเปลี่ยนแปลง สิ่งที่ผ่านไปจะนำมาซึ่งสิ่งใหม่ที่ดีกว่า',power:'พลัง'},
  {id:3,name:'แผ่นดินแม่',element:'ดิน',emoji:'🌱',color:'#86EFAC',meaning:'ความมั่นคงและรากฐานที่แข็งแกร่ง บ้านและครอบครัวจะอบอุ่น',power:'มั่นคง'},
  {id:4,name:'สายลมเทวดา',element:'ลม',emoji:'💨',color:'#BAE6FD',meaning:'การเดินทางและโอกาสใหม่ กลิ่นอายแห่งอิสรภาพกำลังมา',power:'โอกาส'},
  {id:5,name:'ต้นโพธิ์ศักดิ์สิทธิ์',element:'ไม้',emoji:'🌳',color:'#4ADE80',meaning:'ปัญญาและความอดทน ความสำเร็จจะมาถึงผู้ที่รอคอยอย่างสงบ',power:'ปัญญา'},
  {id:6,name:'หยาดน้ำค้าง',element:'น้ำ',emoji:'💧',color:'#93C5FD',meaning:'ความรักที่บริสุทธิ์จะหล่อเลี้ยงจิตใจ ความสัมพันธ์จะลึกซึ้งขึ้น',power:'ความรัก'},
  {id:7,name:'ทองคำแห่งดวงดาว',element:'อากาศ',emoji:'⭐',color:'#FDE68A',meaning:'ทรัพย์สมบัติและโชคลาภกำลังเข้าสู่ชีวิต',power:'โชคลาภ'},
  {id:8,name:'พญานาคราช',element:'น้ำ',emoji:'🐉',color:'#5EEAD4',meaning:'การปกป้องและพลังอำนาจ สิ่งศักดิ์สิทธิ์คุ้มครองคุณอยู่',power:'คุ้มครอง'},
  {id:9,name:'ดอกกระดังงา',element:'หญ้า',emoji:'🌼',color:'#FEF08A',meaning:'กลิ่นหอมแห่งความสุข บ้านเรือนและชีวิตคู่จะราบรื่น',power:'ความสุข'},
  {id:10,name:'ช้างเผือกศักดิ์สิทธิ์',element:'ดิน',emoji:'🐘',color:'#E5E7EB',meaning:'พลังอำนาจและบารมี ผู้คนจะเคารพและนับถือ',power:'บารมี'},
  {id:11,name:'เมฆฝน',element:'น้ำ',emoji:'🌧️',color:'#818CF8',meaning:'ช่วงเวลาแห่งการชำระล้าง สิ่งเก่าจะผ่านพ้น สิ่งใหม่จะงอกงาม',power:'เปลี่ยนแปลง'},
  {id:12,name:'พระอาทิตย์ทอง',element:'ไฟ',emoji:'☀️',color:'#FBBF24',meaning:'พลังชีวิตและสุขภาพ ร่างกายและจิตใจจะแข็งแกร่ง',power:'สุขภาพ'},
  {id:13,name:'พระจันทร์เงิน',element:'น้ำ',emoji:'🌙',color:'#E2E8F0',meaning:'สัญชาตญาณและความลึกซึ้ง ฟังใจตัวเองและจะพบทางออก',power:'สัญชาตญาณ'},
  {id:14,name:'ไม้ไผ่ทอง',element:'ไม้',emoji:'🎋',color:'#86EFAC',meaning:'ความยืดหยุ่นและความแข็งแกร่ง รับมือทุกอุปสรรคได้',power:'อดทน'},
  {id:15,name:'หินผาสูง',element:'ดิน',emoji:'🏔️',color:'#9CA3AF',meaning:'ความมั่นคงในจิตใจ ไม่ว่าพายุจะมาแค่ไหนก็ยืนหยัดได้',power:'มั่นคง'},
  {id:16,name:'นกการเวก',element:'ลม',emoji:'🦅',color:'#93C5FD',meaning:'อิสรภาพและมุมมองกว้างไกล มองปัญหาจากมุมสูงจะเห็นทางออก',power:'อิสระ'},
  {id:17,name:'กระต่ายดาว',element:'อากาศ',emoji:'🐇',color:'#F9A8D4',meaning:'โชคดีและความเร็ว โอกาสดีจะผ่านมา รีบคว้าไว้',power:'โชค'},
  {id:18,name:'ดอกปทุม',element:'น้ำ',emoji:'🌺',color:'#FB7185',meaning:'ความงามที่งอกขึ้นจากโคลนตม สิ่งดีจะเกิดจากความยากลำบาก',power:'หวัง'},
  {id:19,name:'เมล็ดข้าวทอง',element:'หญ้า',emoji:'🌾',color:'#FEF08A',meaning:'ผลลัพธ์แห่งความพยายาม สิ่งที่ทำไปทั้งหมดจะให้ผลดีงาม',power:'ผล'},
  {id:20,name:'น้ำผึ้งป่า',element:'หญ้า',emoji:'🍯',color:'#FBBF24',meaning:'ความหวานในชีวิต ความสัมพันธ์จะหอมหวานและอบอุ่น',power:'ความหวาน'},
  {id:21,name:'ก้อนเมฆขาว',element:'ลม',emoji:'☁️',color:'#F1F5F9',meaning:'จิตใจที่สงบและบริสุทธิ์ ปล่อยวางและจะพบความสุข',power:'สงบ'},
  {id:22,name:'แก้วมณี',element:'ดิน',emoji:'💎',color:'#67E8F9',meaning:'คุณค่าที่แท้จริงในตัวคุณ อย่าประเมินค่าตัวเองต่ำเกินไป',power:'คุณค่า'},
  {id:23,name:'ฟ้าแลบ',element:'ไฟ',emoji:'⚡',color:'#FDE68A',meaning:'พลังงานสูงและความคิดสร้างสรรค์ ช่วงนี้เหมาะเริ่มต้นสิ่งใหม่',power:'สร้างสรรค์'},
  {id:24,name:'รากไม้ลึก',element:'ไม้',emoji:'🌿',color:'#4ADE80',meaning:'รากฐานที่มั่นคง ครอบครัวและรากเหง้าคือแหล่งพลังงาน',power:'รากฐาน'},
  {id:25,name:'เกลียวคลื่น',element:'น้ำ',emoji:'🌊',color:'#38BDF8',meaning:'อารมณ์ที่ไหลลื่นและสัมพันธ์ที่ลึกซึ้ง เข้าใจและเข้าถึงผู้อื่น',power:'เข้าใจ'},
  {id:26,name:'ควันธูป',element:'ลม',emoji:'🌫️',color:'#D1D5DB',meaning:'การสื่อสารกับสิ่งศักดิ์สิทธิ์ คำอธิษฐานของคุณจะได้รับการตอบ',power:'ศักดิ์สิทธิ์'},
  {id:27,name:'ดอกรัก',element:'หญ้า',emoji:'🌷',color:'#FDA4AF',meaning:'ความรักที่กำลังผลิบาน ช่วงเวลาแห่งความโรแมนติก',power:'ความรัก'},
  {id:28,name:'เต่าทะเล',element:'น้ำ',emoji:'🐢',color:'#6EE7B7',meaning:'ความอดทนและอายุยืน ค่อยๆ ก้าวไปจะถึงเป้าหมาย',power:'อดทน'},
  {id:29,name:'ดาวตก',element:'ไฟ',emoji:'🌠',color:'#A78BFA',meaning:'ความปรารถนาลึกๆ จะเป็นจริง อย่าลืมอธิษฐาน',power:'ความปรารถนา'},
  {id:30,name:'เขาไฟ',element:'ไฟ',emoji:'🌋',color:'#F97316',meaning:'การเปลี่ยนแปลงครั้งใหญ่กำลังมา พร้อมรับมือด้วยความกล้า',power:'กล้า'},
  {id:31,name:'บัวเงินบัวทอง',element:'น้ำ',emoji:'🪷',color:'#E879F9',meaning:'ความสมบูรณ์แห่งชีวิต ทั้งทรัพย์สินและความสุขจะมาพร้อมกัน',power:'สมบูรณ์'},
];

// Deities
const DEITIES = [
  {id:'work',name:'พระพิฆเนศ',domain:'การงาน',emoji:'🐘',color:'#FF8C00',
   desc:'เทพแห่งความสำเร็จและการงาน ขจัดอุปสรรคทุกประการ',
   blessing:'การงานราบรื่น โปรเจกต์สำเร็จ ได้รับการยอมรับ'},
  {id:'love',name:'พระแม่ลักษมี',domain:'ความรัก',emoji:'🌸',color:'#FF69B4',
   desc:'เทพีแห่งความรักและความงาม ความสัมพันธ์ที่ดีงาม',
   blessing:'ความรักที่หวาน คู่ครองที่ดี ความสัมพันธ์ที่มั่นคง'},
  {id:'money',name:'พระกุเวร',domain:'การเงิน',emoji:'💰',color:'#FFD700',
   desc:'เทพแห่งทรัพย์สมบัติและความมั่งคั่ง',
   blessing:'ทรัพย์สินเพิ่มพูน ธุรกิจรุ่งเรือง การเงินคล่องตัว'},
  {id:'health',name:'พระแม่โพสพ',domain:'สุขภาพ',emoji:'🌿',color:'#22C55E',
   desc:'เทพีแห่งสุขภาพ ชีวิตและความอุดมสมบูรณ์',
   blessing:'สุขภาพแข็งแรง โรคภัยไม่เบียดเบียน พลังชีวิตเต็มเปี่ยม'},
  {id:'luck',name:'พระอินทร์',domain:'โชคลาภ',emoji:'⭐',color:'#A855F7',
   desc:'เทพราชแห่งสวรรค์ ผู้ประทานโชคและพร',
   blessing:'โชคดีตลอดปี สลากถูก โชคลาภมาโดยไม่คาดฝัน'},
];

// Day fortune data (31 days)
const DAY_FORTUNE = {
  1: {stars:'⭐⭐⭐⭐⭐',love:'💖 ความรักเบ่งบาน',money:'💰 โชคลาภมาเยือน',work:'⚡ การงานก้าวหน้า',health:'🌿 สุขภาพแข็งแรง',lucky_color:'ทอง',lucky_num:'1',summary:'วันแห่งความสมบูรณ์'},
  2: {stars:'⭐⭐⭐⭐',love:'💕 ความรักอ่อนโยน',money:'💵 ออมทรัพย์ดี',work:'📚 เรียนรู้สิ่งใหม่',health:'🍃 พักผ่อนให้พอ',lucky_color:'เงิน',lucky_num:'2',summary:'วันแห่งความสงบ'},
  3: {stars:'⭐⭐⭐⭐⭐',love:'🔥 ความรักหนักแน่น',money:'📈 ลงทุนได้ผล',work:'🏆 ความสำเร็จรออยู่',health:'💪 พลังงานสูง',lucky_color:'แดง',lucky_num:'3',summary:'วันแห่งไฟและพลัง'},
  4: {stars:'⭐⭐⭐',love:'🌱 ความรักงอกงาม',money:'🌾 รายได้มั่นคง',work:'🌳 ทำงานมีหลักการ',health:'🌿 ดูแลสุขภาพดี',lucky_color:'เขียว',lucky_num:'4',summary:'วันแห่งความมั่นคง'},
  5: {stars:'⭐⭐⭐⭐',love:'✨ ความรักเปล่งประกาย',money:'⭐ โชคดีกะทันหัน',work:'🚀 โอกาสใหม่มาถึง',health:'☀️ สุขภาพดีเยี่ยม',lucky_color:'ทอง',lucky_num:'5',summary:'วันแห่งดาวดวงใหม่'},
  6: {stars:'⭐⭐⭐⭐',love:'🌊 ความรักลึกซึ้ง',money:'💧 เงินไหลเข้า',work:'🎯 ตั้งเป้าหมายดี',health:'💙 จิตใจผ่องใส',lucky_color:'น้ำเงิน',lucky_num:'6',summary:'วันแห่งความลึกซึ้ง'},
  7: {stars:'⭐⭐⭐⭐⭐',love:'💜 ความรักลึกลับ',money:'🔮 ทรัพย์สินเพิ่ม',work:'🌙 งานสำเร็จแน่นอน',health:'🌟 สุขภาพสมบูรณ์',lucky_color:'ม่วง',lucky_num:'7',summary:'วันแห่งเวทมนตร์'},
  8: {stars:'⭐⭐⭐',love:'🌸 ความรักบริสุทธิ์',money:'🎋 ออมทรัพย์ได้ผล',work:'📝 ทำงานรอบคอบ',health:'🌺 สุขภาพดี',lucky_color:'ชมพู',lucky_num:'8',summary:'วันแห่งความบริสุทธิ์'},
  9: {stars:'⭐⭐⭐⭐',love:'☀️ ความรักอบอุ่น',money:'💛 ทรัพย์สมบัติมาก',work:'⚡ พลังงานเต็มเปี่ยม',health:'🔥 ร่างกายแข็งแกร่ง',lucky_color:'เหลือง',lucky_num:'9',summary:'วันแห่งพลังสูง'},
  10:{stars:'⭐⭐⭐⭐⭐',love:'💎 ความรักมีค่า',money:'💎 โชคลาภมาก',work:'🏆 ความสำเร็จยิ่งใหญ่',health:'💪 แข็งแกร่งมาก',lucky_color:'ขาว',lucky_num:'10',summary:'วันแห่งความสมบูรณ์แบบ'},
  11:{stars:'⭐⭐⭐',love:'🌙 ความรักลึกลับ',money:'🌫️ ระวังค่าใช้จ่าย',work:'💭 ใช้ความคิด',health:'😴 ต้องพักผ่อน',lucky_color:'เทา',lucky_num:'11',summary:'วันแห่งการพิจารณา'},
  12:{stars:'⭐⭐⭐⭐',love:'🌺 ความรักสวยงาม',money:'🌻 รายได้งอกงาม',work:'🎨 งานสร้างสรรค์',health:'🌸 จิตใจแจ่มใส',lucky_color:'ส้ม',lucky_num:'12',summary:'วันแห่งความสร้างสรรค์'},
  13:{stars:'⭐⭐⭐',love:'💗 ความรักอ่อนโยน',money:'🌿 เงินพอดี',work:'📖 เรียนรู้มาก',health:'🍃 สุขภาพดี',lucky_color:'เขียว',lucky_num:'13',summary:'วันแห่งการเรียนรู้'},
  14:{stars:'⭐⭐⭐⭐',love:'💝 ความรักอุดมสมบูรณ์',money:'💰 โชคดีมาก',work:'🌟 งานดีเยี่ยม',health:'☀️ ร่างกายสมบูรณ์',lucky_color:'ทอง',lucky_num:'14',summary:'วันแห่งความอุดมสมบูรณ์'},
  15:{stars:'⭐⭐⭐⭐⭐',love:'🌕 ความรักเต็มเปี่ยม',money:'🌕 ทรัพย์สมบูรณ์',work:'🌕 งานสำเร็จล้น',health:'🌕 สุขภาพแข็งแรง',lucky_color:'เงิน',lucky_num:'15',summary:'วันแห่งความเต็มเปี่ยม'},
  16:{stars:'⭐⭐⭐',love:'🌱 ความรักเติบโต',money:'💵 รายได้ปานกลาง',work:'🔧 ทำงานแก้ปัญหา',health:'💚 สุขภาพดีพอควร',lucky_color:'เขียว',lucky_num:'16',summary:'วันแห่งการแก้ปัญหา'},
  17:{stars:'⭐⭐⭐⭐',love:'🐇 ความรักโชคดี',money:'🎯 โอกาสทางการเงิน',work:'⚡ พลังงานสูง',health:'🌿 ร่างกายดี',lucky_color:'ขาว',lucky_num:'17',summary:'วันแห่งโอกาสดี'},
  18:{stars:'⭐⭐⭐⭐',love:'🌹 ความรักหวานชื่น',money:'🌺 ทรัพย์งอกงาม',work:'🌟 งานก้าวหน้า',health:'🍀 สุขภาพดีมาก',lucky_color:'แดง',lucky_num:'18',summary:'วันแห่งความหวานชื่น'},
  19:{stars:'⭐⭐⭐⭐⭐',love:'🌾 ความรักเป็นผล',money:'🌾 เก็บเกี่ยวผล',work:'🏆 ผลงานดีเยี่ยม',health:'💪 แข็งแกร่ง',lucky_color:'ทอง',lucky_num:'19',summary:'วันแห่งการเก็บเกี่ยว'},
  20:{stars:'⭐⭐⭐⭐',love:'🍯 ความรักหวาน',money:'💛 โชคทรัพย์ดี',work:'😊 บรรยากาศดี',health:'🌻 มีความสุข',lucky_color:'เหลือง',lucky_num:'20',summary:'วันแห่งความหวาน'},
  21:{stars:'⭐⭐⭐',love:'☁️ ความรักสงบ',money:'🌫️ เงินพอใช้',work:'🧘 ทำงานใจเย็น',health:'😌 พักผ่อนดี',lucky_color:'ขาว',lucky_num:'21',summary:'วันแห่งความสงบ'},
  22:{stars:'⭐⭐⭐⭐',love:'💎 ความรักมีค่า',money:'💎 ทรัพย์มีค่า',work:'✨ งานโดดเด่น',health:'💙 สุขภาพดี',lucky_color:'ฟ้า',lucky_num:'22',summary:'วันแห่งคุณค่า'},
  23:{stars:'⭐⭐⭐⭐⭐',love:'⚡ ความรักไฟแล่บ',money:'⚡ โชคกะทันหัน',work:'🚀 ความก้าวหน้าเร็ว',health:'🔥 พลังล้นเหลือ',lucky_color:'เหลือง',lucky_num:'23',summary:'วันแห่งสายฟ้า'},
  24:{stars:'⭐⭐⭐',love:'🌿 ความรักลึกรากฐาน',money:'🌱 เงินสะสมดี',work:'🌳 งานมีรากฐาน',health:'💚 สุขภาพดีพอควร',lucky_color:'เขียว',lucky_num:'24',summary:'วันแห่งรากฐาน'},
  25:{stars:'⭐⭐⭐⭐',love:'🌊 ความรักไหลลื่น',money:'💧 เงินไหลเวียน',work:'🎯 งานดีมาก',health:'🌊 จิตใจสงบ',lucky_color:'น้ำเงิน',lucky_num:'25',summary:'วันแห่งการไหลลื่น'},
  26:{stars:'⭐⭐⭐⭐⭐',love:'🌫️ ความรักลึกลับ',money:'✨ โชคลาภลึกลับ',work:'🔮 งานลึกลับสำเร็จ',health:'🌟 สุขภาพดีเยี่ยม',lucky_color:'ม่วง',lucky_num:'26',summary:'วันแห่งความศักดิ์สิทธิ์'},
  27:{stars:'⭐⭐⭐⭐',love:'🌷 ความรักบาน',money:'💐 รายได้ดี',work:'🌸 งานสวยงาม',health:'🌺 สุขภาพดี',lucky_color:'ชมพู',lucky_num:'27',summary:'วันแห่งความรัก'},
  28:{stars:'⭐⭐⭐',love:'🐢 ความรักยาวนาน',money:'🌿 เงินออมดี',work:'🐢 ค่อยๆ ก้าวหน้า',health:'💚 สุขภาพดีนาน',lucky_color:'เขียว',lucky_num:'28',summary:'วันแห่งความยั่งยืน'},
  29:{stars:'⭐⭐⭐⭐⭐',love:'🌠 ความรักตามดาว',money:'🌠 โชคลาภดาวตก',work:'🌠 ความสำเร็จดาวตก',health:'⭐ สุขภาพดาวตก',lucky_color:'น้ำเงิน',lucky_num:'29',summary:'วันแห่งความปรารถนา'},
  30:{stars:'⭐⭐⭐⭐',love:'🌋 ความรักร้อนแรง',money:'💥 การเงินเปลี่ยนแปลง',work:'🔥 ทำงานกล้าหาญ',health:'⚡ พลังสูง',lucky_color:'แดง',lucky_num:'30',summary:'วันแห่งการเปลี่ยนแปลง'},
  31:{stars:'⭐⭐⭐⭐⭐',love:'🪷 ความรักสมบูรณ์',money:'💰 ทรัพย์สมบูรณ์',work:'🏆 ความสำเร็จสมบูรณ์',health:'💫 สุขภาพสมบูรณ์',lucky_color:'ทอง',lucky_num:'31',summary:'วันแห่งความสมบูรณ์แบบ'},
};

// ═══════════════════════════════════════════════════════
//  INIT: Populate dropdowns
// ═══════════════════════════════════════════════════════
function initDropdowns(){
  const dayEl = document.getElementById('inp-day');
  const moEl = document.getElementById('inp-month');
  for(let i=1;i<=31;i++){
    dayEl.innerHTML += `<option value="${i}">${i}</option>`;
  }
  MONTHS_TH.forEach((m,i)=>{
    moEl.innerHTML += `<option value="${i+1}">${m}</option>`;
  });
}
initDropdowns();

// Live preview when changing day
document.getElementById('inp-day').addEventListener('change',updateBirthPreview);

function updateBirthPreview(){
  const day = +document.getElementById('inp-day').value;
  const mo = +document.getElementById('inp-month').value;
  const yr = +document.getElementById('inp-year').value;
  if(!day) return;
  const preview = document.getElementById('birth-preview');
  const fortune = DAY_FORTUNE[day] || DAY_FORTUNE[1];
  const yrCE = yr > 0 ? yr - 543 : 1990;
  let dayOfWeek = '';
  if(mo && yr){
    const date = new Date(yrCE, mo-1, day);
    dayOfWeek = DAYS_OF_WEEK[date.getDay()];
  }
  preview.innerHTML = `
    <span class="char-sprite">${fortune.stars.split('').includes('⭐') ? '🌟' : '⭐'}</span>
    <div class="char-info">
      <div class="char-name">วันที่ ${day} ${mo ? MONTHS_TH[mo-1]||'' : ''}</div>
      <div>${fortune.summary}</div>
      ${dayOfWeek ? `<div>วัน${dayOfWeek}</div>`:''}
      <div style="color:var(--gold)">${fortune.stars}</div>
    </div>
  `;
}

// ═══════════════════════════════════════════════════════
//  FORTUNE CALCULATION
// ═══════════════════════════════════════════════════════
let birthData = {};

function calcFortune(){
  const day = +document.getElementById('inp-day').value;
  const mo = +document.getElementById('inp-month').value;
  const yr = +document.getElementById('inp-year').value;

  if(!day||!mo||!yr||yr<2480||yr>2590){
    alert('กรุณากรอกวันเกิดให้ครบถ้วน (ปี พ.ศ.)');
    return;
  }

  const yrCE = yr - 543;
  const dateObj = new Date(yrCE, mo-1, day);
  const dayOfWeek = dateObj.getDay();

  birthData = {day,mo,yr,yrCE,dayOfWeek};

  // Fortune for this day (1-31)
  const fortune = DAY_FORTUNE[day] || DAY_FORTUNE[1];

  // Calculate Takfak date (Thai astrology: day born + 1 = lucky day per month)
  const takfakDay = day % 7; // simplified thai astrology pattern
  const takfakDayName = DAYS_OF_WEEK[takfakDay];

  // Day element
  const elementIdx = dayOfWeek;
  const dayColor = DAY_COLORS[dayOfWeek];
  const dayEmoji = DAY_EMOJI[dayOfWeek];

  // Render
  document.getElementById('fortune-header').innerHTML = `
    <div class="fortune-day-name">${dayEmoji} วันที่ ${day} ${MONTHS_TH[mo-1]} พ.ศ.${yr}</div>
    <div style="font-size:13px;color:var(--text2);margin-top:4px">วัน${DAYS_OF_WEEK[dayOfWeek]} · ธาตุ${DAY_ELEMENT[dayOfWeek]}</div>
    <div class="fortune-stars" style="margin:8px 0">${fortune.stars}</div>
    <div style="font-size:14px;font-weight:700;color:${dayColor}">${fortune.summary}</div>
  `;

  document.getElementById('fortune-grid').innerHTML = `
    <div class="fortune-card" style="border-color:${dayColor}">
      <div class="fortune-card-icon">❤️</div>
      <div class="fortune-card-label">ความรัก</div>
      <div class="fortune-card-val" style="color:var(--pink2)">${fortune.love}</div>
    </div>
    <div class="fortune-card" style="border-color:#FFD700">
      <div class="fortune-card-icon">💰</div>
      <div class="fortune-card-label">การเงิน</div>
      <div class="fortune-card-val" style="color:var(--gold)">${fortune.money}</div>
    </div>
    <div class="fortune-card" style="border-color:var(--teal)">
      <div class="fortune-card-icon">💼</div>
      <div class="fortune-card-label">การงาน</div>
      <div class="fortune-card-val" style="color:var(--teal)">${fortune.work}</div>
    </div>
    <div class="fortune-card" style="border-color:var(--green2)">
      <div class="fortune-card-icon">🌿</div>
      <div class="fortune-card-label">สุขภาพ</div>
      <div class="fortune-card-val" style="color:var(--green)">${fortune.health}</div>
    </div>
  `;

  // Takfak calculation
  const takfakMonthDay = calculateTakfak(day, mo, yr);
  document.getElementById('fortune-takfak').innerHTML = `
    <div class="takfak-title">🗓️ วันตกฝาก (ทักษา)</div>
    <div class="takfak-date">${takfakMonthDay}</div>
    <div class="takfak-desc">
      ตามหลักโหราศาสตร์ไทย วันตกฝากคือวันที่ดาวประจำวันเกิดของคุณอยู่ในตำแหน่งที่เป็นมงคล
      ควรทำบุญหรือเริ่มต้นสิ่งสำคัญในวันนี้
    </div>
  `;

  document.getElementById('fortune-detail').innerHTML = `
    <div style="background:var(--bg-deep);border:3px solid var(--purple2);padding:14px">
      <div style="font-size:11px;letter-spacing:1px;color:var(--purple);text-transform:uppercase;margin-bottom:8px">สีมงคล & เลขนำโชค</div>
      <div style="display:flex;gap:12px;align-items:center">
        <div style="background:var(--border);padding:8px 14px;font-size:13px">
          🎨 สีมงคล: <span style="color:var(--gold);font-weight:700">${fortune.lucky_color}</span>
        </div>
        <div style="background:var(--border);padding:8px 14px;font-size:13px">
          🔢 เลขนำโชค: <span style="color:var(--gold);font-weight:700">${fortune.lucky_num}</span>
        </div>
      </div>
    </div>
  `;

  switchTab('fortune');
  spawnParticles();
}

function calculateTakfak(day, mo, yr){
  // Simplified Thai astrology: วันตกฝาก
  // Based on day of birth modulo 7 pattern
  const yrCE = yr - 543;
  const dateObj = new Date(yrCE, mo-1, day);
  const dayOfWeek = dateObj.getDay();

  // Thai: takfak day = add specific intervals based on birth day
  const intervals = [1,3,5,7,11,13,15];
  const interval = intervals[day % 7];

  const takfakDate = new Date(new Date().getFullYear(), new Date().getMonth(), new Date().getDate());
  // Find next occurrence of birth day of week
  while(takfakDate.getDay() !== dayOfWeek){
    takfakDate.setDate(takfakDate.getDate()+1);
  }

  const thDay = takfakDate.getDate();
  const thMo = takfakDate.getMonth();
  const thYr = takfakDate.getFullYear() + 543;
  return `${thDay} ${MONTHS_TH[thMo]} พ.ศ.${thYr} (วัน${DAYS_OF_WEEK[dayOfWeek]})`;
}

// ═══════════════════════════════════════════════════════
//  CARD SYSTEM
// ═══════════════════════════════════════════════════════
let selectedCards = new Set();
let cardsRevealed = false;

function goToCards(){
  selectedCards.clear();
  cardsRevealed = false;
  buildCardGrid();
  switchTab('cards');
}

function buildCardGrid(){
  const grid = document.getElementById('cards-grid');
  const day = birthData.day || 1;

  // Shuffle cards with seed from birthday
  const shuffled = [...CARDS].sort((a,b)=>((a.id*day)%31)-((b.id*day)%31));

  grid.innerHTML = shuffled.map(card=>`
    <div class="card-item" id="card-${card.id}" onclick="selectCard(${card.id})">
      <div class="card-back">🔮</div>
      <div class="card-num">${card.id}</div>
    </div>
  `).join('');

  document.getElementById('drawn-results').innerHTML='';
  document.getElementById('btn-reveal-cards').style.display='none';
  document.getElementById('btn-go-pray').style.display='none';
  document.getElementById('selected-count').textContent='0';
  document.getElementById('cards-instruction').style.display='block';
}

function selectCard(id){
  if(cardsRevealed) return;
  const el = document.getElementById('card-'+id);

  if(selectedCards.has(id)){
    selectedCards.delete(id);
    el.classList.remove('selected');
  } else if(selectedCards.size < 3){
    selectedCards.add(id);
    el.classList.add('selected');
    spawnParticlesAt(el);
  } else {
    // shake effect
    el.style.animation='none';
    setTimeout(()=>el.style.animation='',100);
    return;
  }

  document.getElementById('selected-count').textContent = selectedCards.size;

  const revealBtn = document.getElementById('btn-reveal-cards');
  revealBtn.style.display = selectedCards.size===3 ? 'block':'none';
}

function revealCards(){
  if(selectedCards.size !== 3) return;
  cardsRevealed = true;

  const selectedArr = [...selectedCards];
  const selectedCardData = CARDS.filter(c=>selectedArr.includes(c.id));

  // Animate reveal
  selectedArr.forEach((id,i)=>{
    setTimeout(()=>{
      const el = document.getElementById('card-'+id);
      const card = CARDS.find(c=>c.id===id);
      el.classList.remove('selected');
      el.classList.add('revealed');
      el.innerHTML = `
        <div style="font-size:${14}px">${card.emoji}</div>
        <div class="card-num">${card.id}</div>
      `;
      el.style.borderColor = card.color;
    }, i*300);
  });

  setTimeout(()=>{
    document.getElementById('drawn-results').innerHTML = `
      <div style="font-size:12px;color:var(--gold);letter-spacing:2px;text-align:center;margin:14px 0 8px;text-transform:uppercase">✨ ไพ่ที่จั่วได้ ✨</div>
      <div class="drawn-cards">
        ${selectedCardData.map((card,i)=>`
          <div class="drawn-card" style="border-color:${card.color};animation-delay:${i*.2}s">
            <div class="drawn-icon">${card.emoji}</div>
            <div class="drawn-info">
              <div class="drawn-name" style="color:${card.color}">${card.name}</div>
              <div class="drawn-element">ธาตุ${card.element} · พลัง${card.power}</div>
              <div class="drawn-meaning">${card.meaning}</div>
            </div>
          </div>
        `).join('')}
      </div>
    `;

    document.getElementById('btn-reveal-cards').style.display='none';
    document.getElementById('btn-go-pray').style.display='block';
    document.getElementById('cards-instruction').style.display='none';
    spawnParticles();
  }, 1200);
}

// ═══════════════════════════════════════════════════════
//  DEITY PRAYER SYSTEM
// ═══════════════════════════════════════════════════════
let activeDeity = null;
let litDeities = new Set();
const prayerTexts = {};

function goToPray(){
  buildDeityScroller();
  switchTab('pray');
}

function buildDeityScroller(){
  const scroller = document.getElementById('deity-scroller');
  scroller.innerHTML = DEITIES.map(d=>`
    <div class="deity-card ${litDeities.has(d.id)?'lit':''}" id="dcard-${d.id}" onclick="selectDeity('${d.id}')">
      <span class="incense-indicator">🪔</span>
      <span class="deity-sprite">${d.emoji}</span>
      <div class="deity-name">${d.name}</div>
      <div class="deity-domain">${d.domain}</div>
      <div style="font-size:9px;color:var(--text2);margin-top:4px;line-height:1.4">${d.desc}</div>
    </div>
  `).join('');
  renderPrayerDoneList();
}

function selectDeity(id){
  activeDeity = DEITIES.find(d=>d.id===id);
  document.querySelectorAll('.deity-card').forEach(el=>el.classList.remove('active'));
  document.getElementById('dcard-'+id).classList.add('active');

  const area = document.getElementById('prayer-area');
  area.style.display='block';
  area.style.borderColor = activeDeity.color;

  document.getElementById('prayer-deity-name').innerHTML = `
    <span>${activeDeity.emoji}</span>
    <span>${activeDeity.name}</span>
    <span style="font-size:11px;color:var(--text2);font-weight:400">${activeDeity.domain}</span>
  `;

  document.getElementById('prayer-text').value = prayerTexts[id] || '';

  // Incense sticks (max 5)
  const sticks = document.getElementById('incense-sticks');
  sticks.innerHTML = Array(5).fill(0).map((_,i)=>`
    <div class="stick ${litDeities.has(activeDeity.id) && i < (prayerTexts[id]?1:0) ? 'burning':''}"></div>
  `).join('');

  // Scroll to prayer area
  setTimeout(()=>area.scrollIntoView({behavior:'smooth',block:'nearest'}),100);
}

function lightIncense(){
  if(!activeDeity){alert('กรุณาเลือกเทพก่อน');return;}
  if(litDeities.size >= 5 && !litDeities.has(activeDeity.id)){
    alert('จุดธูปได้สูงสุด 5 เทพแล้ว');return;
  }
  const text = document.getElementById('prayer-text').value.trim();
  if(!text){alert('กรุณาเขียนคำอธิษฐานก่อน');return;}

  prayerTexts[activeDeity.id] = text;
  litDeities.add(activeDeity.id);

  // Update deity card
  const dcard = document.getElementById('dcard-'+activeDeity.id);
  dcard.classList.add('lit');

  // Update incense sticks
  document.querySelectorAll('.stick').forEach((s,i)=>{
    if(i===0) s.classList.add('burning');
  });

  spawnParticles();
  renderPrayerDoneList();

  // Show blessing
  const area = document.getElementById('prayer-area');
  area.innerHTML += `
    <div style="background:rgba(255,215,0,.1);border:2px solid var(--gold);padding:10px;margin-top:10px;font-size:12px">
      <div style="color:var(--gold);font-weight:700;margin-bottom:4px">🙏 ถวายแด่${activeDeity.name}สำเร็จ</div>
      <div style="color:var(--text2)">${activeDeity.blessing}</div>
    </div>
  `;
}

function renderPrayerDoneList(){
  const list = document.getElementById('prayer-done-list');
  if(litDeities.size===0){list.innerHTML='';return;}
  list.innerHTML = `
    <div style="font-size:12px;color:var(--text2);letter-spacing:1px;text-transform:uppercase;margin-bottom:4px">✦ เทพที่บวงสรวงแล้ว</div>
    ${[...litDeities].map(id=>{
      const d = DEITIES.find(x=>x.id===id);
      return `<div class="prayer-done-item">
        <span>${d.emoji}</span>
        <div>
          <div style="font-weight:700;color:${d.color}">${d.name}</div>
          <div style="font-size:10px;color:var(--text2)">${d.blessing}</div>
        </div>
      </div>`;
    }).join('')}
  `;
}

// ═══════════════════════════════════════════════════════
//  NAVIGATION
// ═══════════════════════════════════════════════════════
const SECTIONS = {birth:'sec-birth',fortune:'sec-fortune',cards:'sec-cards',pray:'sec-pray'};
const TABS = ['birth','fortune','cards','pray'];

function switchTab(tab){
  TABS.forEach(t=>{
    const sec = document.getElementById(SECTIONS[t]);
    const tabEl = document.getElementById('tab-'+t);
    if(t===tab){
      sec.classList.add('active');
      tabEl.classList.add('active');
    } else {
      sec.classList.remove('active');
      tabEl.classList.remove('active');
    }
  });
  window.scrollTo({top:0,behavior:'smooth'});
}

// ═══════════════════════════════════════════════════════
//  PARTICLES
// ═══════════════════════════════════════════════════════
const PARTICLE_EMOJIS = ['✨','⭐','🌟','💫','🌸','🌺','💜','💛','💖'];

function spawnParticles(){
  for(let i=0;i<8;i++){
    setTimeout(()=>{
      const p = document.createElement('div');
      p.className='particle';
      p.textContent = PARTICLE_EMOJIS[Math.floor(Math.random()*PARTICLE_EMOJIS.length)];
      p.style.cssText=`left:${20+Math.random()*60}%;bottom:80px;animation-delay:${Math.random()*.3}s`;
      document.body.appendChild(p);
      setTimeout(()=>p.remove(),1800);
    }, i*80);
  }
}

function spawnParticlesAt(el){
  const rect = el.getBoundingClientRect();
  const p = document.createElement('div');
  p.className='particle';
  p.textContent = '✨';
  p.style.cssText=`position:fixed;left:${rect.left+rect.width/2}px;top:${rect.top}px;pointer-events:none;z-index:999`;
  document.body.appendChild(p);
  setTimeout(()=>p.remove(),1500);
}
</script>
</body>
</html>
