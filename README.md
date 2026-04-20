<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>S K Enterprises – Real Estate Broker | Dombivli, Maharashtra</title>
<meta name="description" content="S K Enterprises – Sunil Katekar, trusted real estate broker in Dombivli with 25+ years of experience. Buy, sell, or rent property with confidence.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,600;0,700;1,600&family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<style>

/* ===== RESET ===== */
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth;font-size:16px}
body{font-family:'Inter',sans-serif;color:#222;background:#fff;overflow-x:hidden;-webkit-text-size-adjust:100%;text-size-adjust:100%}
img,svg,iframe{max-width:100%;display:block}
a{text-decoration:none}
ul{list-style:none}
button{font-family:'Inter',sans-serif}

/* ===== VARS ===== */
:root{
  --gold:#B8962E;--gold-lt:#D4AF4A;
  --dark:#0D1F12;--dark2:#162A1A;--gmid:#1E3A24;
  --cream:#F9F6F0;--text-lt:#555;--border:rgba(0,0,0,0.09);
  --shadow-sm:0 2px 12px rgba(0,0,0,0.08);
  --shadow-md:0 8px 32px rgba(0,0,0,0.12);
  --shadow-lg:0 20px 60px rgba(0,0,0,0.15);
  --r:10px;
  --px:clamp(16px,5vw,72px);
}

/* ===== UTILS ===== */
.wrap{width:100%;max-width:1180px;margin:0 auto;padding:0 var(--px)}
.section{padding:clamp(56px,8vw,104px) 0}
.sec-tag{display:inline-block;font-size:0.7rem;font-weight:700;letter-spacing:0.15em;text-transform:uppercase;color:var(--gold);margin-bottom:10px}
.sec-title{font-family:'Playfair Display',serif;font-size:clamp(1.7rem,3.8vw,2.8rem);font-weight:700;line-height:1.18;color:var(--dark)}
.sec-title em{color:var(--gold);font-style:italic}
.sec-title.light{color:#fff}
.sec-line{width:44px;height:3px;background:linear-gradient(90deg,var(--gold),transparent);margin:14px 0 22px;border-radius:2px}
.sec-line.c{margin:14px auto 22px}
.sec-sub{font-size:clamp(0.86rem,1.8vw,0.97rem);color:var(--text-lt);line-height:1.75;max-width:540px}
.reveal{opacity:0;transform:translateY(22px);transition:opacity .65s ease,transform .65s ease}
.reveal.on{opacity:1;transform:translateY(0)}

/* ===========================
   NAVBAR
=========================== */
.nb{position:fixed;top:0;left:0;right:0;z-index:9999;background:rgba(13,31,18,.96);backdrop-filter:blur(14px);-webkit-backdrop-filter:blur(14px);border-bottom:1px solid rgba(184,150,46,.2);transition:.3s}
.nb-inner{display:flex;align-items:center;justify-content:space-between;height:62px;padding:0 var(--px)}
.nb-logo{font-family:'Playfair Display',serif;font-size:1.3rem;font-weight:700;color:var(--gold-lt);white-space:nowrap}
.nb-logo span{color:#fff}
.nb-desk{display:flex;align-items:center;gap:26px}
.nb-desk a{font-size:0.8rem;font-weight:500;color:rgba(255,255,255,.78);letter-spacing:.05em;text-transform:uppercase;transition:color .2s}
.nb-desk a:hover{color:var(--gold-lt)}
.nb-desk .nbtn{background:var(--gold);color:var(--dark)!important;padding:9px 18px;border-radius:5px;font-weight:700;font-size:.8rem;transition:background .2s,transform .2s}
.nb-desk .nbtn:hover{background:var(--gold-lt);transform:translateY(-1px)}
.hbg{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:8px;background:none;border:none}
.hbg span{display:block;width:22px;height:2px;background:#fff;border-radius:2px;transition:.3s}
.hbg.open span:nth-child(1){transform:translateY(7px) rotate(45deg)}
.hbg.open span:nth-child(2){opacity:0}
.hbg.open span:nth-child(3){transform:translateY(-7px) rotate(-45deg)}
.nb-mob{display:none;flex-direction:column;background:rgba(13,31,18,.98);border-top:1px solid rgba(184,150,46,.12);overflow:hidden;max-height:0;transition:max-height .4s ease}
.nb-mob.open{max-height:360px}
.nb-mob a{padding:13px var(--px);font-size:.92rem;font-weight:500;color:rgba(255,255,255,.82);border-bottom:1px solid rgba(255,255,255,.05);display:block}
.nb-mob a:last-child{border-bottom:none}
.nb-mob .mb-cta{background:var(--gold);color:var(--dark)!important;font-weight:700;margin:10px var(--px) 14px;border-radius:6px;text-align:center;padding:12px var(--px)!important;border-bottom:none!important}

/* ===========================
   HERO
=========================== */
.hero{min-height:100svh;background:linear-gradient(150deg,#0D1F12 0%,#1A3020 55%,#0D1F12 100%);position:relative;overflow:hidden;display:flex;align-items:center;padding-top:62px}
.hero-dots{position:absolute;inset:0;pointer-events:none;background-image:radial-gradient(circle,rgba(184,150,46,.11) 1px,transparent 1px);background-size:36px 36px}
.hero-b1{position:absolute;width:480px;height:480px;background:radial-gradient(circle,rgba(184,150,46,.09) 0%,transparent 70%);top:-130px;right:-60px;pointer-events:none}
.hero-b2{position:absolute;width:340px;height:340px;background:radial-gradient(circle,rgba(30,100,50,.2) 0%,transparent 70%);bottom:-70px;left:5%;pointer-events:none}
.hero-grid{position:relative;z-index:2;width:100%;padding:clamp(44px,7vw,92px) var(--px);display:grid;grid-template-columns:1fr 1fr;gap:clamp(28px,5vw,68px);align-items:center;max-width:1180px;margin:0 auto}
.hero-pill{display:inline-flex;align-items:center;gap:7px;background:rgba(184,150,46,.12);border:1px solid rgba(184,150,46,.3);color:var(--gold-lt);padding:6px 14px;border-radius:40px;font-size:.7rem;font-weight:700;letter-spacing:.1em;text-transform:uppercase;margin-bottom:18px;animation:fadeUp .7s ease both}
.hero-pill::before{content:'✦';font-size:.6rem}
.hero-h1{font-family:'Playfair Display',serif;font-size:clamp(2rem,4.2vw,4rem);font-weight:700;line-height:1.1;color:#fff;animation:fadeUp .7s .12s ease both}
.hero-h1 em{color:var(--gold-lt);font-style:italic}
.hero-sub{margin-top:16px;font-size:clamp(.88rem,1.7vw,1.05rem);color:rgba(255,255,255,.62);line-height:1.72;animation:fadeUp .7s .24s ease both}
.hero-btns{margin-top:28px;display:flex;flex-wrap:wrap;gap:12px;animation:fadeUp .7s .36s ease both}
.btn-gold{background:var(--gold);color:var(--dark);padding:13px 26px;border-radius:6px;font-weight:700;font-size:.9rem;display:inline-flex;align-items:center;gap:7px;transition:all .25s;border:none;cursor:pointer;white-space:nowrap}
.btn-gold:hover{background:var(--gold-lt);transform:translateY(-2px);box-shadow:0 8px 24px rgba(184,150,46,.35)}
.btn-out{background:transparent;color:#fff;padding:13px 26px;border-radius:6px;font-weight:500;font-size:.9rem;display:inline-flex;align-items:center;gap:7px;border:1px solid rgba(255,255,255,.28);transition:all .25s;white-space:nowrap}
.btn-out:hover{border-color:var(--gold-lt);color:var(--gold-lt)}
.hero-stats{margin-top:36px;display:flex;gap:clamp(18px,3.5vw,38px);flex-wrap:wrap;animation:fadeUp .7s .48s ease both}
.hsn{font-family:'Playfair Display',serif;font-size:clamp(1.7rem,3.2vw,2.5rem);font-weight:700;color:var(--gold-lt);line-height:1}
.hsl{font-size:.72rem;color:rgba(255,255,255,.46);margin-top:3px;letter-spacing:.04em}
.hero-vis{display:flex;flex-direction:column;gap:13px;animation:fadeUp .7s .2s ease both}
.hv-main{border-radius:12px;overflow:hidden;border:1px solid rgba(184,150,46,.2);box-shadow:var(--shadow-lg);width:100%;aspect-ratio:4/3}
.hv-row{display:grid;grid-template-columns:1fr 1fr;gap:13px}
.hv-mini{border-radius:10px;overflow:hidden;border:1px solid rgba(184,150,46,.2);background:rgba(13,31,18,.95);padding:16px}
.vm-ico{font-size:1.5rem;margin-bottom:7px}
.vm-lbl{color:var(--gold-lt);font-size:.72rem;font-weight:600;letter-spacing:.04em}
.vm-val{color:#fff;font-size:1.1rem;font-weight:700;margin-top:3px}
.vm-sub{color:rgba(255,255,255,.36);font-size:.68rem;margin-top:2px}

/* ===========================
   ABOUT
=========================== */
.about{background:#fff}
.about-grid{display:grid;grid-template-columns:360px 1fr;gap:clamp(28px,5.5vw,76px);align-items:center}
.about-card-wrap{position:relative;flex-shrink:0}
.about-card{background:linear-gradient(160deg,var(--gmid),var(--dark));border-radius:14px;overflow:hidden;position:relative;aspect-ratio:3/4;display:flex;align-items:flex-end;box-shadow:var(--shadow-lg)}
.about-card-body{width:100%;height:100%;display:flex;align-items:center;justify-content:center}
.about-overlay{position:absolute;bottom:0;left:0;right:0;background:linear-gradient(to top,rgba(13,31,18,.95) 0%,transparent 70%);padding:24px 22px 20px}
.about-nm{font-family:'Playfair Display',serif;font-size:1.38rem;font-weight:700;color:#fff}
.about-rl{color:var(--gold-lt);font-size:.78rem;font-weight:600;margin-top:4px}
.exp-bdg{position:absolute;top:-14px;right:-14px;width:88px;height:88px;border-radius:50%;background:var(--gold);display:flex;flex-direction:column;align-items:center;justify-content:center;box-shadow:0 8px 24px rgba(184,150,46,.45);z-index:10}
.exp-n{font-family:'Playfair Display',serif;font-size:1.8rem;font-weight:700;color:var(--dark);line-height:1}
.exp-l{font-size:.52rem;font-weight:700;color:var(--dark);text-transform:uppercase;letter-spacing:.08em;text-align:center}
.about-txt p{font-size:clamp(.86rem,1.5vw,.96rem);color:var(--text-lt);line-height:1.82;margin-bottom:16px}
.pills{display:grid;grid-template-columns:1fr 1fr;gap:12px;margin-top:26px}
.pill{background:var(--cream);border-left:3px solid var(--gold);border-radius:0 8px 8px 0;padding:13px 14px}
.pill-t{font-size:.84rem;font-weight:700;color:var(--dark)}
.pill-d{font-size:.76rem;color:var(--text-lt);margin-top:3px;line-height:1.5}

/* ===========================
   SERVICES
=========================== */
.services{background:var(--cream)}
.svc-head{text-align:center;margin-bottom:44px}
.svc-head .sec-sub{margin:0 auto}
.svc-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:18px}
.svc-card{background:#fff;border-radius:var(--r);padding:28px 22px;border:1px solid var(--border);position:relative;overflow:hidden;transition:transform .3s,box-shadow .3s}
.svc-card::after{content:'';position:absolute;bottom:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--gold),var(--gold-lt));transform:scaleX(0);transform-origin:left;transition:transform .3s}
.svc-card:hover{transform:translateY(-5px);box-shadow:var(--shadow-md)}
.svc-card:hover::after{transform:scaleX(1)}
.svc-ico{width:52px;height:52px;border-radius:11px;background:linear-gradient(135deg,rgba(184,150,46,.12),rgba(184,150,46,.04));border:1px solid rgba(184,150,46,.2);display:flex;align-items:center;justify-content:center;font-size:1.45rem;margin-bottom:16px}
.svc-t{font-weight:700;font-size:.94rem;color:var(--dark);margin-bottom:8px}
.svc-d{font-size:.82rem;color:var(--text-lt);line-height:1.7}

/* ===========================
   WHY US
=========================== */
.why{background:linear-gradient(145deg,var(--dark) 0%,var(--dark2) 100%);position:relative;overflow:hidden}
.why-pat{position:absolute;inset:0;pointer-events:none;background-image:linear-gradient(rgba(184,150,46,.05) 1px,transparent 1px),linear-gradient(90deg,rgba(184,150,46,.05) 1px,transparent 1px);background-size:44px 44px}
.why-grid{position:relative;z-index:1;display:grid;grid-template-columns:1fr 1fr;gap:clamp(28px,5.5vw,68px);align-items:start}
.why-pts{display:flex;flex-direction:column;gap:20px;margin-top:28px}
.why-pt{display:flex;gap:15px;align-items:flex-start}
.why-num{width:38px;height:38px;min-width:38px;border-radius:50%;background:rgba(184,150,46,.1);border:1px solid rgba(184,150,46,.26);display:flex;align-items:center;justify-content:center;font-family:'Playfair Display',serif;font-size:.95rem;font-weight:700;color:var(--gold-lt)}
.wpt-t{font-weight:600;color:#fff;font-size:.9rem;margin-bottom:4px}
.wpt-d{font-size:.8rem;color:rgba(255,255,255,.46);line-height:1.65}
.why-box{background:rgba(255,255,255,.04);border:1px solid rgba(184,150,46,.14);border-radius:14px;padding:clamp(22px,3.5vw,38px)}
.wb-big{font-family:'Playfair Display',serif;font-size:4.5rem;font-weight:700;color:rgba(184,150,46,.12);line-height:1}
.wb-sub{color:var(--gold-lt);font-weight:600;font-size:.95rem;margin-top:-4px;margin-bottom:26px}
.tr{margin-bottom:20px}
.tr-top{display:flex;justify-content:space-between;margin-bottom:6px}
.tr-l{color:rgba(255,255,255,.42);font-size:.75rem;letter-spacing:.05em}
.tr-p{color:var(--gold-lt);font-weight:700;font-size:.78rem}
.tr-bar{height:4px;background:rgba(255,255,255,.07);border-radius:4px;overflow:hidden}
.tr-fill{height:100%;border-radius:4px;background:linear-gradient(90deg,var(--gold),var(--gold-lt));width:0}
.area-tags{display:flex;flex-wrap:wrap;gap:7px;margin-top:22px;padding-top:22px;border-top:1px solid rgba(184,150,46,.1)}
.a-tag{background:rgba(184,150,46,.1);border:1px solid rgba(184,150,46,.22);color:var(--gold-lt);padding:4px 12px;border-radius:30px;font-size:.74rem;font-weight:500}

/* ===========================
   PROPERTIES
=========================== */
.properties{background:#fff}
.prop-head{text-align:center;margin-bottom:44px}
.prop-head .sec-sub{margin:0 auto}
.prop-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:22px}
.prop-card{border-radius:var(--r);overflow:hidden;border:1px solid var(--border);background:#fff;box-shadow:var(--shadow-sm);transition:transform .3s,box-shadow .3s;display:flex;flex-direction:column}
.prop-card:hover{transform:translateY(-5px);box-shadow:var(--shadow-md)}
.prop-img{position:relative;width:100%;padding-top:60%;overflow:hidden;flex-shrink:0}
.prop-img svg{position:absolute;inset:0;width:100%;height:100%}
.p-badge{position:absolute;top:13px;left:13px;z-index:2;background:var(--gold);color:var(--dark);padding:4px 10px;border-radius:4px;font-size:.68rem;font-weight:700;letter-spacing:.05em;text-transform:uppercase}
.p-type{position:absolute;top:13px;right:13px;z-index:2;background:rgba(13,31,18,.88);color:#fff;padding:4px 10px;border-radius:4px;font-size:.68rem;font-weight:600}
.prop-body{padding:18px;flex:1}
.prop-price{font-family:'Playfair Display',serif;font-size:1.38rem;font-weight:700;color:var(--dark)}
.prop-price small{font-family:'Inter',sans-serif;font-size:.76rem;color:var(--text-lt);font-weight:400}
.prop-title{font-weight:600;font-size:.88rem;margin:6px 0 4px;color:var(--dark)}
.prop-loc{font-size:.78rem;color:var(--text-lt);display:flex;align-items:center;gap:4px}
.prop-feats{display:flex;gap:13px;margin-top:13px;padding-top:13px;border-top:1px solid var(--border)}
.pf{font-size:.76rem;color:var(--text-lt);display:flex;align-items:center;gap:4px}
.prop-more{text-align:center;margin-top:36px}

/* ===========================
   TESTIMONIALS
=========================== */
.testimonials{background:var(--cream)}
.test-head{text-align:center;margin-bottom:44px}
.test-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:20px}
.test-card{background:#fff;border-radius:var(--r);padding:26px;border:1px solid var(--border);box-shadow:var(--shadow-sm);display:flex;flex-direction:column;transition:box-shadow .3s}
.test-card:hover{box-shadow:var(--shadow-md)}
.stars{color:var(--gold);font-size:.82rem;letter-spacing:2px;margin-bottom:9px}
.tq{font-family:'Playfair Display',serif;font-size:3.2rem;line-height:.55;color:var(--gold);opacity:.45;margin-bottom:13px}
.t-body{font-size:.86rem;color:var(--text-lt);line-height:1.78;font-style:italic;flex:1}
.t-author{display:flex;align-items:center;gap:11px;margin-top:18px}
.t-av{width:40px;height:40px;min-width:40px;border-radius:50%;background:linear-gradient(135deg,var(--gmid),var(--dark));display:flex;align-items:center;justify-content:center;font-weight:700;font-size:.82rem;color:var(--gold-lt)}
.t-name{font-weight:700;font-size:.84rem;color:var(--dark)}
.t-meta{font-size:.73rem;color:var(--text-lt);margin-top:1px}

/* ===========================
   CONTACT
=========================== */
.contact{background:var(--dark)}
.c-head{text-align:center;margin-bottom:48px}
.c-sub{color:rgba(255,255,255,.42);max-width:440px;margin:0 auto;font-size:.88rem;line-height:1.72}
.c-grid{display:grid;grid-template-columns:1fr 1.05fr;gap:clamp(24px,5vw,56px)}
.c-items{display:flex;flex-direction:column}
.ci{display:flex;gap:13px;align-items:flex-start;padding:16px 0;border-bottom:1px solid rgba(255,255,255,.06)}
.ci:last-child{border-bottom:none}
.c-ico{width:42px;height:42px;min-width:42px;border-radius:9px;background:rgba(184,150,46,.1);border:1px solid rgba(184,150,46,.18);display:flex;align-items:center;justify-content:center;font-size:1.05rem}
.c-lbl{font-size:.7rem;color:rgba(255,255,255,.36);letter-spacing:.08em;text-transform:uppercase;margin-bottom:3px}
.c-val{font-size:.9rem;font-weight:500;color:#fff}
.c-val a{color:var(--gold-lt)}
.c-val a:hover{text-decoration:underline}
.c-form{background:rgba(255,255,255,.04);border:1px solid rgba(184,150,46,.13);border-radius:14px;padding:clamp(20px,3.5vw,34px)}
.form-title{font-family:'Playfair Display',serif;font-size:1.48rem;font-weight:700;color:#fff;margin-bottom:22px}
.fg{margin-bottom:14px}
.fl{display:block;font-size:.7rem;font-weight:600;color:rgba(255,255,255,.4);letter-spacing:.08em;text-transform:uppercase;margin-bottom:6px}
.fi{width:100%;background:rgba(255,255,255,.05);border:1px solid rgba(255,255,255,.1);border-radius:7px;padding:11px 13px;color:#fff;font-family:'Inter',sans-serif;font-size:.88rem;transition:border-color .2s;outline:none;-webkit-appearance:none;appearance:none}
.fi:focus{border-color:var(--gold-lt);background:rgba(184,150,46,.04)}
.fi::placeholder{color:rgba(255,255,255,.2)}
textarea.fi{resize:vertical;min-height:108px}
.f-btn{width:100%;background:var(--gold);color:var(--dark);border:none;border-radius:7px;padding:13px;font-family:'Inter',sans-serif;font-size:.92rem;font-weight:700;cursor:pointer;transition:all .25s;letter-spacing:.04em;margin-top:4px}
.f-btn:hover{background:var(--gold-lt);transform:translateY(-2px)}
.f-ok{display:none;margin-top:12px;padding:12px;background:rgba(40,160,70,.1);border:1px solid rgba(40,160,70,.26);border-radius:7px;color:#6ddc8b;font-size:.86rem;text-align:center}

/* ===========================
   MAP — FULL WIDTH BELOW CONTACT
=========================== */
.map-wrap{width:100%}
.map-wrap iframe{width:100%;height:360px;border:none;display:block;filter:grayscale(15%)}

/* ===========================
   FOOTER
=========================== */
footer{background:#060f09;padding:clamp(44px,6vw,68px) 0 0;color:rgba(255,255,255,.42)}
.f-grid{display:grid;grid-template-columns:1.8fr 1fr 1fr 1fr;gap:clamp(20px,3.5vw,44px);padding-bottom:44px;border-bottom:1px solid rgba(255,255,255,.06)}
.f-brand{font-family:'Playfair Display',serif;font-size:1.52rem;font-weight:700;color:var(--gold-lt)}
.f-tag{font-size:.8rem;line-height:1.68;margin-top:9px;max-width:210px}
.f-soc{display:flex;gap:9px;margin-top:16px}
.f-s{width:34px;height:34px;border-radius:50%;background:rgba(184,150,46,.08);border:1px solid rgba(184,150,46,.18);display:flex;align-items:center;justify-content:center;font-size:.88rem;transition:background .2s}
.f-s:hover{background:rgba(184,150,46,.2)}
.f-col-t{font-size:.74rem;font-weight:700;text-transform:uppercase;letter-spacing:.1em;color:#fff;margin-bottom:14px}
.f-links{display:flex;flex-direction:column;gap:8px}
.f-links a{font-size:.8rem;color:rgba(255,255,255,.4);transition:color .2s}
.f-links a:hover{color:var(--gold-lt)}
.f-links li{font-size:.8rem}
.f-bot{padding:18px var(--px);display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:8px}
.f-copy{font-size:.75rem}
.f-made{font-size:.75rem}
.f-made span{color:var(--gold-lt)}

@keyframes fadeUp{from{opacity:0;transform:translateY(24px)}to{opacity:1;transform:translateY(0)}}

/* ===========================
   TABLET ≤ 960px
=========================== */
@media(max-width:960px){
  .nb-desk{display:none}
  .hbg{display:flex}
  .nb-mob{display:flex}

  .hero-grid{grid-template-columns:1fr;text-align:center}
  .hero-pill{margin-left:auto;margin-right:auto}
  .hero-btns{justify-content:center}
  .hero-stats{justify-content:center}
  .hero-vis{display:none}

  .about-grid{grid-template-columns:1fr}
  .about-card-wrap{max-width:320px;margin:0 auto}
  .about-card{aspect-ratio:1/1}
  .exp-bdg{top:-10px;right:-10px;width:76px;height:76px}
  .exp-n{font-size:1.55rem}
  .pills{grid-template-columns:1fr}

  .svc-grid{grid-template-columns:repeat(2,1fr)}

  .why-grid{grid-template-columns:1fr}

  .prop-grid{grid-template-columns:repeat(2,1fr)}

  .test-grid{grid-template-columns:repeat(2,1fr)}

  .c-grid{grid-template-columns:1fr}

  .f-grid{grid-template-columns:1fr 1fr}

  .map-wrap iframe{height:300px}
}

/* ===========================
   MOBILE ≤ 600px
=========================== */
@media(max-width:600px){
  :root{--px:15px}

  .svc-grid{grid-template-columns:1fr}
  .prop-grid{grid-template-columns:1fr}
  .test-grid{grid-template-columns:1fr}
  .f-grid{grid-template-columns:1fr}

  .hero-btns{flex-direction:column;align-items:center}
  .btn-gold,.btn-out{width:100%;max-width:290px;justify-content:center}

  .about-card-wrap{max-width:100%}
  .exp-bdg{display:none}

  .hero-stats{gap:16px}

  .f-bot{flex-direction:column;text-align:center}

  .map-wrap iframe{height:260px}
}

/* ===========================
   SMALL MOBILE ≤ 380px
=========================== */
@media(max-width:380px){
  .hero-h1{font-size:1.6rem}
  .sec-title{font-size:1.5rem}
}
</style>
</head>
<body>

<!-- ── NAVBAR ── -->
<nav class="nb" id="nb">
  <div class="nb-inner">
    <a class="nb-logo" href="#home"><span>SK</span> Enterprises</a>
    <ul class="nb-desk">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#why">Why Us</a></li>
      <li><a href="#properties">Properties</a></li>
      <li><a href="#testimonials">Reviews</a></li>
      <li><a href="#contact" class="nbtn">Contact Us</a></li>
    </ul>
    <button class="hbg" id="hbg" onclick="toggleNav()" aria-label="Toggle menu">
      <span></span><span></span><span></span>
    </button>
  </div>
  <div class="nb-mob" id="nbMob">
    <a href="#about"        onclick="closeNav()">About Us</a>
    <a href="#services"     onclick="closeNav()">Services</a>
    <a href="#why"          onclick="closeNav()">Why Choose Us</a>
    <a href="#properties"   onclick="closeNav()">Properties</a>
    <a href="#testimonials" onclick="closeNav()">Reviews</a>
    <a href="#contact"      onclick="closeNav()" class="mb-cta">📞 Contact Now</a>
  </div>
</nav>


<!-- ── HERO ── -->
<section class="hero" id="home">
  <div class="hero-dots"></div>
  <div class="hero-b1"></div>
  <div class="hero-b2"></div>
  <div class="hero-grid">
    <div>
      <div class="hero-pill">Trusted Real Estate Broker · Dombivli, Maharashtra</div>
      <h1 class="hero-h1">Your <em>Dream Home</em><br>Starts Here</h1>
      <p class="hero-sub">Helping you find your new home, delivering the best service — with 25+ years of deep local knowledge and hundreds of happy families settled across Dombivli.</p>
      <div class="hero-btns">
        <a href="#contact" class="btn-gold">🏠 Find Your Home</a>
        <a href="#services" class="btn-out">Our Services →</a>
      </div>
      <div class="hero-stats">
        <div><div class="hsn">25+</div><div class="hsl">Years Experience</div></div>
        <div><div class="hsn">500+</div><div class="hsl">Happy Families</div></div>
        <div><div class="hsn">100%</div><div class="hsl">Transparent Deals</div></div>
      </div>
    </div>
    <div class="hero-vis">
      <div class="hv-main">
        <svg viewBox="0 0 480 360" xmlns="http://www.w3.org/2000/svg" style="width:100%;height:100%;display:block;">
          <defs>
            <linearGradient id="sky" x1="0" y1="0" x2="0" y2="1"><stop offset="0%" stop-color="#0a1a0d"/><stop offset="100%" stop-color="#183520"/></linearGradient>
            <linearGradient id="gl" x1="0" y1="0" x2="1" y2="0"><stop offset="0%" stop-color="#B8962E"/><stop offset="100%" stop-color="#D4AF4A"/></linearGradient>
          </defs>
          <rect width="480" height="360" fill="url(#sky)"/>
          <circle cx="60"  cy="40"  r="1.2" fill="rgba(255,255,255,.35)"/>
          <circle cx="140" cy="22"  r="1"   fill="rgba(255,255,255,.28)"/>
          <circle cx="210" cy="50"  r="1.4" fill="rgba(255,255,255,.32)"/>
          <circle cx="310" cy="28"  r="1"   fill="rgba(255,255,255,.25)"/>
          <circle cx="400" cy="55"  r="1.2" fill="rgba(255,255,255,.3)"/>
          <circle cx="450" cy="35"  r="0.8" fill="rgba(255,255,255,.22)"/>
          <circle cx="400" cy="55"  r="28"  fill="rgba(184,150,46,.07)"/>
          <rect x="165" y="55"  width="150" height="305" fill="#1e3a25" rx="2"/>
          <rect x="165" y="55"  width="150" height="8"   fill="#27502e"/>
          <rect x="180" y="75"  width="14" height="18" rx="2" fill="rgba(184,150,46,.45)"/>
          <rect x="204" y="75"  width="14" height="18" rx="2" fill="rgba(184,150,46,.6)"/>
          <rect x="228" y="75"  width="14" height="18" rx="2" fill="rgba(184,150,46,.3)"/>
          <rect x="252" y="75"  width="14" height="18" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="276" y="75"  width="14" height="18" rx="2" fill="rgba(184,150,46,.4)"/>
          <rect x="180" y="106" width="14" height="18" rx="2" fill="rgba(184,150,46,.3)"/>
          <rect x="204" y="106" width="14" height="18" rx="2" fill="rgba(184,150,46,.55)"/>
          <rect x="228" y="106" width="14" height="18" rx="2" fill="rgba(184,150,46,.4)"/>
          <rect x="252" y="106" width="14" height="18" rx="2" fill="rgba(184,150,46,.25)"/>
          <rect x="276" y="106" width="14" height="18" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="180" y="137" width="14" height="18" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="204" y="137" width="14" height="18" rx="2" fill="rgba(184,150,46,.28)"/>
          <rect x="228" y="137" width="14" height="18" rx="2" fill="rgba(184,150,46,.6)"/>
          <rect x="252" y="137" width="14" height="18" rx="2" fill="rgba(184,150,46,.35)"/>
          <rect x="276" y="137" width="14" height="18" rx="2" fill="rgba(184,150,46,.45)"/>
          <rect x="50"  y="120" width="96"  height="240" fill="#182e1e" rx="2"/>
          <rect x="62"  y="136" width="11" height="14" rx="2" fill="rgba(184,150,46,.4)"/>
          <rect x="82"  y="136" width="11" height="14" rx="2" fill="rgba(184,150,46,.6)"/>
          <rect x="102" y="136" width="11" height="14" rx="2" fill="rgba(184,150,46,.28)"/>
          <rect x="122" y="136" width="11" height="14" rx="2" fill="rgba(184,150,46,.48)"/>
          <rect x="62"  y="162" width="11" height="14" rx="2" fill="rgba(184,150,46,.35)"/>
          <rect x="82"  y="162" width="11" height="14" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="102" y="162" width="11" height="14" rx="2" fill="rgba(184,150,46,.22)"/>
          <rect x="122" y="162" width="11" height="14" rx="2" fill="rgba(184,150,46,.44)"/>
          <rect x="334" y="95"  width="106" height="265" fill="#152a1a" rx="2"/>
          <rect x="346" y="112" width="11" height="14" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="366" y="112" width="11" height="14" rx="2" fill="rgba(184,150,46,.3)"/>
          <rect x="386" y="112" width="11" height="14" rx="2" fill="rgba(184,150,46,.55)"/>
          <rect x="406" y="112" width="11" height="14" rx="2" fill="rgba(184,150,46,.22)"/>
          <rect x="426" y="112" width="11" height="14" rx="2" fill="rgba(184,150,46,.42)"/>
          <rect x="346" y="138" width="11" height="14" rx="2" fill="rgba(184,150,46,.28)"/>
          <rect x="366" y="138" width="11" height="14" rx="2" fill="rgba(184,150,46,.5)"/>
          <rect x="386" y="138" width="11" height="14" rx="2" fill="rgba(184,150,46,.38)"/>
          <rect x="406" y="138" width="11" height="14" rx="2" fill="rgba(184,150,46,.6)"/>
          <rect x="426" y="138" width="11" height="14" rx="2" fill="rgba(184,150,46,.3)"/>
          <rect x="0" y="310" width="480" height="50" fill="rgba(0,0,0,.45)"/>
          <rect x="0" y="308" width="480" height="2"  fill="url(#gl)" opacity=".5"/>
          <circle cx="22"  cy="310" r="17" fill="#12241a"/>
          <circle cx="460" cy="310" r="15" fill="#12241a"/>
        </svg>
      </div>
      <div class="hv-row">
        <div class="hv-mini"><div class="vm-ico">🔑</div><div class="vm-lbl">Deals Closed</div><div class="vm-val">500+</div><div class="vm-sub">Over 25 Years</div></div>
        <div class="hv-mini"><div class="vm-ico">⭐</div><div class="vm-lbl">Client Rating</div><div class="vm-val">4.9 / 5</div><div class="vm-sub">Verified Reviews</div></div>
      </div>
    </div>
  </div>
</section>


<!-- ── ABOUT ── -->
<section class="section about" id="about">
  <div class="wrap">
    <div class="about-grid">
      <div class="about-card-wrap reveal">
        <div class="about-card">
          <div class="about-card-body">
            <svg viewBox="0 0 300 400" width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
              <defs><linearGradient id="abg" x1="0" y1="0" x2=".5" y2="1"><stop offset="0%" stop-color="#1e3a24"/><stop offset="100%" stop-color="#0d1f12"/></linearGradient></defs>
              <rect width="300" height="400" fill="url(#abg)"/>
              <circle cx="150" cy="145" r="70" fill="rgba(184,150,46,.07)" stroke="rgba(184,150,46,.16)" stroke-width="1"/>
              <circle cx="150" cy="145" r="48" fill="rgba(184,150,46,.05)"/>
              <circle cx="150" cy="118" r="34" fill="rgba(184,150,46,.15)"/>
              <path d="M75 260 Q150 195 225 260" fill="rgba(184,150,46,.08)" stroke="rgba(184,150,46,.18)" stroke-width="1"/>
              <rect x="30"  y="300" width="50"  height="100" fill="rgba(184,150,46,.05)"/>
              <rect x="90"  y="275" width="40"  height="125" fill="rgba(184,150,46,.07)"/>
              <rect x="170" y="285" width="45"  height="115" fill="rgba(184,150,46,.06)"/>
              <rect x="225" y="305" width="45"  height="95"  fill="rgba(184,150,46,.04)"/>
              <text x="150" y="162" text-anchor="middle" font-family="Playfair Display,serif" font-size="40" fill="rgba(184,150,46,.32)" font-weight="700">SK</text>
            </svg>
          </div>
          <div class="about-overlay">
            <div class="about-nm">Sunil Katekar</div>
            <div class="about-rl">Founder &amp; Principal Broker — S K Enterprises</div>
          </div>
        </div>
        <div class="exp-bdg">
          <div class="exp-n">25+</div>
          <div class="exp-l">Years<br>Expert</div>
        </div>
      </div>
      <div class="reveal">
        <span class="sec-tag">About Us</span>
        <h2 class="sec-title">Meet <em>Sunil Katekar</em>,<br>Your Trusted Partner</h2>
        <div class="sec-line"></div>
        <div class="about-txt">
          <p>With over <strong>25 years of dedicated experience</strong> in real estate brokerage, Sunil Katekar has been the go-to name in Dombivli for families, investors, and first-time buyers alike. S K Enterprises was built on a simple foundation: honesty, transparency, and genuine care for every client.</p>
          <p>Whether you're buying your first home, searching for a rental, or selling a property — Sunil brings deep local market knowledge and a client-first approach that removes stress and delivers real results. No pressure tactics. No hidden fees. Just trusted guidance every step of the way.</p>
        </div>
        <div class="pills">
          <div class="pill"><div class="pill-t">🤝 Trust First</div><div class="pill-d">Full transparency in every deal, every document, every step.</div></div>
          <div class="pill"><div class="pill-t">📍 Local Expert</div><div class="pill-d">Deep knowledge of Dombivli's localities &amp; market rates.</div></div>
          <div class="pill"><div class="pill-t">💡 Smart Guidance</div><div class="pill-d">Advice that saves you time, money, and stress.</div></div>
          <div class="pill"><div class="pill-t">🎯 Results Driven</div><div class="pill-d">Committed to closing the right deal at the right price.</div></div>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- ── SERVICES ── -->
<section class="section services" id="services">
  <div class="wrap">
    <div class="svc-head reveal">
      <span class="sec-tag">What We Offer</span>
      <h2 class="sec-title">Our <em>Core Services</em></h2>
      <div class="sec-line c"></div>
      <p class="sec-sub">From finding your dream flat to negotiating the best deal — we handle it all with expertise and personal attention.</p>
    </div>
    <div class="svc-grid">
      <div class="svc-card reveal"><div class="svc-ico">🏠</div><div class="svc-t">Property Buying Assistance</div><div class="svc-d">We guide you through the entire buying process — shortlisting, legal verification, negotiation, and registration. No surprises, ever.</div></div>
      <div class="svc-card reveal"><div class="svc-ico">🏢</div><div class="svc-t">Rental Services</div><div class="svc-d">Looking for a room, flat, or apartment on rent? We connect you with verified landlords and quality listings across Dombivli.</div></div>
      <div class="svc-card reveal"><div class="svc-ico">💰</div><div class="svc-t">Property Selling Support</div><div class="svc-d">Sell your property at the right price. We market it effectively, find serious buyers, and handle all negotiations for you.</div></div>
      <div class="svc-card reveal"><div class="svc-ico">📋</div><div class="svc-t">Expert Consultation</div><div class="svc-d">Not sure where to start? Book a free consultation and get honest, practical advice on pricing, market trends, and investment potential.</div></div>
    </div>
  </div>
</section>


<!-- ── WHY US ── -->
<section class="section why" id="why">
  <div class="why-pat"></div>
  <div class="wrap">
    <div class="why-grid">
      <div>
        <span class="sec-tag">Why Choose Us</span>
        <h2 class="sec-title light">The <em>S K Enterprises</em><br>Difference</h2>
        <div class="sec-line" style="background:linear-gradient(90deg,var(--gold),transparent)"></div>
        <div class="why-pts">
          <div class="why-pt reveal"><div class="why-num">01</div><div><div class="wpt-t">25+ Years of Local Expertise</div><div class="wpt-d">Sunil has worked in the Dombivli market for over two decades — knowing every locality, builder, and price trend. This saves you from costly mistakes.</div></div></div>
          <div class="why-pt reveal"><div class="why-num">02</div><div><div class="wpt-t">Trusted by Hundreds of Families</div><div class="wpt-d">Our reputation is built entirely on client referrals. When your neighbours recommend us, you know you're in the right hands.</div></div></div>
          <div class="why-pt reveal"><div class="why-num">03</div><div><div class="wpt-t">100% Transparent Deals</div><div class="wpt-d">No hidden charges. No last-minute surprises. Every deal is clearly explained before you sign anything.</div></div></div>
          <div class="why-pt reveal"><div class="why-num">04</div><div><div class="wpt-t">End-to-End Support</div><div class="wpt-d">From the first site visit to the final key handover — we are with you at every step. One contact, zero confusion.</div></div></div>
        </div>
      </div>
      <div class="why-box reveal">
        <div class="wb-big">25</div>
        <div class="wb-sub">Years of Excellence</div>
        <div class="tr"><div class="tr-top"><span class="tr-l">Client Satisfaction</span><span class="tr-p">98%</span></div><div class="tr-bar"><div class="tr-fill" data-w="98"></div></div></div>
        <div class="tr"><div class="tr-top"><span class="tr-l">Deal Success Rate</span><span class="tr-p">95%</span></div><div class="tr-bar"><div class="tr-fill" data-w="95"></div></div></div>
        <div class="tr"><div class="tr-top"><span class="tr-l">On-Time Closings</span><span class="tr-p">92%</span></div><div class="tr-bar"><div class="tr-fill" data-w="92"></div></div></div>
        <div class="tr"><div class="tr-top"><span class="tr-l">Repeat &amp; Referral Clients</span><span class="tr-p">87%</span></div><div class="tr-bar"><div class="tr-fill" data-w="87"></div></div></div>
        <div class="area-tags">
          <span class="a-tag">Dombivli East</span><span class="a-tag">Dombivli West</span>
          <span class="a-tag">Kalyan</span><span class="a-tag">Ulhasnagar</span>
          <span class="a-tag">Thane</span><span class="a-tag">Ambernath</span>
        </div>
      </div>
    </div>
  </div>
</section>


<!-- ── PROPERTIES ── -->
<section class="section properties" id="properties">
  <div class="wrap">
    <div class="prop-head reveal">
      <span class="sec-tag">Featured Listings</span>
      <h2 class="sec-title">Sample <em>Property Listings</em></h2>
      <div class="sec-line c"></div>
      <p class="sec-sub">Here are examples of the properties we actively handle. Contact us for current live listings tailored to your needs and budget.</p>
    </div>
    <div class="prop-grid">

      <!-- Card 1 -->
      <div class="prop-card reveal">
        <div class="prop-img">
          <svg viewBox="0 0 400 240" xmlns="http://www.w3.org/2000/svg">
            <rect width="400" height="240" fill="#1a3020"/>
            <polygon points="200,38 95,128 305,128" fill="#223a28"/>
            <rect x="105" y="128" width="190" height="112" fill="#1e3525"/>
            <rect x="122" y="148" width="38" height="32" rx="3" fill="rgba(184,150,46,.45)"/>
            <rect x="181" y="148" width="38" height="32" rx="3" fill="rgba(184,150,46,.35)"/>
            <rect x="240" y="148" width="38" height="32" rx="3" fill="rgba(184,150,46,.55)"/>
            <rect x="172" y="196" width="56" height="44" rx="3" fill="#162a1e"/>
            <circle cx="220" cy="219" r="3" fill="rgba(184,150,46,.6)"/>
            <rect x="60"  y="218" width="28" height="10" fill="#122018" rx="5"/>
            <rect x="312" y="218" width="26" height="10" fill="#122018" rx="5"/>
            <rect width="400" height="240" fill="url(#pg1)"/>
            <defs><linearGradient id="pg1" x1="0" y1="1" x2="0" y2="0"><stop offset="0%" stop-color="rgba(13,31,18,.5)"/><stop offset="60%" stop-color="transparent"/></linearGradient></defs>
          </svg>
          <div class="p-badge">🏠 For Sale</div>
          <div class="p-type">2 BHK Flat</div>
        </div>
        <div class="prop-body">
          <div class="prop-price">₹45 Lakh <small>onwards</small></div>
          <div class="prop-title">Spacious 2 BHK in Dombivli East</div>
          <div class="prop-loc">📍 Near Dombivli Railway Station</div>
          <div class="prop-feats">
            <div class="pf">🛏 2 Beds</div>
            <div class="pf">🚿 2 Baths</div>
            <div class="pf">📐 950 sq ft</div>
          </div>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="prop-card reveal">
        <div class="prop-img">
          <svg viewBox="0 0 400 240" xmlns="http://www.w3.org/2000/svg">
            <rect width="400" height="240" fill="#0e1e2e"/>
            <rect x="88" y="28" width="224" height="212" fill="#132234" rx="3"/>
            <rect x="88" y="28" width="224" height="6" fill="#1a3048"/>
            <rect x="88" y="90"  width="224" height="2" fill="rgba(255,255,255,.04)"/>
            <rect x="88" y="152" width="224" height="2" fill="rgba(255,255,255,.04)"/>
            <rect x="104" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.55)"/>
            <rect x="134" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.3)"/>
            <rect x="164" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.5)"/>
            <rect x="194" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.25)"/>
            <rect x="224" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.48)"/>
            <rect x="254" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.35)"/>
            <rect x="284" y="42" width="18" height="22" rx="2" fill="rgba(184,150,46,.42)"/>
            <rect x="104" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.32)"/>
            <rect x="134" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.56)"/>
            <rect x="164" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.22)"/>
            <rect x="194" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.48)"/>
            <rect x="224" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.36)"/>
            <rect x="254" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.52)"/>
            <rect x="284" y="100" width="18" height="22" rx="2" fill="rgba(184,150,46,.28)"/>
            <rect x="104" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.5)"/>
            <rect x="134" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.24)"/>
            <rect x="164" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.58)"/>
            <rect x="194" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.3)"/>
            <rect x="224" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.44)"/>
            <rect x="254" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.2)"/>
            <rect x="284" y="160" width="18" height="22" rx="2" fill="rgba(184,150,46,.5)"/>
            <rect x="174" y="202" width="52" height="38" rx="3" fill="#0a1828"/>
            <rect width="400" height="240" fill="url(#pg2)"/>
            <defs><linearGradient id="pg2" x1="0" y1="1" x2="0" y2="0"><stop offset="0%" stop-color="rgba(8,18,28,.5)"/><stop offset="60%" stop-color="transparent"/></linearGradient></defs>
          </svg>
          <div class="p-badge">🏢 For Rent</div>
          <div class="p-type">1 BHK Flat</div>
        </div>
        <div class="prop-body">
          <div class="prop-price">₹8,000 <small>/month</small></div>
          <div class="prop-title">1 BHK Rental – Manpada Area</div>
          <div class="prop-loc">📍 Manpada, Dombivli West</div>
          <div class="prop-feats">
            <div class="pf">🛏 1 Bed</div>
            <div class="pf">🚿 1 Bath</div>
            <div class="pf">📐 550 sq ft</div>
          </div>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="prop-card reveal">
        <div class="prop-img">
          <svg viewBox="0 0 400 240" xmlns="http://www.w3.org/2000/svg">
            <rect width="400" height="240" fill="#141e0a"/>
            <rect x="68" y="18" width="264" height="222" fill="#1a2c0c" rx="3"/>
            <rect x="68" y="78"  width="264" height="3" fill="rgba(184,150,46,.1)"/>
            <rect x="68" y="148" width="264" height="3" fill="rgba(184,150,46,.1)"/>
            <rect x="84"  y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.48)"/>
            <rect x="116" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.28)"/>
            <rect x="148" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.6)"/>
            <rect x="180" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.35)"/>
            <rect x="212" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.5)"/>
            <rect x="244" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.22)"/>
            <rect x="276" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.44)"/>
            <rect x="308" y="28" width="20" height="26" rx="2" fill="rgba(184,150,46,.36)"/>
            <rect x="84"  y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.32)"/>
            <rect x="116" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.55)"/>
            <rect x="148" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.24)"/>
            <rect x="180" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.5)"/>
            <rect x="212" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.38)"/>
            <rect x="244" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.6)"/>
            <rect x="276" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.28)"/>
            <rect x="308" y="90" width="20" height="26" rx="2" fill="rgba(184,150,46,.48)"/>
            <rect x="84"  y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.52)"/>
            <rect x="116" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.3)"/>
            <rect x="148" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.45)"/>
            <rect x="180" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.22)"/>
            <rect x="212" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.58)"/>
            <rect x="244" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.34)"/>
            <rect x="276" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.48)"/>
            <rect x="308" y="158" width="20" height="26" rx="2" fill="rgba(184,150,46,.26)"/>
            <rect x="163" y="204" width="74" height="36" rx="3" fill="#0e160a"/>
            <rect width="400" height="240" fill="url(#pg3)"/>
            <defs><linearGradient id="pg3" x1="0" y1="1" x2="0" y2="0"><stop offset="0%" stop-color="rgba(10,16,5,.5)"/><stop offset="60%" stop-color="transparent"/></linearGradient></defs>
          </svg>
          <div class="p-badge">🏠 For Sale</div>
          <div class="p-type">3 BHK Flat</div>
        </div>
        <div class="prop-body">
          <div class="prop-price">₹72 Lakh <small>onwards</small></div>
          <div class="prop-title">Premium 3 BHK with Amenities</div>
          <div class="prop-loc">📍 Tilak Nagar, Dombivli East</div>
          <div class="prop-feats">
            <div class="pf">🛏 3 Beds</div>
            <div class="pf">🚿 2 Baths</div>
            <div class="pf">📐 1300 sq ft</div>
          </div>
        </div>
      </div>

    </div>
    <div class="prop-more reveal">
      <p style="color:var(--text-lt);margin-bottom:16px;font-size:.86rem;">These are sample listings. Contact us for current live properties matching your needs.</p>
      <a href="#contact" class="btn-gold">📞 Get Latest Listings</a>
    </div>
  </div>
