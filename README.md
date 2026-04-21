<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<meta name="description" content="HULK GYM – Premium fitness transformation zone. Expert trainers, proven results, and a community that pushes you beyond limits. Join today."/>
<title>HULK GYM – Build The Body. Unleash The Hulk.</title>
<link rel="preconnect" href="https://fonts.googleapis.com"/>
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin/>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Barlow+Condensed:wght@300;400;600;700;900&family=Barlow:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  :root {
    --black: #000000;
    --deep: #080808;
    --charcoal: #111111;
    --card: #141414;
    --border: #1e1e1e;
    --neon: #AAFF00;
    --neon-dim: rgba(170,255,0,0.12);
    --neon-mid: rgba(170,255,0,0.4);
    --gold: #C9A84C;
    --white: #FFFFFF;
    --grey: #888888;
    --light-grey: #AAAAAA;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body {
    background: var(--black);
    color: var(--white);
    font-family: 'Barlow', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
    cursor: none;
  }

  /* CUSTOM CURSOR */
  .cursor {
    position: fixed; width: 10px; height: 10px;
    background: var(--neon); border-radius: 50%;
    pointer-events: none; z-index: 9999;
    transition: transform 0.1s; mix-blend-mode: exclusion;
  }
  .cursor-ring {
    position: fixed; width: 36px; height: 36px;
    border: 1px solid var(--neon); border-radius: 50%;
    pointer-events: none; z-index: 9998;
    transition: width 0.2s, height 0.2s;
    mix-blend-mode: exclusion;
  }

  /* GRAIN */
  body::before {
    content:''; position: fixed; inset: 0;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.035'/%3E%3C/svg%3E");
    pointer-events: none; z-index: 1; opacity: 0.7;
  }

  /* SCROLLBAR */
  ::-webkit-scrollbar { width: 3px; }
  ::-webkit-scrollbar-track { background: var(--black); }
  ::-webkit-scrollbar-thumb { background: var(--neon); border-radius: 2px; }

  /* TYPOGRAPHY */
  .display { font-family: 'Bebas Neue', sans-serif; line-height: 0.92; letter-spacing: 0.01em; }
  .condensed { font-family: 'Barlow Condensed', sans-serif; }
  .label {
    font-family: 'Barlow Condensed', sans-serif;
    font-size: 11px; letter-spacing: 0.3em;
    text-transform: uppercase; color: var(--neon); font-weight: 600;
  }

  /* BUTTONS */
  .btn-primary {
    display: inline-flex; align-items: center; gap: 10px;
    background: var(--neon); color: var(--black);
    font-family: 'Barlow Condensed', sans-serif;
    font-weight: 900; font-size: 14px; letter-spacing: 0.2em;
    text-transform: uppercase; padding: 16px 36px;
    border: none; cursor: none; text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 12px) 0, 100% 12px, 100% 100%, 12px 100%, 0 calc(100% - 12px));
    transition: box-shadow 0.2s, transform 0.2s; position: relative; overflow: hidden;
  }
  .btn-primary::before {
    content: ''; position: absolute; inset: 0;
    background: rgba(255,255,255,0.18);
    transform: translateX(-110%) skewX(-18deg); transition: transform 0.4s;
  }
  .btn-primary:hover::before { transform: translateX(120%) skewX(-18deg); }
  .btn-primary:hover { box-shadow: 0 0 40px rgba(170,255,0,0.5); transform: translateY(-2px); }

  .btn-outline {
    display: inline-flex; align-items: center; gap: 10px;
    background: transparent; color: var(--white);
    font-family: 'Barlow Condensed', sans-serif;
    font-weight: 900; font-size: 14px; letter-spacing: 0.2em;
    text-transform: uppercase; padding: 14px 34px;
    border: 1px solid rgba(255,255,255,0.3); cursor: none; text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 12px) 0, 100% 12px, 100% 100%, 12px 100%, 0 calc(100% - 12px));
    transition: border-color 0.2s, color 0.2s, box-shadow 0.2s, transform 0.2s;
  }
  .btn-outline:hover { border-color: var(--neon); color: var(--neon); box-shadow: 0 0 20px rgba(170,255,0,0.2); transform: translateY(-2px); }

  /* NAV */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    padding: 0 6vw; display: flex; align-items: center; justify-content: space-between;
    height: 72px; background: rgba(0,0,0,0.55);
    backdrop-filter: blur(20px) saturate(1.4);
    border-bottom: 1px solid rgba(170,255,0,0.07);
    transition: background 0.3s, border-color 0.3s;
  }
  nav.scrolled { background: rgba(0,0,0,0.93); border-bottom-color: rgba(170,255,0,0.18); }
  .nav-logo {
    font-family: 'Bebas Neue', sans-serif; font-size: 28px; letter-spacing: 0.06em;
    color: var(--white); text-decoration: none; display: flex; align-items: center; gap: 10px;
  }
  .nav-logo span { color: var(--neon); }
  .nav-logo-icon {
    width: 34px; height: 34px; background: var(--neon);
    display: grid; place-items: center;
    clip-path: polygon(20% 0%,80% 0%,100% 20%,100% 80%,80% 100%,20% 100%,0% 80%,0% 20%);
  }
  .nav-logo-icon svg { width: 18px; height: 18px; fill: var(--black); }
  .nav-links { display: flex; align-items: center; gap: 32px; }
  .nav-links a {
    font-family: 'Barlow Condensed', sans-serif; font-size: 13px;
    letter-spacing: 0.15em; text-transform: uppercase;
    color: var(--light-grey); text-decoration: none; transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--neon); }
  .nav-cta { display: flex; align-items: center; gap: 14px; }
  .nav-phone {
    font-family: 'Barlow Condensed', sans-serif; font-size: 15px;
    font-weight: 700; letter-spacing: 0.08em; color: var(--neon);
    text-decoration: none; display: flex; align-items: center; gap: 6px;
  }
  .nav-phone svg { width: 14px; height: 14px; fill: var(--neon); }
  .nav-phone:hover { color: var(--white); }
  .nav-join {
    background: var(--neon); color: var(--black);
    font-family: 'Barlow Condensed', sans-serif; font-weight: 900;
    font-size: 12px; letter-spacing: 0.2em; text-transform: uppercase;
    padding: 10px 22px; border: none; cursor: none; text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 8px) 0, 100% 8px, 100% 100%, 8px 100%, 0 calc(100% - 8px));
    transition: box-shadow 0.2s, transform 0.2s;
  }
  .nav-join:hover { box-shadow: 0 0 24px rgba(170,255,0,0.6); transform: translateY(-1px); }
  .hamburger { display: none; flex-direction: column; gap: 5px; cursor: none; background: none; border: none; }
  .hamburger span { width: 24px; height: 2px; background: var(--white); display: block; }

  /* HERO */
  #hero { position: relative; height: 100vh; min-height: 700px; display: flex; align-items: center; overflow: hidden; }
  .hero-bg {
    position: absolute; inset: 0;
    background-image: url('https://images.unsplash.com/photo-1534438327276-14e5300c3a48?w=1900&q=85&auto=format');
    background-size: cover; background-position: center 30%;
    animation: heroZoom 12s ease-out forwards;
  }
  @keyframes heroZoom { from { transform: scale(1.06); } to { transform: scale(1); } }
  .hero-overlay { position: absolute; inset: 0; background: linear-gradient(105deg, rgba(0,0,0,0.93) 38%, rgba(0,0,0,0.45) 100%); }
  .hero-overlay2 { position: absolute; inset: 0; background: linear-gradient(to bottom, transparent 55%, var(--black) 100%); }
  .hero-neon-line {
    position: absolute; left: 0; top: 0; bottom: 0; width: 3px;
    background: var(--neon); box-shadow: 0 0 30px var(--neon), 0 0 60px var(--neon);
    animation: neonPulse 3s ease-in-out infinite;
  }
  @keyframes neonPulse { 0%,100% { opacity: 1; } 50% { opacity: 0.35; } }
  .hero-content { position: relative; z-index: 2; padding: 0 6vw; max-width: 860px; }
  .hero-label { display: inline-flex; align-items: center; gap: 12px; margin-bottom: 28px; animation: fadeUp 0.8s 0.2s both; }
  .hero-label-line { width: 40px; height: 1px; background: var(--neon); }
  .hero-eyebrow { font-size: clamp(52px, 9vw, 112px); color: var(--white); animation: fadeUp 0.8s 0.35s both; }
  .hero-eyebrow .accent { color: var(--neon); }
  .hero-sub { font-size: 18px; font-weight: 300; line-height: 1.7; color: rgba(255,255,255,0.62); max-width: 520px; margin: 20px 0 44px; animation: fadeUp 0.8s 0.5s both; }
  .hero-sub strong { color: var(--white); font-weight: 500; }
  .hero-btns { display: flex; gap: 16px; flex-wrap: wrap; animation: fadeUp 0.8s 0.65s both; }
  .hero-scroll { position: absolute; bottom: 36px; left: 6vw; display: flex; align-items: center; gap: 12px; z-index: 2; animation: fadeUp 0.8s 1s both; }
  .scroll-line { width: 1px; height: 50px; background: linear-gradient(to bottom, var(--neon), transparent); animation: scrollDrop 2s ease-in-out infinite; }
  @keyframes scrollDrop { 0%,100% { opacity: 1; } 50% { opacity: 0.3; } }
  .scroll-text { font-family: 'Barlow Condensed', sans-serif; font-size: 11px; letter-spacing: 0.3em; color: var(--grey); text-transform: uppercase; writing-mode: vertical-rl; }
  .hero-stats { position: absolute; right: 6vw; bottom: 80px; z-index: 2; display: flex; gap: 40px; animation: fadeUp 0.8s 0.8s both; }
  .stat { text-align: center; }
  .stat-number { font-family: 'Bebas Neue', sans-serif; font-size: 48px; color: var(--neon); line-height: 1; }
  .stat-label { font-size: 11px; letter-spacing: 0.2em; color: var(--grey); text-transform: uppercase; margin-top: 4px; }
  @keyframes fadeUp { from { opacity: 0; transform: translateY(32px); } to { opacity: 1; transform: translateY(0); } }

  /* SECTIONS */
  section { position: relative; z-index: 2; }
  .section-pad { padding: 100px 6vw; }
  .section-header { margin-bottom: 60px; }
  .section-title { font-size: clamp(44px, 6vw, 82px); color: var(--white); }
  .section-title .accent { color: var(--neon); }
  .section-desc { font-size: 17px; color: var(--light-grey); line-height: 1.7; max-width: 560px; margin-top: 16px; }

  /* WHY */
  #why { background: var(--deep); }
  .why-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 2px; }
  .why-card {
    background: var(--charcoal); padding: 40px 32px; position: relative; overflow: hidden;
    transition: transform 0.3s; border-bottom: 2px solid transparent;
  }
  .why-card::after { content: ''; position: absolute; bottom: 0; left: 0; right: 0; height: 2px; background: var(--neon); transform: scaleX(0); transform-origin: left; transition: transform 0.4s; }
  .why-card:hover { transform: translateY(-4px); }
  .why-card:hover::after { transform: scaleX(1); }
  .why-icon {
    width: 52px; height: 52px; background: var(--neon-dim); border: 1px solid rgba(170,255,0,0.22);
    display: grid; place-items: center; margin-bottom: 24px;
    clip-path: polygon(20% 0%,80% 0%,100% 20%,100% 80%,80% 100%,20% 100%,0% 80%,0% 20%);
    transition: background 0.3s;
  }
  .why-card:hover .why-icon { background: rgba(170,255,0,0.22); }
  .why-icon svg { width: 22px; height: 22px; stroke: var(--neon); fill: none; stroke-width: 2; }
  .why-card h3 { font-family: 'Barlow Condensed', sans-serif; font-size: 22px; font-weight: 700; letter-spacing: 0.05em; text-transform: uppercase; margin-bottom: 12px; }
  .why-card p { font-size: 15px; line-height: 1.7; color: var(--light-grey); }
  .why-card .card-number { position: absolute; top: 24px; right: 24px; font-family: 'Bebas Neue', sans-serif; font-size: 64px; color: rgba(255,255,255,0.025); line-height: 1; }

  /* TRANSFORM */
  #transform { background: var(--black); overflow: hidden; }
  .transform-inner { display: grid; grid-template-columns: 1fr 1fr; min-height: 600px; }
  .transform-left { padding: 80px 6vw; display: flex; flex-direction: column; justify-content: center; }
  .transform-right { position: relative; overflow: hidden; }
  .transform-img { width: 100%; height: 100%; object-fit: cover; filter: grayscale(20%); transition: filter 0.4s, transform 5s ease; }
  .transform-right:hover .transform-img { filter: grayscale(0%); transform: scale(1.04); }
  .transform-overlay { position: absolute; inset: 0; background: linear-gradient(to right, var(--black) 0%, transparent 30%); pointer-events: none; }
  .result-tag { display: inline-flex; align-items: center; gap: 8px; background: var(--neon); color: var(--black); font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 12px; letter-spacing: 0.2em; text-transform: uppercase; padding: 6px 16px; margin-bottom: 20px; }
  .transform-title { font-size: clamp(42px, 5vw, 74px); color: var(--white); margin-bottom: 24px; }
  .transform-body { font-size: 16px; color: var(--light-grey); line-height: 1.8; margin-bottom: 36px; max-width: 460px; }
  .result-bars { display: flex; flex-direction: column; gap: 18px; margin-bottom: 40px; }
  .result-bar-top { display: flex; justify-content: space-between; align-items: center; margin-bottom: 8px; }
  .result-bar-label { font-family: 'Barlow Condensed', sans-serif; font-size: 13px; letter-spacing: 0.15em; text-transform: uppercase; color: var(--light-grey); }
  .result-bar-pct { font-family: 'Bebas Neue', sans-serif; font-size: 22px; color: var(--neon); }
  .result-bar-track { height: 3px; background: var(--border); }
  .result-bar-fill { height: 100%; background: var(--neon); transform-origin: left; transform: scaleX(0); transition: transform 1.2s cubic-bezier(0.4,0,0.2,1); }

  /* TRAINERS */
  #trainers { background: var(--charcoal); }
  .trainers-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr)); gap: 24px; }
  .trainer-card { background: var(--card); overflow: hidden; transition: transform 0.3s; }
  .trainer-card:hover { transform: translateY(-6px); }
  .trainer-img-wrap { position: relative; height: 420px; overflow: hidden; }
  .trainer-img { width: 100%; height: 100%; object-fit: cover; filter: grayscale(30%); transition: filter 0.4s, transform 0.6s; }
  .trainer-card:hover .trainer-img { filter: grayscale(0%); transform: scale(1.05); }
  .trainer-img-overlay { position: absolute; inset: 0; background: linear-gradient(to top, rgba(0,0,0,0.95) 0%, rgba(0,0,0,0.25) 60%, transparent 100%); }
  .trainer-badge { position: absolute; top: 20px; right: 20px; background: var(--neon); color: var(--black); font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase; padding: 5px 12px; }
  .trainer-info { padding: 28px 28px 32px; }
  .trainer-name { font-family: 'Bebas Neue', sans-serif; font-size: 36px; letter-spacing: 0.05em; }
  .trainer-role { color: var(--neon); font-size: 12px; letter-spacing: 0.25em; text-transform: uppercase; font-weight: 600; margin-bottom: 14px; font-family: 'Barlow Condensed', sans-serif; }
  .trainer-bio { font-size: 15px; color: var(--light-grey); line-height: 1.7; }
  .trainer-tags { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 18px; }
  .trainer-tag { background: var(--neon-dim); border: 1px solid rgba(170,255,0,0.2); color: var(--neon); font-size: 11px; letter-spacing: 0.15em; text-transform: uppercase; padding: 4px 12px; font-family: 'Barlow Condensed', sans-serif; font-weight: 600; }

  /* TESTIMONIALS */
  #testimonials { background: var(--deep); overflow: hidden; }
  .testi-track-wrap { overflow: hidden; position: relative; }
  .testi-track-wrap::before, .testi-track-wrap::after { content: ''; position: absolute; top: 0; bottom: 0; width: 140px; z-index: 2; pointer-events: none; }
  .testi-track-wrap::before { left: 0; background: linear-gradient(to right, var(--deep), transparent); }
  .testi-track-wrap::after { right: 0; background: linear-gradient(to left, var(--deep), transparent); }
  .testi-track { display: flex; gap: 24px; animation: scrollTrack 34s linear infinite; width: max-content; }
  .testi-track:hover { animation-play-state: paused; }
  @keyframes scrollTrack { from { transform: translateX(0); } to { transform: translateX(-50%); } }
  .testi-card { background: var(--card); border: 1px solid var(--border); padding: 36px 32px; width: 380px; flex-shrink: 0; position: relative; overflow: hidden; transition: border-color 0.3s, transform 0.3s; }
  .testi-card::before { content: '\201C'; font-family: 'Bebas Neue', sans-serif; font-size: 130px; color: var(--neon); opacity: 0.06; position: absolute; top: -10px; left: 20px; line-height: 1; pointer-events: none; }
  .testi-card:hover { border-color: rgba(170,255,0,0.28); transform: translateY(-4px); }
  .stars { display: flex; gap: 4px; margin-bottom: 18px; }
  .star { color: var(--gold); font-size: 15px; }
  .testi-text { font-size: 16px; line-height: 1.75; color: var(--white); font-style: italic; margin-bottom: 24px; font-weight: 300; }
  .testi-author { display: flex; align-items: center; gap: 14px; }
  .testi-avatar { width: 42px; height: 42px; background: var(--neon); display: grid; place-items: center; font-family: 'Bebas Neue', sans-serif; font-size: 18px; color: var(--black); clip-path: polygon(20% 0%,80% 0%,100% 20%,100% 80%,80% 100%,20% 100%,0% 80%,0% 20%); flex-shrink: 0; }
  .testi-name { font-family: 'Barlow Condensed', sans-serif; font-weight: 700; font-size: 15px; letter-spacing: 0.08em; text-transform: uppercase; }
  .testi-member { font-size: 12px; color: var(--neon); letter-spacing: 0.15em; text-transform: uppercase; font-family: 'Barlow Condensed', sans-serif; }

  /* PRICING */
  #pricing { background: var(--black); }
  .pricing-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 24px; max-width: 1000px; }
  .price-card { background: var(--charcoal); border: 1px solid var(--border); padding: 40px 32px; position: relative; overflow: hidden; transition: transform 0.3s, border-color 0.3s; }
  .price-card.featured { background: var(--card); border-color: var(--neon); box-shadow: 0 0 60px rgba(170,255,0,0.12); transform: scale(1.03); }
  .price-card:hover { transform: translateY(-6px); border-color: rgba(170,255,0,0.35); }
  .price-card.featured:hover { transform: scale(1.03) translateY(-6px); }
  .price-badge { position: absolute; top: 20px; right: 20px; background: var(--neon); color: var(--black); font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 10px; letter-spacing: 0.25em; text-transform: uppercase; padding: 4px 12px; }
  .price-plan { font-family: 'Barlow Condensed', sans-serif; font-size: 13px; letter-spacing: 0.3em; text-transform: uppercase; color: var(--grey); margin-bottom: 10px; }
  .price-amount { font-family: 'Bebas Neue', sans-serif; font-size: 72px; line-height: 1; color: var(--white); margin-bottom: 4px; }
  .price-amount span { font-size: 28px; color: var(--grey); }
  .price-period { font-size: 13px; color: var(--grey); letter-spacing: 0.1em; margin-bottom: 28px; font-family: 'Barlow Condensed', sans-serif; }
  .price-divider { height: 1px; background: var(--border); margin-bottom: 24px; }
  .price-features { list-style: none; display: flex; flex-direction: column; gap: 12px; margin-bottom: 32px; }
  .price-features li { display: flex; align-items: center; gap: 12px; font-size: 15px; color: var(--light-grey); }
  .price-features li::before { content: ''; width: 6px; height: 6px; background: var(--neon); flex-shrink: 0; clip-path: polygon(20% 0%,80% 0%,100% 20%,100% 80%,80% 100%,20% 100%,0% 80%,0% 20%); }
  .price-card.featured .price-features li { color: var(--white); }

  /* CTA SECTION */
  #cta { position: relative; overflow: hidden; padding: 130px 6vw; display: flex; align-items: center; justify-content: center; text-align: center; }
  .cta-bg { position: absolute; inset: 0; background-image: url('https://images.unsplash.com/photo-1571019613454-1cb2f99b2d8b?w=1600&q=85&auto=format'); background-size: cover; background-position: center; filter: brightness(0.18) saturate(0.7); }
  .cta-overlay { position: absolute
