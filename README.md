<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Hulk Gym – Dombivli East's most affordable, beginner-friendly gym. Expert trainers, excellent facilities. Near Grampanchayat Office, Gavdevi Mandir Road, Dombivli East.">
  <meta name="keywords" content="Hulk Gym, gym Dombivli East, affordable gym Kalyan, beginner gym, personal training Dombivli, fitness center Maharashtra">
  <meta name="theme-color" content="#080808">
  <title>Hulk Gym | Best Gym in Dombivli East</title>

  <!-- Preconnect for fonts -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet">

  <style>
    /* ============================================================
       RESET
    ============================================================ */
    *, *::before, *::after {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
      overflow-x: hidden;
    }

    body {
      overflow-x: hidden;
      background-color: #080808;
      color: #E5E5E5;
      font-family: 'DM Sans', sans-serif;
      font-size: 16px;
      line-height: 1.65;
      -webkit-font-smoothing: antialiased;
      -moz-osx-font-smoothing: grayscale;
    }

    img, svg { display: block; max-width: 100%; }
    a { color: inherit; text-decoration: none; }
    ul, ol { list-style: none; }
    button { font-family: inherit; cursor: pointer; border: none; background: none; }

    /* ============================================================
       DESIGN TOKENS
    ============================================================ */
    :root {
      --c-gold:        #F5C518;
      --c-gold-dim:    rgba(245,197,24,0.10);
      --c-gold-glow:   rgba(245,197,24,0.28);
      --c-gold-border: rgba(245,197,24,0.22);
      --c-black:       #080808;
      --c-s1:          #101010;
      --c-s2:          #161616;
      --c-s3:          #1E1E1E;
      --c-s4:          #282828;
      --c-border:      rgba(255,255,255,0.07);
      --c-t1:          #F0F0F0;
      --c-t2:          #A0A0A0;
      --c-t3:          #606060;
      --f-display:     'Oswald', sans-serif;
      --f-body:        'DM Sans', sans-serif;
      --ease:          cubic-bezier(0.22, 1, 0.36, 1);
      --nav-h:         68px;
      --radius:        8px;
      --radius-lg:     14px;
    }

    /* ============================================================
       SCROLLBAR
    ============================================================ */
    ::-webkit-scrollbar { width: 4px; }
    ::-webkit-scrollbar-track { background: var(--c-black); }
    ::-webkit-scrollbar-thumb { background: var(--c-gold); border-radius: 4px; }

    /* ============================================================
       LAYOUT HELPERS
    ============================================================ */
    .w {
      width: min(1160px, 92%);
      margin-inline: auto;
    }

    section {
      padding-top: 96px;
      padding-bottom: 96px;
      /* no overflow:hidden here – prevents scrollbar bugs */
    }

    /* ============================================================
       TYPOGRAPHY COMPONENTS
    ============================================================ */
    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      font-family: var(--f-display);
      font-size: 0.72rem;
      font-weight: 400;
      letter-spacing: 0.25em;
      text-transform: uppercase;
      color: var(--c-gold);
      margin-bottom: 16px;
    }
    .eyebrow::before {
      content: '';
      display: block;
      width: 26px;
      height: 2px;
      background: var(--c-gold);
      flex-shrink: 0;
    }

    .section-title {
      font-family: var(--f-display);
      font-size: clamp(2rem, 4.2vw, 3.4rem);
      font-weight: 700;
      line-height: 1.06;
      letter-spacing: 0.01em;
      color: var(--c-t1);
    }
    .section-title .hi { color: var(--c-gold); }

    .section-sub {
      font-size: 1rem;
      font-weight: 300;
      color: var(--c-t2);
      line-height: 1.75;
      margin-top: 14px;
      max-width: 520px;
    }

    .gold-rule {
      display: block;
      width: 44px;
      height: 3px;
      background: var(--c-gold);
      border-radius: 2px;
      margin-top: 20px;
      margin-bottom: 22px;
    }

    /* ============================================================
       BUTTONS
    ============================================================ */
    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      font-family: var(--f-display);
      font-size: 0.85rem;
      font-weight: 500;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      border-radius: var(--radius);
      padding: 0.85rem 1.9rem;
      white-space: nowrap;
      transition: transform 0.25s var(--ease),
                  box-shadow 0.25s var(--ease),
                  background 0.25s,
                  color 0.25s,
                  border-color 0.25s;
    }
    .btn:focus-visible {
      outline: 2px solid var(--c-gold);
      outline-offset: 3px;
    }
    .btn-gold {
      background: var(--c-gold);
      color: #080808;
    }
    .btn-gold:hover {
      background: #ffd740;
      transform: translateY(-2px);
      box-shadow: 0 12px 36px var(--c-gold-glow);
    }
    .btn-outline {
      background: transparent;
      color: var(--c-t1);
      border: 1.5px solid rgba(255,255,255,0.18);
    }
    .btn-outline:hover {
      border-color: var(--c-gold);
      color: var(--c-gold);
      transform: translateY(-2px);
    }
    .btn-dark {
      background: #080808;
      color: var(--c-gold);
      border: 1.5px solid #080808;
    }
    .btn-dark:hover {
      background: #141414;
      transform: translateY(-2px);
      box-shadow: 0 12px 32px rgba(0,0,0,0.6);
    }
    .btn-dark-outline {
      background: transparent;
      color: #080808;
      border: 1.5px solid rgba(0,0,0,0.35);
    }
    .btn-dark-outline:hover {
      background: rgba(0,0,0,0.08);
      transform: translateY(-2px);
    }

    /* ============================================================
       SCROLL REVEAL
    ============================================================ */
    .reveal {
      opacity: 0;
      transform: translateY(32px);
      transition: opacity 0.6s var(--ease), transform 0.6s var(--ease);
    }
    .reveal.from-left  { transform: translateX(-32px); }
    .reveal.from-right { transform: translateX(32px); }
    .reveal.visible {
      opacity: 1;
      transform: translate(0, 0);
    }

    /* ============================================================
       NAV
    ============================================================ */
    #nav {
      position: fixed;
      inset: 0 0 auto 0;
      z-index: 1000;
      height: var(--nav-h);
      transition: background 0.35s var(--ease), box-shadow 0.35s var(--ease);
    }
    #nav.scrolled {
      background: rgba(8,8,8,0.97);
      backdrop-filter: blur(20px);
      -webkit-backdrop-filter: blur(20px);
      box-shadow: 0 1px 0 var(--c-border);
    }
    .nav-inner {
      height: var(--nav-h);
      display: flex;
      align-items: center;
      justify-content: space-between;
    }
    .nav-logo {
      font-family: var(--f-display);
      font-size: 1.6rem;
      font-weight: 700;
      letter-spacing: 0.05em;
      color: var(--c-t1);
      line-height: 1;
    }
    .nav-logo span { color: var(--c-gold); }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.8rem;
    }
    .nav-links a {
      font-family: var(--f-display);
      font-size: 0.78rem;
      font-weight: 400;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--c-t2);
      position: relative;
      padding-bottom: 2px;
      transition: color 0.2s;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: 0; left: 0;
      width: 0; height: 1.5px;
      background: var(--c-gold);
      transition: width 0.3s var(--ease);
    }
    .nav-links a:hover       { color: var(--c-gold); }
    .nav-links a:hover::after { width: 100%; }

    .nav-cta { padding: 0.58rem 1.4rem; font-size: 0.76rem; }

    /* Hamburger */
    .burger {
      display: none;
      flex-direction: column;
      gap: 5px;
      padding: 4px;
      background: none;
      border: none;
    }
    .burger span {
      display: block;
      width: 24px; height: 2px;
      background: var(--c-t1);
      border-radius: 2px;
      transition: transform 0.28s, opacity 0.28s;
    }
    .burger.open span:nth-child(1) { transform: rotate(45deg) translate(5px,5px); }
    .burger.open span:nth-child(2) { opacity: 0; width: 0; }
    .burger.open span:nth-child(3) { transform: rotate(-45deg) translate(5px,-5px); }

    /* Mobile drawer */
    #drawer {
      display: none;
      position: fixed;
      inset: var(--nav-h) 0 0 0;
      z-index: 999;
      background: rgba(8,8,8,0.99);
      backdrop-filter: blur(24px);
      flex-direction: column;
      padding: 2rem 1.5rem 3rem;
      overflow-y: auto;
      overflow-x: hidden;
    }
    #drawer.open { display: flex; }
    #drawer a {
      font-family: var(--f-display);
      font-size: 1.6rem;
      font-weight: 600;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      color: var(--c-t2);
      padding: 0.95rem 0;
      border-bottom: 1px solid var(--c-border);
      transition: color 0.2s;
    }
    #drawer a:hover { color: var(--c-gold); }
    #drawer .btn { margin-top: 1.8rem; width: 100%; }

    /* ============================================================
       HERO
    ============================================================ */
    #hero {
      min-height: 100svh;
      display: flex;
      align-items: center;
      position: relative;
      padding-top: 0;
      padding-bottom: 0;
      overflow: hidden;
    }

    .hero-bg {
      position: absolute;
      inset: 0;
      z-index: 0;
      pointer-events: none;
    }
    /* Diagonal grid lines */
    .hero-bg::before {
      content: '';
      position: absolute;
      inset: 0;
      background-image:
        linear-gradient(rgba(255,255,255,0.025) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,0.025) 1px, transparent 1px);
      background-size: 64px 64px;
    }
    /* Radial gold glow right side */
    .hero-bg::after {
      content: '';
      position: absolute;
      right: -15%;
      top: 50%;
      transform: translateY(-50%);
      width: 70vw;
      height: 70vw;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(245,197,24,0.06) 0%, transparent 65%);
    }
    /* Fade bottom */
    .hero-fade {
      position: absolute;
      bottom: 0; left: 0; right: 0;
      height: 220px;
      background: linear-gradient(to top, #080808 0%, transparent 100%);
      pointer-events: none;
      z-index: 1;
    }

    /* Big background word */
    .hero-word {
      position: absolute;
      right: -3%;
      top: 50%;
      transform: translateY(-50%);
      font-family: var(--f-display);
      font-size: clamp(9rem, 22vw, 24rem);
      font-weight: 700;
      letter-spacing: -0.03em;
      color: rgba(255,255,255,0.016);
      line-height: 1;
      pointer-events: none;
      user-select: none;
      white-space: nowrap;
      z-index: 0;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      padding-top: calc(var(--nav-h) + 2.5rem);
      padding-bottom: 5rem;
    }

    .hero-pill {
      display: inline-flex;
      align-items: center;
      gap: 9px;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: 100px;
      padding: 6px 15px;
      font-family: var(--f-display);
      font-size: 0.7rem;
      font-weight: 400;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--c-gold);
      margin-bottom: 24px;
      animation: aFadeDown 0.65s both;
    }
    .hero-pill .blink {
      width: 7px; height: 7px;
      border-radius: 50%;
      background: var(--c-gold);
      animation: aPulse 2s infinite;
    }
    @keyframes aPulse {
      0%,100% { opacity:1; transform:scale(1); }
      50%      { opacity:.4; transform:scale(1.5); }
    }
    @keyframes aFadeDown {
      from { opacity:0; transform:translateY(-14px); }
      to   { opacity:1; transform:none; }
    }
    @keyframes aFadeUp {
      from { opacity:0; transform:translateY(22px); }
      to   { opacity:1; transform:none; }
    }

    .hero-h1 {
      font-family: var(--f-display);
      font-size: clamp(2.9rem, 9vw, 7.8rem);
      font-weight: 700;
      line-height: 0.95;
      letter-spacing: 0.015em;
      color: var(--c-t1);
      animation: aFadeUp 0.7s 0.1s both;
    }
    .hero-h1 .gold { color: var(--c-gold); }

    .hero-sub {
      max-width: 500px;
      font-size: clamp(0.95rem, 1.5vw, 1.08rem);
      font-weight: 300;
      color: var(--c-t2);
      line-height: 1.72;
      margin-top: 20px;
      animation: aFadeUp 0.7s 0.2s both;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 34px;
      animation: aFadeUp 0.7s 0.3s both;
    }
    .hero-actions .btn { font-size: 0.9rem; padding: 0.9rem 2rem; }

    .hero-chips {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 48px;
      padding-top: 32px;
      border-top: 1px solid var(--c-border);
      animation: aFadeUp 0.7s 0.4s both;
    }
    .chip {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 7px 14px;
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: 100px;
      font-size: 0.82rem;
      font-weight: 400;
      color: var(--c-t2);
      white-space: nowrap;
      transition: border-color 0.2s, color 0.2s;
    }
    .chip:hover { border-color: var(--c-gold-border); color: var(--c-gold); }

    /* Scroll cue */
    .scroll-cue {
      position: absolute;
      bottom: 2rem;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 6px;
      z-index: 3;
      pointer-events: none;
    }
    .scroll-cue span {
      font-family: var(--f-display);
      font-size: 0.62rem;
      letter-spacing: 0.3em;
      text-transform: uppercase;
      color: var(--c-t3);
    }
    .cue-arrow {
      width: 18px; height: 18px;
      border-right: 1.5px solid var(--c-gold);
      border-bottom: 1.5px solid var(--c-gold);
      transform: rotate(45deg);
      animation: aBounce 2s infinite;
    }
    @keyframes aBounce {
      0%,100% { transform:rotate(45deg) translateY(0); }
      50%      { transform:rotate(45deg) translateY(7px); }
    }

    /* ============================================================
       MARQUEE
    ============================================================ */
    .marquee {
      background: var(--c-gold);
      overflow: hidden;
      padding: 10px 0;
      white-space: nowrap;
    }
    .marquee-track {
      display: inline-flex;
      animation: aMarquee 30s linear infinite;
    }
    .marquee-track:hover { animation-play-state: paused; }
    .m-item {
      font-family: var(--f-display);
      font-size: 0.75rem;
      font-weight: 500;
      letter-spacing: 0.2em;
      text-transform: uppercase;
      color: #080808;
      padding: 0 2.5rem;
    }
    @keyframes aMarquee {
      from { transform: translateX(0); }
      to   { transform: translateX(-50%); }
    }

    /* ============================================================
       ABOUT
    ============================================================ */
    #about { background: var(--c-s1); }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 72px;
      align-items: center;
    }

    /* Placeholder visual */
    .about-visual { position: relative; }

    .about-img {
      width: 100%;
      aspect-ratio: 4/5;
      background: var(--c-s2);
      border-radius: var(--radius-lg);
      border: 1px solid var(--c-border);
      overflow: hidden;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
    }
    .about-img::before {
      content: '';
      position: absolute;
      inset: 0;
      background: repeating-linear-gradient(
        45deg,
        var(--c-s3) 0, var(--c-s3) 1px,
        transparent 1px, transparent 52px
      );
    }
    .about-img .gym-icon {
      position: relative;
      z-index: 1;
      opacity: 0.10;
    }
    .about-img::after {
      content: 'GYM PHOTO';
      position: absolute;
      bottom: 18px;
      left: 50%;
      transform: translateX(-50%);
      font-family: var(--f-display);
      font-size: 0.65rem;
      letter-spacing: 0.3em;
      color: var(--c-t3);
    }

    .about-stars {
      position: absolute;
      bottom: -18px;
      right: -18px;
      background: var(--c-gold);
      border-radius: var(--radius);
      padding: 15px 18px;
      text-align: center;
      box-shadow: 0 10px 36px var(--c-gold-glow);
      z-index: 2;
    }
    .about-stars .num {
      font-family: var(--f-display);
      font-size: 1.75rem;
      font-weight: 700;
      color: #080808;
      line-height: 1;
    }
    .about-stars .lbl {
      font-family: var(--f-display);
      font-size: 0.58rem;
      font-weight: 400;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: rgba(0,0,0,0.55);
      margin-top: 3px;
    }

    .about-text { }
    .about-text p + p { margin-top: 14px; }

    .check-list {
      margin-top: 28px;
      display: flex;
      flex-direction: column;
      gap: 12px;
    }
    .check-list li {
      display: flex;
      align-items: flex-start;
      gap: 12px;
      font-size: 0.95rem;
      font-weight: 300;
      color: var(--c-t2);
    }
    .check-list .ck {
      flex-shrink: 0;
      width: 20px; height: 20px;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 3px;
      color: var(--c-gold);
      font-size: 0.6rem;
      font-weight: 700;
    }

    /* ============================================================
       WHY CHOOSE US
    ============================================================ */
    #why { background: var(--c-black); }

    .center-head {
      text-align: center;
      margin-bottom: 60px;
    }
    .center-head .eyebrow { justify-content: center; }
    .center-head .eyebrow::before { display: none; }
    .center-head .section-title { font-size: clamp(1.9rem, 3.6vw, 3rem); }
    .center-head .section-sub { margin-inline: auto; text-align: center; }

    .why-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }
    .why-card {
      background: var(--c-s1);
      border: 1px solid var(--c-border);
      border-radius: var(--radius-lg);
      padding: 28px 22px;
      position: relative;
      overflow: hidden;
      transition: transform 0.3s var(--ease), border-color 0.3s, box-shadow 0.3s;
    }
    .why-card::before {
      content: '';
      position: absolute;
      top: 0; left: 0;
      width: 3px; height: 0;
      background: var(--c-gold);
      transition: height 0.4s var(--ease);
    }
    .why-card:hover {
      transform: translateY(-7px);
      border-color: var(--c-gold-border);
      box-shadow: 0 22px 50px rgba(0,0,0,0.5);
    }
    .why-card:hover::before { height: 100%; }
    .why-icon {
      width: 50px; height: 50px;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.4rem;
      margin-bottom: 18px;
      transition: background 0.3s;
    }
    .why-card:hover .why-icon { background: rgba(245,197,24,0.18); }
    .why-card h3 {
      font-family: var(--f-display);
      font-size: 0.98rem;
      font-weight: 600;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      color: var(--c-t1);
      margin-bottom: 9px;
    }
    .why-card p {
      font-size: 0.88rem;
      font-weight: 300;
      color: var(--c-t3);
      line-height: 1.65;
    }

    /* ============================================================
       SERVICES
    ============================================================ */
    #services { background: var(--c-s1); }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 18px;
    }
    .svc {
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: var(--radius-lg);
      padding: 32px 28px;
      display: grid;
      grid-template-columns: 60px 1fr;
      gap: 22px;
      align-items: start;
      transition: transform 0.3s var(--ease), border-color 0.3s, box-shadow 0.3s;
    }
    .svc:hover {
      transform: translateY(-4px);
      border-color: var(--c-gold-border);
      box-shadow: 0 18px 44px rgba(0,0,0,0.5);
    }
    .svc-icon {
      width: 60px; height: 60px;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.7rem;
      flex-shrink: 0;
      transition: background 0.3s;
    }
    .svc:hover .svc-icon { background: rgba(245,197,24,0.18); }
    .svc-body h3 {
      font-family: var(--f-display);
      font-size: 1.08rem;
      font-weight: 600;
      letter-spacing: 0.04em;
      text-transform: uppercase;
      color: var(--c-t1);
      margin-bottom: 9px;
    }
    .svc-body p {
      font-size: 0.9rem;
      font-weight: 300;
      color: var(--c-t3);
      line-height: 1.68;
    }

    /* ============================================================
       TIMINGS
    ============================================================ */
    #timings { background: var(--c-black); }

    .timings-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 72px;
      align-items: start;
    }
    .timings-left .section-sub { max-width: 400px; }
    .timings-left .btn { margin-top: 32px; }

    .timetable {
      background: var(--c-s1);
      border: 1px solid var(--c-border);
      border-radius: var(--radius-lg);
      overflow: hidden;
    }
    .timetable-head {
      background: var(--c-gold);
      padding: 13px 22px;
      font-family: var(--f-display);
      font-size: 0.75rem;
      font-weight: 500;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: #080808;
      display: flex;
      align-items: center;
      gap: 8px;
    }
    .trow {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 14px 22px;
      border-top: 1px solid var(--c-border);
      transition: background 0.2s;
    }
    .trow:hover { background: var(--c-s2); }
    .trow-day {
      display: flex;
      align-items: center;
      gap: 10px;
      font-family: var(--f-display);
      font-size: 0.86rem;
      font-weight: 400;
      letter-spacing: 0.07em;
      text-transform: uppercase;
      color: var(--c-t2);
    }
    .trow-day .dot {
      width: 6px; height: 6px;
      border-radius: 50%;
      background: var(--c-gold);
      flex-shrink: 0;
    }
    .trow-time {
      font-family: var(--f-display);
      font-size: 0.86rem;
      font-weight: 500;
      letter-spacing: 0.06em;
      color: var(--c-t1);
    }
    .trow.sunday .trow-day,
    .trow.sunday .trow-time { color: var(--c-gold); }

    /* ============================================================
       TESTIMONIALS
    ============================================================ */
    #reviews { background: var(--c-s1); }

    .rv-grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
      max-width: 840px;
      margin-inline: auto;
    }
    .rv-card {
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: var(--radius-lg);
      padding: 30px;
      position: relative;
      overflow: hidden;
      transition: transform 0.3s var(--ease), border-color 0.3s;
    }
    .rv-card:hover {
      transform: translateY(-4px);
      border-color: var(--c-gold-border);
    }
    .rv-card::before {
      content: '"';
      position: absolute;
      top: -6px; right: 18px;
      font-family: Georgia, serif;
      font-size: 7.5rem;
      line-height: 1;
      color: var(--c-gold);
      opacity: 0.06;
      pointer-events: none;
    }
    .rv-stars {
      display: flex;
      gap: 3px;
      color: var(--c-gold);
      font-size: 0.9rem;
      margin-bottom: 14px;
    }
    .rv-text {
      font-size: 0.96rem;
      font-weight: 300;
      font-style: italic;
      color: var(--c-t2);
      line-height: 1.75;
      margin-bottom: 22px;
    }
    .rv-author {
      display: flex;
      align-items: center;
      gap: 12px;
    }
    .rv-ava {
      width: 40px; height: 40px;
      border-radius: 50%;
      background: var(--c-s3);
      border: 2px solid var(--c-gold-border);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: var(--f-display);
      font-size: 1rem;
      font-weight: 600;
      color: var(--c-gold);
      flex-shrink: 0;
    }
    .rv-name {
      font-family: var(--f-display);
      font-size: 0.9rem;
      font-weight: 500;
      letter-spacing: 0.05em;
      text-transform: uppercase;
      color: var(--c-t1);
    }
    .rv-meta {
      font-size: 0.76rem;
      color: var(--c-t3);
      margin-top: 2px;
    }
    .google-note {
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      margin-top: 40px;
      font-family: var(--f-display);
      font-size: 0.72rem;
      letter-spacing: 0.18em;
      text-transform: uppercase;
      color: var(--c-t3);
    }

    /* ============================================================
       GALLERY
    ============================================================ */
    #gallery { background: var(--c-black); }

    .gallery-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 12px;
    }
    .g-cell {
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: var(--radius-lg);
      overflow: hidden;
      aspect-ratio: 1;
      position: relative;
      cursor: pointer;
      transition: transform 0.3s var(--ease), border-color 0.3s;
    }
    .g-cell:first-child {
      grid-column: span 2;
      aspect-ratio: 2/1;
    }
    .g-cell:hover {
      transform: scale(1.014);
      border-color: var(--c-gold-border);
    }
    .g-inner {
      width: 100%; height: 100%;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      gap: 8px;
      background: repeating-linear-gradient(
        -45deg,
        var(--c-s3) 0, var(--c-s3) 1px,
        transparent 1px, transparent 38px
      ),
      var(--c-s2);
    }
    .g-ico  { font-size: 2.2rem; opacity: 0.14; }
    .g-lbl  {
      font-family: var(--f-display);
      font-size: 0.67rem;
      letter-spacing: 0.24em;
      text-transform: uppercase;
      color: var(--c-t3);
    }
    .g-hover {
      position: absolute;
      inset: 0;
      background: linear-gradient(to top, rgba(8,8,8,0.8) 0%, transparent 55%);
      opacity: 0;
      transition: opacity 0.3s;
      display: flex;
      align-items: flex-end;
      padding: 16px;
    }
    .g-cell:hover .g-hover { opacity: 1; }
    .g-hover span {
      font-family: var(--f-display);
      font-size: 0.78rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--c-t1);
    }

    /* ============================================================
       CTA BAND
    ============================================================ */
    #cta {
      padding-top: 80px;
      padding-bottom: 80px;
      background: var(--c-gold);
      position: relative;
      overflow: hidden;
    }
    #cta::before {
      content: 'HULK';
      position: absolute;
      right: -2%;
      top: 50%;
      transform: translateY(-50%);
      font-family: var(--f-display);
      font-size: clamp(7rem, 18vw, 18rem);
      font-weight: 700;
      color: rgba(0,0,0,0.055);
      letter-spacing: -0.03em;
      pointer-events: none;
      user-select: none;
      line-height: 1;
    }
    .cta-row {
      position: relative;
      z-index: 1;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 32px;
      flex-wrap: wrap;
    }
    .cta-copy h2 {
      font-family: var(--f-display);
      font-size: clamp(1.8rem, 4.2vw, 3.4rem);
      font-weight: 700;
      color: #080808;
      line-height: 1.06;
      letter-spacing: 0.015em;
    }
    .cta-copy p {
      font-size: 1rem;
      color: rgba(0,0,0,0.52);
      margin-top: 7px;
      font-weight: 300;
    }
    .cta-btns { display: flex; gap: 12px; flex-wrap: wrap; }

    /* ============================================================
       CONTACT
    ============================================================ */
    #contact { background: var(--c-s1); }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 68px;
      align-items: start;
    }
    .contact-left .section-sub { max-width: 390px; }

    .c-details {
      display: flex;
      flex-direction: column;
      gap: 22px;
      margin-top: 36px;
    }
    .c-row {
      display: flex;
      align-items: flex-start;
      gap: 15px;
    }
    .c-icon {
      width: 42px; height: 42px;
      flex-shrink: 0;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1rem;
      margin-top: 1px;
    }
    .c-label {
      font-family: var(--f-display);
      font-size: 0.68rem;
      font-weight: 400;
      letter-spacing: 0.22em;
      text-transform: uppercase;
      color: var(--c-gold);
      margin-bottom: 4px;
    }
    .c-val {
      font-size: 0.92rem;
      font-weight: 300;
      color: var(--c-t2);
      line-height: 1.55;
    }
    .c-val a {
      color: var(--c-t1);
      transition: color 0.2s;
    }
    .c-val a:hover { color: var(--c-gold); }

    .call-bar {
      display: flex;
      align-items: center;
      gap: 14px;
      margin-top: 30px;
      padding: 17px 20px;
      background: var(--c-gold-dim);
      border: 1px solid var(--c-gold-border);
      border-radius: var(--radius-lg);
      text-decoration: none;
      transition: background 0.25s, transform 0.25s var(--ease);
    }
    .call-bar:hover {
      background: rgba(245,197,24,0.18);
      transform: translateY(-2px);
    }
    .call-bar .ci { font-size: 1.5rem; }
    .call-bar .ct {
      font-family: var(--f-display);
      font-size: 1.08rem;
      font-weight: 500;
      letter-spacing: 0.04em;
      color: var(--c-gold);
    }
    .call-bar .cs {
      display: block;
      font-size: 0.75rem;
      color: var(--c-t3);
      margin-top: 2px;
    }

    .map-frame {
      border-radius: var(--radius-lg);
      overflow: hidden;
      border: 1px solid var(--c-border);
      box-shadow: 0 24px 60px rgba(0,0,0,0.5);
    }
    .map-frame iframe {
      width: 100%;
      height: 450px;
      display: block;
      filter: grayscale(22%) contrast(1.06);
    }

    /* ============================================================
       FOOTER
    ============================================================ */
    footer {
      background: var(--c-black);
      border-top: 1px solid var(--c-border);
      padding: 56px 0 24px;
    }
    .footer-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      gap: 44px;
      padding-bottom: 44px;
      border-bottom: 1px solid var(--c-border);
    }
    .f-brand .nav-logo { display: block; margin-bottom: 14px; }
    .f-brand p {
      font-size: 0.87rem;
      font-weight: 300;
      color: var(--c-t3);
      line-height: 1.72;
      max-width: 270px;
    }
    .socials {
      display: flex;
      gap: 8px;
      margin-top: 18px;
    }
    .soc {
      width: 34px; height: 34px;
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--c-t3);
      font-size: 0.88rem;
      text-decoration: none;
      transition: border-color 0.2s, color 0.2s;
    }
    .soc:hover { border-color: var(--c-gold-border); color: var(--c-gold); }
    .f-col h4 {
      font-family: var(--f-display);
      font-size: 0.7rem;
      font-weight: 400;
      letter-spacing: 0.26em;
      text-transform: uppercase;
      color: var(--c-gold);
      margin-bottom: 18px;
    }
    .f-col ul { display: flex; flex-direction: column; gap: 9px; }
    .f-col ul li a {
      font-size: 0.87rem;
      font-weight: 300;
      color: var(--c-t3);
      transition: color 0.2s;
    }
    .f-col ul li a:hover { color: var(--c-t1); }
    .footer-bottom {
      padding-top: 24px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      gap: 8px;
      font-size: 0.78rem;
      font-weight: 300;
      color: var(--c-t3);
    }

    /* ============================================================
       FLOATING BUTTONS
    ============================================================ */
    .floats {
      position: fixed;
      bottom: 24px;
      right: 20px;
      z-index: 900;
      display: flex;
      flex-direction: column;
      gap: 10px;
      align-items: flex-end;
    }
    .fbw {
      position: relative;
      display: flex;
      align-items: center;
    }
    .fb-tip {
      position: absolute;
      right: 58px;
      background: rgba(8,8,8,0.95);
      border: 1px solid var(--c-border);
      border-radius: var(--radius);
      padding: 4px 10px;
      font-family: var(--f-display);
      font-size: 0.68rem;
      letter-spacing: 0.14em;
      text-transform: uppercase;
      color: var(--c-t2);
      white-space: nowrap;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.2s;
    }
    .fbw:hover .fb-tip { opacity: 1; }
    .fb {
      width: 50px; height: 50px;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 1.3rem;
      box-shadow: 0 4px 20px rgba(0,0,0,0.45);
      text-decoration: none;
      transition: transform 0.25s var(--ease), box-shadow 0.25s;
    }
    .fb:hover { transform: scale(1.1); box-shadow: 0 8px 28px rgba(0,0,0,0.55); }
    .fb-wa   { background: #25D366; }
    .fb-call { background: var(--c-gold); }

    /* Back to top */
    #btt {
      position: fixed;
      bottom: 24px;
      left: 20px;
      z-index: 900;
      width: 40px; height: 40px;
      background: var(--c-s2);
      border: 1px solid var(--c-border);
      border-radius: var(--radius);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--c-t3);
      cursor: pointer;
      opacity: 0;
      pointer-events: none;
      transition: opacity 0.3s, color 0.2s, border-color 0.2s, transform 0.25s;
    }
    #btt.show { opacity: 1; pointer-events: all; }
    #btt:hover { color: var(--c-gold); border-color: var(--c-gold-border); transform: translateY(-2px); }

    /* ============================================================
       RESPONSIVE — TABLET (≤1024px)
    ============================================================ */
    @media (max-width: 1024px) {
      .why-grid { grid-template-columns: repeat(2, 1fr); }
      .about-grid { gap: 44px; }
      .timings-grid { gap: 44px; }
      .contact-grid { gap: 44px; }
    }

    /* ============================================================
       RESPONSIVE — MOBILE (≤768px)
    ============================================================ */
    @media (max-width: 768px) {
      section { padding-top: 64px; padding-bottom: 64px; }

      /* Nav */
      .nav-links, .nav-cta { display: none; }
      .burger { display: flex; }

      /* Hero */
      .hero-word { display: none; }
      .hero-h1 { font-size: clamp(2.5rem, 12vw, 4rem); }
      .hero-actions .btn { flex: 1 1 140px; }

      /* About */
      .about-grid {
        grid-template-columns: 1fr;
        gap: 40px;
      }
      .about-img { aspect-ratio: 16/9; }
      .about-stars { right: 10px; bottom: -14px; }

      /* Why */
      .why-grid { grid-template-columns: repeat(2, 1fr); gap: 14px; }

      /* Services */
      .services-grid { grid-template-columns: 1fr; }

      /* Timings */
      .timings-grid { grid-template-columns: 1fr; gap: 36px; }

      /* Reviews */
      .rv-grid { grid-template-columns: 1fr; max-width: 100%; }

      /* Gallery */
      .gallery-grid { grid-template-columns: repeat(2, 1fr); }
      .g-cell:first-child { grid-column: span 2; aspect-ratio: 16/9; }

      /* CTA */
      .cta-row {
        flex-direction: column;
        text-align: center;
      }
      .cta-btns { justify-content: center; }

      /* Contact */
      .contact-grid { grid-template-columns: 1fr; gap: 40px; }
      .map-frame iframe { height: 320px; }

      /* Footer */
      .footer-grid { grid-template-columns: 1fr; gap: 32px; }
      .footer-bottom { flex-direction: column; align-items: center; text-align: center; }
    }

    /* ============================================================
       RESPONSIVE — SMALL (≤480px)
    ============================================================ */
    @media (max-width: 480px) {
      .why-grid { grid-template-columns: 1fr; }
      .gallery-grid { grid-template-columns: 1fr; }
      .g-cell:first-child { grid-column: span 1; aspect-ratio: 16/9; }
      .hero-actions { flex-direction: column; }
      .hero-actions .btn { width: 100%; }
      .cta-btns { flex-direction: column; width: 100%; }
      .cta-btns .btn { width: 100%; }
    }
  </style>