</section>


<!-- ── TESTIMONIALS ── -->
<section class="section testimonials" id="testimonials">
  <div class="wrap">
    <div class="test-head reveal">
      <span class="sec-tag">Client Reviews</span>
      <h2 class="sec-title">What Our <em>Clients Say</em></h2>
      <div class="sec-line c"></div>
    </div>
    <div class="test-grid">
      <div class="test-card reveal">
        <div class="stars">★★★★★</div>
        <div class="tq">"</div>
        <p class="t-body">Sunilji helped us find our perfect 2 BHK in Dombivli East within our budget. He was patient, honest, and never pressured us. After visiting a few homes, he guided us to exactly what we needed. We are so grateful!</p>
        <div class="t-author"><div class="t-av">RK</div><div><div class="t-name">Ramesh &amp; Kavita Sharma</div><div class="t-meta">Home Buyers · Dombivli East</div></div></div>
      </div>
      <div class="test-card reveal">
        <div class="stars">★★★★★</div>
        <div class="tq">"</div>
        <p class="t-body">I had been trying to sell my flat for 8 months with no luck. A friend referred me to Sunil Katekar. Within 6 weeks, the deal was done at a great price. His local network and negotiation skills are truly impressive.</p>
        <div class="t-author"><div class="t-av">AP</div><div><div class="t-name">Amit Patil</div><div class="t-meta">Property Seller · Dombivli West</div></div></div>
      </div>
      <div class="test-card reveal">
        <div class="stars">★★★★★</div>
        <div class="tq">"</div>
        <p class="t-body">As a working professional new to Dombivli, finding a good rental felt stressful. S K Enterprises made it completely simple — they showed me 3 flats in one day and the second one was perfect. Clean process, no games.</p>
        <div class="t-author"><div class="t-av">PM</div><div><div class="t-name">Priya Mehta</div><div class="t-meta">Tenant · Manpada, Dombivli</div></div></div>
      </div>
    </div>
  </div>
