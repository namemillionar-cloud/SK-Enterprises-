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
  .cta-overlay { position: absolute; inset: 0; background: radial-gradient(ellipse at center, rgba(170,255,0,0.07) 0%, rgba(0,0,0,0.85) 70%); }
  .cta-content { position: relative; z-index: 2; max-width: 800px; }
  .cta-label { margin-bottom: 20px; }
  .cta-title { font-size: clamp(48px, 7vw, 96px); color: var(--white); margin-bottom: 20px; }
  .cta-title .accent { color: var(--neon); }
  .cta-sub { font-size: 18px; color: rgba(255,255,255,0.58); line-height: 1.6; margin-bottom: 52px; }
  .cta-btns { display: flex; flex-wrap: wrap; justify-content: center; gap: 16px; }
  .btn-call {
    display: inline-flex; align-items: center; gap: 12px;
    background: transparent; color: var(--white);
    font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 22px;
    letter-spacing: 0.08em; text-transform: uppercase; padding: 20px 48px;
    border: 2px solid var(--neon); cursor: none; text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 14px) 0, 100% 14px, 100% 100%, 14px 100%, 0 calc(100% - 14px));
    transition: background 0.3s, box-shadow 0.3s, transform 0.2s, color 0.3s;
  }
  .btn-call:hover { background: var(--neon); color: var(--black); box-shadow: 0 0 60px rgba(170,255,0,0.5); transform: translateY(-3px); }
  .btn-call svg { width: 20px; height: 20px; fill: currentColor; }
  .btn-wa {
    display: inline-flex; align-items: center; gap: 10px;
    background: #25D366; color: var(--white);
    font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 15px;
    letter-spacing: 0.15em; text-transform: uppercase; padding: 20px 36px;
    border: none; cursor: none; text-decoration: none;
    clip-path: polygon(0 0, calc(100% - 14px) 0, 100% 14px, 100% 100%, 14px 100%, 0 calc(100% - 14px));
    transition: filter 0.3s, transform 0.2s;
  }
  .btn-wa:hover { filter: brightness(1.2); transform: translateY(-3px); }
  .btn-wa svg { width: 18px; height: 18px; fill: white; }

  /* FLOATING */
  .floating-cta { position: fixed; bottom: 30px; right: 24px; z-index: 90; display: flex; flex-direction: column; gap: 12px; align-items: flex-end; }
  .float-btn { display: flex; align-items: center; gap: 10px; padding: 14px 20px; border: none; cursor: none; text-decoration: none; font-family: 'Barlow Condensed', sans-serif; font-weight: 900; font-size: 13px; letter-spacing: 0.15em; text-transform: uppercase; transition: transform 0.2s, box-shadow 0.2s; box-shadow: 0 4px 24px rgba(0,0,0,0.6); clip-path: polygon(0 0, calc(100% - 10px) 0, 100% 10px, 100% 100%, 10px 100%, 0 calc(100% - 10px)); }
  .float-btn svg { width: 18px; height: 18px; flex-shrink: 0; }
  .float-btn:hover { transform: translateX(-4px) scale(1.04); }
  .float-wa { background: #25D366; color: white; }
  .float-wa svg { fill: white; }
  .float-call { background: var(--neon); color: var(--black); }
  .float-call svg { fill: var(--black); }
  .float-call:hover { box-shadow: 0 0 30px rgba(170,255,0,0.5); }

  /* MARQUEE */
  .marquee-strip { background: var(--neon); padding: 14px 0; overflow: hidden; white-space: nowrap; position: relative; z-index: 3; }
  .marquee-inner { display: inline-flex; animation: marquee 20s linear infinite; }
  .marquee-item { font-family: 'Bebas Neue', sans-serif; font-size: 18px; letter-spacing: 0.08em; color: var(--black); padding: 0 32px; display: inline-flex; align-items: center; gap: 16px; }
  .marquee-dot { width: 6px; height: 6px; background: rgba(0,0,0,0.28); border-radius: 50%; }
  @keyframes marquee { from { transform: translateX(0); } to { transform: translateX(-50%); } }

  /* FOOTER */
  footer { background: var(--charcoal); border-top: 1px solid var(--border); padding: 60px 6vw 36px; }
  .footer-inner { display: grid; grid-template-columns: 1.5fr 1fr 1fr; gap: 40px; margin-bottom: 48px; }
  .footer-logo { font-family: 'Bebas Neue', sans-serif; font-size: 32px; margin-bottom: 12px; }
  .footer-logo span { color: var(--neon); }
  .footer-tagline { font-size: 15px; color: var(--grey); line-height: 1.7; max-width: 280px; margin-bottom: 20px; }
  .footer-social { display: flex; gap: 12px; }
  .social-btn { width: 38px; height: 38px; background: var(--border); display: grid; place-items: center; text-decoration: none; transition: background 0.2s; clip-path: polygon(20% 0%,80% 0%,100% 20%,100% 80%,80% 100%,20% 100%,0% 80%,0% 20%); }
  .social-btn:hover { background: var(--neon); }
  .social-btn svg { width: 16px; height: 16px; stroke: var(--grey); fill: none; stroke-width: 2; transition: stroke 0.2s; }
  .social-btn:hover svg { stroke: var(--black); }
  .footer-col h4 { font-family: 'Barlow Condensed', sans-serif; font-size: 13px; letter-spacing: 0.25em; text-transform: uppercase; color: var(--neon); margin-bottom: 20px; font-weight: 600; }
  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: 10px; }
  .footer-col ul li a { font-size: 14px; color: var(--grey); text-decoration: none; transition: color 0.2s; }
  .footer-col ul li a:hover { color: var(--white); }
  .footer-contact { font-size: 14px; color: var(--grey); line-height: 2; }
  .footer-contact a { color: var(--neon); text-decoration: none; }
  .footer-bottom { border-top: 1px solid var(--border); padding-top: 24px; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 12px; }
  .footer-copy { font-size: 13px; color: rgba(255,255,255,0.22); }
  .footer-copy span { color: var(--neon); }

  /* REVEAL */
  .reveal { opacity: 0; transform: translateY(40px); transition: opacity 0.8s cubic-bezier(0.4,0,0.2,1), transform 0.8s cubic-bezier(0.4,0,0.2,1); }
  .reveal.visible { opacity: 1; transform: translateY(0); }
  .reveal-left { opacity: 0; transform: translateX(-50px); transition: opacity 0.8s ease, transform 0.8s ease; }
  .reveal-left.visible { opacity: 1; transform: translateX(0); }
  .reveal-right { opacity: 0; transform: translateX(50px); transition: opacity 0.8s ease, transform 0.8s ease; }
  .reveal-right.visible { opacity: 1; transform: translateX(0); }
  .stagger > * { opacity: 0; transform: translateY(30px); transition: opacity 0.6s ease, transform 0.6s ease; }
  .stagger.visible > *:nth-child(1) { opacity:1; transform:none; transition-delay:0.08s; }
  .stagger.visible > *:nth-child(2) { opacity:1; transform:none; transition-delay:0.18s; }
  .stagger.visible > *:nth-child(3) { opacity:1; transform:none; transition-delay:0.28s; }
  .stagger.visible > *:nth-child(4) { opacity:1; transform:none; transition-delay:0.38s; }
  .stagger.visible > *:nth-child(5) { opacity:1; transform:none; transition-delay:0.48s; }

  /* RESPONSIVE */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .hamburger { display: flex; }
    .transform-inner { grid-template-columns: 1fr; }
    .transform-right { height: 360px; }
    .hero-stats { position: static; display: flex; flex-wrap: wrap; margin-top: 36px; }
    .footer-inner { grid-template-columns: 1fr 1fr; }
    .pricing-grid { max-width: 440px; }
    .price-card.featured { transform: scale(1); }
  }
  @media (max-width: 600px) {
    nav { padding: 0 4vw; }
    .nav-cta { gap: 8px; }
    .nav-phone { font-size: 13px; }
    .hero-btns { flex-direction: column; align-items: flex-start; }
    .cta-btns { flex-direction: column; align-items: center; }
    .footer-inner { grid-template-columns: 1fr; }
    .float-btn span { display: none; }
    .float-btn { padding: 14px; }
    .section-pad { padding: 70px 5vw; }
    .hero-content { padding: 0 5vw; }
    .btn-call { font-size: 16px; padding: 18px 32px; }
    .pricing-grid { grid-template-columns: 1fr; }
  }