</head>
<body>

<!-- ══════════════════════════════
     NAVBAR
══════════════════════════════ -->
<nav id="nav" role="navigation" aria-label="Main navigation">
  <div class="w nav-inner">
    <a href="#hero" class="nav-logo" aria-label="Hulk Gym Home">HULK<span>GYM</span></a>

    <ul class="nav-links" role="list">
      <li><a href="#about">About</a></li>
      <li><a href="#why">Why Us</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#timings">Timings</a></li>
      <li><a href="#reviews">Reviews</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>

    <a href="tel:+919930548676" class="btn btn-gold nav-cta" aria-label="Call Hulk Gym">📞 Call Now</a>

    <button class="burger" id="burger" aria-label="Open navigation menu" aria-expanded="false" aria-controls="drawer">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<!-- Mobile Drawer -->
<nav id="drawer" aria-label="Mobile navigation" aria-hidden="true">
  <a href="#about"    onclick="closeDrawer()">About</a>
  <a href="#why"      onclick="closeDrawer()">Why Us</a>
  <a href="#services" onclick="closeDrawer()">Services</a>
  <a href="#timings"  onclick="closeDrawer()">Timings</a>
  <a href="#reviews"  onclick="closeDrawer()">Reviews</a>
  <a href="#gallery"  onclick="closeDrawer()">Gallery</a>
  <a href="#contact"  onclick="closeDrawer()">Contact</a>
  <a href="tel:+919930548676" class="btn btn-gold" onclick="closeDrawer()">📞 +91 99305 48676</a>