</section>


<!-- ── CONTACT ── -->
<section class="section contact" id="contact">
  <div class="wrap">
    <div class="c-head reveal">
      <span class="sec-tag">Get In Touch</span>
      <h2 class="sec-title light">Let's Find Your <em>Perfect Property</em></h2>
      <div class="sec-line c" style="background:linear-gradient(90deg,var(--gold),transparent)"></div>
      <p class="c-sub">Ready to buy, sell, or rent? Drop us a message and Sunil will personally get back to you within 24 hours.</p>
    </div>
    <div class="c-grid">
      <div class="c-items reveal">
        <div class="ci"><div class="c-ico">📞</div><div><div class="c-lbl">Phone / WhatsApp</div><div class="c-val"><a href="tel:+918108399088">+91 81083 99088</a></div></div></div>
        <div class="ci"><div class="c-ico">✉️</div><div><div class="c-lbl">Email Address</div><div class="c-val"><a href="mailto:lakshoganiya10@gmail.com" style="word-break:break-all;">lakshoganiya10@gmail.com</a></div></div></div>
        <div class="ci"><div class="c-ico">📍</div><div><div class="c-lbl">Office Location</div><div class="c-val">Dombivli, Maharashtra, India</div></div></div>
        <div class="ci"><div class="c-ico">🕒</div><div><div class="c-lbl">Working Hours</div><div class="c-val">Monday – Saturday: 9 AM – 7 PM</div></div></div>
        <div style="margin-top:24px;">
          <a href="https://wa.me/918108399088" target="_blank" class="btn-gold">💬 Chat on WhatsApp</a>
        </div>
      </div>
      <div class="c-form reveal">
        <div class="form-title">Send a Message</div>
        <div class="fg"><label class="fl">Your Name</label><input type="text" class="fi" placeholder="Enter your full name" id="cN"></div>
        <div class="fg"><label class="fl">Phone Number</label><input type="tel" class="fi" placeholder="+91 XXXXX XXXXX" id="cP"></div>
        <div class="fg">
          <label class="fl">I'm Interested In</label>
          <select class="fi" id="cI"><option value="">Select a service...</option><option>Buying a Property</option><option>Renting a Property</option><option>Selling My Property</option><option>General Consultation</option></select>
        </div>
        <div class="fg"><label class="fl">Your Message</label><textarea class="fi" placeholder="Tell us your budget, preferred location, property type..." id="cM"></textarea></div>
        <button class="f-btn" onclick="doSubmit()">Send Message →</button>
        <div class="f-ok" id="fOk">✅ Message sent! Sunil will contact you soon.</div>
      </div>
    </div>
  </div>
