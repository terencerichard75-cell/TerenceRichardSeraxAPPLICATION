<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Terence Richard - Serax France</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">
<style>
:root{--cream:#F5F0E8;--cream-dark:#EDE7D9;--ink:#1A1714;--sand:#C9B99A;--sand-light:#DDD0BA;--terra:#8B6B4A;--white:#FDFAF5;}
*{margin:0;padding:0;box-sizing:border-box;}html{scroll-behavior:smooth;}
body{background:var(--cream);color:var(--ink);font-family:'Jost',Georgia,sans-serif;font-weight:300;overflow-x:hidden;}
nav{position:fixed;top:0;left:0;right:0;z-index:100;padding:0 48px;height:64px;display:flex;align-items:center;justify-content:space-between;background:rgba(245,240,232,0.95);backdrop-filter:blur(12px);border-bottom:1px solid rgba(201,185,154,0.3);transition:border-color 0.4s,top 0.3s;}
nav.scrolled{border-bottom-color:rgba(201,185,154,0.6);}
.nav-logo{font-family:'Cormorant Garamond',Georgia,serif;font-size:15px;font-weight:400;letter-spacing:0.15em;text-transform:uppercase;color:var(--ink);text-decoration:none;}
.nav-links{display:flex;gap:36px;list-style:none;}
.nav-links a{font-size:10px;font-weight:400;letter-spacing:0.18em;text-transform:uppercase;color:var(--ink);text-decoration:none;opacity:0.5;transition:opacity 0.3s;padding-bottom:3px;}
.nav-links a:hover{opacity:1;}.nav-links a.active{opacity:1;border-bottom:1px solid var(--sand);}
.hamburger{display:none;flex-direction:column;justify-content:center;gap:5px;width:36px;height:36px;background:none;border:none;cursor:pointer;padding:4px;z-index:200;}
.hamburger span{display:block;width:22px;height:1.5px;background:var(--ink);transition:transform 0.3s,opacity 0.3s;transform-origin:center;}
.hamburger.open span:nth-child(1){transform:translateY(6.5px) rotate(45deg);}
.hamburger.open span:nth-child(2){opacity:0;}
.hamburger.open span:nth-child(3){transform:translateY(-6.5px) rotate(-45deg);}
.mobile-menu{display:none;position:fixed;top:64px;left:0;right:0;bottom:0;background:rgba(245,240,232,0.98);backdrop-filter:blur(16px);z-index:99;flex-direction:column;align-items:center;justify-content:center;gap:4px;}
.mobile-menu.open{display:flex;}
.mobile-menu a{font-size:11px;font-weight:400;letter-spacing:0.26em;text-transform:uppercase;color:var(--ink);text-decoration:none;padding:18px 40px;opacity:0.6;transition:opacity 0.25s;border-bottom:1px solid rgba(201,185,154,0.2);width:260px;text-align:center;}
.mobile-menu a:last-child{border-bottom:none;}.mobile-menu a:hover,.mobile-menu a:active{opacity:1;}
#hero{min-height:100vh;display:flex;flex-direction:column;justify-content:center;padding:120px 48px 80px;position:relative;overflow:hidden;}
.hero-bg-letter{position:absolute;top:50%;right:-30px;transform:translateY(-50%);font-family:'Cormorant Garamond',Georgia,serif;font-size:30vw;font-weight:300;color:transparent;-webkit-text-stroke:1px rgba(201,185,154,0.15);pointer-events:none;user-select:none;line-height:1;}
.hero-eyebrow{font-size:11px;font-weight:400;letter-spacing:0.22em;text-transform:uppercase;color:var(--terra);margin-bottom:32px;opacity:0;animation:fadeUp 0.8s 0.3s ease forwards;}
.hero-title{font-family:'Cormorant Garamond',Georgia,serif;font-size:clamp(38px,5.5vw,82px);font-weight:300;line-height:1.12;max-width:820px;opacity:0;animation:fadeUp 0.9s 0.5s ease forwards;}
.hero-title em{font-style:italic;color:var(--terra);}
.hero-sub{margin-top:40px;font-size:14px;font-weight:300;letter-spacing:0.04em;line-height:1.85;max-width:480px;opacity:0;animation:fadeUp 0.8s 0.8s ease forwards;color:rgba(26,23,20,0.7);}
.hero-scroll{position:absolute;bottom:48px;left:48px;display:flex;align-items:center;gap:16px;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:var(--sand);opacity:0;animation:fadeIn 1s 1.4s ease forwards;}
.hero-scroll::before{content:'';display:block;width:40px;height:1px;background:var(--sand);}
section{padding:110px 48px;}
.s-num{font-family:'Cormorant Garamond',Georgia,serif;font-size:88px;font-weight:300;color:transparent;-webkit-text-stroke:1px rgba(201,185,154,0.35);line-height:1;margin-bottom:-16px;user-select:none;}
.s-label{font-size:10px;font-weight:400;letter-spacing:0.26em;text-transform:uppercase;color:var(--terra);margin-bottom:18px;}
.s-title{font-family:'Cormorant Garamond',Georgia,serif;font-size:clamp(30px,3.8vw,52px);font-weight:300;line-height:1.2;margin-bottom:16px;max-width:680px;}
.s-title em{font-style:italic;color:var(--terra);}
.s-divider{width:44px;height:1px;background:var(--sand);margin-bottom:48px;margin-top:8px;}
.reveal{opacity:0;transform:translateY(28px);transition:opacity 0.75s ease,transform 0.75s ease;}
.reveal.visible{opacity:1;transform:none;}
#understanding{background:var(--white);}
.cards-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:3px;margin-top:56px;}
.card{background:var(--cream);padding:44px 36px;transition:background 0.35s;}
.card:hover{background:var(--cream-dark);}
.card-n{font-family:'Cormorant Garamond',Georgia,serif;font-size:44px;font-weight:300;color:rgba(201,185,154,0.45);margin-bottom:20px;line-height:1;}
.card-h{font-family:'Cormorant Garamond',Georgia,serif;font-size:21px;font-weight:400;line-height:1.35;margin-bottom:14px;}
.card-p{font-size:13.5px;line-height:1.9;color:rgba(26,23,20,0.72);}
.card-tag{display:inline-block;margin-top:18px;font-size:9.5px;letter-spacing:0.2em;text-transform:uppercase;color:var(--terra);border-bottom:1px solid var(--sand-light);padding-bottom:2px;}
#challenges{background:var(--ink);color:var(--cream);}
#challenges .s-label{color:var(--sand);}#challenges .s-title{color:var(--cream);}
#challenges .s-num{-webkit-text-stroke-color:rgba(245,240,232,0.07);}
#challenges .s-divider{background:rgba(201,185,154,0.4);}
.ch-list{display:flex;flex-direction:column;gap:2px;margin-top:52px;}
.ch-item{display:grid;grid-template-columns:72px 1fr 280px;align-items:center;gap:24px;padding:32px 36px;background:rgba(255,255,255,0.03);border-left:1px solid rgba(201,185,154,0.12);transition:background 0.35s,border-color 0.35s;}
.ch-item:hover{background:rgba(255,255,255,0.06);border-left-color:var(--sand);}
.ch-idx{font-family:'Cormorant Garamond',Georgia,serif;font-size:26px;font-weight:300;color:rgba(201,185,154,0.35);}
.ch-text{font-family:'Cormorant Garamond',Georgia,serif;font-size:21px;font-weight:300;line-height:1.45;color:var(--cream);}
.ch-note{font-size:11.5px;letter-spacing:0.06em;color:rgba(201,185,154,0.55);line-height:1.75;text-align:right;}
.ch-verdict{margin-top:52px;padding:44px;border:1px solid rgba(201,185,154,0.2);font-family:'Cormorant Garamond',Georgia,serif;font-size:24px;font-style:italic;font-weight:300;color:var(--sand);line-height:1.65;max-width:760px;}
#objection{background:var(--cream);}
.obj-grid{display:grid;grid-template-columns:1fr 1fr;gap:72px;align-items:start;margin-top:52px;}
.obj-left{background:var(--ink);color:var(--cream);padding:52px 44px;}
.obj-lbl{font-size:10px;letter-spacing:0.24em;text-transform:uppercase;color:var(--sand);margin-bottom:22px;}
.obj-quote{font-family:'Cormorant Garamond',Georgia,serif;font-size:26px;font-style:italic;font-weight:300;line-height:1.55;color:rgba(245,240,232,0.82);}
.resp-step{display:flex;gap:22px;padding:28px 0;border-bottom:1px solid rgba(201,185,154,0.28);}
.resp-step:last-child{border-bottom:none;}
.step-dot{width:30px;height:30px;border:1px solid var(--sand);display:flex;align-items:center;justify-content:center;font-family:'Cormorant Garamond',Georgia,serif;font-size:15px;font-weight:400;color:var(--terra);flex-shrink:0;margin-top:2px;}
.step-h{font-family:'Cormorant Garamond',Georgia,serif;font-size:17px;font-weight:500;margin-bottom:9px;}
.step-p{font-size:13.5px;line-height:1.9;color:rgba(26,23,20,0.72);}
.bridge{display:flex;align-items:center;justify-content:space-around;gap:12px;margin-top:52px;padding:36px 32px;background:var(--cream-dark);}
.b-node{text-align:center;flex:1;}
.b-lbl{font-size:9.5px;letter-spacing:0.2em;text-transform:uppercase;color:var(--terra);margin-bottom:10px;}
.b-val{font-family:'Cormorant Garamond',Georgia,serif;font-size:19px;font-weight:400;line-height:1.4;}
.b-arrow{color:var(--sand);font-size:18px;flex-shrink:0;}
#preuves{background:var(--white);}
.tabs-bar{display:flex;border-bottom:1px solid rgba(201,185,154,0.38);margin-top:44px;overflow-x:auto;}
@media(max-width:680px){.tabs-bar{display:grid;grid-template-columns:1fr 1fr;overflow-x:visible;border-bottom:none;gap:3px;}.tabs-bar .tab-btn{border:1px solid rgba(201,185,154,0.38);border-bottom:2px solid transparent;margin-bottom:0;padding:12px 8px;}.tabs-bar .tab-btn.active{border-color:var(--terra);color:var(--ink);}}
.tab-btn{padding:14px 26px;font-size:10.5px;font-weight:400;letter-spacing:0.15em;text-transform:uppercase;color:rgba(26,23,20,0.42);background:none;border:none;border-bottom:2px solid transparent;cursor:pointer;transition:color 0.3s,border-color 0.3s;white-space:nowrap;font-family:'Jost',Georgia,sans-serif;margin-bottom:-1px;}
.tab-btn:hover{color:var(--ink);}.tab-btn.active{color:var(--ink);border-bottom-color:var(--terra);}
.tab-pane{display:none;padding-top:52px;}.tab-pane.active{display:block;}
.proof-grid{display:grid;grid-template-columns:1fr 1fr;gap:72px;align-items:start;}
.proof-ch-lbl{font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:var(--terra);margin-bottom:14px;}
.proof-ch-box{padding:36px 32px;background:var(--cream);border-left:3px solid var(--sand);font-family:'Cormorant Garamond',Georgia,serif;font-size:21px;font-weight:300;line-height:1.5;}
.proof-ev-lbl{font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:var(--terra);margin-bottom:18px;}
.proof-ev-p{font-size:14px;line-height:1.9;color:rgba(26,23,20,0.78);}
.kpis{display:flex;gap:28px;margin-top:28px;padding-top:28px;border-top:1px solid rgba(201,185,154,0.28);flex-wrap:wrap;}
.kpi-val{font-family:'Cormorant Garamond',Georgia,serif;font-size:38px;font-weight:300;color:var(--terra);line-height:1;margin-bottom:5px;}
.kpi-lbl{font-size:10.5px;letter-spacing:0.08em;color:rgba(26,23,20,0.48);line-height:1.45;}
#jours{background:var(--cream);}
.phases{display:grid;grid-template-columns:repeat(3,1fr);gap:3px;margin-top:52px;}
.phase{padding:44px 36px;background:var(--white);transition:background 0.35s;position:relative;overflow:hidden;}
.phase:hover{background:var(--cream-dark);}
.phase-period{font-size:10px;letter-spacing:0.22em;text-transform:uppercase;color:var(--terra);margin-bottom:10px;}
.phase-h{font-family:'Cormorant Garamond',Georgia,serif;font-size:24px;font-weight:400;line-height:1.3;margin-bottom:28px;}
.phase-items{list-style:none;display:flex;flex-direction:column;gap:13px;}
.phase-item{font-size:13px;line-height:1.75;color:rgba(26,23,20,0.72);padding-left:14px;position:relative;}
.phase-item::before{content:'\2014';position:absolute;left:0;color:var(--sand);font-size:10px;top:1px;}
.phase-accent{position:absolute;bottom:0;left:0;right:0;height:2px;background:transparent;transition:background 0.4s;}
.phase:hover .phase-accent{background:var(--sand);}
#cta{background:var(--ink);color:var(--cream);text-align:center;padding:110px 48px;}
#cta .s-label{color:var(--sand);}
#cta .s-num{-webkit-text-stroke-color:rgba(245,240,232,0.06);}
.cta-title{font-family:'Cormorant Garamond',Georgia,serif;font-size:clamp(34px,4.5vw,62px);font-weight:300;line-height:1.22;max-width:680px;margin:0 auto 28px;color:var(--cream);}
.cta-title em{font-style:italic;color:var(--sand);}
.cta-sub{font-size:14.5px;line-height:1.85;color:rgba(245,240,232,0.55);max-width:540px;margin:0 auto 52px;}
.cta-btns{display:flex;gap:18px;justify-content:center;flex-wrap:wrap;}
.btn-p{padding:15px 38px;background:var(--cream);color:var(--ink);font-size:10.5px;letter-spacing:0.2em;text-transform:uppercase;text-decoration:none;font-family:'Jost',Georgia,sans-serif;font-weight:400;transition:background 0.3s;}
.btn-p:hover{background:var(--sand-light);}
.btn-s{padding:15px 38px;border:1px solid rgba(201,185,154,0.36);color:rgba(245,240,232,0.65);font-size:10.5px;letter-spacing:0.2em;text-transform:uppercase;text-decoration:none;font-family:'Jost',Georgia,sans-serif;font-weight:400;transition:border-color 0.3s,color 0.3s;}
.btn-s:hover{border-color:var(--sand);color:var(--cream);}
footer{background:var(--ink);border-top:1px solid rgba(201,185,154,0.1);padding:28px 48px;display:flex;align-items:center;justify-content:space-between;}
.ft-name{font-family:'Cormorant Garamond',Georgia,serif;font-size:12px;letter-spacing:0.1em;color:rgba(245,240,232,0.35);}
.ft-note{font-size:10.5px;letter-spacing:0.1em;color:rgba(245,240,232,0.22);}
@keyframes fadeUp{from{opacity:0;transform:translateY(24px);}to{opacity:1;transform:translateY(0);}}
@keyframes fadeIn{from{opacity:0;}to{opacity:1;}}
@media(max-width:960px){.cards-grid{grid-template-columns:1fr 1fr;}.phases{grid-template-columns:1fr;}.ch-item{grid-template-columns:56px 1fr;}.ch-note{display:none;}.obj-grid{grid-template-columns:1fr;gap:40px;}.proof-grid{grid-template-columns:1fr;gap:36px;}.bridge{flex-direction:column;}}
@media(max-width:680px){nav{padding:0 20px;}.nav-links{display:none;}.hamburger{display:flex;}section{padding:72px 20px;}#hero{padding:96px 20px 56px;}.cards-grid{grid-template-columns:1fr;}footer{flex-direction:column;gap:10px;text-align:center;}.cta-btns{flex-direction:column;align-items:center;}}
#about { background: var(--cream); }
.about-body { max-width: 820px; }
.about-quote { font-family: 'Cormorant Garamond', Georgia, serif; font-size: 22px; font-style: italic; font-weight: 300; color: var(--terra); line-height: 1.6; margin-top: 8px; }
.about-p { font-size: 15px; line-height: 1.9; color: rgba(26,23,20,0.78); margin-bottom: 28px; }
/* EDITOR */
#edit-fab{position:fixed;bottom:28px;right:28px;z-index:9000;width:52px;height:52px;border-radius:50%;background:#1A1714;border:1.5px solid #C9B99A;color:#C9B99A;font-size:20px;cursor:pointer;display:flex;align-items:center;justify-content:center;box-shadow:0 4px 24px rgba(0,0,0,0.4);transition:transform 0.2s,background 0.2s;}
#edit-fab:hover{transform:scale(1.08);background:#2a2420;}
#edit-login{display:none;position:fixed;inset:0;z-index:9100;background:rgba(26,23,20,0.9);backdrop-filter:blur(10px);align-items:center;justify-content:center;}
#edit-login.show{display:flex;}
.elb{background:#F5F0E8;padding:52px 48px;min-width:360px;text-align:center;}
.elb h2{font-family:'Cormorant Garamond',Georgia,serif;font-size:28px;font-weight:300;margin-bottom:8px;}
.elb p.sub{font-size:11px;letter-spacing:0.16em;text-transform:uppercase;color:#8B6B4A;margin-bottom:36px;}
.elb input{width:100%;padding:13px 16px;border:1px solid #C9B99A;background:#FDFAF5;font-family:'Jost',sans-serif;font-size:14px;margin-bottom:14px;outline:none;letter-spacing:0.1em;text-align:center;}
.elb input:focus{border-color:#8B6B4A;}
.elb .ebtn{width:100%;padding:14px;background:#1A1714;color:#F5F0E8;border:none;font-family:'Jost',sans-serif;font-size:10.5px;letter-spacing:0.22em;text-transform:uppercase;cursor:pointer;transition:background 0.2s;}
.elb .ebtn:hover{background:#2a2420;}
.elb-err{color:#b03030;font-size:11.5px;margin-top:12px;display:none;}
#edit-bar{display:none;position:fixed;top:0;left:0;right:0;z-index:9000;height:50px;background:#1A1714;border-bottom:1px solid rgba(201,185,154,0.4);align-items:center;justify-content:space-between;padding:0 20px;}
#edit-bar.show{display:flex;}
.eb-badge{background:#8B6B4A;color:#F5F0E8;font-size:9px;letter-spacing:0.22em;text-transform:uppercase;padding:4px 11px;font-family:'Jost',sans-serif;}
.eb-hint{font-size:11px;color:rgba(245,240,232,0.38);letter-spacing:0.04em;font-family:'Jost',sans-serif;margin-left:12px;}
.eb-right{display:flex;gap:8px;}
.eb-btn{padding:7px 18px;font-size:9.5px;letter-spacing:0.18em;text-transform:uppercase;cursor:pointer;border:none;font-family:'Jost',sans-serif;}
.eb-export{background:#C9B99A;color:#1A1714;}.eb-export:hover{background:#DDD0BA;}
.eb-exit{background:transparent;color:rgba(245,240,232,0.5);border:1px solid rgba(201,185,154,0.25);}.eb-exit:hover{color:#F5F0E8;border-color:#C9B99A;}
body.emode{padding-top:50px;}
body.emode nav{top:50px;}
body.emode .mobile-menu{top:114px;}
body.emode [data-ed]{outline:1px dashed rgba(139,107,74,0.35);cursor:text;min-height:1em;}
body.emode [data-ed]:hover{outline:1.5px solid #C9B99A;background:rgba(201,185,154,0.06);}
body.emode [data-ed]:focus{outline:2px solid #8B6B4A;background:rgba(201,185,154,0.1);}
#exp-toast{position:fixed;bottom:92px;right:28px;background:#1A1714;color:#C9B99A;padding:13px 20px;font-size:11px;letter-spacing:0.1em;z-index:9500;border:1px solid rgba(201,185,154,0.3);opacity:0;pointer-events:none;transition:opacity 0.3s;font-family:'Jost',sans-serif;}
#exp-toast.show{opacity:1;}
</style>
</head>
<body>
<nav id="navbar">
  <a href="#hero" class="nav-logo">SERAX</a>
  <ul class="nav-links">
    <li><a href="#about" data-s="about">Profile</a></li>
    <li><a href="#understanding" data-s="understanding">Understanding</a></li>
    <li><a href="#challenges" data-s="challenges">Challenges</a></li>
    <li><a href="#objection" data-s="objection">Objection</a></li>
    <li><a href="#preuves" data-s="preuves">Evidence</a></li>
    <li><a href="#jours" data-s="jours">First 90 Days</a></li>
    <li><a href="#cta" data-s="cta">Contact</a></li>
  </ul>
  <button class="hamburger" id="hamburger" aria-label="Menu"><span></span><span></span><span></span></button>
</nav>
<div class="mobile-menu" id="mobileMenu">
  <a href="#about" class="mobile-link">Profile</a>
  <a href="#understanding" class="mobile-link">Understanding</a>
  <a href="#challenges" class="mobile-link">Challenges</a>
  <a href="#objection" class="mobile-link">Objection</a>
  <a href="#preuves" class="mobile-link">Evidence</a>
  <a href="#jours" class="mobile-link">First 90 Days</a>
  <a href="#cta" class="mobile-link">Contact</a>
</div>
<section id="hero">
  <div class="hero-bg-letter" aria-hidden="true">S</div>
  <p class="hero-eyebrow">Terence Richard &nbsp;&middot;&nbsp; Commercial Director France &nbsp;&middot;&nbsp; Serax</p>
  <h1 class="hero-title">Serax France doesn&rsquo;t need a revolution.<br>It needs the right person to <em>protect what works</em> -<br>and unlock what&rsquo;s next.</h1>
  <p class="hero-sub">This page reflects what I took away from our conversation - my understanding of Serax, its challenges in France, and the case for my candidacy.</p>
  <div class="hero-scroll">Following our interview</div>
</section>

<section id="about">
  <div class="reveal">
    <p class="s-num">00</p>
    <p class="s-label">Who I am</p>
    <h2 class="s-title">Twenty years building<br><em>networks that sell</em></h2>
    <div class="s-divider"></div>
  </div>
  <div class="reveal" class="about-body">
    <p class="about-p">Twenty years building networks that sell. Not managing pipelines - creating the conditions where partners, prescribers and teams become your best commercial asset.</p>
    <p class="about-p">At Exta Archis, I built a network of 700+ architects and interior designers across France from the ground up. Each one activated, educated, equipped to recommend the right product to the right project. A network of prescribers that functioned exactly like points of sale - because that&rsquo;s what they were. That&rsquo;s the discipline I bring to 600 Serax retail partners.</p>
    <p class="about-p">At BCD Travel and CWT, I inherited teams and P&amp;Ls under pressure. I delivered growth without disruption, retained clients others would have lost, and coordinated commercial operations across 13 countries. I know how to walk into a structured organization, read it fast, earn trust - and move things forward without breaking what works.</p>
    <p class="about-quote">I don&rsquo;t come with a transformation agenda. I come with the experience to know what to protect, the instinct to know where to push, and the track record to back it up.</p>
  </div>
</section>

<section id="understanding">
  <div class="reveal">
    <p class="s-num">01</p><p class="s-label">What I understand about Serax</p>
    <h2 class="s-title">A brand built on collaboration,<br><em>not just production</em></h2>
    <div class="s-divider"></div>
  </div>
  <div class="cards-grid reveal">
    <div class="card"><div class="card-n">01</div><h3 class="card-h">65+ designers. One consistent philosophy.</h3><p class="card-p">Serax is not a manufacturer - it&rsquo;s a creative ecosystem. From Ann Demeulemeester to Yotam Ottolenghi, Marni to Kelly Wearstler, each collection carries a story. The commercial role is to translate that story into commercial reality, market after market.</p><span class="card-tag">Brand DNA</span></div>
    <div class="card"><div class="card-n">02</div><h3 class="card-h">France is a top-3 market - and in growth.</h3><p class="card-p">Alongside the Netherlands and Germany, France is explicitly cited as a growing market in 2025. With 500&ndash;600 retail points already active, the network exists. The mission is to deepen it, activate the Living Lab concept, and convert presence into performance.</p><span class="card-tag">Market Position</span></div>
    <div class="card"><div class="card-n">03</div><h3 class="card-h">Two strategic ambitions, running in parallel.</h3><p class="card-p">Serax is simultaneously anchoring retail leadership via the blended shopping Living Lab model, and building its global hospitality capabilities. A Global Hospitality Director was recently recruited. France - with 654 Michelin-starred restaurants - is the premier test case for both.</p><span class="card-tag">Strategic Moment</span></div>
  </div>
</section>
<section id="challenges">
  <div class="reveal">
    <p class="s-num">02</p><p class="s-label">What I heard in our conversation</p>
    <h2 class="s-title">The four real<br><em>challenges</em> ahead</h2>
    <div class="s-divider"></div>
  </div>
  <div class="ch-list reveal">
    <div class="ch-item"><div class="ch-idx">01</div><div class="ch-text">Consolidate, activate and expand the existing retail network of around 600 points of sale.</div><div class="ch-note">Living Lab deployment in France<br>3 PDV already interested (Paris / Lille)</div></div>
    <div class="ch-item"><div class="ch-idx">02</div><div class="ch-text">Rebuild trust with the team - 3 commercial reps + 1 agent who need direction, not disruption.</div><div class="ch-note">Stability as the priority<br>Listening before acting</div></div>
    <div class="ch-item"><div class="ch-idx">03</div><div class="ch-text">Open the gifting channel - B2B corporate from scratch, low investment, quick wins needed.</div><div class="ch-note">Go-to-market construction<br>Network activation</div></div>
    <div class="ch-item"><div class="ch-idx">04</div><div class="ch-text">Lay the groundwork for 2027 - hospitality, A&amp;D prescription, new growth relays.</div><div class="ch-note">654 Michelin stars in France<br>Untapped A&amp;D bridge</div></div>
  </div>
  <blockquote class="ch-verdict reveal">&ldquo;What you&rsquo;re not looking for: someone who arrives with a grand transformation plan. What you are looking for: someone who understands the value of what exists - and knows where to push to go further.&rdquo;</blockquote>
</section>
<section id="objection">
  <div class="reveal">
    <p class="s-num">03</p><p class="s-label">The legitimate question</p>
    <h2 class="s-title">Addressing the retail<br><em>experience gap</em> directly</h2>
    <div class="s-divider"></div>
  </div>
  <div class="obj-grid reveal">
    <div class="obj-left"><p class="obj-lbl">The objection</p><p class="obj-quote">&ldquo;I don&rsquo;t come from retail. 75% of our French business is retail. How will I manage the retail of about 600+ points of sale?&rdquo;</p></div>
    <div>
      <div class="resp-step"><div class="step-dot">I</div><div><h4 class="step-h">Acknowledge</h4><p class="step-p">You&rsquo;re right - I haven&rsquo;t managed a 500-store retail network directly. That&rsquo;s a fair observation and I won&rsquo;t sidestep it.</p></div></div>
      <div class="resp-step"><div class="step-dot">II</div><div><h4 class="step-h">The bridge</h4><p class="step-p">But here&rsquo;s what I know about your 500 retailers: most were introduced to Serax by an architect, a designer, or a decorator. That&rsquo;s exactly the network I&rsquo;ve spent 4 years building at Exta Archis - 700+ A&amp;D professionals who specify products, influence purchasing decisions, and bridge design culture with commercial reality.</p></div></div>
      <div class="resp-step"><div class="step-dot">III</div><div><h4 class="step-h">The conclusion</h4><p class="step-p">In a market where Serax retail is premium by definition - Le Bon March&eacute;, Galeries Lafayette, Merci, concept stores - the language spoken is design, not distribution. My network doesn&rsquo;t compete with your retail. <strong>It feeds it.</strong></p></div></div>
    </div>
  </div>
  <div class="bridge reveal">
    <div class="b-node"><div class="b-lbl">My network</div><div class="b-val">700+<br>Architects &amp; Designers</div></div>
    <div class="b-arrow">&rarr;</div>
    <div class="b-node"><div class="b-lbl">They prescribe to</div><div class="b-val">Retail clients<br>+ Hospitality projects</div></div>
    <div class="b-arrow">&rarr;</div>
    <div class="b-node"><div class="b-lbl">Which feeds</div><div class="b-val">Both Serax<br>channels simultaneously</div></div>
  </div>
</section>
<section id="preuves">
  <div class="reveal">
    <p class="s-num">04</p><p class="s-label">Aligned to your specific challenges</p>
    <h2 class="s-title">Four proofs,<br><em>not promises</em></h2>
    <div class="s-divider"></div>
  </div>
  <div class="reveal">
    <div class="tabs-bar">
      <button class="tab-btn active" onclick="showTab(0)">Team Stability</button>
      <button class="tab-btn" onclick="showTab(1)">Premium Retail</button>
      <button class="tab-btn" onclick="showTab(2)">Matrix Org</button>
      <button class="tab-btn" onclick="showTab(3)">New Channels</button>
    </div>
    <div class="tab-pane active" id="tp0"><div class="proof-grid"><div><p class="proof-ch-lbl">Your challenge</p><div class="proof-ch-box">The role has seen recent changes. The team needs reassurance, not rebuilding. Continuity and trust must come first.</div></div><div><p class="proof-ev-lbl">My evidence</p><p class="proof-ev-p">At BCD Travel, I inherited a team of 10 and a P&amp;L under significant cost pressure. My response wasn&rsquo;t to rebuild - it was to listen, clarify priorities, and let the team understand where we were going together. The team itself became the asset. Clients stayed because the people stayed.</p><div class="kpis"><div><div class="kpi-val">98%</div><div class="kpi-lbl">Client<br>retention rate</div></div><div><div class="kpi-val">+25%</div><div class="kpi-lbl">Revenue<br>growth</div></div><div><div class="kpi-val">0</div><div class="kpi-lbl">Voluntary<br>team departures</div></div></div></div></div></div>
    <div class="tab-pane" id="tp1"><div class="proof-grid"><div><p class="proof-ch-lbl">Your challenge</p><div class="proof-ch-box">500+ premium retail points need activation, not administration. Each partner must tell the right Serax story - the right space, the right collections, the right narrative.</div></div><div><p class="proof-ev-lbl">My evidence</p><p class="proof-ev-p">Managing 130+ European suppliers at Exta Archis taught me that a network is only as strong as each partner&rsquo;s ability to tell your story. I structured joint business plans, CRM tracking, and KPI frameworks with partners who had never worked that way. The Living Lab model - shop-in-shop, samples only, commission-based - requires commercial trust, partner education, and operational discipline. That&rsquo;s exactly what I do.</p><div class="kpis"><div><div class="kpi-val">130+</div><div class="kpi-lbl">Supplier network<br>managed directly</div></div><div><div class="kpi-val">3</div><div class="kpi-lbl">First Living Lab<br>France targets ready</div></div></div></div></div></div>
    <div class="tab-pane" id="tp2"><div class="proof-grid"><div><p class="proof-ch-lbl">Your challenge</p><div class="proof-ch-box">Reporting to the Global Retail Director, coordinating 4 Country Managers, aligning with hospitality, marketing, and product teams in Antwerp simultaneously.</div></div><div><p class="proof-ev-lbl">My evidence</p><p class="proof-ev-p">At CWT, I managed a multinational account across 13 countries with 12 FTEs, coordinating global functions, local operations, and executive stakeholders simultaneously. Matrix organizations are not a complexity I navigate - they&rsquo;re the environment I perform in. The key is clear escalation paths, transparent reporting, and over-communication across time zones and functions.</p><div class="kpis"><div><div class="kpi-val">13</div><div class="kpi-lbl">Countries<br>coordinated</div></div><div><div class="kpi-val">12</div><div class="kpi-lbl">FTEs under<br>management</div></div><div><div class="kpi-val">20+</div><div class="kpi-lbl">Years in matrix<br>organizations</div></div></div></div></div></div>
    <div class="tab-pane" id="tp3"><div class="proof-grid"><div><p class="proof-ch-lbl">Your challenge</p><div class="proof-ch-box">Build a B2B corporate gifting channel in France - from zero, with a constrained budget, in a new-to-category market.</div></div><div><p class="proof-ev-lbl">My evidence</p><p class="proof-ev-p">At Workforce Logiq, I launched a product with zero French market presence, zero brand awareness, and a lean team. The challenge wasn&rsquo;t product - it was go-to-market construction: identifying the right entry points, building a short list of strategic targets, and closing before the organization doubted the investment. A &euro;1M strategic contract in 18 months with no marketing budget. The gifting opportunity at Serax is the same muscle - applied to a brand people already love.</p><div class="kpis"><div><div class="kpi-val">&euro;1M</div><div class="kpi-lbl">Contract from<br>zero base</div></div><div><div class="kpi-val">18</div><div class="kpi-lbl">Months to<br>first major win</div></div></div></div></div></div>
  </div>
</section>
<section id="jours">
  <div class="reveal">
    <p class="s-num">05</p><p class="s-label">A concrete plan, not a promise</p>
    <h2 class="s-title">The first<br><em>90 days</em></h2>
    <div class="s-divider"></div>
  </div>
  <div class="phases reveal">
    <div class="phase"><div class="phase-period">Days 0 &ndash; 30</div><h3 class="phase-h">Listen before acting</h3><ul class="phase-items"><li class="phase-item">Individual meetings with all 3 commercial reps + agent - understand the real terrain, frustrations, and strengths</li><li class="phase-item">Deep dives with key retail accounts - what works, what doesn&rsquo;t, what&rsquo;s been promised</li><li class="phase-item">Alignment with Global Retail Director on France KPIs and priorities</li><li class="phase-item">Network cartography: top performers, at-risk accounts, under-exploited partners</li></ul><div class="phase-accent"></div></div>
    <div class="phase"><div class="phase-period">Days 30 &ndash; 60</div><h3 class="phase-h">Stabilize and prioritize</h3><ul class="phase-items"><li class="phase-item">Identify 10&ndash;15 retail accounts with strong untapped potential</li><li class="phase-item">First Living Lab candidate conversations in France (Paris / Lille pipeline)</li><li class="phase-item">Initial A&amp;D network activation - hospitality and gifting opportunities</li><li class="phase-item">Simple gifting B2B proposal - fast, budget-controlled, measurable</li></ul><div class="phase-accent"></div></div>
    <div class="phase"><div class="phase-period">Days 60 &ndash; 90</div><h3 class="phase-h">Build for growth</h3><ul class="phase-items"><li class="phase-item">Present France 2025&ndash;2026 plan to leadership: retail + gifting + A&amp;D relays</li><li class="phase-item">CRM, reporting, and shared forecast operational with Antwerp</li><li class="phase-item">First concrete quick wins launched and measurable</li><li class="phase-item">Country Manager alignment on shared practices and synergies</li></ul><div class="phase-accent"></div></div>
  </div>
</section>
<section id="cta">
  <div class="reveal">
    <p class="s-num">06</p><p class="s-label">Let&rsquo;s continue the conversation</p>
    <h2 class="cta-title">One conversation changed my understanding of Serax. <em>A second one</em> might change everything.</h2>
    <p class="cta-sub">I came into our interview knowing Serax as a design brand. I left understanding it as a commercial ecosystem with specific human and structural needs - and a clear window of opportunity in France. I&rsquo;d welcome the chance to go further.</p>
    <div class="cta-btns">
      <a href="/cdn-cgi/l/email-protection#5c28392e39323f39722e353f343d2e386b691c3b313d3530723f3331" class="btn-p">Send an email</a>
      <a href="https://linkedin.com/in/terencerichard" class="btn-s" target="_blank" rel="noopener">LinkedIn</a>
      <a href="tel:+33658841085" class="btn-s">Call directly</a>
    </div>
    <p style="margin-top:52px;font-family:'Cormorant Garamond',Georgia,serif;font-size:20px;font-style:italic;font-weight:300;color:rgba(245,240,232,0.55);line-height:1.7;max-width:620px;margin-left:auto;margin-right:auto;">&ldquo;Choosing the right flower pot, preparing the right soil, and creating the conditions for something to truly grow is something that deeply drives me.&rdquo;<br><span style="display:block;margin-top:14px;font-family:'Jost',sans-serif;font-size:10px;letter-spacing:0.22em;text-transform:uppercase;font-style:normal;color:rgba(245,240,232,0.35);">Terence Richard</span></p>
  </div>
</section>
<footer>
  <span class="ft-name">Terence Richard - Commercial Director France candidacy</span>
  <span class="ft-note">Prepared following interview with Serax &middot; 2026</span>
</footer>
<button id="edit-fab" title="Mode edition">&#9998;</button>
<div id="edit-login">
  <div class="elb">
    <h2>Mode &Eacute;dition</h2>
    <p class="sub">Entrez le mot de passe</p>
    <input type="password" id="epw" placeholder="Mot de passe" autocomplete="off"/>
    <button class="ebtn" id="epw-btn">Acc&eacute;der &rarr;</button>
    <p class="elb-err" id="epw-err">Mot de passe incorrect</p>
  </div>
</div>
<div id="edit-bar">
  <div style="display:flex;align-items:center;">
    <span class="eb-badge">&#9998; Mode Edition</span>
    <span class="eb-hint">Cliquez sur n'importe quel texte pour modifier</span>
  </div>
  <div class="eb-right">
    <button class="eb-btn eb-export" id="eb-export">&#11015; Telecharger index.html</button>
    <button class="eb-btn eb-exit" id="eb-exit">Quitter</button>
  </div>
</div>
<div id="exp-toast">Fichier exporte !</div>
<script data-cfasync="false" src="/cdn-cgi/scripts/5c5dd728/cloudflare-static/email-decode.min.js"></script><script>
var navbar=document.getElementById('navbar');
window.addEventListener('scroll',function(){navbar.classList.toggle('scrolled',window.scrollY>40);});
var hamburger=document.getElementById('hamburger'),mobileMenu=document.getElementById('mobileMenu');
hamburger.addEventListener('click',function(){hamburger.classList.toggle('open');mobileMenu.classList.toggle('open');document.body.style.overflow=mobileMenu.classList.contains('open')?'hidden':'';});
document.querySelectorAll('.mobile-link').forEach(function(a){a.addEventListener('click',function(){hamburger.classList.remove('open');mobileMenu.classList.remove('open');document.body.style.overflow='';});});
var navLinks=document.querySelectorAll('.nav-links a[data-s]');
if('IntersectionObserver' in window){
  var sObs=new IntersectionObserver(function(entries){entries.forEach(function(e){if(e.isIntersecting){navLinks.forEach(function(l){l.classList.remove('active');});var lnk=document.querySelector('.nav-links a[data-s="'+e.target.id+'"]');if(lnk)lnk.classList.add('active');}});},{threshold:0.35});
  document.querySelectorAll('section[id]').forEach(function(s){sObs.observe(s);});
  var rObs=new IntersectionObserver(function(entries){entries.forEach(function(e){if(e.isIntersecting){e.target.classList.add('visible');rObs.unobserve(e.target);}});},{threshold:0.1});
  document.querySelectorAll('.reveal').forEach(function(r){rObs.observe(r);});
}else{document.querySelectorAll('.reveal').forEach(function(r){r.classList.add('visible');});}
function showTab(idx){document.querySelectorAll('.tab-btn').forEach(function(b,i){b.classList.toggle('active',i===idx);});document.querySelectorAll('.tab-pane').forEach(function(p,i){p.classList.toggle('active',i===idx);});}
document.querySelectorAll('a[href^="#"]').forEach(function(a){a.addEventListener('click',function(e){var href=a.getAttribute('href');if(href==='#')return;var t=document.querySelector(href);if(t){e.preventDefault();t.scrollIntoView({behavior:'smooth'});}});});
/* EDITOR */
var PASS='serax2026';
var fab=document.getElementById('edit-fab'),loginEl=document.getElementById('edit-login'),editBar=document.getElementById('edit-bar'),toast=document.getElementById('exp-toast'),epw=document.getElementById('epw');
var EDS=['.hero-eyebrow','.hero-title','.hero-sub','.hero-scroll','.s-label','.s-title','.card-h','.card-p','.card-tag','.ch-text','.ch-note','.ch-verdict','.obj-quote','.step-h','.step-p','.b-lbl','.b-val','.proof-ch-box','.proof-ev-p','.kpi-val','.kpi-lbl','.phase-period','.phase-h','.phase-item','.cta-title','.cta-sub','.ft-name','.ft-note','.tab-btn','.nav-logo','h1','h2','h3','h4'];
function markEd(){EDS.forEach(function(sel){document.querySelectorAll(sel).forEach(function(el){if(!el.hasAttribute('data-ed')){el.setAttribute('data-ed','1');el.setAttribute('contenteditable','false');}});});}
function enableEdit(){document.body.classList.add('emode');editBar.classList.add('show');fab.style.display='none';document.querySelectorAll('[data-ed]').forEach(function(el){el.setAttribute('contenteditable','true');});}
function disableEdit(){document.body.classList.remove('emode');editBar.classList.remove('show');fab.style.display='';document.querySelectorAll('[data-ed]').forEach(function(el){el.setAttribute('contenteditable','false');});}
function exportHTML(){
  var clone=document.documentElement.cloneNode(true);
  ['edit-fab','edit-login','edit-bar','exp-toast'].forEach(function(id){var el=clone.querySelector('#'+id);if(el)el.remove();});
  clone.querySelectorAll('[contenteditable]').forEach(function(el){el.removeAttribute('contenteditable');});
  clone.querySelectorAll('[data-ed]').forEach(function(el){el.removeAttribute('data-ed');});
  var b=clone.querySelector('body');if(b){b.classList.remove('emode');b.style.paddingTop='';}
  var n=clone.querySelector('nav');if(n)n.style.top='';
  var mm=clone.querySelector('.mobile-menu');if(mm)mm.style.top='';
  var html='<!DOCTYPE html>\n'+clone.outerHTML;
  var blob=new Blob([html],{type:'text/html;charset=utf-8'});
  var url=URL.createObjectURL(blob);
  var a=document.createElement('a');a.href=url;a.download='index.html';
  document.body.appendChild(a);a.click();document.body.removeChild(a);URL.revokeObjectURL(url);
  toast.classList.add('show');setTimeout(function(){toast.classList.remove('show');},3000);
}
fab.addEventListener('click',function(){loginEl.classList.add('show');setTimeout(function(){epw.focus();},80);});
document.getElementById('epw-btn').addEventListener('click',function(){
  if(epw.value===PASS){loginEl.classList.remove('show');document.getElementById('epw-err').style.display='none';epw.value='';enableEdit();}
  else{document.getElementById('epw-err').style.display='block';epw.value='';epw.focus();}
});
epw.addEventListener('keydown',function(e){if(e.key==='Enter')document.getElementById('epw-btn').click();if(e.key==='Escape'){loginEl.classList.remove('show');epw.value='';document.getElementById('epw-err').style.display='none';}});
loginEl.addEventListener('click',function(e){if(e.target===loginEl){loginEl.classList.remove('show');epw.value='';document.getElementById('epw-err').style.display='none';}});
document.getElementById('e