</nav>


<!-- ══════════════════════════════
     HERO
══════════════════════════════ -->
<section id="hero" aria-label="Hero">
  <div class="hero-bg" aria-hidden="true"></div>
  <div class="hero-fade" aria-hidden="true"></div>
  <div class="hero-word" aria-hidden="true">GYM</div>

  <div class="w hero-content">
    <div class="hero-pill">
      <span class="blink" aria-hidden="true"></span>
      Dombivli East's Favourite Gym
    </div>

    <h1 class="hero-h1">
      TRANSFORM<br>
      <span class="gold">YOUR BODY</span><br>
      AT HULK GYM.
    </h1>

    <p class="hero-sub">
      Affordable memberships, supportive trainers, and a beginner-friendly environment that helps you achieve real results — right here in Dombivli East.
    </p>

    <div class="hero-actions">
      <a href="tel:+919930548676" class="btn btn-gold">📞 Call Now</a>
      <a href="#contact"          class="btn btn-outline">Visit Gym →</a>
    </div>

    <div class="hero-chips" role="list">
      <span class="chip" role="listitem">💰 Affordable Pricing</span>
      <span class="chip" role="listitem">🤝 Supportive Trainers</span>
      <span class="chip" role="listitem">🌱 Beginner Friendly</span>
      <span class="chip" role="listitem">🏆 Best Gym in Area</span>
      <span class="chip" role="listitem">✅ All Facilities Available</span>
    </div>
  </div>

  <div class="scroll-cue" aria-hidden="true">
    <span>Scroll</span>
    <div class="cue-arrow"></div>
  </div>