</style>
</head>
<body>

<div class="cursor" id="cursor"></div>
<div class="cursor-ring" id="cursorRing"></div>

<!-- FLOATING CTAs -->
<div class="floating-cta">
  <a href="https://wa.me/919930548676" class="float-btn float-wa" target="_blank" rel="noopener">
    <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347zM12 0C5.373 0 0 5.373 0 12c0 2.124.556 4.118 1.527 5.845L.057 23.998l6.344-1.44A11.945 11.945 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.898 0-3.668-.52-5.183-1.426L3 21.818l1.27-4.698A9.939 9.939 0 012 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z"/></svg>
    <span>WhatsApp Us</span>
  </a>
  <a href="tel:09930548676" class="float-btn float-call">
    <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
    <span>Call Now</span>
  </a>
</div>

<!-- NAV -->
<nav id="navbar">
  <a href="#hero" class="nav-logo">
    <div class="nav-logo-icon">
      <svg viewBox="0 0 24 24"><path d="M20.57 14.86L22 13.43 20.57 12 17 15.57 8.43 7 12 3.43 10.57 2 9.14 3.43 7.71 2 5.57 4.14 4.14 2.71 2.71 4.14l1.43 1.43L2 7.71l1.43 1.43L2 10.57 3.43 12 7 8.43 15.57 17 12 20.57 13.43 22l1.43-1.43L16.29 22l2.14-2.14 1.43 1.43 1.43-1.43-1.43-1.43L22 16.29z"/></svg>
    </div>
    HULK <span>GYM</span>
  </a>
  <div class="nav-links" id="navLinks">
    <a href="#why">Why Us</a>
    <a href="#transform">Results</a>
    <a href="#trainers">Trainers</a>
    <a href="#testimonials">Reviews</a>
    <a href="#pricing">Pricing</a>
  </div>
  <div class="nav-cta">
    <a href="tel:09930548676" class="nav-phone">
      <svg viewBox="0 0 24 24"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
      099305 48676
    </a>
    <a href="#cta" class="nav-join">Join Now</a>
    <button class="hamburger" id="hamburger" onclick="toggleMenu()" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg" id="heroBg"></div>
  <div class="hero-overlay"></div>
  <div class="hero-overlay2"></div>
  <div class="hero-neon-line"></div>
  <div class="hero-content">
    <div class="hero-label">
      <div class="hero-label-line"></div>
      <span class="label">Premium Fitness Club · Est. 2020</span>
    </div>
    <h1 class="display hero-eyebrow">
      Build<br>The Body.<br>
      <span class="accent">Unleash</span><br>The Hulk.
    </h1>
    <p class="hero-sub">
      This is not just a gym. This is your <strong>transformation zone</strong> — where limits shatter, strength is born, and champions are made.
    </p>
    <div class="hero-btns">
      <a href="#cta" class="btn-primary">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M8 5v14l11-7z"/></svg>
        Join Now
      </a>
      <a href="tel:09930548676" class="btn-outline">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="currentColor"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
        Book Free Trial
      </a>
    </div>
    <div class="hero-stats">
      <div class="stat"><div class="stat-number" data-target="500" data-suffix="+">0+</div><div class="stat-label">Members</div></div>
      <div class="stat"><div class="stat-number" data-target="98" data-suffix="%">0%</div><div class="stat-label">Success Rate</div></div>
      <div class="stat"><div class="stat-number" data-target="5" data-suffix="★">0★</div><div class="stat-label">Rating</div></div>
    </div>
  </div>
  <div class="hero-scroll">
    <div class="scroll-line"></div>
    <div class="scroll-text">Scroll Down</div>
  </div>
