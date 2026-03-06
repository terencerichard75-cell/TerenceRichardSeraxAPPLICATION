<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Terence Richard — Serax France</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;0,600;1,300;1,400&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --cream: #F5F0E8;
    --cream-dark: #EDE7D9;
    --ink: #1A1714;
    --sand: #C9B99A;
    --sand-light: #DDD0BA;
    --terra: #8B6B4A;
    --white: #FDFAF5;
    --accent: #6B4F35;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--cream);
    color: var(--ink);
    font-family: 'Jost', sans-serif;
    font-weight: 300;
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 0 48px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(245,240,232,0.92);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(201,185,154,0.3);
    transition: all 0.4s ease;
  }
  nav.scrolled {
    background: rgba(245,240,232,0.98);
    border-bottom-color: rgba(201,185,154,0.6);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 15px;
    font-weight: 400;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: var(--ink);
    text-decoration: none;
  }
  .nav-links {
    display: flex;
    gap: 40px;
    list-style: none;
  }
  .nav-links a {
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--ink);
    text-decoration: none;
    opacity: 0.6;
    transition: opacity 0.3s;
  }
  .nav-links a:hover,
  .nav-links a.active { opacity: 1; }
  .nav-links a.active {
    border-bottom: 1px solid var(--sand);
    padding-bottom: 2px;
  }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    padding: 120px 48px 80px;
    position: relative;
    overflow: hidden;
  }
  .hero-bg-text {
    position: absolute;
    top: 50%;
    right: -40px;
    transform: translateY(-50%);
    font-family: 'Cormorant Garamond', serif;
    font-size: 28vw;
    font-weight: 300;
    color: transparent;
    -webkit-text-stroke: 1px rgba(201,185,154,0.18);
    pointer-events: none;
    user-select: none;
    line-height: 1;
  }
  .hero-eyebrow {
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 32px;
    opacity: 0;
    transform: translateY(20px);
    animation: fadeUp 0.8s 0.2s forwards;
  }
  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(42px, 6vw, 88px);
    font-weight: 300;
    line-height: 1.1;
    max-width: 820px;
    opacity: 0;
    transform: translateY(30px);
    animation: fadeUp 0.9s 0.4s forwards;
  }
  .hero-title em {
    font-style: italic;
    color: var(--terra);
  }
  .hero-sub {
    margin-top: 40px;
    font-size: 14px;
    font-weight: 300;
    letter-spacing: 0.06em;
    color: var(--ink);
    opacity: 0;
    transform: translateY(20px);
    animation: fadeUp 0.8s 0.7s forwards;
    max-width: 500px;
    line-height: 1.8;
  }
  .hero-line {
    position: absolute;
    bottom: 60px;
    left: 48px;
    display: flex;
    align-items: center;
    gap: 16px;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--sand);
    opacity: 0;
    animation: fadeIn 1s 1.2s forwards;
  }
  .hero-line::before {
    content: '';
    display: block;
    width: 48px;
    height: 1px;
    background: var(--sand);
  }
  .scroll-indicator {
    position: absolute;
    bottom: 56px;
    right: 48px;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 8px;
    opacity: 0;
    animation: fadeIn 1s 1.5s forwards;
  }
  .scroll-indicator span {
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--sand);
    writing-mode: vertical-rl;
  }
  .scroll-indicator::after {
    content: '';
    width: 1px;
    height: 48px;
    background: linear-gradient(to bottom, var(--sand), transparent);
  }

  /* ── SECTIONS ── */
  section {
    padding: 120px 48px;
  }
  .section-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 96px;
    font-weight: 300;
    color: transparent;
    -webkit-text-stroke: 1px rgba(201,185,154,0.4);
    line-height: 1;
    margin-bottom: -20px;
    user-select: none;
  }
  .section-label {
    font-size: 10px;
    font-weight: 400;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 20px;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(32px, 4vw, 54px);
    font-weight: 300;
    line-height: 1.2;
    margin-bottom: 48px;
    max-width: 700px;
  }
  .section-title em { font-style: italic; color: var(--terra); }

  .divider {
    width: 48px;
    height: 1px;
    background: var(--sand);
    margin-bottom: 32px;
  }

  /* ── SECTION UNDERSTANDING ── */
  #understanding { background: var(--white); }
  .understanding-grid {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 2px;
    margin-top: 60px;
  }
  .understanding-card {
    background: var(--cream);
    padding: 48px 40px;
    position: relative;
    overflow: hidden;
    transition: background 0.4s;
  }
  .understanding-card:hover { background: var(--cream-dark); }
  .card-number {
    font-family: 'Cormorant Garamond', serif;
    font-size: 48px;
    font-weight: 300;
    color: rgba(201,185,154,0.5);
    margin-bottom: 24px;
  }
  .card-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 400;
    margin-bottom: 16px;
    line-height: 1.3;
  }
  .card-body {
    font-size: 14px;
    line-height: 1.9;
    color: rgba(26,23,20,0.75);
  }
  .card-tag {
    display: inline-block;
    margin-top: 20px;
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--terra);
    border-bottom: 1px solid var(--sand-light);
    padding-bottom: 2px;
  }

  /* ── SECTION CHALLENGES ── */
  #challenges { background: var(--ink); color: var(--cream); }
  #challenges .section-label { color: var(--sand); }
  #challenges .section-title { color: var(--cream); }
  #challenges .section-number { -webkit-text-stroke-color: rgba(245,240,232,0.08); }
  .challenge-list { display: flex; flex-direction: column; gap: 2px; margin-top: 60px; }
  .challenge-item {
    display: grid;
    grid-template-columns: 80px 1fr 320px;
    align-items: center;
    padding: 36px 40px;
    background: rgba(255,255,255,0.03);
    border-left: 1px solid rgba(201,185,154,0.15);
    transition: all 0.4s;
    cursor: default;
  }
  .challenge-item:hover {
    background: rgba(255,255,255,0.06);
    border-left-color: var(--sand);
  }
  .challenge-idx {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px;
    font-weight: 300;
    color: rgba(201,185,154,0.4);
  }
  .challenge-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 300;
    line-height: 1.4;
    color: var(--cream);
  }
  .challenge-note {
    font-size: 12px;
    letter-spacing: 0.08em;
    color: rgba(201,185,154,0.6);
    line-height: 1.7;
    text-align: right;
  }
  .challenge-verdict {
    margin-top: 60px;
    padding: 48px;
    border: 1px solid rgba(201,185,154,0.2);
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px;
    font-style: italic;
    font-weight: 300;
    color: var(--sand);
    line-height: 1.6;
    max-width: 780px;
  }

  /* ── OBJECTION ── */
  #objection { background: var(--cream); }
  .objection-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
    margin-top: 60px;
  }
  .objection-left {
    padding: 56px;
    background: var(--ink);
    color: var(--cream);
  }
  .objection-label {
    font-size: 10px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--sand);
    margin-bottom: 24px;
  }
  .objection-quote {
    font-family: 'Cormorant Garamond', serif;
    font-size: 28px;
    font-style: italic;
    font-weight: 300;
    line-height: 1.5;
    color: rgba(245,240,232,0.85);
  }
  .objection-right {}
  .response-step {
    display: flex;
    gap: 24px;
    padding: 32px 0;
    border-bottom: 1px solid rgba(201,185,154,0.3);
  }
  .response-step:last-child { border-bottom: none; }
  .step-marker {
    width: 32px;
    height: 32px;
    border: 1px solid var(--sand);
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 16px;
    font-weight: 400;
    color: var(--terra);
    flex-shrink: 0;
    margin-top: 2px;
  }
  .step-content {}
  .step-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 18px;
    font-weight: 500;
    margin-bottom: 10px;
  }
  .step-body {
    font-size: 14px;
    line-height: 1.9;
    color: rgba(26,23,20,0.75);
  }
  .bridge-visual {
    margin-top: 60px;
    padding: 40px;
    background: var(--cream-dark);
    display: flex;
    align-items: center;
    justify-content: space-around;
    gap: 16px;
  }
  .bridge-node {
    text-align: center;
    flex: 1;
  }
  .bridge-node-label {
    font-size: 10px;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 12px;
  }
  .bridge-node-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 20px;
    font-weight: 400;
    line-height: 1.4;
  }
  .bridge-arrow {
    color: var(--sand);
    font-size: 20px;
    flex-shrink: 0;
  }

  /* ── PREUVES ── */
  #preuves { background: var(--white); }
  .preuves-tabs {
    display: flex;
    gap: 0;
    border-bottom: 1px solid rgba(201,185,154,0.4);
    margin-bottom: 0;
    margin-top: 48px;
    overflow-x: auto;
  }
  .tab-btn {
    padding: 16px 28px;
    font-size: 11px;
    font-weight: 400;
    letter-spacing: 0.15em;
    text-transform: uppercase;
    color: rgba(26,23,20,0.45);
    background: none;
    border: none;
    border-bottom: 2px solid transparent;
    cursor: pointer;
    transition: all 0.3s;
    white-space: nowrap;
    font-family: 'Jost', sans-serif;
    margin-bottom: -1px;
  }
  .tab-btn:hover { color: var(--ink); }
  .tab-btn.active {
    color: var(--ink);
    border-bottom-color: var(--terra);
  }
  .tab-content { display: none; padding: 60px 0 0; }
  .tab-content.active { display: block; }
  .proof-layout {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 80px;
    align-items: start;
  }
  .proof-challenge {
    padding: 40px;
    background: var(--cream);
    border-left: 3px solid var(--sand);
  }
  .proof-challenge-label {
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 16px;
  }
  .proof-challenge-text {
    font-family: 'Cormorant Garamond', serif;
    font-size: 22px;
    font-weight: 300;
    line-height: 1.5;
  }
  .proof-evidence-label {
    font-size: 10px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 20px;
  }
  .proof-evidence-text {
    font-size: 15px;
    line-height: 1.9;
    color: rgba(26,23,20,0.8);
  }
  .proof-kpi {
    display: flex;
    gap: 32px;
    margin-top: 32px;
    padding-top: 32px;
    border-top: 1px solid rgba(201,185,154,0.3);
  }
  .kpi-item {}
  .kpi-value {
    font-family: 'Cormorant Garamond', serif;
    font-size: 40px;
    font-weight: 300;
    color: var(--terra);
    line-height: 1;
    margin-bottom: 6px;
  }
  .kpi-label {
    font-size: 11px;
    letter-spacing: 0.1em;
    color: rgba(26,23,20,0.5);
    line-height: 1.4;
  }

  /* ── 90 JOURS ── */
  #jours { background: var(--cream); }
  .phases {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 2px;
    margin-top: 60px;
  }
  .phase {
    padding: 48px 40px;
    background: var(--white);
    transition: background 0.4s;
    position: relative;
  }
  .phase:hover { background: var(--cream-dark); }
  .phase-period {
    font-size: 10px;
    letter-spacing: 0.22em;
    text-transform: uppercase;
    color: var(--terra);
    margin-bottom: 12px;
  }
  .phase-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 26px;
    font-weight: 400;
    margin-bottom: 32px;
    line-height: 1.3;
  }
  .phase-items {
    list-style: none;
    display: flex;
    flex-direction: column;
    gap: 14px;
  }
  .phase-item {
    font-size: 13px;
    line-height: 1.7;
    color: rgba(26,23,20,0.75);
    padding-left: 16px;
    position: relative;
  }
  .phase-item::before {
    content: '—';
    position: absolute;
    left: 0;
    color: var(--sand);
    font-size: 10px;
  }
  .phase-bar {
    position: absolute;
    bottom: 0; left: 0; right: 0;
    height: 3px;
    background: transparent;
    transition: background 0.4s;
  }
  .phase:hover .phase-bar { background: var(--sand); }

  /* ── CTA ── */
  #cta {
    background: var(--ink);
    color: var(--cream);
    padding: 120px 48px;
    text-align: center;
  }
  #cta .section-label { color: var(--sand); }
  #cta .section-number { -webkit-text-stroke-color: rgba(245,240,232,0.06); }
  .cta-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(38px, 5vw, 68px);
    font-weight: 300;
    line-height: 1.2;
    max-width: 700px;
    margin: 0 auto 32px;
    color: var(--cream);
  }
  .cta-title em { font-style: italic; color: var(--sand); }
  .cta-sub {
    font-size: 15px;
    line-height: 1.9;
    color: rgba(245,240,232,0.6);
    max-width: 560px;
    margin: 0 auto 56px;
  }
  .cta-buttons {
    display: flex;
    gap: 20px;
    justify-content: center;
    flex-wrap: wrap;
  }
  .btn-primary {
    padding: 16px 40px;
    background: var(--cream);
    color: var(--ink);
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    text-decoration: none;
    font-family: 'Jost', sans-serif;
    transition: all 0.3s;
  }
  .btn-primary:hover { background: var(--sand-light); }
  .btn-secondary {
    padding: 16px 40px;
    border: 1px solid rgba(201,185,154,0.4);
    color: rgba(245,240,232,0.7);
    font-size: 11px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    text-decoration: none;
    font-family: 'Jost', sans-serif;
    transition: all 0.3s;
  }
  .btn-secondary:hover {
    border-color: var(--sand);
    color: var(--cream);
  }

  /* ── FOOTER ── */
  footer {
    background: var(--ink);
    padding: 32px 48px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-top: 1px solid rgba(201,185,154,0.1);
  }
  .footer-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 13px;
    letter-spacing: 0.12em;
    color: rgba(245,240,232,0.4);
  }
  .footer-note {
    font-size: 11px;
    letter-spacing: 0.12em;
    color: rgba(245,240,232,0.25);
  }

  /* ── REVEAL ANIMATIONS ── */
  .reveal {
    opacity: 0;
    transform: translateY(32px);
    transition: opacity 0.8s ease, transform 0.8s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: none;
  }

  @keyframes fadeUp {
    to { opacity: 1; transform: none; }
  }
  @keyframes fadeIn {
    to { opacity: 1; }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 1024px) {
    .understanding-grid { grid-template-columns: 1fr 1fr; }
    .phases { grid-template-columns: 1fr; }
    .challenge-item { grid-template-columns: 60px 1fr; }
    .challenge-note { display: none; }
  }
  @media (max-width: 768px) {
    nav { padding: 0 24px; }
    .nav-links { display: none; }
    section { padding: 80px 24px; }
    #hero { padding: 100px 24px 60px; }
    .understanding-grid { grid-template-columns: 1fr; }
    .objection-layout { grid-template-columns: 1fr; gap: 40px; }
    .proof-layout { grid-template-columns: 1fr; gap: 40px; }
    footer { flex-direction: column; gap: 12px; text-align: center; }
    .bridge-visual { flex-direction: column; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav id="navbar">
  <a href="#hero" class="nav-logo">T · R</a>
  <ul class="nav-links">
    <li><a href="#understanding" data-section="understanding">Understanding</a></li>
    <li><a href="#challenges" data-section="challenges">Challenges</a></li>
    <li><a href="#objection" data-section="objection">Objection</a></li>
    <li><a href="#preuves" data-section="preuves">Evidence</a></li>
    <li><a href="#jours" data-section="jours">First 90 Days</a></li>
    <li><a href="#cta" data-section="cta">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-text">S</div>
  <p class="hero-eyebrow">Terence Richard · Commercial Director France · Serax</p>
  <h1 class="hero-title">
    Serax France doesn't need a revolution.<br>
    It needs the right person to <em>protect what works</em> —<br>
    and unlock what's next.
  </h1>
  <p class="hero-sub">
    This page reflects what I took away from our conversation — my understanding of Serax, its challenges, and the case for my candidacy.
  </p>
  <div class="hero-line">Following our interview</div>
  <div class="scroll-indicator"><span>Scroll</span></div>
</section>

<!-- UNDERSTANDING -->
<section id="understanding">
  <div class="reveal">
    <div class="section-number">01</div>
    <p class="section-label">What I understand about Serax</p>
    <h2 class="section-title">A brand built on collaboration,<br><em>not just production</em></h2>
    <div class="divider"></div>
  </div>
  <div class="understanding-grid reveal">
    <div class="understanding-card">
      <div class="card-number">①</div>
      <h3 class="card-title">65+ designers. One consistent philosophy.</h3>
      <p class="card-body">Serax is not a manufacturer — it's a creative ecosystem. From Ann Demeulemeester to Yotam Ottolenghi, Marni to Kelly Wearstler, each collection carries a story. The commercial role is to translate that story into commercial reality, market after market.</p>
      <span class="card-tag">Brand DNA</span>
    </div>
    <div class="understanding-card">
      <div class="card-number">②</div>
      <h3 class="card-title">France is a top-3 market — and in growth.</h3>
      <p class="card-body">Alongside the Netherlands, France is explicitly cited as a growing market in 2025. With 500–600 retail points already active, the network exists. The mission is to deepen it, activate the Living Lab concept, and convert presence into performance.</p>
      <span class="card-tag">Market Position</span>
    </div>
    <div class="understanding-card">
      <div class="card-number">③</div>
      <h3 class="card-title">Two ambitions running in parallel.</h3>
      <p class="card-body">Serax is simultaneously anchoring its retail leadership (blended shopping, Living Lab rollout) and building its hospitality capabilities globally — a Global Hospitality Director was recently recruited. France is the test case for both. In 2025, 654 Michelin-starred restaurants make France the world's premier hospitality market.</p>
      <span class="card-tag">Strategic Moment</span>
    </div>
  </div>
</section>

<!-- CHALLENGES -->
<section id="challenges">
  <div class="reveal">
    <div class="section-number">02</div>
    <p class="section-label">What I heard in our conversation</p>
    <h2 class="section-title">The four real<br><em>challenges</em> ahead</h2>
    <div class="divider" style="background: rgba(201,185,154,0.4);"></div>
  </div>
  <div class="challenge-list reveal">
    <div class="challenge-item">
      <div class="challenge-idx">01</div>
      <div class="challenge-text">Stabilize the retail network — 500+ points of sale need activation, not administration.</div>
      <div class="challenge-note">Living Lab deployment in France<br>First 3 PDV already interested</div>
    </div>
    <div class="challenge-item">
      <div class="challenge-idx">02</div>
      <div class="challenge-text">Rebuild trust with the team — 3 commercial reps + 1 agent who need direction, not disruption.</div>
      <div class="challenge-note">Stability as the priority<br>Listening before acting</div>
    </div>
    <div class="challenge-item">
      <div class="challenge-idx">03</div>
      <div class="challenge-text">Open the gifting channel — B2B corporate from scratch, low investment, quick wins.</div>
      <div class="challenge-note">Go-to-market construction<br>Network activation</div>
    </div>
    <div class="challenge-item">
      <div class="challenge-idx">04</div>
      <div class="challenge-text">Lay the groundwork for 2027 — hospitality, A&D prescription, new growth relays.</div>
      <div class="challenge-note">654 Michelin stars in France<br>Untapped A&D bridge</div>
    </div>
  </div>
  <div class="challenge-verdict reveal">
    "What you're not looking for: someone who arrives with a grand transformation plan. What you are looking for: someone who understands the value of what exists — and knows where to push to go further."
  </div>
</section>

<!-- OBJECTION -->
<section id="objection">
  <div class="reveal">
    <div class="section-number">03</div>
    <p class="section-label">The legitimate question</p>
    <h2 class="section-title">Addressing the retail<br><em>experience gap</em> directly</h2>
    <div class="divider"></div>
  </div>
  <div class="objection-layout reveal">
    <div class="objection-left">
      <p class="objection-label">The objection</p>
      <p class="objection-quote">"He doesn't come from retail. 75% of our French business is retail. How will he manage 500+ points of sale?"</p>
    </div>
    <div class="objection-right">
      <div class="response-step">
        <div class="step-marker">I</div>
        <div class="step-content">
          <h4 class="step-title">Acknowledge</h4>
          <p class="step-body">You're right — I haven't managed a 500-store retail network directly. That's a fair observation and I won't sidestep it.</p>
        </div>
      </div>
      <div class="response-step">
        <div class="step-marker">II</div>
        <div class="step-content">
          <h4 class="step-title">The bridge</h4>
          <p class="step-body">But here's what I know about your 500 retailers: most of them were introduced to Serax by an architect, a designer, or a decorator. That's exactly the network I've spent 4 years building at Exta Archis — 700+ A&D professionals who specify products, influence purchasing decisions, and bridge design culture with commercial reality.</p>
        </div>
      </div>
      <div class="response-step">
        <div class="step-marker">III</div>
        <div class="step-content">
          <h4 class="step-title">The conclusion</h4>
          <p class="step-body">In a market where Serax retail is premium by definition — Le Bon Marché, Galeries Lafayette, Merci, concept stores — the language spoken is design, not distribution. My network doesn't compete with your retail. <strong>It feeds it.</strong></p>
        </div>
      </div>
    </div>
  </div>
  <div class="bridge-visual reveal">
    <div class="bridge-node">
      <div class="bridge-node-label">My network</div>
      <div class="bridge-node-value">700+<br>Architects & Designers</div>
    </div>
    <div class="bridge-arrow">→</div>
    <div class="bridge-node">
      <div class="bridge-node-label">They prescribe to</div>
      <div class="bridge-node-value">Retail clients<br>+ Hospitality projects</div>
    </div>
    <div class="bridge-arrow">→</div>
    <div class="bridge-node">
      <div class="bridge-node-label">Which feeds</div>
      <div class="bridge-node-value">Both Serax<br>channels simultaneously</div>
    </div>
  </div>
</section>

<!-- PREUVES -->
<section id="preuves">
  <div class="reveal">
    <div class="section-number">04</div>
    <p class="section-label">Aligned to your specific challenges</p>
    <h2 class="section-title">Four proofs,<br><em>not promises</em></h2>
    <div class="divider"></div>
  </div>
  <div class="preuves-tabs reveal">
    <button class="tab-btn active" onclick="switchTab(0)">Team Stability</button>
    <button class="tab-btn" onclick="switchTab(1)">Premium Retail</button>
    <button class="tab-btn" onclick="switchTab(2)">Matrix Org</button>
    <button class="tab-btn" onclick="switchTab(3)">New Channels</button>
  </div>

  <div class="tab-content active" id="tab-0">
    <div class="proof-layout">
      <div>
        <p class="proof-challenge-label">Your challenge</p>
        <div class="proof-challenge">
          <p class="proof-challenge-text">The role has seen recent changes. The team needs reassurance, not rebuilding. Continuity and trust come first.</p>
        </div>
      </div>
      <div>
        <p class="proof-evidence-label">My evidence</p>
        <p class="proof-evidence-text">At BCD Travel, I inherited a team of 10 and a P&L under significant cost pressure. My response wasn't to rebuild — it was to listen, clarify priorities, and let the team understand where we were going together. The result: the team itself became the asset. Clients stayed because the people stayed.</p>
        <div class="proof-kpi">
          <div class="kpi-item">
            <div class="kpi-value">98%</div>
            <div class="kpi-label">Client<br>retention rate</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">+25%</div>
            <div class="kpi-label">Revenue<br>growth</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">0</div>
            <div class="kpi-label">Voluntary<br>team departures</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab-1">
    <div class="proof-layout">
      <div>
        <p class="proof-challenge-label">Your challenge</p>
        <div class="proof-challenge">
          <p class="proof-challenge-text">500+ premium retail points need activation, not administration. Each partner must tell the right Serax story — with the right space, the right collections, the right narrative.</p>
        </div>
      </div>
      <div>
        <p class="proof-evidence-label">My evidence</p>
        <p class="proof-evidence-text">Managing 130+ European suppliers at Exta Archis taught me that a network is only as strong as each partner's ability to tell your story. I structured joint business plans, CRM tracking, and KPI frameworks with partners who had never worked that way. The Living Lab model — shop-in-shop, samples only, commission-based — is a governance model I can implement. It requires commercial trust, partner education, and operational discipline. That's what I do.</p>
        <div class="proof-kpi">
          <div class="kpi-item">
            <div class="kpi-value">130+</div>
            <div class="kpi-label">Supplier network<br>managed directly</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">3</div>
            <div class="kpi-label">First Living Lab<br>France targets ready</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab-2">
    <div class="proof-layout">
      <div>
        <p class="proof-challenge-label">Your challenge</p>
        <div class="proof-challenge">
          <p class="proof-challenge-text">Reporting to the Global Retail Director, collaborating with 4 Country Managers, aligning with hospitality, marketing, and product teams in Antwerp simultaneously.</p>
        </div>
      </div>
      <div>
        <p class="proof-evidence-label">My evidence</p>
        <p class="proof-evidence-text">At CWT, I managed a multinational account across 13 countries with 12 FTEs, coordinating global functions, local operations, and executive stakeholders simultaneously. Matrix organizations are not a complexity I navigate — they're the environment I perform in. The key is clear escalation paths, transparent reporting, and over-communication across time zones and functions.</p>
        <div class="proof-kpi">
          <div class="kpi-item">
            <div class="kpi-value">13</div>
            <div class="kpi-label">Countries<br>coordinated</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">12</div>
            <div class="kpi-label">FTEs under<br>management</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">20+</div>
            <div class="kpi-label">Years in matrix<br>organizations</div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="tab-content" id="tab-3">
    <div class="proof-layout">
      <div>
        <p class="proof-challenge-label">Your challenge</p>
        <div class="proof-challenge">
          <p class="proof-challenge-text">Build a B2B corporate gifting channel in France — from zero, with constrained budget, in a new-to-category market.</p>
        </div>
      </div>
      <div>
        <p class="proof-evidence-label">My evidence</p>
        <p class="proof-evidence-text">At Workforce Logiq, I launched a product with zero French market presence, zero brand awareness, and a lean team. The challenge wasn't product — it was go-to-market construction: identifying the right entry points, building a short list of strategic targets, and closing before the organization doubted the investment. A €1M strategic contract in 18 months with no marketing budget. The gifting opportunity at Serax is the same muscle — applied to a brand people already love.</p>
        <div class="proof-kpi">
          <div class="kpi-item">
            <div class="kpi-value">€1M</div>
            <div class="kpi-label">Contract from<br>zero base</div>
          </div>
          <div class="kpi-item">
            <div class="kpi-value">18</div>
            <div class="kpi-label">Months to<br>first major win</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- 90 JOURS -->
<section id="jours">
  <div class="reveal">
    <div class="section-number">05</div>
    <p class="section-label">A concrete plan, not a promise</p>
    <h2 class="section-title">The first<br><em>90 days</em></h2>
    <div class="divider"></div>
  </div>
  <div class="phases reveal">
    <div class="phase">
      <div class="phase-period">Days 0 – 30</div>
      <h3 class="phase-title">Listen before acting</h3>
      <ul class="phase-items">
        <li class="phase-item">Individual meetings with all 3 commercial reps + agent — understand the real terrain, frustrations, strengths</li>
        <li class="phase-item">Deep dives with key retail accounts — what works, what doesn't, what's been promised</li>
        <li class="phase-item">Alignment with Global Retail Director on France KPIs and priorities</li>
        <li class="phase-item">Network cartography: top performers, at-risk accounts, under-exploited partners</li>
      </ul>
      <div class="phase-bar"></div>
    </div>
    <div class="phase">
      <div class="phase-period">Days 30 – 60</div>
      <h3 class="phase-title">Stabilize and prioritize</h3>
      <ul class="phase-items">
        <li class="phase-item">Identify 10–15 retail accounts with strong untapped potential</li>
        <li class="phase-item">First Living Lab candidate conversations in France (Paris / Lille pipeline)</li>
        <li class="phase-item">Initial A&D network activation — identify hospitality & gifting opportunities</li>
        <li class="phase-item">Simple gifting B2B proposal — fast, budget-controlled, measurable</li>
      </ul>
      <div class="phase-bar"></div>
    </div>
    <div class="phase">
      <div class="phase-period">Days 60 – 90</div>
      <h3 class="phase-title">Build for growth</h3>
      <ul class="phase-items">
        <li class="phase-item">Present France 2025–2026 plan to leadership: retail + gifting + A&D relays</li>
        <li class="phase-item">CRM, reporting, and shared forecast system with Antwerp operational</li>
        <li class="phase-item">First concrete quick wins launched and measurable</li>
        <li class="phase-item">Country Manager alignment on shared practices and synergies</li>
      </ul>
      <div class="phase-bar"></div>
    </div>
  </div>
</section>

<!-- CTA -->
<section id="cta">
  <div class="reveal">
    <div class="section-number" style="text-align:center;">06</div>
    <p class="section-label" style="text-align:center;">Let's continue</p>
    <h2 class="cta-title">One conversation changed my understanding of Serax. <em>A second one</em> might change everything.</h2>
    <p class="cta-sub">I came into our interview knowing Serax as a design brand. I left understanding it as a commercial ecosystem with specific human and structural needs — and a clear window of opportunity in France.</p>
    <div class="cta-buttons">
      <a href="mailto:terence.richard@email.com" class="btn-primary">Send an email</a>
      <a href="https://linkedin.com/in/terencerichard" class="btn-secondary" target="_blank">LinkedIn</a>
      <a href="tel:+33600000000" class="btn-secondary">Call directly</a>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <span class="footer-name">Terence Richard — Commercial Director France candidacy</span>
  <span class="footer-note">Prepared following interview with Serax · 2026</span>
</footer>

<script>
  // ── NAV SCROLL ──
  const navbar = document.getElementById('navbar');
  window.addEventListener('scroll', () => {
    if (window.scrollY > 40) navbar.classList.add('scrolled');
    else navbar.classList.remove('scrolled');
  });

  // ── ACTIVE NAV LINK ──
  const sections = document.querySelectorAll('section[id]');
  const navLinks = document.querySelectorAll('.nav-links a[data-section]');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        navLinks.forEach(l => l.classList.remove('active'));
        const active = document.querySelector(`.nav-links a[data-section="${entry.target.id}"]`);
        if (active) active.classList.add('active');
      }
    });
  }, { threshold: 0.35 });
  sections.forEach(s => observer.observe(s));

  // ── REVEAL ON SCROLL ──
  const reveals = document.querySelectorAll('.reveal');
  const revealObserver = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => entry.target.classList.add('visible'), i * 80);
        revealObserver.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(r => revealObserver.observe(r));

  // ── TABS ──
  function switchTab(index) {
    document.querySelectorAll('.tab-btn').forEach((b, i) => {
      b.classList.toggle('active', i === index);
    });
    document.querySelectorAll('.tab-content').forEach((c, i) => {
      c.classList.toggle('active', i === index);
    });
  }

  // ── SMOOTH SCROLL FOR NAV ──
  document.querySelectorAll('a[href^="#"]').forEach(a => {
    a.addEventListener('click', e => {
      e.preventDefault();
      const target = document.querySelector(a.getAttribute('href'));
      if (target) target.scrollIntoView({ behavior: 'smooth' });
    });
  });
</script>
</body>
</html>
