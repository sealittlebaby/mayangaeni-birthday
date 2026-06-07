/* ===========================
   CSS VARIABLES & BASE
=========================== */
:root {
  --pink-soft: #f8c8d4;
  --pink-mid: #f4a0b8;
  --pink-deep: #e07a9a;
  --pink-dark: #c9637f;
  --rose-gold: #c9a0a8;
  --cream: #fff5f0;
  --cream-warm: #fdeee8;
  --white: #fffafa;
  --text-dark: #6b3a47;
  --text-mid: #9c5a6e;
  --text-light: #d4a0b0;
  --shadow: rgba(199, 100, 130, 0.25);
  --glow: rgba(248, 180, 200, 0.6);
  --font-fancy: 'Dancing Script', cursive;
  --font-display: 'Pacifico', cursive;
  --font-script: 'Sacramento', cursive;
  --font-body: 'Lato', sans-serif;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

html, body {
  width: 100%; height: 100%;
  overflow: hidden;
  background: var(--pink-soft);
  font-family: var(--font-body);
  color: var(--text-dark);
}

/* ===========================
   SCENES
=========================== */
.scene {
  position: fixed; inset: 0;
  display: flex; align-items: center; justify-content: center;
  opacity: 0; pointer-events: none;
  transition: opacity 0.8s ease;
  overflow: hidden;
  z-index: 1;
}
.scene.active {
  opacity: 1; pointer-events: all; z-index: 10;
}
.hidden { display: none !important; }

/* ===========================
   FLORIST BACKGROUND
=========================== */
.florist-bg {
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse at 10% 20%, rgba(255,182,193,0.4) 0%, transparent 50%),
    radial-gradient(ellipse at 90% 80%, rgba(255,160,175,0.35) 0%, transparent 50%),
    radial-gradient(ellipse at 50% 50%, rgba(255,240,245,0.6) 0%, transparent 70%),
    linear-gradient(160deg, #fde8ef 0%, #fff0f5 40%, #fce4ed 100%);
  z-index: 0;
}
.florist-bg::before {
  content: '';
  position: absolute; inset: 0;
  background-image:
    radial-gradient(circle at 15% 85%, rgba(255,130,160,0.12) 0%, transparent 35%),
    radial-gradient(circle at 85% 15%, rgba(255,150,175,0.1) 0%, transparent 30%);
}

/* ===========================
   SCENE 1: LOADING
=========================== */
#scene-loading {
  background: linear-gradient(145deg, #fce4ed 0%, #ffd6e7 50%, #ffe4ef 100%);
  flex-direction: column;
}

.loading-flowers {
  position: absolute; inset: 0; pointer-events: none;
}

.bloom {
  position: absolute;
  font-size: clamp(2rem, 5vw, 4rem);
  opacity: 0;
  animation: bloomIn 1.5s ease forwards;
}
.bloom-1 { top: 8%; left: 5%; animation-delay: 0.2s; }
.bloom-2 { top: 15%; right: 8%; animation-delay: 0.5s; font-size: clamp(2.5rem,6vw,5rem); }
.bloom-3 { bottom: 20%; left: 3%; animation-delay: 0.8s; }
.bloom-4 { bottom: 10%; right: 5%; animation-delay: 1.1s; }
.bloom-5 { top: 50%; left: 2%; animation-delay: 0.4s; transform: translateY(-50%); }
.bloom-6 { top: 40%; right: 2%; animation-delay: 0.9s; transform: translateY(-50%); }

@keyframes bloomIn {
  0% { opacity: 0; transform: scale(0) rotate(-30deg); }
  60% { opacity: 1; transform: scale(1.15) rotate(5deg); }
  100% { opacity: 0.7; transform: scale(1) rotate(0deg); }
}

.loading-content {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; align-items: center; gap: 20px;
  text-align: center; padding: 40px 20px;
}

.loading-flower-icon {
  font-size: clamp(3rem, 8vw, 5rem);
  animation: spin-float 3s ease-in-out infinite;
}
@keyframes spin-float {
  0%, 100% { transform: translateY(0) rotate(0deg); }
  50% { transform: translateY(-10px) rotate(15deg); }
}

.loading-text {
  font-family: var(--font-fancy);
  font-size: clamp(1.2rem, 3.5vw, 1.8rem);
  color: var(--pink-dark);
  letter-spacing: 0.5px;
}

.progress-bar-wrap {
  width: min(300px, 80vw);
  height: 10px;
  background: rgba(255,255,255,0.6);
  border-radius: 999px;
  overflow: hidden;
  box-shadow: 0 2px 10px var(--shadow);
}
.progress-bar {
  height: 100%;
  width: 0%;
  background: linear-gradient(90deg, var(--pink-mid), var(--rose-gold), var(--pink-deep));
  border-radius: 999px;
  transition: width 0.1s linear;
  position: relative;
}
.progress-bar::after {
  content: '';
  position: absolute; right: 0; top: 0; bottom: 0;
  width: 20px;
  background: rgba(255,255,255,0.5);
  border-radius: 999px;
  animation: shimmer 1s ease infinite;
}
@keyframes shimmer { 0%,100%{ opacity:0.5; } 50%{ opacity:1; } }

.loading-sub {
  font-size: clamp(0.75rem, 2vw, 0.95rem);
  color: var(--text-light);
  letter-spacing: 1px;
  font-style: italic;
}

/* ===========================
   SCENE 2: VERIFICATION
=========================== */
#scene-verify {
  background: linear-gradient(135deg, #fce8ef 0%, #fff0f8 60%, #fde0ea 100%);
}

.petal-bg {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse at 30% 70%, rgba(255,182,193,0.3), transparent 60%),
              radial-gradient(ellipse at 70% 30%, rgba(255,160,175,0.2), transparent 50%);
}

.verify-card {
  position: relative; z-index: 2;
  background: rgba(255,255,255,0.92);
  backdrop-filter: blur(10px);
  border-radius: 30px;
  padding: 50px 40px 40px;
  width: min(420px, 90vw);
  box-shadow: 0 20px 60px var(--shadow), 0 0 0 1px rgba(255,160,175,0.3);
  text-align: center;
  animation: cardFloat 4s ease-in-out infinite;
}
@keyframes cardFloat {
  0%,100%{ transform: translateY(0); }
  50%{ transform: translateY(-8px); }
}

.verify-flowers { position: absolute; top: -25px; left: 0; right: 0; display: flex; justify-content: center; gap: 10px; }
.vf { font-size: 1.8rem; animation: spin-float 3s ease-in-out infinite; }
.vf2 { animation-delay: 0.5s; }
.vf3 { animation-delay: 1s; }
.vf4 { animation-delay: 1.5s; }

.verify-icon { font-size: 3rem; margin-bottom: 10px; }
.verify-title {
  font-family: var(--font-display);
  font-size: clamp(1.8rem, 5vw, 2.5rem);
  color: var(--pink-dark);
  margin-bottom: 12px;
}
.verify-question {
  font-size: clamp(0.95rem, 2.5vw, 1.15rem);
  color: var(--text-mid);
  margin-bottom: 30px;
  line-height: 1.6;
}
.verify-question strong { color: var(--pink-dark); }

.verify-buttons { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; }