</section>

<!-- MARQUEE -->
<div class="marquee-strip">
  <div class="marquee-inner">
    <span class="marquee-item">Expert Trainers <span class="marquee-dot"></span></span>
    <span class="marquee-item">Proven Results <span class="marquee-dot"></span></span>
    <span class="marquee-item">Friendly Environment <span class="marquee-dot"></span></span>
    <span class="marquee-item">Value For Money <span class="marquee-dot"></span></span>
    <span class="marquee-item">Real Transformations <span class="marquee-dot"></span></span>
    <span class="marquee-item">Join The Hulk Family <span class="marquee-dot"></span></span>
    <span class="marquee-item">Expert Trainers <span class="marquee-dot"></span></span>
    <span class="marquee-item">Proven Results <span class="marquee-dot"></span></span>
    <span class="marquee-item">Friendly Environment <span class="marquee-dot"></span></span>
    <span class="marquee-item">Value For Money <span class="marquee-dot"></span></span>
    <span class="marquee-item">Real Transformations <span class="marquee-dot"></span></span>
    <span class="marquee-item">Join The Hulk Family <span class="marquee-dot"></span></span>
  </div>
</div>

<!-- WHY HULK -->
<section id="why" class="section-pad">
  <div class="section-header reveal">
    <p class="label">Why Choose Us</p>
    <h2 class="display section-title">The Hulk <span class="accent">Difference</span></h2>
    <p class="section-desc">We don't do mediocre. Every rep, every session, every trainer — engineered to push you further than you thought possible.</p>
  </div>
  <div class="why-grid stagger">
    <div class="why-card">
      <div class="card-number">01</div>
      <div class="why-icon">
        <svg viewBox="0 0 24 24"><path d="M20.57 14.86L22 13.43 20.57 12 17 15.57 8.43 7 12 3.43 10.57 2 9.14 3.43 7.71 2 5.57 4.14 4.14 2.71 2.71 4.14l1.43 1.43L2 7.71l1.43 1.43L2 10.57 3.43 12 7 8.43 15.57 17 12 20.57 13.43 22l1.43-1.43L16.29 22l2.14-2.14 1.43 1.43 1.43-1.43-1.43-1.43L22 16.29z"/></svg>
      </div>
      <h3>Elite Expert Trainers</h3>
      <p>Our coaches bring real knowledge and unmatched passion. Every concept explained with depth and zero shortcuts — because your results deserve nothing less.</p>
    </div>
    <div class="why-card">
      <div class="card-number">02</div>
      <div class="why-icon">
        <svg viewBox="0 0 24 24"><circle cx="12" cy="12" r="10"/><path d="M8 14s1.5 2 4 2 4-2 4-2M9 9h.01M15 9h.01"/></svg>
      </div>
      <h3>Warm Friendly Atmosphere</h3>
      <p>Feel at home from day one. Whether you're a beginner or a seasoned lifter, our community uplifts, encourages, and celebrates every milestone together.</p>
    </div>
    <div class="why-card">
      <div class="card-number">03</div>
      <div class="why-icon">
        <svg viewBox="0 0 24 24"><path d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"/></svg>
      </div>
      <h3>Always There For You</h3>
      <p>No confusion ever left behind. Our trainers are always available to solve doubts, correct form, and fine-tune technique so every session counts to the max.</p>
    </div>
    <div class="why-card">
      <div class="card-number">04</div>
      <div class="why-icon">
        <svg viewBox="0 0 24 24"><polyline points="22 12 18 12 15 21 9 3 6 12 2 12"/></svg>
      </div>
      <h3>Proven Real Results</h3>
      <p>We don't promise — we deliver. Hundreds of transformations in fat loss, muscle gain, and endurance. Real people. Real strength. Real change.</p>
    </div>
    <div class="why-card">
      <div class="card-number">05</div>
      <div class="why-icon">
        <svg viewBox="0 0 24 24"><path d="M12 2l3.09 6.26L22 9.27l-5 4.87 1.18 6.88L12 17.77l-6.18 3.25L7 14.14 2 9.27l6.91-1.01L12 2z"/></svg>
      </div>
      <h3>Worth Every Rupee</h3>
      <p>Premium quality at honest pricing. The best investment you'll ever make is in yourself — and HULK GYM ensures that investment pays back tenfold.</p>
    </div>
  </div>