</section>


<!-- ══════════════════════════════
     MARQUEE
══════════════════════════════ -->
<div class="marquee" aria-hidden="true">
  <div class="marquee-track" id="mq"></div>
</div>


<!-- ══════════════════════════════
     ABOUT
══════════════════════════════ -->
<section id="about" aria-labelledby="about-h">
  <div class="w">
    <div class="about-grid">

      <!-- Visual -->
      <div class="about-visual reveal from-left">
        <div class="about-img" role="img" aria-label="Hulk Gym facility placeholder">
          <!-- Dumbbell SVG -->
          <svg class="gym-icon" width="190" height="95" viewBox="0 0 190 95" fill="none" aria-hidden="true">
            <rect x="25" y="37" width="140" height="21" rx="4" fill="white"/>
            <rect x="10" y="25" width="21" height="45" rx="7" fill="white"/>
            <rect y="31"   width="14" height="33" rx="5" fill="white"/>
            <rect x="159" y="25" width="21" height="45" rx="7" fill="white"/>
            <rect x="176" y="31" width="14" height="33" rx="5" fill="white"/>
          </svg>
        </div>
        <div class="about-stars" aria-label="4.9 star Google rating">
          <div class="num">⭐ 4.9</div>
          <div class="lbl">Google<br>Rating</div>
        </div>
      </div>

      <!-- Text -->
      <div class="about-text reveal from-right">
        <span class="eyebrow" id="about-h">About Hulk Gym</span>
        <h2 class="section-title">Built for <span class="hi">Everyone</span> Who Wants to Get Fit</h2>
        <span class="gold-rule"></span>
        <p class="section-sub" style="max-width:100%">
          Hulk Gym is Dombivli East's trusted fitness destination — known for its welcoming atmosphere, genuine care for members, and trainers who go the extra mile.
        </p>
        <p class="section-sub" style="max-width:100%; margin-top:12px;">
          Whether you're picking up a weight for the first time or working toward a serious fitness goal, you'll find the right guidance and motivation here every single day.
        </p>

        <ul class="check-list" role="list">
          <li><span class="ck" aria-hidden="true">✓</span>Supportive, cooperative trainers who care about your progress</li>
          <li><span class="ck" aria-hidden="true">✓</span>Perfect for beginners — step-by-step guidance, no judgment</li>
          <li><span class="ck" aria-hidden="true">✓</span>All essential gym facilities and equipment available</li>
          <li><span class="ck" aria-hidden="true">✓</span>Clean, well-maintained, and safe training environment</li>
          <li><span class="ck" aria-hidden="true">✓</span>Highly affordable membership plans for every budget</li>
        </ul>
      </div>

    </div>
  </div>