.btn-yes, .btn-no, .btn-close {
  padding: 14px 30px;
  border: none; border-radius: 999px;
  font-family: var(--font-fancy);
  font-size: 1.05rem;
  cursor: pointer;
  transition: all 0.3s ease;
  font-weight: 600;
}
.btn-yes {
  background: linear-gradient(135deg, var(--pink-mid), var(--pink-deep));
  color: white;
  box-shadow: 0 8px 20px rgba(224,122,154,0.4);
}
.btn-yes:hover { transform: translateY(-3px); box-shadow: 0 12px 28px rgba(224,122,154,0.5); }

.btn-no {
  background: rgba(248,200,212,0.4);
  color: var(--pink-dark);
  border: 2px solid var(--pink-soft);
}
.btn-no:hover { background: var(--pink-soft); }

.verify-denied {
  margin-top: 24px;
  padding: 20px;
  background: rgba(255,240,245,0.8);
  border-radius: 16px;
  border: 1px dashed var(--pink-mid);
}
.verify-denied p { margin-bottom: 10px; color: var(--text-mid); font-size: 0.95rem; line-height: 1.5; }
.btn-close {
  background: var(--cream);
  color: var(--pink-dark);
  border: 2px solid var(--pink-soft);
  margin-top: 10px;
}

/* ===========================
   SCENE 3: INTRO
=========================== */
#scene-intro {
  background: linear-gradient(145deg, #fdeef5 0%, #fff5f8 100%);
}

.falling-petals { position: absolute; inset: 0; pointer-events: none; }
.petal {
  position: absolute;
  top: -60px;
  font-size: clamp(1rem, 2.5vw, 1.8rem);
  animation: petalFall linear infinite;
  opacity: 0.6;
}
@keyframes petalFall {
  0% { transform: translateY(-60px) rotate(0deg); opacity: 0.7; }
  100% { transform: translateY(110vh) rotate(360deg); opacity: 0; }
}

.intro-content {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; align-items: center; gap: 40px;
  padding: 20px;
}

.intro-text-wrap {
  background: rgba(255,255,255,0.85);
  backdrop-filter: blur(8px);
  border-radius: 24px;
  padding: 40px 50px;
  box-shadow: 0 16px 50px var(--shadow);
  border: 1px solid rgba(255,160,175,0.3);
  text-align: center;
  min-height: 80px;
  min-width: min(340px, 80vw);
  display: flex; align-items: center; justify-content: center;
}

.intro-typing {
  font-family: var(--font-fancy);
  font-size: clamp(1.4rem, 4vw, 2.2rem);
  color: var(--pink-dark);
  line-height: 1.6;
}

.btn-gift {
  background: linear-gradient(135deg, #f4a0b8, #e07a9a, #c9637f);
  color: white;
  border: none; border-radius: 999px;
  padding: 18px 50px;
  font-family: var(--font-fancy);
  font-size: clamp(1.1rem, 3vw, 1.4rem);
  font-weight: 700;
  cursor: pointer;
  box-shadow: 0 10px 30px rgba(200,100,130,0.4), 0 0 0 4px rgba(255,160,175,0.2);
  transition: all 0.3s ease;
  animation: giftPulse 2s ease-in-out infinite;
}
@keyframes giftPulse {
  0%,100%{ box-shadow: 0 10px 30px rgba(200,100,130,0.4), 0 0 0 4px rgba(255,160,175,0.2); }
  50%{ box-shadow: 0 14px 40px rgba(200,100,130,0.6), 0 0 0 8px rgba(255,160,175,0.3); transform: translateY(-3px); }
}

/* ===========================
   SCENE 4: CAKE
=========================== */
#scene-cake {
  background: linear-gradient(145deg, #3a1525 0%, #5a2535 50%, #3a1520 100%);
  flex-direction: column;
}

.cake-overlay {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse at 50% 70%, rgba(255,100,150,0.1), transparent 60%);
}

.cake-wrap {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; align-items: center;
}

.cake-container {
  display: flex; flex-direction: column; align-items: center;
  animation: cakeRise 1s cubic-bezier(0.34,1.56,0.64,1) forwards;
  opacity: 0; transform: translateY(80px) scale(0.8);
}
@keyframes cakeRise {
  to { opacity: 1; transform: translateY(0) scale(1); }
}

.tier {
  display: flex; flex-direction: column; align-items: center;
}