</section>

<!-- TRANSFORMATION -->
<section id="transform">
  <div class="transform-inner">
    <div class="transform-left reveal-left">
      <div class="result-tag">Real Results</div>
      <h2 class="display transform-title">Real Strength.<br><span style="color:var(--neon)">Real Change.</span></h2>
      <p class="transform-body">Your transformation isn't a myth — it's a method. We combine science-backed training, expert guidance, and relentless motivation to sculpt the body you've always envisioned.</p>
      <div class="result-bars" id="resultBars">
        <div class="result-bar-item">
          <div class="result-bar-top"><span class="result-bar-label">Fat Loss</span><span class="result-bar-pct">94%</span></div>
          <div class="result-bar-track"><div class="result-bar-fill" style="--w:0.94"></div></div>
        </div>
        <div class="result-bar-item">
          <div class="result-bar-top"><span class="result-bar-label">Muscle Gain</span><span class="result-bar-pct">89%</span></div>
          <div class="result-bar-track"><div class="result-bar-fill" style="--w:0.89"></div></div>
        </div>
        <div class="result-bar-item">
          <div class="result-bar-top"><span class="result-bar-label">Strength & Endurance</span><span class="result-bar-pct">97%</span></div>
          <div class="result-bar-track"><div class="result-bar-fill" style="--w:0.97"></div></div>
        </div>
        <div class="result-bar-item">
          <div class="result-bar-top"><span class="result-bar-label">Member Satisfaction</span><span class="result-bar-pct">100%</span></div>
          <div class="result-bar-track"><div class="result-bar-fill" style="--w:1.0"></div></div>
        </div>
      </div>
      <a href="tel:09930548676" class="btn-primary">Start Your Transformation</a>
    </div>
    <div class="transform-right reveal-right">
      <img class="transform-img"
        src="https://images.unsplash.com/photo-1581009146145-b5ef050c2e1e?w=900&q=85&auto=format"
        alt="Intense gym training" loading="lazy"/>
      <div class="transform-overlay"></div>
    </div>
  </div>