</section>


<!-- ══════════════════════════════
     WHY CHOOSE US
══════════════════════════════ -->
<section id="why" aria-labelledby="why-h">
  <div class="w">
    <div class="center-head reveal">
      <span class="eyebrow">Why Choose Us</span>
      <h2 class="section-title" id="why-h">Everything You Need<br>to <span class="hi">Succeed</span></h2>
      <p class="section-sub">We've designed Hulk Gym around one goal — helping you reach yours.</p>
    </div>

    <div class="why-grid">
      <div class="why-card reveal" style="transition-delay:.00s">
        <div class="why-icon" aria-hidden="true">💰</div>
        <h3>Affordable Pricing</h3>
        <p>Premium gym experience at prices that fit every budget. Getting fit in Dombivli has never been this accessible.</p>
      </div>
      <div class="why-card reveal" style="transition-delay:.07s">
        <div class="why-icon" aria-hidden="true">🤝</div>
        <h3>Friendly Trainers</h3>
        <p>Kind, patient, and knowledgeable trainers who guide you with proper form and keep you motivated every step of the way.</p>
      </div>
      <div class="why-card reveal" style="transition-delay:.14s">
        <div class="why-icon" aria-hidden="true">🌱</div>
        <h3>Beginner Support</h3>
        <p>Never set foot in a gym before? No problem. Our beginner-first approach makes sure you start with confidence.</p>
      </div>
      <div class="why-card reveal" style="transition-delay:.21s">
        <div class="why-icon" aria-hidden="true">🏋️</div>
        <h3>Great Facilities</h3>
        <p>All the equipment and facilities you need for a complete, effective workout — always clean and ready to use.</p>
      </div>
    </div>
  </div>