.tier-top .tier-body {
  width: clamp(110px, 30vw, 160px);
  height: clamp(55px, 12vw, 80px);
  background: linear-gradient(135deg, #fff0f5, #ffe0ec, #ffd0e6);
  border-radius: 12px 12px 0 0;
  border: 2px solid rgba(255,180,200,0.5);
  position: relative;
  overflow: visible;
  display: flex; align-items: flex-end; justify-content: center;
  padding-bottom: 8px;
  box-shadow: 0 -4px 20px rgba(255,100,150,0.3);
}

.tier-mid .tier-body {
  width: clamp(155px, 40vw, 210px);
  height: clamp(55px, 12vw, 80px);
  background: linear-gradient(135deg, #ffe8f0, #ffc8de, #ffb0d0);
  border-radius: 4px;
  border: 2px solid rgba(255,160,185,0.6);
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 4px 20px rgba(220,80,130,0.3);
}

.tier-bot .tier-body {
  width: clamp(200px, 52vw, 270px);
  height: clamp(60px, 13vw, 90px);
  background: linear-gradient(135deg, #ffd0e0, #ffb8d0, #ff9cbf);
  border-radius: 4px;
  border: 2px solid rgba(255,140,170,0.6);
  display: flex; align-items: center; justify-content: center;
  box-shadow: 0 4px 25px rgba(200,60,120,0.4);
}

.tier-base {
  height: 12px;
  background: linear-gradient(90deg, #c9637f, #e07a9a, #c9637f);
  border-radius: 0 0 4px 4px;
}
.tier-top .tier-base { width: clamp(120px, 32vw, 170px); }
.tier-mid .tier-base { width: clamp(165px, 42vw, 220px); }
.tier-bot .tier-base { width: clamp(210px, 54vw, 280px); }

.tier-deco {
  width: 100%; height: 8px;
  background: repeating-linear-gradient(90deg, #ffb8d0 0px, #ffb8d0 10px, #ff8fb0 10px, #ff8fb0 20px);
  border-radius: 8px 8px 0 0;
}

.tier-decor {
  font-family: var(--font-fancy);
  font-size: clamp(0.65rem, 1.8vw, 0.9rem);
  color: #8a2040;
  font-weight: 700;
  text-align: center;
  text-shadow: 0 1px 2px rgba(255,255,255,0.5);
}

.cake-plate {
  width: clamp(240px, 62vw, 320px);
  height: 16px;
  background: linear-gradient(90deg, #e8b0c0, #f0c8d8, #e8b0c0);
  border-radius: 999px;
  box-shadow: 0 4px 15px rgba(180,80,120,0.3), 0 8px 25px rgba(0,0,0,0.2);
}

/* Candles */
.candles-row { display: flex; gap: 16px; justify-content: center; }
.candle-slot { display: flex; flex-direction: column; align-items: center; gap: 2px; }
.candle {
  width: 10px; height: 36px;
  background: linear-gradient(to bottom, #fffacd, #ffd700, #ffa500);
  border-radius: 3px 3px 0 0;
  position: relative;
}
.candle::before {
  content: '';
  position: absolute; top: -4px; left: 50%; transform: translateX(-50%);
  width: 2px; height: 8px;
  background: #333; border-radius: 1px;
}
.candle-num {
  font-family: var(--font-display);
  font-size: 0.6rem;
  color: rgba(255,255,255,0.7);
}

.flame {
  position: absolute; top: -22px; left: 50%; transform: translateX(-50%);
  width: 14px; height: 22px;
  background: radial-gradient(ellipse at 50% 80%, #fff 0%, #ffeb3b 30%, #ff9800 60%, rgba(255,80,0,0) 100%);
  border-radius: 50% 50% 30% 30%;
  opacity: 0;
  box-shadow: 0 0 10px 4px rgba(255,200,0,0.6), 0 0 20px 8px rgba(255,150,0,0.3);
  animation: none;
}
.flame.lit {
  opacity: 1;
  animation: flicker 0.3s ease-in-out infinite alternate;
}
@keyframes flicker {
  from { transform: translateX(-50%) scaleY(1) scaleX(1); }
  to   { transform: translateX(-50%) scaleY(1.12) scaleX(0.9); }
}

/* Balloons */
.balloons { position: absolute; bottom: 0; left: 0; right: 0; height: 100%; pointer-events: none; }
.balloon {
  position: absolute; bottom: -120px;
  width: clamp(45px, 8vw, 65px); height: clamp(55px, 10vw, 80px);
  border-radius: 50%;
  animation: balloonRise linear forwards;
}
.balloon::after {
  content: '';
  position: absolute; bottom: -30px; left: 50%; transform: translateX(-50%);
  width: 1px; height: 30px;
  background: rgba(150,80,100,0.6);
}
@keyframes balloonRise {
  to { transform: translateY(-110vh); }
}

/* Confetti */
.confetti-container { position: absolute; inset: 0; pointer-events: none; }
.confetti-piece {
  position: absolute; top: -20px;
  width: 8px; height: 12px;
  border-radius: 2px;
  animation: confettiFall linear forwards;
}
@keyframes confettiFall {
  to { transform: translateY(110vh) rotate(720deg); opacity: 0; }
}

/* Stars */
.stars-container { position: absolute; inset: 0; pointer-events: none; }
.star {
  position: absolute;
  font-size: 1.2rem;
  animation: starTwinkle 1.5s ease-in-out infinite;
}
@keyframes starTwinkle {
  0%,100%{ opacity:0.3; transform:scale(0.8); }
  50%{ opacity:1; transform:scale(1.2); }
}

/* ===========================
   SCENE 5: LETTER
=========================== */
#scene-letter {
  background: linear-gradient(145deg, #fce8ef 0%, #fff5f0 100%);
  overflow: auto;
}

.letter-bg {
  position: absolute; inset: 0;
  background: radial-gradient(ellipse at 40% 40%, rgba(255,200,210,0.3), transparent 60%),
              radial-gradient(ellipse at 80% 80%, rgba(255,180,195,0.2), transparent 50%);
}

.envelope-wrap {
  position: relative; z-index: 2;
  display: flex; align-items: center; justify-content: center;
}
.envelope {
  width: clamp(180px, 45vw, 280px);
  height: clamp(120px, 30vw, 190px);
  position: relative;
  cursor: pointer;
  transition: transform 0.3s;
  animation: envFloat 3s ease-in-out infinite;
}
@keyframes envFloat { 0%,100%{transform:translateY(0);} 50%{transform:translateY(-12px);} }

.envelope-body {
  width: 100%; height: 100%;
  background: linear-gradient(145deg, #fff0f5, #ffe8f0);
  border-radius: 8px;
  border: 2px solid rgba(255,160,180,0.6);
  box-shadow: 0 20px 50px var(--shadow);
  display: flex; align-items: center; justify-content: center;
}
.envelope-flap {
  position: absolute; top: 0; left: 0; right: 0;
  height: 55%;
  background: linear-gradient(180deg, #ffd0e0, #ffc0d5);
  clip-path: polygon(0 0, 100% 0, 50% 65%);
  border-radius: 8px 8px 0 0;
  z-index: 1;
  transition: transform 0.6s ease;
  transform-origin: top center;
}
.envelope.open .envelope-flap { transform: rotateX(180deg); }
.envelope-seal { font-size: clamp(2rem, 5vw, 3rem); z-index: 2; position: relative; }

/* Letter Paper */
.letter-paper {
  position: relative; z-index: 2;
  width: min(560px, 92vw);
  max-height: 80vh;
  background:
    url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100' height='100'%3E%3Crect fill='%23fff8f0' width='100' height='100'/%3E%3C/svg%3E"),
    linear-gradient(180deg, #fffbf8 0%, #fff8f2 100%);
  border-radius: 4px;
  box-shadow:
    0 25px 60px rgba(180,80,120,0.2),
    inset 0 0 50px rgba(255,200,180,0.1),
    0 0 0 1px rgba(200,150,130,0.3);
  overflow-y: auto;
  border: 1px solid rgba(200,150,150,0.3);
  animation: letterOpen 0.7s cubic-bezier(0.34,1.56,0.64,1) forwards;
}
@keyframes letterOpen {
  from { opacity: 0; transform: scale(0.7) translateY(30px); }
  to   { opacity: 1; transform: scale(1) translateY(0); }
}

/* Vintage border */
.letter-paper::before {
  content: '';
  position: absolute; inset: 12px;
  border: 1.5px dashed rgba(200,150,150,0.3);
  border-radius: 2px;
  pointer-events: none;
  z-index: 0;
}

.letter-corner {
  position: sticky;
  font-size: 1.4rem;
  opacity: 0.6;
  z-index: 1;
}
.lc-tl { top: 14px; left: 14px; float: left; }
.lc-tr { top: 14px; right: 14px; float: right; }
.lc-bl { bottom: 14px; left: 14px; float: left; }
.lc-br { bottom: 14px; right: 14px; float: right; }

.letter-inner {
  position: relative; z-index: 1;
  padding: clamp(30px, 6vw, 50px) clamp(30px, 7vw, 55px);
}

.letter-heading {
  font-family: var(--font-fancy);
  font-size: clamp(1.3rem, 3.5vw, 1.9rem);
  color: var(--pink-dark);
  text-align: center;
  margin-bottom: 28px;
  line-height: 1.4;
}

.letter-body-text {
  font-family: var(--font-fancy);
  font-size: clamp(0.95rem, 2.4vw, 1.15rem);
  color: var(--text-dark);
  line-height: 2;
  white-space: pre-wrap;
}

.letter-sign {
  font-family: var(--font-script);
  font-size: clamp(1.3rem, 3.5vw, 1.9rem);
  color: var(--pink-dark);
  text-align: right;
  margin-top: 24px;
}

.btn-next-letter {
  display: block;
  margin: 20px auto 30px;
  padding: 14px 40px;
  background: linear-gradient(135deg, var(--pink-mid), var(--pink-deep));
  color: white; border: none; border-radius: 999px;
  font-family: var(--font-fancy); font-size: 1.05rem; font-weight: 600;
  cursor: pointer;
  box-shadow: 0 8px 20px var(--shadow);
  transition: all 0.3s;
}
.btn-next-letter:hover { transform: translateY(-2px); box-shadow: 0 12px 28px var(--shadow); }

/* Letter scrollbar */
.letter-paper::-webkit-scrollbar { width: 6px; }
.letter-paper::-webkit-scrollbar-track { background: rgba(255,220,230,0.2); }
.letter-paper::-webkit-scrollbar-thumb { background: var(--pink-soft); border-radius: 3px; }

/* ===========================
   SCENE 6: VIDEO
=========================== */
#scene-video {
  background: linear-gradient(145deg, #fce4ed 0%, #fff0f5 100%);
  flex-direction: column;
  gap: 30px;
}

.video-wrap {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; align-items: center; gap: 24px;
  width: min(660px, 94vw);
}

.video-intro {
  font-family: var(--font-fancy);
  font-size: clamp(1.4rem, 4vw, 2rem);
  color: var(--pink-dark);
  text-align: center;
  animation: fadeInUp 0.6s ease;
}

.video-player-box {
  width: 100%; position: relative;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 20px 60px var(--shadow), 0 0 0 4px rgba(255,160,175,0.3);
}

#birthdayVideo {
  width: 100%; display: block; border-radius: 20px;
  background: #1a0810;
  min-height: 200px;
}

.video-placeholder-overlay {
  position: absolute; inset: 0;
  background: linear-gradient(145deg, #3a1525, #5a2535);
  display: flex; flex-direction: column; align-items: center; justify-content: center;
  gap: 14px; color: white; text-align: center; padding: 40px;
  border-radius: 20px;
}
.vp-icon { font-size: 3.5rem; }
.video-placeholder-overlay p {
  font-family: var(--font-fancy); font-size: 1.4rem; color: #ffb8d0;
}
.video-placeholder-overlay small { color: rgba(255,180,200,0.6); font-size: 0.85rem; }
.video-placeholder-overlay code {
  background: rgba(255,255,255,0.1); padding: 2px 6px; border-radius: 4px;
  font-family: monospace; color: #ffcce0;
}

.btn-skip-video {
  margin-top: 10px; padding: 12px 32px;
  background: linear-gradient(135deg, var(--pink-mid), var(--pink-deep));
  color: white; border: none; border-radius: 999px;
  font-family: var(--font-fancy); font-size: 1rem; font-weight: 600;
  cursor: pointer; box-shadow: 0 6px 18px rgba(200,80,120,0.4);
  transition: all 0.3s;
}
.btn-skip-video:hover { transform: translateY(-2px); }

/* ===========================
   SCENE 7: VOUCHER
=========================== */
#scene-voucher {
  background: linear-gradient(145deg, #fde8ef 0%, #fff5f0 100%);
}

.voucher-wrap {
  position: relative; z-index: 2;
  display: flex; flex-direction: column; align-items: center; gap: 28px;
  animation: voucherSlide 0.8s cubic-bezier(0.34,1.56,0.64,1) forwards;
  opacity: 0; transform: translateY(60px);
}
@keyframes voucherSlide {
  to { opacity: 1; transform: translateY(0); }
}

.voucher {
  display: flex; align-items: stretch;
  background: linear-gradient(135deg, #fff0f5 0%, #ffe8f0 50%, #fff0f5 100%);
  border: 2.5px solid rgba(255,150,180,0.5);
  border-radius: 20px;
  width: min(500px, 92vw);
  box-shadow: 0 20px 60px var(--shadow), 0 0 30px rgba(255,160,180,0.2);
  position: relative; overflow: hidden;
}
.voucher::before {
  content: '';
  position: absolute; inset: 6px;
  border: 1px dashed rgba(255,140,170,0.5);
  border-radius: 16px;
  pointer-events: none;
}

/* Shimmer */
.voucher-shine {
  position: absolute;
  top: -50%; left: -60%;
  width: 60%; height: 200%;
  background: linear-gradient(105deg, transparent 30%, rgba(255,255,255,0.5) 50%, transparent 70%);
  animation: voucherShine 3s ease-in-out infinite;
  pointer-events: none;
}
@keyframes voucherShine {
  0%   { left: -60%; }
  50%, 100% { left: 120%; }
}

.voucher-left, .voucher-right {
  width: 60px; display: flex; align-items: center; justify-content: center;
  background: linear-gradient(180deg, #ffd0e0, #ffb8d0);
  font-size: 1.8rem;
  flex-shrink: 0;
}
.voucher-left { border-radius: 16px 0 0 16px; border-right: 2px dashed rgba(255,160,180,0.6); }
.voucher-right { border-radius: 0 16px 16px 0; border-left: 2px dashed rgba(255,160,180,0.6); }

.voucher-main {
  flex: 1; padding: 24px 20px;
  display: flex; flex-direction: column; gap: 10px;
  text-align: center;
}

.voucher-floral-top, .voucher-floral-bot { font-size: 1rem; letter-spacing: 4px; }
.voucher-label {
  font-family: var(--font-display);
  font-size: clamp(0.9rem, 2.5vw, 1.2rem);
  color: var(--pink-dark);
  letter-spacing: 2px;
}
.voucher-divider {
  height: 1px; background: linear-gradient(90deg, transparent, var(--pink-mid), transparent);
}
.voucher-desc {
  font-family: var(--font-fancy);
  font-size: clamp(0.85rem, 2.2vw, 1rem);
  color: var(--text-mid); line-height: 1.6;
}
.voucher-info {
  display: flex; flex-direction: column; gap: 4px;
  background: rgba(255,220,230,0.3); border-radius: 10px; padding: 12px;
}
.voucher-info div { font-size: 0.85rem; color: var(--text-mid); }
.voucher-info span { color: var(--text-light); margin-right: 4px; }
.voucher-info strong { color: var(--pink-dark); }

.btn-claim {
  padding: 18px 56px;
  background: linear-gradient(135deg, #f4a0b8, #e07a9a, #c9637f);
  color: white; border: none; border-radius: 999px;
  font-family: var(--font-fancy); font-size: clamp(1.05rem, 3vw, 1.3rem); font-weight: 700;
  cursor: pointer;
  box-shadow: 0 10px 30px rgba(200,80,130,0.45);
  transition: all 0.3s;
  animation: claimPulse 2s ease-in-out infinite;
}
@keyframes claimPulse {
  0%,100%{ transform: scale(1); }
  50%{ transform: scale(1.04); }
}
.btn-claim:hover { transform: translateY(-3px) scale(1.03); box-shadow: 0 15px 40px rgba(200,80,130,0.55); }

/* ===========================
   SCENE 8: FINAL
=========================== */
#scene-final {
  background: linear-gradient(145deg, #fce0ec 0%, #fff0f8 50%, #fde4ef 100%);
  flex-direction: column;
}

.final-bg {
  position: absolute; inset: 0;
  background:
    radial-gradient(ellipse at 20% 30%, rgba(255,180,200,0.4), transparent 50%),
    radial-gradient(ellipse at 80% 70%, rgba(255,160,185,0.35), transparent 50%),
    radial-gradient(ellipse at 50% 50%, rgba(255,240,248,0.5), transparent 70%);
}

/* Fairy lights */
.fairy-lights {
  position: absolute; top: 0; left: 0; right: 0; height: 60px;
  display: flex; gap: 16px; align-items: center; padding: 0 20px;
  z-index: 2;
  flex-wrap: wrap;
}
.fairy-light {
  width: 10px; height: 14px; border-radius: 50%;
  animation: lightGlow 1.5s ease-in-out infinite;
  position: relative;
}
.fairy-light::before {
  content: '';
  position: absolute; top: -6px; left: 50%; transform: translateX(-50%);
  width: 1px; height: 8px; background: rgba(150,100,100,0.4);
}
@keyframes lightGlow {
  0%,100%{ opacity:0.5; box-shadow: 0 0 4px 2px currentColor; }
  50%{ opacity:1; box-shadow: 0 0 10px 5px currentColor; }
}

.final-petals, .sparkles { position: absolute; inset: 0; pointer-events: none; z-index: 1; }

.sparkle {
  position: absolute;
  font-size: clamp(0.8rem, 2vw, 1.3rem);
  animation: sparkleAnim ease-in-out infinite;
}
@keyframes sparkleAnim {
  0%,100%{ opacity:0.2; transform:scale(0.8) rotate(0deg); }
  50%{ opacity:1; transform:scale(1.2) rotate(20deg); }
}

.final-content {
  position: relative; z-index: 3;
  display: flex; flex-direction: column; align-items: center; gap: 20px;
  text-align: center; padding: 20px;
}

.final-flowers-top { font-size: clamp(1.3rem, 4vw, 2rem); letter-spacing: 6px; }

.final-title {
  font-family: var(--font-fancy);
  font-size: clamp(1.4rem, 4vw, 2.2rem);
  color: var(--pink-dark);
  line-height: 1.4;
  animation: fadeInUp 0.8s ease;
}
.final-birthday {
  font-family: var(--font-display);
  font-size: clamp(1.6rem, 5vw, 2.8rem);
  color: var(--pink-deep);
  text-shadow: 0 4px 15px rgba(224,122,154,0.4);
  animation: fadeInUp 0.8s 0.2s ease both;
}
.final-wish {
  font-family: var(--font-script);
  font-size: clamp(1.2rem, 3.5vw, 1.8rem);
  color: var(--text-mid);
  line-height: 1.6;
  animation: fadeInUp 0.8s 0.4s ease both;
}
.final-divider {
  font-size: 1.5rem; letter-spacing: 8px;
  animation: fadeInUp 0.8s 0.5s ease both;
}
.final-credit {
  font-family: var(--font-fancy);
  font-size: clamp(0.9rem, 2.5vw, 1.15rem);
  color: var(--text-light);
  animation: fadeInUp 0.8s 0.6s ease both;
}
.final-credit strong { color: var(--pink-dark); }

.final-confetti { position: absolute; inset: 0; pointer-events: none; z-index: 4; }

@keyframes fadeInUp {
  from { opacity: 0; transform: translateY(25px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ===========================
   RESPONSIVE
=========================== */
@media (max-width: 480px) {
  .verify-card { padding: 45px 24px 32px; }
  .verify-buttons { flex-direction: column; align-items: stretch; }
  .btn-yes, .btn-no { width: 100%; }
  .intro-text-wrap { padding: 28px 24px; }
  .letter-inner { padding: 28px 24px; }
  .voucher-left, .voucher-right { width: 44px; }
}

/* Utility */
.fade-in { animation: fadeInUp 0.6s ease forwards; }

/* ==============================
   BIRTHDAY WEBSITE - script.js
   For: Mayang Aeni (May)
   From: anisnurs
============================== */

// ── GLOBALS ─────────────────────────────────────────────
let currentScene = 'scene-loading';
const music = document.getElementById('bgMusic');
let musicStarted = false;

// ── UTILITY ─────────────────────────────────────────────
function goToScene(targetId) {
  const current = document.querySelector('.scene.active');
  if (current) {
    current.style.transition = 'opacity 0.7s ease';
    current.style.opacity = '0';
    current.style.pointerEvents = 'none';
    setTimeout(() => {
      current.classList.remove('active');
      current.style.opacity = '';
      current.style.pointerEvents = '';
    }, 700);
  }
  setTimeout(() => {
    const next = document.getElementById(targetId);
    if (!next) return;
    next.classList.add('active');
    currentScene = targetId;
    onSceneEnter(targetId);
  }, 600);
}

function onSceneEnter(id) {
  if (id === 'scene-intro')   startIntroScene();
  if (id === 'scene-cake')    startCakeScene();
  if (id === 'scene-letter')  startLetterScene();
  if (id === 'scene-video')   startVideoScene();
  if (id === 'scene-voucher') startVoucherScene();
  if (id === 'scene-final')   startFinalScene();
}

// ── MUSIC ─────────────────────────────────────────────
function tryPlayMusic() {
  if (musicStarted) return;
  music.volume = 0;
  music.play().then(() => {
    musicStarted = true;
    fadeInMusic();
  }).catch(() => {});
}

function fadeInMusic() {
  let vol = 0;
  const interval = setInterval(() => {
    vol = Math.min(vol + 0.02, 0.5);
    music.volume = vol;
    if (vol >= 0.5) clearInterval(interval);
  }, 100);
}

// ── SCENE 1: LOADING ────────────────────────────────────
(function initLoading() {
  const bar = document.getElementById('progressBar');
  let progress = 0;
  const interval = setInterval(() => {
    progress += Math.random() * 3 + 1;
    if (progress >= 100) {
      progress = 100;
      clearInterval(interval);
      bar.style.width = '100%';
      setTimeout(() => goToScene('scene-verify'), 600);
    }
    bar.style.width = progress + '%';
  }, 60);
})();

// ── SCENE 2: VERIFICATION ───────────────────────────────
function verifyYes() {
  tryPlayMusic();
  goToScene('scene-intro');
}
function verifyNo() {
  const btns = document.querySelector('.verify-buttons');
  const denied = document.getElementById('verifyDenied');
  if (btns) btns.style.display = 'none';
  if (denied) denied.classList.remove('hidden');
}

// ── SCENE 3: INTRO ──────────────────────────────────────
function startIntroScene() {
  // Falling petals
  const container = document.getElementById('fallingPetals');
  container.innerHTML = '';
  const petals = ['🌸','🌷','💮','🌺','✿','❀'];
  for (let i = 0; i < 20; i++) {
    const p = document.createElement('div');
    p.className = 'petal';
    p.textContent = petals[Math.floor(Math.random() * petals.length)];
    p.style.left = Math.random() * 100 + '%';
    p.style.animationDuration = (4 + Math.random() * 6) + 's';
    p.style.animationDelay = (Math.random() * 5) + 's';
    p.style.fontSize = (0.8 + Math.random() * 1.2) + 'rem';
    container.appendChild(p);
  }

  // Typing effect
  const lines = ['Hai May...', 'Ada sesuatu untukmu 🎁'];
  const el = document.getElementById('introTyping');
  el.textContent = '';
  let lineIdx = 0, charIdx = 0;

  function typeChar() {
    if (lineIdx >= lines.length) {
      setTimeout(() => {
        const btn = document.getElementById('btnGift');
        btn.classList.remove('hidden');
      }, 600);
      return;
    }
    const line = lines[lineIdx];
    if (charIdx < line.length) {
      el.textContent += line[charIdx];
      charIdx++;
      setTimeout(typeChar, 70);
    } else {
      lineIdx++;
      charIdx = 0;
      if (lineIdx < lines.length) {
        el.textContent += '\n';
        setTimeout(typeChar, 900);
      } else {
        setTimeout(() => {
          const btn = document.getElementById('btnGift');
          btn.classList.remove('hidden');
        }, 600);
      }
    }
  }
  setTimeout(typeChar, 400);
}

// ── SCENE 4: CAKE ───────────────────────────────────────
function startCakeScene() {
  tryPlayMusic();
  const container = document.getElementById('cakeContainer');
  container.style.animation = 'none';
  container.style.opacity = '0';
  container.style.transform = 'translateY(80px) scale(0.8)';

  setTimeout(() => {
    container.style.transition = 'all 0.9s cubic-bezier(0.34,1.56,0.64,1)';
    container.style.opacity = '1';
    container.style.transform = 'translateY(0) scale(1)';
  }, 200);

  // Light candles one by one
  const flames = document.querySelectorAll('.flame');
  flames.forEach((flame, i) => {
    setTimeout(() => {
      flame.classList.add('lit');
      createStarBurst(flame);
    }, 800 + i * 600);
  });

  // Stars
  const allLit = 800 + flames.length * 600;
  setTimeout(() => {
    spawnStars();
    spawnBalloons();
    spawnConfetti('confetti');
    setTimeout(() => goToScene('scene-letter'), 4000);
  }, allLit + 400);
}

function createStarBurst(el) {
  const sc = document.getElementById('starsContainer');
  for (let i = 0; i < 5; i++) {
    const s = document.createElement('div');
    s.textContent = '✨';
    s.style.cssText = `
      position:absolute;
      font-size:${0.8 + Math.random()}rem;
      left:${30 + Math.random() * 40}%;
      top:${20 + Math.random() * 30}%;
      opacity:0;
      animation:sparkleAnim ${1 + Math.random()}s ease-in-out infinite;
      animation-delay:${Math.random() * 0.5}s;
    `;
    sc.appendChild(s);
    setTimeout(() => s.remove(), 3000);
  }
}

function spawnStars() {
  const sc = document.getElementById('starsContainer');
  const emojis = ['✨','⭐','💫','🌟','✦'];
  for (let i = 0; i < 20; i++) {
    const s = document.createElement('div');
    s.className = 'star';
    s.textContent = emojis[Math.floor(Math.random() * emojis.length)];
    s.style.left = Math.random() * 100 + '%';
    s.style.top  = Math.random() * 100 + '%';
    s.style.animationDelay = (Math.random() * 2) + 's';
    sc.appendChild(s);
  }
}

function spawnBalloons() {
  const container = document.getElementById('balloons');
  container.innerHTML = '';
  const colors = [
    'radial-gradient(circle at 35% 35%, #ffb8d0, #e07a9a)',
    'radial-gradient(circle at 35% 35%, #ffd6e8, #f4a0b8)',
    'radial-gradient(circle at 35% 35%, #ffe8f0, #ffc0d5)',
    'radial-gradient(circle at 35% 35%, #ffcce0, #e090a8)',
    'radial-gradient(circle at 35% 35%, #c9a0c8, #a07090)',
  ];
  for (let i = 0; i < 12; i++) {
    const b = document.createElement('div');
    b.className = 'balloon';
    b.style.background = colors[Math.floor(Math.random() * colors.length)];
    b.style.left = (5 + Math.random() * 90) + '%';
    b.style.animationDuration = (4 + Math.random() * 4) + 's';
    b.style.animationDelay = (Math.random() * 2) + 's';
    b.style.opacity = 0.85;
    container.appendChild(b);
  }
}

function spawnConfetti(containerId) {
  const container = document.getElementById(containerId);
  if (!container) return;
  container.innerHTML = '';
  const colors = ['#f4a0b8','#e07a9a','#ffd6e8','#c9a0c8','#ffecd2','#fff0f5','#ffb347'];
  for (let i = 0; i < 60; i++) {
    const c = document.createElement('div');
    c.className = 'confetti-piece';
    c.style.left = Math.random() * 100 + '%';
    c.style.background = colors[Math.floor(Math.random() * colors.length)];
    c.style.width = (6 + Math.random() * 8) + 'px';
    c.style.height = (8 + Math.random() * 10) + 'px';
    c.style.borderRadius = Math.random() > 0.5 ? '50%' : '2px';
    c.style.animationDuration = (2.5 + Math.random() * 3) + 's';
    c.style.animationDelay = (Math.random() * 2.5) + 's';
    c.style.opacity = 0.9;
    container.appendChild(c);
  }
}

// ── SCENE 5: LETTER ─────────────────────────────────────
function startLetterScene() {
  const envWrap = document.getElementById('envelopeWrap');
  const letterPaper = document.getElementById('letterPaper');
  const env = document.getElementById('envelope');

  envWrap.classList.remove('hidden');
  letterPaper.classList.add('hidden');

  // Auto-open envelope after short delay
  setTimeout(() => {
    env.classList.add('open');
    setTimeout(() => {
      envWrap.style.display = 'none';
      letterPaper.classList.remove('hidden');
      typeLetterContent();
    }, 800);
  }, 1000);
}

function typeLetterContent() {
  const letterText = `Sometimes I wonder what my life would look like if I had never met you. And honestly, it would have been a little less colorful, a little less warm, and a lot less meaningful.

You've been there through ordinary days and difficult ones, through laughter, random conversations, and moments when words weren't even necessary. Your presence alone has been a gift.

I don't think I say this enough, but thank you. Thank you for being you. Thank you for your kindness, your patience, your genuine heart, and for making people around you feel loved (gue maksudnya wkwk)

As you celebrate your 29th birthday, my wish for you is simple: may life be gentle with you. May your heart always find reasons to smile. May the love you so freely give to others return to you tenfold. And may you always know that you are deeply appreciated, deeply valued, and deeply loved.

No matter how many birthdays pass, I hope we'll always have the chance to celebrate them together, year after year. 🤍

Happy Birthday, Mayaaangku~

The world is brighter because you're in it. 🌷✨
So please stay by my side as my Westie, and let's continue celebrating life's little moments together. Here's to more adventures, more laughter, and more unforgettable WilliamEst memories in the years ahead. 💖`;

  const el = document.getElementById('letterBodyText');
  el.textContent = '';
  let i = 0;
  const speed = 28;

  function typeNext() {
    if (i < letterText.length) {
      el.textContent += letterText[i];
      i++;
      // Auto-scroll
      const paper = document.getElementById('letterPaper');
      paper.scrollTop = paper.scrollHeight;
      setTimeout(typeNext, speed);
    } else {
      const btn = document.getElementById('btnNextLetter');
      if (btn) btn.style.display = 'block';
    }
  }
  setTimeout(typeNext, 400);
}

// ── SCENE 6: VIDEO ──────────────────────────────────────
function startVideoScene() {
  const video = document.getElementById('birthdayVideo');
  const placeholder = document.getElementById('videoPlaceholder');

  // Try to detect if video source is available
  video.addEventListener('error', () => {
    placeholder.style.display = 'flex';
  }, { once: true });

  video.addEventListener('loadeddata', () => {
    placeholder.style.display = 'none';
  }, { once: true });

  // Auto-advance when video ends
  video.addEventListener('ended', () => {
    setTimeout(() => goToScene('scene-voucher'), 1200);
  }, { once: true });

  // If src is placeholder, show overlay
  fetch('assets/video.mp4', { method: 'HEAD' })
    .catch(() => {
      placeholder.style.display = 'flex';
    });
}

// ── SCENE 7: VOUCHER ────────────────────────────────────
function startVoucherScene() {
  const wrap = document.getElementById('voucherWrap');
  wrap.style.animation = 'none';
  wrap.style.opacity = '0';
  wrap.style.transform = 'translateY(60px)';
  setTimeout(() => {
    wrap.style.transition = 'all 0.8s cubic-bezier(0.34,1.56,0.64,1)';
    wrap.style.opacity = '1';
    wrap.style.transform = 'translateY(0)';
  }, 100);
}

function claimGift() {
  spawnConfetti('confetti2');
  // Big confetti burst
  for (let i = 0; i < 4; i++) {
    setTimeout(() => spawnConfetti('confetti2'), i * 400);
  }
  setTimeout(() => goToScene('scene-final'), 2800);
}

// ── SCENE 8: FINAL ──────────────────────────────────────
function startFinalScene() {
  // Fairy lights
  const fl = document.getElementById('fairyLights');
  fl.innerHTML = '';
  const lightColors = ['#ff9bba','#ffb347','#b0e0e6','#fffacd','#dda0dd','#f4a0b8','#98fb98'];
  for (let i = 0; i < 30; i++) {
    const l = document.createElement('div');
    l.className = 'fairy-light';
    const color = lightColors[Math.floor(Math.random() * lightColors.length)];
    l.style.background = color;
    l.style.color = color;
    l.style.animationDelay = (Math.random() * 2) + 's';
    l.style.animationDuration = (1 + Math.random() * 1.5) + 's';
    fl.appendChild(l);
  }

  // Falling petals (final)
  const fp = document.getElementById('finalPetals');
  fp.innerHTML = '';
  const petals2 = ['🌸','🌷','💮','🌺','✿'];
  for (let i = 0; i < 25; i++) {
    const p = document.createElement('div');
    p.className = 'petal';
    p.textContent = petals2[Math.floor(Math.random() * petals2.length)];
    p.style.left = Math.random() * 100 + '%';
    p.style.animationDuration = (5 + Math.random() * 8) + 's';
    p.style.animationDelay = (Math.random() * 6) + 's';
    p.style.fontSize = (0.8 + Math.random() * 1.3) + 'rem';
    fp.appendChild(p);
  }

  // Sparkles
  const sp = document.getElementById('sparkles');
  sp.innerHTML = '';
  for (let i = 0; i < 16; i++) {
    const s = document.createElement('div');
    s.className = 'sparkle';
    s.textContent = ['✨','💫','⭐','🌟','✦'][Math.floor(Math.random()*5)];
    s.style.left = Math.random() * 100 + '%';
    s.style.top  = Math.random() * 100 + '%';
    s.style.animationDuration = (2 + Math.random() * 2) + 's';
    s.style.animationDelay = (Math.random() * 3) + 's';
    sp.appendChild(s);
  }

  // Final confetti shower
  spawnConfetti('finalConfetti');
  setTimeout(() => spawnConfetti('finalConfetti'), 2000);
  setTimeout(() => spawnConfetti('finalConfetti'), 4500);
}

// ── GLOBAL EVENT: tap anywhere to advance letter ────────
document.addEventListener('click', (e) => {
  // Allow video placeholder button clicks
  if (e.target.closest('.btn-skip-video')) return;
  if (e.target.closest('.btn-claim')) return;
  if (e.target.closest('.btn-gift')) return;
  if (e.target.closest('.btn-next-letter')) return;
  if (e.target.closest('.btn-yes') || e.target.closest('.btn-no') || e.target.closest('.btn-close')) return;

  // Try to play music on any interaction
  tryPlayMusic();
});

// ── PREVENT CONTEXT MENU (optional polish) ──────────────
document.addEventListener('contextmenu', e => e.preventDefault());

console.log('🌷 Happy Birthday, May! Made with love by anisnurs 💖');

# 🌷 Happy Birthday, Mayang Aeni!

Website ulang tahun interaktif bertema **Cute Soft Pink Florist**.

## 📁 Struktur File
```
/
├── index.html
├── style.css
├── script.js
├── README.md
└── assets/
    ├── video.mp4     ← Upload video kamu di sini
    └── music.mp3     ← Upload musik di sini
```

## 🚀 Cara Upload ke GitHub Pages

1. Buat repository baru di GitHub (contoh: `birthday-may`)
2. Upload semua file (index.html, style.css, script.js, assets/)
3. Masuk ke **Settings → Pages**
4. Source: pilih `main` branch → `/root`
5. Klik **Save** → website akan live di:
   `https://username.github.io/birthday-may`

## 🎬 Cara Tambah Video & Musik
- Letakkan file `video.mp4` di folder `assets/`
- Letakkan file `music.mp3` di folder `assets/`
- File ukuran besar? Gunakan [Git LFS](https://git-lfs.github.com/)

## 🌸 Scenes
1. **Loading** — Animasi bunga bermekaran (3 detik)
2. **Verifikasi** — "Apakah kamu Mayang Aeni?"
3. **Gift Intro** — Typing effect + tombol buka hadiah
4. **Birthday Cake** — Kue 3 tingkat + lilin + balon + konfeti
5. **Birthday Letter** — Amplop + surat vintage dengan typing effect
6. **Video Memory** — Video player (letakkan video.mp4 di assets/)
7. **Gift Voucher** — Voucher cantik bisa di-claim
8. **Final Message** — Fairy lights + bunga jatuh + pesan akhir

Made with 💖 by anisnurs

<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Happy Birthday, May 🌷</title>
  <link rel="stylesheet" href="style.css" />
  <link href="https://fonts.googleapis.com/css2?family=Dancing+Script:wght@400;600;700&family=Pacifico&family=Sacramento&family=Lato:wght@300;400&display=swap" rel="stylesheet" />
</head>
<body>

  <!-- ===== SCENE 1: LOADING ===== -->
  <div id="scene-loading" class="scene active">
    <div class="loading-flowers">
      <div class="bloom bloom-1">🌸</div>
      <div class="bloom bloom-2">🌷</div>
      <div class="bloom bloom-3">🌺</div>
      <div class="bloom bloom-4">🌸</div>
      <div class="bloom bloom-5">💐</div>
      <div class="bloom bloom-6">🌷</div>
    </div>
    <div class="loading-content">
      <div class="loading-flower-icon">🌷</div>
      <p class="loading-text">Preparing your birthday surprise...</p>
      <div class="progress-bar-wrap">
        <div class="progress-bar" id="progressBar"></div>
      </div>
      <p class="loading-sub">Please wait a moment ✨</p>
    </div>
  </div>

  <!-- ===== SCENE 2: VERIFICATION ===== -->
  <div id="scene-verify" class="scene">
    <div class="petal-bg"></div>
    <div class="verify-card">
      <div class="verify-flowers">
        <span class="vf vf1">🌷</span>
        <span class="vf vf2">🌸</span>
        <span class="vf vf3">🌺</span>
        <span class="vf vf4">💮</span>
      </div>
      <div class="verify-content">
        <div class="verify-icon">🌷</div>
        <h2 class="verify-title">Hello!</h2>
        <p class="verify-question">Apakah kamu <strong>Mayang Aeni</strong>?</p>
        <div class="verify-buttons">
          <button class="btn-yes" onclick="verifyYes()">Ya, itu aku 💖</button>
          <button class="btn-no" onclick="verifyNo()">Bukan 😅</button>
        </div>
      </div>
      <div id="verifyDenied" class="verify-denied hidden">
        <p>Website ini dibuat khusus untuk <strong>Mayang Aeni</strong>.</p>
        <p>Silakan tutup halaman ini ya 🌸</p>
        <button class="btn-close" onclick="window.close()">Close</button>
      </div>
    </div>
  </div>

  <!-- ===== SCENE 3: GIFT INTRO ===== -->
  <div id="scene-intro" class="scene">
    <div class="florist-bg">
      <div class="falling-petals" id="fallingPetals"></div>
    </div>
    <div class="intro-content">
      <div class="intro-text-wrap">
        <p class="intro-typing" id="introTyping"></p>
      </div>
      <button class="btn-gift hidden" id="btnGift" onclick="goToScene('scene-cake')">
        <span>🎁</span> Buka Hadiah
      </button>
    </div>
  </div>

  <!-- ===== SCENE 4: BIRTHDAY CAKE ===== -->
  <div id="scene-cake" class="scene">
    <div class="cake-overlay"></div>
    <div class="balloons" id="balloons"></div>
    <div class="confetti-container" id="confetti"></div>
    <div class="cake-wrap">
      <div class="cake-container" id="cakeContainer">
        <!-- Tier 3 (top) -->
        <div class="tier tier-top">
          <div class="tier-deco"></div>
          <div class="tier-body">
            <div class="candles-row" id="candlesTop">
              <div class="candle-slot" data-n="0"><div class="candle"><div class="flame" id="f0"></div></div><span class="candle-num">2</span></div>
              <div class="candle-slot" data-n="1"><div class="candle"><div class="flame" id="f1"></div></div><span class="candle-num">9</span></div>
            </div>
          </div>
          <div class="tier-base"></div>
        </div>
        <!-- Tier 2 (middle) -->
        <div class="tier tier-mid">
          <div class="tier-body">
            <div class="tier-decor">🌷 Happy Birthday 🌷</div>
          </div>
          <div class="tier-base"></div>
        </div>
        <!-- Tier 1 (bottom) -->
        <div class="tier tier-bot">
          <div class="tier-body">
            <div class="tier-decor">May 🌸</div>
          </div>
          <div class="tier-base"></div>
        </div>
        <div class="cake-plate"></div>
      </div>
      <div class="stars-container" id="starsContainer"></div>
    </div>
  </div>

  <!-- ===== SCENE 5: LETTER ===== -->
  <div id="scene-letter" class="scene">
    <div class="letter-bg"></div>
    <div class="envelope-wrap" id="envelopeWrap">
      <div class="envelope" id="envelope">
        <div class="envelope-flap"></div>
        <div class="envelope-body">
          <div class="envelope-seal">💌</div>
        </div>
      </div>
    </div>
    <div class="letter-paper hidden" id="letterPaper">
      <div class="letter-corner lc-tl">🌸</div>
      <div class="letter-corner lc-tr">🌷</div>
      <div class="letter-corner lc-bl">💐</div>
      <div class="letter-corner lc-br">🌺</div>
      <div class="letter-inner" id="letterInner">
        <h3 class="letter-heading">Happy Birthday, My Dearest May 🤍</h3>
        <div class="letter-body-text" id="letterBodyText"></div>
        <p class="letter-sign">With all my love,<br><strong>anisnurs</strong> 🌷</p>
      </div>
      <button class="btn-next-letter" id="btnNextLetter" onclick="goToScene('scene-video')" style="display:none">Lanjut ➜</button>
    </div>
  </div>

  <!-- ===== SCENE 6: VIDEO ===== -->
  <div id="scene-video" class="scene">
    <div class="florist-bg"></div>
    <div class="video-wrap">
      <p class="video-intro">One more thing... 🌷</p>
      <div class="video-player-box">
        <video id="birthdayVideo" controls playsinline preload="metadata">
          <source src="assets/video.mp4" type="video/mp4" />
          <div class="video-placeholder">
            <span>🎬</span>
            <p>Video akan segera hadir</p>
          </div>
        </video>
        <div class="video-placeholder-overlay" id="videoPlaceholder">
          <span class="vp-icon">🎬</span>
          <p>Video Memory</p>
          <small>Letakkan file <code>video.mp4</code> di folder <code>assets/</code></small>
          <button class="btn-skip-video" onclick="goToScene('scene-voucher')">Lanjut ke Hadiah ➜</button>
        </div>
      </div>
    </div>
  </div>

  <!-- ===== SCENE 7: VOUCHER ===== -->
  <div id="scene-voucher" class="scene">
    <div class="florist-bg"></div>
    <div class="confetti-container" id="confetti2"></div>
    <div class="voucher-wrap" id="voucherWrap">
      <div class="voucher" id="voucher">
        <div class="voucher-left">
          <span class="voucher-icon">🎁</span>
        </div>
        <div class="voucher-main">
          <div class="voucher-floral-top">🌸 ✨ 🌷 ✨ 🌸</div>
          <p class="voucher-label">BIRTHDAY GIFT VOUCHER</p>
          <div class="voucher-divider"></div>
          <p class="voucher-desc">Bawa kupon ini untuk menukarkan<br>dengan hadiah ulang tahun mu</p>
          <div class="voucher-info">
            <div><span>Untuk:</span> <strong>Mayang Aeni</strong></div>
            <div><span>Dari:</span> <strong>anisnurs</strong></div>
            <div><span>Valid:</span> <strong>Anytime you want 💖</strong></div>
          </div>
          <div class="voucher-floral-bot">🌺 🌷 💮 🌷 🌺</div>
        </div>
        <div class="voucher-right">
          <span class="voucher-icon">🎀</span>
        </div>
      </div>
      <div class="voucher-shine"></div>
      <button class="btn-claim" id="btnClaim" onclick="claimGift()">Claim Your Gift 🎁</button>
    </div>
  </div>

  <!-- ===== SCENE 8: FINAL ===== -->
  <div id="scene-final" class="scene">
    <div class="final-bg"></div>
    <div class="fairy-lights" id="fairyLights"></div>
    <div class="final-petals" id="finalPetals"></div>
    <div class="sparkles" id="sparkles"></div>
    <div class="final-content">
      <div class="final-flowers-top">🌸 🌷 💐 🌷 🌸</div>
      <h1 class="final-title">Thank you for being part of my life 🌷</h1>
      <h2 class="final-birthday">Happy 29th Birthday, Mayaang 💖</h2>
      <p class="final-wish">May all your dreams bloom beautifully,<br>just like these flowers.</p>
      <div class="final-divider">✨ 🌷 ✨</div>
      <p class="final-credit">Made with love by <strong>anisnurs</strong> 💖</p>
    </div>
    <div class="final-confetti" id="finalConfetti"></div>
  </div>

  <!-- Audio -->
  <audio id="bgMusic" loop>
    <source src="assets/music.mp3" type="audio/mpeg" />
  </audio>

  <script src="script.js"></script>
</body>
</html>