</section>

<!-- TRAINERS -->
<section id="trainers" class="section-pad">
  <div class="section-header reveal">
    <p class="label">Meet The Masters</p>
    <h2 class="display section-title">Our <span class="accent">Expert</span> Trainers</h2>
    <p class="section-desc">World-class expertise. Unmatched passion. Your trainers aren't just coaches — they're architects of transformation.</p>
  </div>
  <div class="trainers-grid stagger">
    <div class="trainer-card">
      <div class="trainer-img-wrap">
        <img class="trainer-img"
          src="https://images.unsplash.com/photo-1567013127542-490d757e51fc?w=800&q=85&auto=format"
          alt="Latesh Sir – Head Trainer" loading="lazy"/>
        <div class="trainer-img-overlay"></div>
        <div class="trainer-badge">Head Trainer</div>
      </div>
      <div class="trainer-info">
        <div class="trainer-name">Latesh Sir</div>
        <div class="trainer-role">Strength & Conditioning Expert</div>
        <p class="trainer-bio">Renowned for explaining every concept with exceptional depth and clarity. With Latesh Sir, no doubt goes unsolved — his methodical approach ensures you don't just train, you master your craft completely.</p>
        <div class="trainer-tags">
          <span class="trainer-tag">Strength Training</span>
          <span class="trainer-tag">Body Composition</span>
          <span class="trainer-tag">Nutrition</span>
        </div>
      </div>
    </div>
    <div class="trainer-card">
      <div class="trainer-img-wrap">
        <img class="trainer-img"
          src="https://images.unsplash.com/photo-1518611012118-696072aa579a?w=800&q=85&auto=format"
          alt="Pooja Teacher – Senior Coach" loading="lazy"/>
        <div class="trainer-img-overlay"></div>
        <div class="trainer-badge">Senior Coach</div>
      </div>
      <div class="trainer-info">
        <div class="trainer-name">Pooja Teacher</div>
        <div class="trainer-role">Fitness & Conditioning Coach</div>
        <p class="trainer-bio">Outstanding, clear, engaging, and conceptually powerful. Pooja's high-energy sessions break down complex fitness science into actionable steps that deliver real, visible results faster than you thought possible.</p>
        <div class="trainer-tags">
          <span class="trainer-tag">HIIT & Cardio</span>
          <span class="trainer-tag">Flexibility</span>
          <span class="trainer-tag">Weight Management</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials" class="section-pad" style="padding-bottom:0">
  <div class="section-header reveal" style="text-align:center; max-width:600px; margin:0 auto 60px;">
    <p class="label">Member Stories</p>
    <h2 class="display section-title">What Our <span class="accent">Members</span> Say</h2>
    <p class="section-desc" style="margin:16px auto 0;">Real voices. Real transformations. Real proof that HULK GYM delivers on every single promise made.</p>
  </div>
  <div class="testi-track-wrap">
    <div class="testi-track">
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Latesh Sir explains every concept with exceptional depth and clarity. My entire understanding of training transformed — doubts dissolved, strength multiplied beyond belief."</p>
        <div class="testi-author"><div class="testi-avatar">KC</div><div><div class="testi-name">Ketan Choudhari</div><div class="testi-member">Member · 1 Year</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Pooja Teacher's coaching is absolutely outstanding — clear, engaging, and conceptually strong. Every session leaves me feeling powerful and unstoppable."</p>
        <div class="testi-author"><div class="testi-avatar">PK</div><div><div class="testi-name">Priya Kulkarni</div><div class="testi-member">Member · 8 Months</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Amazing faculty, always available for doubt solving, very friendly environment. This is more than just a gym — it truly is a second home for me."</p>
        <div class="testi-author"><div class="testi-avatar">SR</div><div><div class="testi-name">Shubham Rathod</div><div class="testi-member">Member · 1.5 Years</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Worth every rupee — hands down the best gym in the area. I saw more results in 3 months at HULK than anywhere else in an entire year combined."</p>
        <div class="testi-author"><div class="testi-avatar">YP</div><div><div class="testi-name">Yash Prasad</div><div class="testi-member">Member · 6 Months</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"HULK GYM gave me more than a body transformation — it gave me confidence, discipline, and a community that genuinely cares. I wake up excited to train."</p>
        <div class="testi-author"><div class="testi-avatar">RK</div><div><div class="testi-name">Rahul Kale</div><div class="testi-member">Member · 2 Years</div></div></div>
      </div>
      <!-- Duplicates for infinite loop -->
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Latesh Sir explains every concept with exceptional depth and clarity. My entire understanding of training transformed — doubts dissolved, strength multiplied beyond belief."</p>
        <div class="testi-author"><div class="testi-avatar">KC</div><div><div class="testi-name">Ketan Choudhari</div><div class="testi-member">Member · 1 Year</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Pooja Teacher's coaching is absolutely outstanding — clear, engaging, and conceptually strong. Every session leaves me feeling powerful and unstoppable."</p>
        <div class="testi-author"><div class="testi-avatar">PK</div><div><div class="testi-name">Priya Kulkarni</div><div class="testi-member">Member · 8 Months</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Amazing faculty, always available for doubt solving, very friendly environment. This is more than just a gym — it truly is a second home for me."</p>
        <div class="testi-author"><div class="testi-avatar">SR</div><div><div class="testi-name">Shubham Rathod</div><div class="testi-member">Member · 1.5 Years</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"Worth every rupee — hands down the best gym in the area. I saw more results in 3 months at HULK than anywhere else in an entire year combined."</p>
        <div class="testi-author"><div class="testi-avatar">YP</div><div><div class="testi-name">Yash Prasad</div><div class="testi-member">Member · 6 Months</div></div></div>
      </div>
      <div class="testi-card">
        <div class="stars">★★★★★</div>
        <p class="testi-text">"HULK GYM gave me more than a body transformation — it gave me confidence, discipline, and a community that genuinely cares. I wake up excited to train."</p>
        <div class="testi-author"><div class="testi-avatar">RK</div><div><div class="testi-name">Rahul Kale</div><div class="testi-member">Member · 2 Years</div></div></div>
      </div>
    </div>
  </div>