</section>


<!-- ══════════════════════════════
     SERVICES
══════════════════════════════ -->
<section id="services" aria-labelledby="svc-h">
  <div class="w">
    <div class="reveal" style="margin-bottom:52px">
      <span class="eyebrow">What We Offer</span>
      <h2 class="section-title" id="svc-h">Our <span class="hi">Services</span></h2>
      <p class="section-sub">Training programs designed for every goal and every starting point.</p>
    </div>

    <div class="services-grid">
      <div class="svc reveal" style="transition-delay:.00s">
        <div class="svc-icon" aria-hidden="true">🏋️</div>
        <div class="svc-body">
          <h3>Strength Training</h3>
          <p>Build muscle and strength using free weights, barbells, and machines — with trainer guidance for safe, correct technique at every stage.</p>
        </div>
      </div>
      <div class="svc reveal" style="transition-delay:.07s">
        <div class="svc-icon" aria-hidden="true">🔥</div>
        <div class="svc-body">
          <h3>Weight Loss Programs</h3>
          <p>Structured cardio and resistance training plans that burn fat effectively and sustainably — no crash diets, just consistent progress.</p>
        </div>
      </div>
      <div class="svc reveal" style="transition-delay:.14s">
        <div class="svc-icon" aria-hidden="true">🎯</div>
        <div class="svc-body">
          <h3>Personal Training</h3>
          <p>One-on-one sessions with a dedicated trainer who builds a plan tailored to your unique body, goals, and schedule.</p>
        </div>
      </div>
      <div class="svc reveal" style="transition-delay:.21s">
        <div class="svc-icon" aria-hidden="true">🌟</div>
        <div class="svc-body">
          <h3>Beginner Fitness Guidance</h3>
          <p>New to fitness? Our beginner orientation covers equipment, proper form, and goal-setting so you start smart and stay safe.</p>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- ══════════════════════════════
     TIMINGS
══════════════════════════════ -->
<section id="timings" aria-labelledby="tim-h">
  <div class="w">
    <div class="timings-grid">

      <div class="timings-left reveal from-left">
        <span class="eyebrow">Gym Schedule</span>
        <h2 class="section-title" id="tim-h">Open Early,<br>Open <span class="hi">Late</span></h2>
        <span class="gold-rule"></span>
        <p class="section-sub" style="max-width:100%">
          We're here before the sun rises and long after the work day ends — because your schedule shouldn't stop your fitness journey.
        </p>
        <p class="section-sub" style="max-width:100%; margin-top:12px;">
          Walk in any day during opening hours. No appointment needed — just bring your energy.
        </p>
        <a href="tel:+919930548676" class="btn btn-gold" style="margin-top:32px;">📞 Call to Enquire</a>
      </div>

      <div class="reveal from-right">
        <div class="timetable" role="table" aria-label="Hulk Gym weekly schedule">
          <div class="timetable-head" role="rowgroup">
            <span>🕐</span> Weekly Schedule
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Monday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Tuesday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Wednesday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Thursday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Friday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Saturday</span>
            <span class="trow-time" role="cell">05:30 AM – 10:30 PM</span>
          </div>
          <div class="trow sunday" role="row">
            <span class="trow-day" role="cell"><span class="dot" aria-hidden="true"></span>Sunday</span>
            <span class="trow-time" role="cell">07:00 AM – 12:00 PM</span>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>


<!-- ══════════════════════════════
     TESTIMONIALS