</section>


<!-- ── MAP — FULL WIDTH STRIP ── -->
<div class="map-wrap">
  <iframe
    src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d60320.0!2d73.0791634!3d19.2166681!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3be7954f18e9cbcd%3A0x8a65c85ee7cce5b0!2sDombivli%2C%20Maharashtra!5e0!3m2!1sen!2sin!4v1700000000000!5m2!1sen!2sin"
    allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"
    title="S K Enterprises – Dombivli, Maharashtra">
  </iframe>
</div>


<!-- ── FOOTER ── -->
<footer>
  <div class="wrap">
    <div class="f-grid">
      <div>
        <div class="f-brand">S K Enterprises</div>
        <div class="f-tag">Helping you find your new home, delivering the best service. Your trusted real estate partner in Dombivli since 1999.</div>
        <div class="f-soc">
          <a class="f-s" href="tel:+918108399088" title="Call">📞</a>
          <a class="f-s" href="mailto:lakshoganiya10@gmail.com" title="Email">✉️</a>
          <a class="f-s" href="https://wa.me/918108399088" target="_blank" title="WhatsApp">💬</a>
        </div>
      </div>
      <div>
        <div class="f-col-t">Quick Links</div>
        <ul class="f-links">
          <li><a href="#home">Home</a></li>
          <li><a href="#about">About Us</a></li>
          <li><a href="#services">Services</a></li>
          <li><a href="#why">Why Choose Us</a></li>
          <li><a href="#properties">Properties</a></li>
        </ul>
      </div>
      <div>
        <div class="f-col-t">Services</div>
        <ul class="f-links">
          <li><a href="#services">Buy Property</a></li>
          <li><a href="#services">Rent a Flat</a></li>
          <li><a href="#services">Sell Property</a></li>
          <li><a href="#services">Consultation</a></li>
          <li><a href="#testimonials">Client Reviews</a></li>
        </ul>
      </div>
      <div>
        <div class="f-col-t">Contact</div>
        <ul class="f-links">
          <li><a href="tel:+918108399088">+91 81083 99088</a></li>
          <li><a href="mailto:lakshoganiya10@gmail.com" style="word-break:break-all;">lakshoganiya10@gmail.com</a></li>
          <li>Dombivli, Maharashtra</li>
          <li>Mon–Sat: 9 AM – 7 PM</li>
        </ul>
      </div>
    </div>
  </div>
  <div class="f-bot">
    <div class="f-copy">© 2024 S K Enterprises. All rights reserved.</div>
    <div class="f-made">Made with <span>♥</span> for happy homeowners</div>
  </div>