</section>

<!-- PRICING -->
<section id="pricing" class="section-pad">
  <div class="section-header reveal" style="text-align:center; max-width:600px; margin:0 auto 60px;">
    <p class="label">Membership Plans</p>
    <h2 class="display section-title">Invest In Your <span class="accent">Strength</span></h2>
    <p class="section-desc" style="margin:16px auto 0;">Transparent pricing. No hidden fees. Premium value for real results — every plan is built to help you win.</p>
  </div>
  <div class="pricing-grid stagger" style="margin:0 auto;">
    <div class="price-card">
      <div class="price-plan">Starter</div>
      <div class="price-amount"><span>₹</span>1,299</div>
      <div class="price-period">/ month</div>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Full Gym Access</li>
        <li>Locker & Changing Room</li>
        <li>Basic Trainer Guidance</li>
        <li>Group Workout Sessions</li>
      </ul>
      <a href="tel:09930548676" class="btn-outline" style="width:100%;justify-content:center;">Get Started</a>
    </div>
    <div class="price-card featured">
      <div class="price-badge">Most Popular</div>
      <div class="price-plan">Champion</div>
      <div class="price-amount"><span>₹</span>2,199</div>
      <div class="price-period">/ month</div>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Everything in Starter</li>
        <li>Personal Training (4 sessions)</li>
        <li>Custom Diet & Nutrition Plan</li>
        <li>Weekly Progress Tracking</li>
        <li>Priority Trainer Access</li>
      </ul>
      <a href="tel:09930548676" class="btn-primary" style="width:100%;justify-content:center;">Join Champion</a>
    </div>
    <div class="price-card">
      <div class="price-plan">Elite</div>
      <div class="price-amount"><span>₹</span>3,499</div>
      <div class="price-period">/ month</div>
      <div class="price-divider"></div>
      <ul class="price-features">
        <li>Everything in Champion</li>
        <li>Unlimited Personal Training</li>
        <li>Custom Workout Programming</li>
        <li>Body Composition Analysis</li>
        <li>24/7 WhatsApp Support</li>
      </ul>
      <a href="tel:09930548676" class="btn-outline" style="width:100%;justify-content:center;">Go Elite</a>
    </div>
  </div>
  <p style="text-align:center;margin-top:28px;font-size:14px;color:var(--grey);">
    * Annual plans available at up to 30% discount &nbsp;·&nbsp; Call for custom packages
  </p>