══════════════════════════════ -->
<section id="reviews" aria-labelledby="rv-h">
  <div class="w">
    <div class="center-head reveal">
      <span class="eyebrow">Real Reviews</span>
      <h2 class="section-title" id="rv-h">What Our <span class="hi">Members</span> Say</h2>
      <p class="section-sub">Honest feedback from real Hulk Gym members in Dombivli East.</p>
    </div>

    <div class="rv-grid">

      <article class="rv-card reveal" style="transition-delay:.00s">
        <div class="rv-stars" aria-label="5 stars">★★★★★</div>
        <p class="rv-text">
          "Excellent trainer and all facilities are available. I personally saw great results after joining Hulk Gym. The environment is very motivating and the staff always makes you feel welcome."
        </p>
        <div class="rv-author">
          <div class="rv-ava" aria-hidden="true">SM</div>
          <div>
            <div class="rv-name">Shubham M.</div>
            <div class="rv-meta">Google Review · Dombivli East Member</div>
          </div>
        </div>
      </article>

      <article class="rv-card reveal" style="transition-delay:.09s">
        <div class="rv-stars" aria-label="5 stars">★★★★★</div>
        <p class="rv-text">
          "Worth every rupee — easily the best gym in the area. Great equipment, affordable membership, and trainers who are genuinely supportive and cooperative. Highly recommend to everyone."
        </p>
        <div class="rv-author">
          <div class="rv-ava" aria-hidden="true">RK</div>
          <div>
            <div class="rv-name">Rahul K.</div>
            <div class="rv-meta">Google Review · Dombivli East Member</div>
          </div>
        </div>
      </article>

    </div>

    <div class="google-note reveal" style="margin-top:40px;" aria-label="Verified Google Reviews">
      <svg width="17" height="17" viewBox="0 0 24 24" aria-hidden="true">
        <path d="M22.56 12.25c0-.78-.07-1.53-.2-2.25H12v4.26h5.92c-.26 1.37-1.04 2.53-2.21 3.31v2.77h3.57c2.08-1.92 3.28-4.74 3.28-8.09z" fill="#4285F4"/>
        <path d="M12 23c2.97 0 5.46-.98 7.28-2.66l-3.57-2.77c-.98.66-2.23 1.06-3.71 1.06-2.86 0-5.29-1.93-6.16-4.53H2.18v2.84C3.99 20.53 7.7 23 12 23z" fill="#34A853"/>
        <path d="M5.84 14.09c-.22-.66-.35-1.36-.35-2.09s.13-1.43.35-2.09V7.07H2.18C1.43 8.55 1 10.22 1 12s.43 3.45 1.18 4.93l2.85-2.22.81-.62z" fill="#FBBC05"/>
        <path d="M12 5.38c1.62 0 3.06.56 4.21 1.64l3.15-3.15C17.45 2.09 14.97 1 12 1 7.7 1 3.99 3.47 2.18 7.07l3.66 2.84c.87-2.6 3.3-4.53 6.16-4.53z" fill="#EA4335"/>
      </svg>
      Verified Google Reviews from Hulk Gym Members
    </div>
  </div>
</section>


<!-- ══════════════════════════════
     GALLERY
══════════════════════════════ -->
<section id="gallery" aria-labelledby="gal-h">
  <div class="w">
    <div class="reveal" style="margin-bottom:40px">
      <span class="eyebrow">Our Facility</span>
      <h2 class="section-title" id="gal-h">Inside <span class="hi">Hulk Gym</span></h2>
      <p class="section-sub">A clean, well-equipped space built for serious training.</p>
    </div>

    <div class="gallery-grid">
      <div class="g-cell reveal">
        <div class="g-inner"><span class="g-ico" aria-hidden="true">🏋️</span><span class="g-lbl">Main Training Floor</span></div>
        <div class="g-hover"><span>Main Training Floor</span></div>
      </div>
      <div class="g-cell reveal" style="transition-delay:.06s">
        <div class="g-inner"><span class="g-ico" aria-hidden="true">💪</span><span class="g-lbl">Free Weights</span></div>
        <div class="g-hover"><span>Free Weights Zone</span></div>
      </div>
      <div class="g-cell reveal" style="transition-delay:.12s">
        <div class="g-inner"><span class="g-ico" aria-hidden="true">🏃</span><span class="g-lbl">Cardio Area</span></div>
        <div class="g-hover"><span>Cardio Area</span></div>
      </div>
      <div class="g-cell reveal" style="transition-delay:.08s">
        <div class="g-inner"><span class="g-ico" aria-hidden="true">⚙️</span><span class="g-lbl">Cable Machines</span></div>
        <div class="g-hover"><span>Cable Machines</span></div>
      </div>
      <div class="g-cell reveal" style="transition-delay:.14s">
        <div class="g-inner"><span class="g-ico" aria-hidden="true">🧘</span><span class="g-lbl">Stretching Area</span></div>
        <div class="g-hover"><span>Stretching & Recovery</span></div>
      </div>
    </div>
  </div>
</section>


<!-- ══════════════════════════════
     CTA BAND
══════════════════════════════ -->
<section id="cta" aria-label="Call to action">
  <div class="w cta-row">
    <div class="cta-copy reveal from-left">
      <h2>START YOUR FITNESS<br>JOURNEY TODAY.</h2>
      <p>Walk in anytime. No experience needed. Just the will to begin.</p>
    </div>
    <div class="cta-btns reveal from-right">
      <a href="tel:+919930548676" class="btn btn-dark">📞 Call Us Now</a>
      <a href="#contact"          class="btn btn-dark-outline">Get Directions</a>
    </div>
  </div>
</section>


<!-- ══════════════════════════════
     CONTACT
══════════════════════════════ -->
<section id="contact" aria-labelledby="con-h">
  <div class="w">
    <div class="contact-grid">

      <!-- Info -->
      <div class="contact-left reveal from-left">
        <span class="eyebrow">Find Us</span>
        <h2 class="section-title" id="con-h">Visit <span class="hi">Hulk Gym</span></h2>
        <p class="section-sub" style="max-width:100%">We're easy to reach and always ready to welcome new members. Come visit us any day during opening hours.</p>

        <div class="c-details">
          <div class="c-row">
            <div class="c-icon" aria-hidden="true">📍</div>
            <div>
              <div class="c-label">Address</div>
              <div class="c-val">
                Near Grampanchayat Office,<br>
                Gavdevi Mandir Road,<br>
                Dombivli East, Kalyan,<br>
                Maharashtra – 421204, India
              </div>
            </div>
          </div>
          <div class="c-row">
            <div class="c-icon" aria-hidden="true">📞</div>
            <div>
              <div class="c-label">Phone</div>
              <div class="c-val"><a href="tel:+919930548676">+91 99305 48676</a></div>
            </div>
          </div>
          <div class="c-row">
            <div class="c-icon" aria-hidden="true">✉️</div>
            <div>
              <div class="c-label">Email</div>
              <div class="c-val"><a href="mailto:hulkgymfitness@gmail.com">hulkgymfitness@gmail.com</a></div>
            </div>
          </div>
          <div class="c-row">
            <div class="c-icon" aria-hidden="true">⏰</div>
            <div>
              <div class="c-label">Timings</div>
              <div class="c-val">
                Mon – Sat: 05:30 AM – 10:30 PM<br>
                Sunday: 07:00 AM – 12:00 PM
              </div>
            </div>
          </div>
        </div>

        <a href="tel:+919930548676" class="call-bar" aria-label="Call +91 99305 48676">
          <span class="ci" aria-hidden="true">📞</span>
          <div>
            <div class="ct">+91 99305 48676</div>
            <span class="cs">Tap to call directly — we'll answer!</span>
          </div>
        </a>
      </div>

      <!-- Map -->
      <div class="map-frame reveal from-right">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3768.0!2d73.0880!3d19.2195!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3be7954b5555aaab%3A0x1!2sGavdevi+Mandir+Road%2C+Dombivli+East%2C+Maharashtra+421204!5e0!3m2!1sen!2sin!4v1700000000000"
          allowfullscreen
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
          title="Hulk Gym location map — Near Grampanchayat Office, Gavdevi Mandir Road, Dombivli East"
        ></iframe>
      </div>

    </div>
  </div>