</footer>


<script>
/* Nav */
function toggleNav(){
  const m=document.getElementById('nbMob'),h=document.getElementById('hbg');
  const o=m.classList.toggle('open');
  h.classList.toggle('open',o);
}
function closeNav(){
  document.getElementById('nbMob').classList.remove('open');
  document.getElementById('hbg').classList.remove('open');
}
document.addEventListener('click',function(e){
  if(!document.querySelector('.nb').contains(e.target)) closeNav();
});
window.addEventListener('scroll',function(){
  document.getElementById('nb').style.background=
    window.scrollY>60?'rgba(13,31,18,.99)':'rgba(13,31,18,.96)';
},{passive:true});

/* Scroll reveal */
const revs=document.querySelectorAll('.reveal');
const ro=new IntersectionObserver((entries)=>{
  entries.forEach((e,i)=>{
    if(e.isIntersecting){
      setTimeout(()=>{e.target.classList.add('on');ro.unobserve(e.target);},i*65);
    }
  });
},{threshold:.09,rootMargin:'0px 0px -36px 0px'});
revs.forEach(el=>ro.observe(el));

/* Trust bars */
const fills=document.querySelectorAll('.tr-fill');
const bo=new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      const w=e.target.getAttribute('data-w');
      e.target.style.transition='width 1.15s ease .18s';
      e.target.style.width=w+'%';
      bo.unobserve(e.target);
    }
  });
},{threshold:.4});
fills.forEach(b=>bo.observe(b));

/* Form */
function doSubmit(){
  const n=document.getElementById('cN').value.trim();
  const p=document.getElementById('cP').value.trim();
  if(!n||!p){alert('Please fill in your name and phone number.');return;}
  const ok=document.getElementById('fOk');
  ok.style.display='block';
  document.getElementById('cN').value='';
  document.getElementById('cP').value='';
  document.getElementById('cI').value='';
  document.getElementById('cM').value='';
  setTimeout(()=>{ok.style.display='none';},5000);
}
</script>
</body>
</html>