</section>

<!-- CTA -->
<section id="cta">
  <div class="cta-bg"></div>
  <div class="cta-overlay"></div>
  <div class="cta-content reveal">
    <p class="label cta-label">Your Time Is Now</p>
    <h2 class="display cta-title">Your Transformation<br><span class="accent">Starts Today.</span></h2>
    <p class="cta-sub">Stop waiting. Stop overthinking. The only bad workout is the one that never happened. Pick up the phone — we'll handle everything else.</p>
    <div class="cta-btns">
      <a href="tel:09930548676" class="btn-call">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24 1.12.37 2.33.57 3.57.57.55 0 1 .45 1 1V20c0 .55-.45 1-1 1-9.39 0-17-7.61-17-17 0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1 0 1.25.2 2.45.57 3.57.11.35.03.74-.25 1.02l-2.2 2.2z"/></svg>
        Call Now — 099305 48676
      </a>
      <a href="https://wa.me/919930548676" class="btn-wa" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347zM12 0C5.373 0 0 5.373 0 12c0 2.124.556 4.118 1.527 5.845L.057 23.998l6.344-1.44A11.945 11.945 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.898 0-3.668-.52-5.183-1.426L3 21.818l1.27-4.698A9.939 9.939 0 012 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z"/></svg>
        WhatsApp Us
      </a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-inner">
    <div>
      <div class="footer-logo">HULK <span>GYM</span></div>
      <p class="footer-tagline">Where iron meets will. Where ordinary becomes legendary. Your transformation zone — open daily, waiting for you.</p>
      <div class="footer-social">
        <a href="#" class="social-btn" aria-label="Instagram">
          <svg viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="20" rx="5" ry="5"/><path d="M16 11.37A4 4 0 1112.63 8 4 4 0 0116 11.37z"/><line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/></svg>
        </a>
        <a href="#" class="social-btn" aria-label="Facebook">
          <svg viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"/></svg>
        </a>
        <a href="https://wa.me/919930548676" class="social-btn" aria-label="WhatsApp">
          <svg viewBox="0 0 24 24"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347zM12 0C5.373 0 0 5.373 0 12c0 2.124.556 4.118 1.527 5.845L.057 23.998l6.344-1.44A11.945 11.945 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 22c-1.898 0-3.668-.52-5.183-1.426L3 21.818l1.27-4.698A9.939 9.939 0 012 12C2 6.477 6.477 2 12 2s10 4.477 10 10-4.477 10-10 10z" stroke="none" fill="currentColor"/></svg>
        </a>
        <a href="#" class="social-btn" aria-label="YouTube">
          <svg viewBox="0 0 24 24"><path d="M22.54 6.42a2.78 2.78 0 00-1.95-1.96C18.88 4 12 4 12 4s-6.88 0-8.59.46a2.78 2.78 0 00-1.95 1.96A29 29 0 001 12a29 29 0 00.46 5.58A2.78 2.78 0 003.41 19.6C5.12 20 12 20 12 20s6.88 0 8.59-.46a2.78 2.78 0 001.95-1.95A29 29 0 0023 12a29 29 0 00-.46-5.58z" fill="currentColor" stroke="none"/><polygon points="9.75 15.02 15.5 12 9.75 8.98 9.75 15.02" fill="var(--charcoal)" stroke="none"/></svg>
        </a>
      </div>
    </div>
    <div class="footer-col">
      <h4>Quick Links</h4>
      <ul>
        <li><a href="#why">Why HULK GYM</a></li>
        <li><a href="#transform">Transformations</a></li>
        <li><a href="#trainers">Our Trainers</a></li>
        <li><a href="#testimonials">Testimonials</a></li>
        <li><a href="#pricing">Membership</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Contact Us</h4>
      <div class="footer-contact">
        <div>📞 Call / WhatsApp<br><a href="tel:09930548676">099305 48676</a></div>
        <div style="margin-top:12px">🕒 Open Daily<br>5:00 AM – 10:00 PM</div>
        <div style="margin-top:12px">📍 HULK GYM<br>Your City, Maharashtra</div>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <p class="footer-copy">© 2025 <span>HULK GYM</span>. All rights reserved. Built for Champions.</p>
    <p class="footer-copy">Forged with 💚 by <span>HULK CREATIVE</span></p>
  </div>