</section>


<!-- ══════════════════════════════
     FOOTER
══════════════════════════════ -->
<footer>
  <div class="w">
    <div class="footer-grid">

      <div class="f-brand">
        <a href="#hero" class="nav-logo" aria-label="Hulk Gym Home">HULK<span>GYM</span></a>
        <p>Dombivli East's most affordable, beginner-friendly gym. Real trainers. Real results. Real community.</p>
        <div class="socials" aria-label="Social media">
          <a href="#" class="soc" aria-label="Instagram">
            <svg width="15" height="15" fill="currentColor" viewBox="0 0 24 24"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          </a>
          <a href="#" class="soc" aria-label="Facebook">
            <svg width="15" height="15" fill="currentColor" viewBox="0 0 24 24"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
          </a>
          <a href="https://wa.me/919930548676" class="soc" aria-label="WhatsApp" target="_blank" rel="noopener noreferrer">
            <svg width="15" height="15" fill="currentColor" viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
          </a>
        </div>
      </div>

      <div class="f-col">
        <h4>Quick Links</h4>
        <ul>
          <li><a href="#about">About Us</a></li>
          <li><a href="#why">Why Choose Us</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#timings">Timings</a></li>
          <li><a href="#reviews">Reviews</a></li>
          <li><a href="#gallery">Gallery</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>

      <div class="f-col">
        <h4>Contact Info</h4>
        <ul>
          <li><a href="tel:+919930548676">+91 99305 48676</a></li>
          <li><a href="mailto:hulkgymfitness@gmail.com">hulkgymfitness@gmail.com</a></li>
          <li><a href="#contact">Dombivli East – 421204</a></li>
          <li><a href="#timings">Mon–Sat: 5:30AM–10:30PM</a></li>
          <li><a href="#timings">Sun: 7:00AM–12:00PM</a></li>
        </ul>
      </div>

    </div>

    <div class="footer-bottom">
      <span>© 2025 Hulk Gym, Dombivli East. All rights reserved.</span>
      <span>Made with ❤️ for the Dombivli fitness community</span>
    </div>
  </div>
</footer>


<!-- ══════════════════════════════
     FLOATING BUTTONS
══════════════════════════════ -->
<div class="floats" aria-label="Quick contact">
  <div class="fbw">
    <span class="fb-tip" aria-hidden="true">WhatsApp Us</span>
    <a href="https://wa.me/919930548676?text=Hi%20Hulk%20Gym%2C%20I%27d%20like%20to%20know%20about%20your%20membership!"
       class="fb fb-wa"
       target="_blank"
       rel="noopener noreferrer"
       aria-label="Contact Hulk Gym on WhatsApp">
      <svg width="24" height="24" fill="white" viewBox="0 0 24 24" aria-hidden="true">
        <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
      </svg>
    </a>
  </div>
  <div class="fbw">
    <span class="fb-tip" aria-hidden="true">Call Now</span>
    <a href="tel:+919930548676" class="fb fb-call" aria-label="Call Hulk Gym now">
      <svg width="22" height="22" fill="#080808" viewBox="0 0 24 24" aria-hidden="true">
        <path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/>
      </svg>
    </a>
  </div>
</div>

<!-- Back to top -->
<button id="btt" aria-label="Back to top" onclick="window.scrollTo({top:0,behavior:'smooth'})">
  <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
    <path d="M7.41 15.41L12 10.83l4.59 4.58L18 14l-6-6-6 6 1.41 1.41z"/>
  </svg>
</button>


<!-- ══════════════════════════════
     JAVASCRIPT
══════════════════════════════ -->
<script>
(function () {
  'use strict';

  /* ─── Navbar scroll ─────────────────── */
  var nav = document.getElementById('nav');
  var btt = document.getElementById('btt');

  function handleScroll() {
    var y = window.pageYOffset;
    if (y > 60) {
      nav.classList.add('scrolled');
    } else {
      nav.classList.remove('scrolled');
    }
    if (y > 500) {
      btt.classList.add('show');
    } else {
      btt.classList.remove('show');
    }
  }
  window.addEventListener('scroll', handleScroll, { passive: true });
  handleScroll();

  /* ─── Mobile drawer ─────────────────── */
  var burger = document.getElementById('burger');
  var drawer = document.getElementById('drawer');

  burger.addEventListener('click', function () {
    var isOpen = drawer.classList.toggle('open');
    burger.classList.toggle('open', isOpen);
    burger.setAttribute('aria-expanded', isOpen ? 'true' : 'false');
    drawer.setAttribute('aria-hidden', isOpen ? 'false' : 'true');
    document.body.style.overflow = isOpen ? 'hidden' : '';
  });

  window.closeDrawer = function () {
    drawer.classList.remove('open');
    burger.classList.remove('open');
    burger.setAttribute('aria-expanded', 'false');
    drawer.setAttribute('aria-hidden', 'true');
    document.body.style.overflow = '';
  };

  /* Close drawer on Escape */
  document.addEventListener('keydown', function (e) {
    if (e.key === 'Escape') window.closeDrawer();
  });

  /* ─── Smooth anchor scroll ───────────── */
  document.querySelectorAll('a[href^="#"]').forEach(function (a) {
    a.addEventListener('click', function (e) {
      var href = a.getAttribute('href');
      if (!href || href === '#') return;
      var target = document.querySelector(href);
      if (!target) return;
      e.preventDefault();
      var navH = parseInt(
        getComputedStyle(document.documentElement).getPropertyValue('--nav-h')
      ) || 68;
      var top = target.getBoundingClientRect().top + window.pageYOffset - navH;
      window.scrollTo({ top: top, behavior: 'smooth' });
      window.closeDrawer();
    });
  });

  /* ─── Scroll reveal ─────────────────── */
  var revealEls = document.querySelectorAll('.reveal');

  if ('IntersectionObserver' in window) {
    var revealObs = new IntersectionObserver(function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          var el = entry.target;
          /* honour inline transition-delay if set */
          var delay = el.style.transitionDelay || '0s';
          el.style.transitionDelay = delay;
          el.classList.add('visible');
          revealObs.unobserve(el);
        }
      });
    }, { threshold: 0.1, rootMargin: '0px 0px -44px 0px' });

    revealEls.forEach(function (el) { revealObs.observe(el); });
  } else {
    /* Fallback for older browsers */
    revealEls.forEach(function (el) { el.classList.add('visible'); });
  }

  /* ─── Marquee content ───────────────── */
  var mqItems = [
    'Strength Training',
    'Weight Loss',
    'Personal Training',
    'Beginner Friendly',
    'Affordable Gym',
    'Expert Trainers',
    'Dombivli East',
    'All Facilities'
  ];

  var mq = document.getElementById('mq');
  if (mq) {
    /* Duplicate for seamless loop */
    var full = mqItems.concat(mqItems);
    full.forEach(function (txt) {
      var s = document.createElement('span');
      s.className = 'm-item';
      s.textContent = txt + '  ✦  ';
      mq.appendChild(s);
    });
  }

})();
</script>

</body>
</html>