</footer>

<script>
/* ── CURSOR ── */
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursorRing');
let mx = -200, my = -200, rx = -200, ry = -200;
document.addEventListener('mousemove', e => { mx = e.clientX; my = e.clientY; });
(function tick() {
  cursor.style.cssText = `left:${mx-5}px;top:${my-5}px`;
  rx += (mx - rx - 18) * 0.13; ry += (my - ry - 18) * 0.13;
  ring.style.cssText = `left:${rx}px;top:${ry}px;width:${ring._w||36}px;height:${ring._h||36}px`;
  requestAnimationFrame(tick);
})();
document.querySelectorAll('a,button').forEach(el => {
  el.addEventListener('mouseenter', () => { cursor.style.transform='scale(3)'; ring._w=60; ring._h=60; });
  el.addEventListener('mouseleave', () => { cursor.style.transform='scale(1)'; ring._w=36; ring._h=36; });
});

/* ── STICKY NAV ── */
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => navbar.classList.toggle('scrolled', scrollY > 60), { passive: true });

/* ── SCROLL REVEAL ── */
const revObs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); revObs.unobserve(e.target); } });
}, { threshold: 0.14 });
document.querySelectorAll('.reveal,.reveal-left,.reveal-right,.stagger').forEach(el => revObs.observe(el));

/* ── RESULT BARS ── */
const barObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (e.isIntersecting) {
      e.target.querySelectorAll('.result-bar-fill').forEach(b => {
        const w = parseFloat(b.style.getPropertyValue('--w'));
        b.style.transform = `scaleX(${w})`;
      });
      barObs.unobserve(e.target);
    }
  });
}, { threshold: 0.3 });
const tb = document.getElementById('resultBars');
if (tb) barObs.observe(tb);

/* ── COUNTER ── */
const cntObs = new IntersectionObserver(entries => {
  entries.forEach(e => {
    if (!e.isIntersecting) return;
    e.target.querySelectorAll('[data-target]').forEach(el => {
      const end = +el.dataset.target, sfx = el.dataset.suffix || '';
      let s = 0, step = end / 80;
      const t = setInterval(() => {
        s = Math.min(s + step, end);
        el.textContent = Math.floor(s) + sfx;
        if (s >= end) clearInterval(t);
      }, 20);
    });
    cntObs.unobserve(e.target);
  });
}, { threshold: 0.5 });
document.querySelectorAll('.hero-stats').forEach(el => cntObs.observe(el));

/* ── PARALLAX ── */
const heroBg = document.getElementById('heroBg');
window.addEventListener('scroll', () => {
  if (heroBg) heroBg.style.transform = `translateY(${scrollY * 0.28}px)`;
}, { passive: true });

/* ── HAMBURGER ── */
let menuOpen = false;
const navLinks = document.getElementById('navLinks');
function toggleMenu() {
  menuOpen = !menuOpen;
  if (menuOpen) {
    navLinks.style.cssText = 'display:flex;flex-direction:column;position:fixed;top:72px;left:0;right:0;background:rgba(0,0,0,0.97);backdrop-filter:blur(20px);padding:36px 6vw;gap:28px;border-bottom:1px solid rgba(170,255,0,0.15);z-index:99;';
  } else {
    navLinks.style.cssText = '';
    if (window.innerWidth < 900) navLinks.style.display = 'none';
  }
}
navLinks.querySelectorAll('a').forEach(a => a.addEventListener('click', () => { menuOpen = false; navLinks.style.cssText = ''; if(window.innerWidth<900) navLinks.style.display='none'; }));
window.addEventListener('resize', () => { if (window.innerWidth >= 900) { navLinks.style.cssText = ''; menuOpen = false; } else if (!menuOpen) navLinks.style.display = 'none'; });
if (window.innerWidth < 900) navLinks.style.display = 'none';
</script>
</body>
</html>
