<!DOCTYPE html>
<html lang="fr">
<meta name="apple-mobile-web-app-title" content="TR Candidature">
<meta name="application-name" content="TR Candidature">
<link rel="icon" href="data:;base64,iVBORw0KGgo=">

<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<!-- AJOUTEZ ICI LES 3 LIGNES -->
<meta name="title" content="Candidature Directeur Commercial Serax">
<meta name="apple-mobile-web-app-title" content="TR Candidature">
<meta property="og:title" content="Candidature Directeur Commercial Serax">
<title>Vision Stratégique France — Terence Richard</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<!-- reste du code... -->
</head>


<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Vision Stratégique France — Terence Richard</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Jost:wght@200;300;400;500&display=swap" rel="stylesheet">
<style>
/* ═══════════════════════════════════════
   RESET & VARIABLES
═══════════════════════════════════════ */
*, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }
:root {
  --cream: #f5f0e8; --cream-dark: #ede6d6; --cream-mid: #f9f5ef;
  --sand: #c9b99a; --sand-light: #e2d8c8;
  --ink: #1a1714; --ink-soft: #3a3530; --ink-muted: #7a7268;
  --white: #fdfaf6;
  --nav-h: 54px;
}
html { scroll-behavior: smooth; }
body { background: var(--cream-mid); color: var(--ink); font-family: 'Jost', sans-serif; font-weight: 300; letter-spacing: 0.02em; overflow-x: hidden; }

/* ═══════════════════════════════════════
   ANNOUNCE BAR
═══════════════════════════════════════ */
.announce {
  background: var(--ink); color: var(--cream);
  text-align: center; font-size: 10.5px;
  letter-spacing: 0.18em; text-transform: uppercase;
  padding: 9px 20px; font-weight: 400;
  white-space: nowrap; overflow: hidden; text-overflow: ellipsis;
}
.announce em { color: var(--sand); font-style: normal; }

/* ═══════════════════════════════════════
   TOP BAR (desktop only)
═══════════════════════════════════════ */
.topbar {
  height: 36px; background: var(--cream-mid);
  border-bottom: 1px solid var(--sand-light);
  display: flex; align-items: center;
  justify-content: flex-end; padding: 0 48px; gap: 28px;
}
.topbar-item {
  font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase;
  color: var(--ink-muted); text-decoration: none; cursor: pointer;
  transition: color 0.2s; display: flex; align-items: center; gap: 5px;
}
.topbar-item:hover { color: var(--ink); }
.topbar-item svg { width: 12px; height: 12px; }
.topbar-langs { display: flex; gap: 1px; font-size: 10px; letter-spacing: 0.14em; text-transform: uppercase; }
.topbar-langs span { color: var(--ink-muted); padding: 2px 5px; cursor: pointer; transition: color 0.2s; }
.topbar-langs span.active, .topbar-langs span:hover { color: var(--ink); }
.topbar-langs .sep { color: var(--sand-light); display: flex; align-items: center; }

/* ═══════════════════════════════════════
   NAVBAR — DESKTOP
═══════════════════════════════════════ */
.sticky-header { position: sticky; top: 0; z-index: 1000; }

.navbar {
  height: var(--nav-h); background: var(--cream-mid);
  border-bottom: 1px solid var(--sand-light);
  display: grid; grid-template-columns: 1fr auto 1fr;
  align-items: center; padding: 0 48px;
  position: relative; transition: box-shadow 0.3s;
}
.navbar.scrolled { box-shadow: 0 2px 32px rgba(26,23,20,0.08); }
.nav-left { display: flex; align-items: center; }
.nav-right { display: flex; align-items: center; justify-content: flex-end; gap: 2px; }
.logo {
  font-family: 'Cormorant Garamond', serif; font-size: 21px;
  font-weight: 500; letter-spacing: 0.32em; text-transform: uppercase;
  color: var(--ink); text-decoration: none;
}

.nav-item { position: relative; height: var(--nav-h); display: flex; align-items: center; }
.nav-link {
  font-size: 10.5px; letter-spacing: 0.16em; text-transform: uppercase;
  color: var(--ink-soft); text-decoration: none; padding: 0 14px;
  height: 100%; display: flex; align-items: center; cursor: pointer;
  transition: color 0.22s; white-space: nowrap; font-weight: 400;
  border: none; background: none; position: relative;
}
.nav-link:hover, .nav-item.open .nav-link { color: var(--ink); }
.nav-link::after {
  content: ''; position: absolute; bottom: 0; left: 14px; right: 14px;
  height: 1.5px; background: var(--ink);
  transform: scaleX(0); transform-origin: left;
  transition: transform 0.3s cubic-bezier(0.4,0,0.2,1);
}
.nav-item:hover .nav-link::after, .nav-item.open .nav-link::after { transform: scaleX(1); }

.icon-btn {
  width: 40px; height: var(--nav-h); display: flex;
  align-items: center; justify-content: center;
  cursor: pointer; color: var(--ink-soft);
  transition: color 0.2s; text-decoration: none;
}
.icon-btn:hover { color: var(--ink); }
.icon-btn svg { width: 17px; height: 17px; stroke-width: 1.4; }

/* Hamburger (hidden on desktop) */
.hamburger {
  display: none; flex-direction: column; justify-content: center;
  align-items: center; gap: 5px; cursor: pointer;
  width: 40px; height: var(--nav-h); border: none; background: none;
  padding: 0; z-index: 1001;
}
.hamburger span {
  display: block; width: 22px; height: 1.5px;
  background: var(--ink); transition: all 0.3s ease;
  transform-origin: center;
}
.hamburger.open span:nth-child(1) { transform: translateY(6.5px) rotate(45deg); }
.hamburger.open span:nth-child(2) { opacity: 0; transform: scaleX(0); }
.hamburger.open span:nth-child(3) { transform: translateY(-6.5px) rotate(-45deg); }

/* ═══════════════════════════════════════
   MEGA MENU — DESKTOP
═══════════════════════════════════════ */
.mega-wrapper { position: absolute; top: 100%; left: 0; right: 0; z-index: 999; }
.mega-menu {
  background: var(--white);
  border-top: 1px solid var(--sand-light);
  border-bottom: 1px solid var(--sand-light);
  box-shadow: 0 12px 48px rgba(26,23,20,0.1);
  opacity: 0; transform: translateY(-8px);
  transition: opacity 0.28s ease, transform 0.28s ease;
  pointer-events: none; display: none;
}
.mega-menu.active { opacity: 1; transform: translateY(0); pointer-events: all; display: block; }
.mega-inner {
  max-width: 1280px; margin: 0 auto;
  padding: 44px 48px 48px; display: grid;
}
.mega-col-title {
  font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase;
  color: var(--ink-muted); margin-bottom: 16px; padding-bottom: 10px;
  border-bottom: 1px solid var(--sand-light); font-weight: 400;
}
.mega-col-links { list-style: none; display: flex; flex-direction: column; gap: 10px; }
.mega-col-links a {
  font-size: 12.5px; letter-spacing: 0.06em; color: var(--ink-soft);
  text-decoration: none; transition: color 0.2s, padding-left 0.2s;
  display: block; font-weight: 300;
}
.mega-col-links a:hover { color: var(--ink); padding-left: 4px; }
.mega-see-all {
  display: inline-block; margin-top: 16px; font-size: 10px;
  letter-spacing: 0.18em; text-transform: uppercase; color: var(--ink-muted);
  text-decoration: none; border-bottom: 1px solid var(--sand);
  padding-bottom: 2px; transition: color 0.2s, border-color 0.2s;
}
.mega-see-all:hover { color: var(--ink); border-color: var(--ink); }

/* Backdrop */
.menu-overlay {
  position: fixed; inset: 0; background: rgba(26,23,20,0.18);
  backdrop-filter: blur(1px); z-index: 998;
  opacity: 0; pointer-events: none; transition: opacity 0.28s;
}
.menu-overlay.active { opacity: 1; pointer-events: all; }

/* ═══════════════════════════════════════
   MOBILE DRAWER
═══════════════════════════════════════ */
.mobile-drawer {
  position: fixed; top: 0; right: 0; bottom: 0;
  width: min(85vw, 340px);
  background: var(--white);
  z-index: 1002;
  transform: translateX(100%);
  transition: transform 0.38s cubic-bezier(0.4,0,0.2,1);
  overflow-y: auto;
  display: flex; flex-direction: column;
  box-shadow: -8px 0 40px rgba(26,23,20,0.12);
}
.mobile-drawer.open { transform: translateX(0); }

.drawer-header {
  display: flex; align-items: center; justify-content: space-between;
  padding: 20px 24px; border-bottom: 1px solid var(--sand-light);
}
.drawer-logo {
  font-family: 'Cormorant Garamond', serif; font-size: 20px;
  font-weight: 500; letter-spacing: 0.3em; color: var(--ink);
}
.drawer-close {
  width: 36px; height: 36px; display: flex;
  align-items: center; justify-content: center;
  border: none; background: none; cursor: pointer; color: var(--ink-muted);
  transition: color 0.2s;
}
.drawer-close:hover { color: var(--ink); }
.drawer-close svg { width: 18px; height: 18px; }

.drawer-nav { flex: 1; padding: 8px 0; }
.drawer-section { border-bottom: 1px solid var(--sand-light); }

.drawer-item {
  display: flex; align-items: center; justify-content: space-between;
  padding: 16px 24px; cursor: pointer;
  font-size: 11px; letter-spacing: 0.18em; text-transform: uppercase;
  color: var(--ink-soft); font-weight: 400;
  transition: background 0.2s, color 0.2s;
  border: none; background: none; width: 100%; text-align: left;
}
.drawer-item:hover { background: var(--cream-mid); color: var(--ink); }
.drawer-item svg { width: 14px; height: 14px; transition: transform 0.3s; flex-shrink: 0; }
.drawer-item.expanded svg { transform: rotate(180deg); }

.drawer-sub {
  max-height: 0; overflow: hidden;
  transition: max-height 0.35s ease;
  background: var(--cream-mid);
}
.drawer-sub.open { max-height: 500px; }
.drawer-sub a {
  display: block; padding: 12px 24px 12px 36px;
  font-size: 12.5px; color: var(--ink-muted);
  text-decoration: none; font-weight: 300;
  letter-spacing: 0.04em;
  transition: color 0.2s, padding-left 0.2s;
}
.drawer-sub a:hover { color: var(--ink); padding-left: 40px; }
.drawer-sub-title {
  padding: 10px 24px 6px 36px;
  font-size: 9.5px; letter-spacing: 0.2em;
  text-transform: uppercase; color: var(--sand); font-weight: 400;
  margin-top: 4px;
}

.drawer-footer {
  padding: 24px; border-top: 1px solid var(--sand-light);
  display: flex; gap: 16px;
}
.drawer-footer a {
  flex: 1; text-align: center; padding: 12px;
  font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase;
  color: var(--ink-muted); text-decoration: none; border: 1px solid var(--sand-light);
  transition: all 0.2s; font-weight: 400;
}
.drawer-footer a:hover { border-color: var(--ink); color: var(--ink); }
.drawer-footer a.primary { background: var(--ink); color: var(--cream); border-color: var(--ink); }
.drawer-footer a.primary:hover { background: var(--ink-soft); }

/* Drawer backdrop */
.drawer-overlay {
  position: fixed; inset: 0; background: rgba(26,23,20,0.3);
  z-index: 1001; opacity: 0; pointer-events: none; transition: opacity 0.3s;
}
.drawer-overlay.open { opacity: 1; pointer-events: all; }

/* ═══════════════════════════════════════
   HERO
═══════════════════════════════════════ */
.hero { min-height: 92vh; display: grid; grid-template-columns: 1fr 1fr; }
.hero-visual { background: var(--cream-dark); position: relative; overflow: hidden; }
.hero-pattern {
  position: absolute; inset: 0;
  background:
    repeating-linear-gradient(45deg,transparent,transparent 40px,rgba(201,185,154,0.12) 40px,rgba(201,185,154,0.12) 41px),
    repeating-linear-gradient(-45deg,transparent,transparent 40px,rgba(201,185,154,0.08) 40px,rgba(201,185,154,0.08) 41px);
}
.hero-monogram {
  position: absolute; top: 50%; left: 50%;
  transform: translate(-50%,-50%);
  font-family: 'Cormorant Garamond', serif; font-size: 260px;
  font-weight: 300; color: rgba(201,185,154,0.2);
  line-height: 1; user-select: none;
  animation: fadeIn 1.2s ease both;
}
.hero-label {
  position: absolute; bottom: 48px; left: 48px;
  writing-mode: vertical-lr; text-orientation: mixed;
  transform: rotate(180deg);
  font-size: 10px; letter-spacing: 0.24em; text-transform: uppercase;
  color: var(--ink-muted);
}
.hero-content {
  background: var(--white); display: flex; flex-direction: column;
  justify-content: center; padding: 80px 72px 80px 64px;
  animation: slideUp 0.9s 0.2s ease both;
}
.hero-eyebrow { font-size: 10px; letter-spacing: 0.28em; text-transform: uppercase; color: var(--sand); margin-bottom: 24px; font-weight: 400; }
.hero-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(36px, 4.5vw, 62px); font-weight: 400; line-height: 1.08; color: var(--ink); margin-bottom: 12px; }
.hero-title em { font-style: italic; font-weight: 300; color: var(--ink-soft); }
.hero-subtitle { font-family: 'Cormorant Garamond', serif; font-size: 18px; font-weight: 300; color: var(--ink-muted); letter-spacing: 0.08em; margin-bottom: 36px; font-style: italic; }
.hero-divider { width: 48px; height: 1px; background: var(--sand); margin-bottom: 32px; }
.hero-intro { font-size: 14.5px; line-height: 1.85; color: var(--ink-soft); margin-bottom: 48px; max-width: 420px; font-weight: 300; }
.hero-cta { display: inline-flex; align-items: center; gap: 14px; font-size: 10.5px; letter-spacing: 0.2em; text-transform: uppercase; color: var(--ink); text-decoration: none; font-weight: 400; cursor: pointer; transition: gap 0.3s; }
.hero-cta:hover { gap: 20px; }
.hero-cta-line { width: 32px; height: 1px; background: var(--ink); display: inline-block; transition: width 0.3s; }
.hero-cta:hover .hero-cta-line { width: 48px; }

/* ═══════════════════════════════════════
   SECTIONS — COMMONS
═══════════════════════════════════════ */
.section { padding: 88px 0; }
.section-inner { max-width: 1200px; margin: 0 auto; padding: 0 48px; }
.section-header { margin-bottom: 52px; }
.section-tag { font-size: 10px; letter-spacing: 0.28em; text-transform: uppercase; color: var(--sand); margin-bottom: 14px; display: block; font-weight: 400; }
.section-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(26px, 3vw, 40px); font-weight: 400; line-height: 1.12; color: var(--ink); }
.section-title em { font-style: italic; font-weight: 300; }

/* ═══════════════════════════════════════
   PROFIL
═══════════════════════════════════════ */
.profil-section { background: var(--white); }
.profil-grid { display: grid; grid-template-columns: 1fr 2px 1fr; gap: 64px; align-items: start; }
.profil-div-v { background: var(--sand-light); }
.profil-text { font-size: 15px; line-height: 1.9; color: var(--ink-soft); font-weight: 300; }
.profil-text p + p { margin-top: 16px; }
.tags { display: flex; flex-wrap: wrap; gap: 10px; margin-top: 32px; }
.tag { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; border: 1px solid var(--sand); color: var(--ink-muted); padding: 7px 14px; font-weight: 400; transition: all 0.2s; cursor: default; }
.tag:hover { border-color: var(--ink); color: var(--ink); }
.stats-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light); }
.stat-card { background: var(--white); padding: 30px 24px; transition: background 0.2s; cursor: default; }
.stat-card:hover { background: var(--cream-mid); }
.stat-num { font-family: 'Cormorant Garamond', serif; font-size: 48px; font-weight: 300; color: var(--ink); line-height: 1; margin-bottom: 8px; }
.stat-num sup { font-size: 22px; }
.stat-label { font-size: 10px; letter-spacing: 0.16em; text-transform: uppercase; color: var(--ink-muted); line-height: 1.4; font-weight: 400; }

/* ═══════════════════════════════════════
   MARCHÉ
═══════════════════════════════════════ */
.marche-section { background: var(--cream-mid); }
.marche-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light); }
.marche-card { background: var(--white); padding: 40px 32px; position: relative; overflow: hidden; cursor: default; transition: background 0.25s; }
.marche-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 3px; background: var(--sand); transform: scaleX(0); transform-origin: left; transition: transform 0.35s ease; }
.marche-card:hover { background: var(--cream-mid); }
.marche-card:hover::before { transform: scaleX(1); }
.marche-icon { width: 38px; height: 38px; margin-bottom: 22px; color: var(--sand); }
.marche-icon svg { width: 100%; height: 100%; stroke-width: 1; }
.marche-card-title { font-family: 'Cormorant Garamond', serif; font-size: 22px; font-weight: 400; color: var(--ink); margin-bottom: 12px; }
.marche-card-text { font-size: 13px; line-height: 1.8; color: var(--ink-muted); font-weight: 300; }
.marche-list { list-style: none; margin-top: 14px; display: flex; flex-direction: column; gap: 7px; }
.marche-list li { font-size: 12.5px; color: var(--ink-soft); padding-left: 14px; position: relative; font-weight: 300; }
.marche-list li::before { content: '—'; position: absolute; left: 0; color: var(--sand); font-size: 10px; }

/* ═══════════════════════════════════════
   STRATÉGIE
═══════════════════════════════════════ */
.strategie-section { background: var(--ink); color: var(--cream); }
.strategie-section .section-title { color: var(--cream); }
.axes-grid { display: grid; grid-template-columns: repeat(3,1fr); gap: 1px; background: rgba(201,185,154,0.2); border: 1px solid rgba(201,185,154,0.2); }
.axe-card { background: var(--ink); padding: 48px 36px; position: relative; overflow: hidden; transition: background 0.25s; cursor: default; }
.axe-card:hover { background: #262219; }
.axe-num { font-family: 'Cormorant Garamond', serif; font-size: 80px; font-weight: 300; color: rgba(201,185,154,0.12); line-height: 1; position: absolute; top: 20px; right: 24px; transition: color 0.3s; }
.axe-card:hover .axe-num { color: rgba(201,185,154,0.22); }
.axe-tag { font-size: 10px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--sand); margin-bottom: 16px; display: block; font-weight: 400; }
.axe-title { font-family: 'Cormorant Garamond', serif; font-size: 22px; font-weight: 400; color: var(--cream); margin-bottom: 16px; line-height: 1.2; }
.axe-text { font-size: 13px; line-height: 1.8; color: rgba(245,240,232,0.6); font-weight: 300; }
.axe-list { list-style: none; margin-top: 18px; display: flex; flex-direction: column; gap: 8px; }
.axe-list li { font-size: 12.5px; color: rgba(245,240,232,0.6); padding-left: 16px; position: relative; font-weight: 300; }
.axe-list li::before { content: ''; position: absolute; left: 0; top: 9px; width: 6px; height: 1px; background: var(--sand); }

/* ═══════════════════════════════════════
   PLAN 90 JOURS
═══════════════════════════════════════ */
.plan-section { background: var(--cream-mid); }
.plan-timeline { display: grid; grid-template-columns: repeat(3,1fr); position: relative; }
.plan-timeline::before { content: ''; position: absolute; top: 32px; left: 16.6%; right: 16.6%; height: 1px; background: var(--sand-light); }
.plan-phase { padding: 0 28px 40px; text-align: center; }
.plan-dot { width: 64px; height: 64px; border-radius: 50%; border: 1px solid var(--sand-light); background: var(--white); display: flex; align-items: center; justify-content: center; margin: 0 auto 24px; font-family: 'Cormorant Garamond', serif; font-size: 20px; font-weight: 400; color: var(--sand); position: relative; z-index: 1; transition: all 0.3s; }
.plan-phase:hover .plan-dot { background: var(--ink); border-color: var(--ink); color: var(--cream); }
.plan-period { font-size: 10px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--sand); margin-bottom: 10px; font-weight: 400; }
.plan-phase-title { font-family: 'Cormorant Garamond', serif; font-size: 20px; font-weight: 400; color: var(--ink); margin-bottom: 16px; }
.plan-items { list-style: none; text-align: left; display: flex; flex-direction: column; gap: 9px; }
.plan-items li { font-size: 13px; color: var(--ink-soft); padding-left: 18px; position: relative; font-weight: 300; line-height: 1.6; }
.plan-items li::before { content: '—'; position: absolute; left: 0; color: var(--sand); font-size: 10px; top: 2px; }

/* ═══════════════════════════════════════
   VISION QUOTE
═══════════════════════════════════════ */
.vision-section { background: var(--cream-dark); padding: 100px 0; }
.vision-inner { max-width: 860px; margin: 0 auto; padding: 0 48px; text-align: center; }
.vision-quote { font-family: 'Cormorant Garamond', serif; font-size: clamp(22px, 3.5vw, 40px); font-weight: 300; font-style: italic; line-height: 1.5; color: var(--ink); margin-bottom: 36px; position: relative; padding-top: 20px; }
.vision-quote::before { content: '\201C'; font-size: 100px; color: rgba(201,185,154,0.35); position: absolute; top: -20px; left: -10px; line-height: 1; font-family: 'Cormorant Garamond', serif; }
.vision-divider { width: 40px; height: 1px; background: var(--sand); margin: 18px auto; }
.vision-author { font-size: 11px; letter-spacing: 0.24em; text-transform: uppercase; color: var(--ink-muted); font-weight: 400; }

/* ═══════════════════════════════════════
   LEADERSHIP
═══════════════════════════════════════ */
.leadership-section { background: var(--white); }
.lead-grid { display: grid; grid-template-columns: repeat(4,1fr); gap: 1px; background: var(--sand-light); border: 1px solid var(--sand-light); }
.lead-card { background: var(--white); padding: 36px 28px; text-align: center; transition: background 0.25s; cursor: default; }
.lead-card:hover { background: var(--cream-mid); }
.lead-icon { width: 44px; height: 44px; margin: 0 auto 18px; color: var(--sand); }
.lead-icon svg { width: 100%; height: 100%; stroke-width: 1; }
.lead-title { font-family: 'Cormorant Garamond', serif; font-size: 18px; font-weight: 400; color: var(--ink); margin-bottom: 10px; }
.lead-text { font-size: 12.5px; line-height: 1.75; color: var(--ink-muted); font-weight: 300; }

/* ═══════════════════════════════════════
   CONTACT
═══════════════════════════════════════ */
.contact-section { background: var(--cream-dark); padding: 88px 0; }
.contact-inner { max-width: 680px; margin: 0 auto; padding: 0 48px; text-align: center; }
.contact-title { font-family: 'Cormorant Garamond', serif; font-size: clamp(28px,4vw,38px); font-weight: 400; color: var(--ink); margin-bottom: 16px; }
.contact-sub { font-size: 14px; color: var(--ink-muted); margin-bottom: 44px; line-height: 1.7; font-weight: 300; }
.contact-info { display: flex; justify-content: center; gap: 40px; flex-wrap: wrap; margin-bottom: 8px; }
.contact-item-label { font-size: 9.5px; letter-spacing: 0.22em; text-transform: uppercase; color: var(--sand); margin-bottom: 5px; font-weight: 400; }
.contact-item-value { font-size: 14px; color: var(--ink); font-weight: 300; }
.btn-primary { display: inline-block; margin-top: 36px; background: var(--ink); color: var(--cream); font-size: 10.5px; letter-spacing: 0.22em; text-transform: uppercase; padding: 16px 40px; text-decoration: none; font-weight: 400; transition: background 0.25s, letter-spacing 0.3s; }
.btn-primary:hover { background: var(--ink-soft); letter-spacing: 0.28em; }

/* ═══════════════════════════════════════
   FOOTER
═══════════════════════════════════════ */
.footer { background: var(--ink); color: rgba(245,240,232,0.6); padding: 56px 48px 28px; }
.footer-grid { max-width: 1200px; margin: 0 auto; display: grid; grid-template-columns: 1.5fr 1fr 1fr 1fr; gap: 40px; padding-bottom: 40px; border-bottom: 1px solid rgba(201,185,154,0.15); margin-bottom: 28px; }
.footer-logo { font-family: 'Cormorant Garamond', serif; font-size: 20px; font-weight: 500; letter-spacing: 0.28em; color: var(--cream); display: block; margin-bottom: 14px; }
.footer-tagline { font-size: 12px; line-height: 1.7; color: rgba(245,240,232,0.45); font-weight: 300; max-width: 220px; }
.footer-col-title { font-size: 10px; letter-spacing: 0.2em; text-transform: uppercase; color: var(--sand); margin-bottom: 16px; font-weight: 400; }
.footer-links { list-style: none; display: flex; flex-direction: column; gap: 10px; }
.footer-links a { font-size: 12.5px; color: rgba(245,240,232,0.55); text-decoration: none; transition: color 0.2s; font-weight: 300; }
.footer-links a:hover { color: var(--cream); }
.footer-bottom { max-width: 1200px; margin: 0 auto; display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 8px; }
.footer-copy { font-size: 10.5px; color: rgba(245,240,232,0.3); letter-spacing: 0.1em; }
.footer-year { font-family: 'Cormorant Garamond', serif; color: var(--sand); font-size: 13px; }

/* ═══════════════════════════════════════
   SCROLL REVEAL
═══════════════════════════════════════ */
.reveal { opacity: 0; transform: translateY(20px); transition: opacity 0.7s ease, transform 0.7s ease; }
.reveal.visible { opacity: 1; transform: none; }

@keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
@keyframes slideUp { from { opacity: 0; transform: translateY(28px); } to { opacity: 1; transform: none; } }

/* ═══════════════════════════════════════
   RESPONSIVE — TABLET (≤ 1024px)
═══════════════════════════════════════ */
@media (max-width: 1024px) {
  .topbar { display: none; }
  .navbar { padding: 0 24px; grid-template-columns: auto 1fr auto; }
  .nav-left, .nav-right { display: none; }
  .hamburger { display: flex; }
  .logo { font-size: 19px; }

  .hero { grid-template-columns: 1fr; min-height: auto; }
  .hero-visual { min-height: 280px; }
  .hero-monogram { font-size: 180px; }
  .hero-label { display: none; }
  .hero-content { padding: 56px 40px; }

  .profil-grid { grid-template-columns: 1fr; gap: 40px; }
  .profil-div-v { display: none; }

  .marche-grid { grid-template-columns: 1fr 1fr; }
  .marche-grid .marche-card:last-child { grid-column: 1 / -1; }

  .axes-grid { grid-template-columns: 1fr; }
  .axe-card { padding: 40px 32px; }

  .plan-timeline { grid-template-columns: 1fr; }
  .plan-timeline::before { display: none; }
  .plan-phase { padding: 0 0 32px; text-align: left; display: grid; grid-template-columns: 64px 1fr; gap: 0 20px; align-items: start; }
  .plan-dot { margin: 0; }
  .plan-period { grid-column: 2; }
  .plan-phase-title { grid-column: 2; }
  .plan-items { grid-column: 2; }

  .lead-grid { grid-template-columns: 1fr 1fr; }

  .footer-grid { grid-template-columns: 1fr 1fr; }
  .section-inner { padding: 0 32px; }
  .section { padding: 64px 0; }
}

/* ═══════════════════════════════════════
   RESPONSIVE — MOBILE (≤ 640px)
═══════════════════════════════════════ */
@media (max-width: 640px) {
  .announce { font-size: 9.5px; letter-spacing: 0.12em; padding: 8px 16px; }

  .navbar { padding: 0 16px; }
  .logo { font-size: 18px; letter-spacing: 0.24em; }

  .hero-visual { min-height: 200px; }
  .hero-monogram { font-size: 120px; }
  .hero-content { padding: 40px 24px 48px; }
  .hero-eyebrow { font-size: 9.5px; }
  .hero-intro { font-size: 13.5px; margin-bottom: 36px; }
  .hero-subtitle { font-size: 16px; }

  .section { padding: 52px 0; }
  .section-inner { padding: 0 20px; }
  .section-header { margin-bottom: 36px; }

  .profil-text { font-size: 14px; }
  .stats-grid { grid-template-columns: 1fr 1fr; }
  .stat-num { font-size: 40px; }

  .marche-grid { grid-template-columns: 1fr; }
  .marche-grid .marche-card:last-child { grid-column: auto; }
  .marche-card { padding: 32px 24px; }

  .axe-card { padding: 36px 24px; }
  .axe-num { font-size: 60px; }

  .plan-phase { grid-template-columns: 48px 1fr; gap: 0 16px; }
  .plan-dot { width: 48px; height: 48px; font-size: 16px; }

  .vision-section { padding: 64px 0; }
  .vision-inner { padding: 0 24px; }
  .vision-quote::before { font-size: 72px; left: -4px; }

  .lead-grid { grid-template-columns: 1fr; }
  .lead-card { padding: 28px 24px; text-align: left; display: flex; gap: 18px; align-items: flex-start; }
  .lead-icon { flex-shrink: 0; margin: 0; }

  .contact-section { padding: 56px 0; }
  .contact-inner { padding: 0 20px; }
  .contact-info { flex-direction: column; gap: 20px; align-items: center; }

  .footer { padding: 44px 20px 24px; }
  .footer-grid { grid-template-columns: 1fr; gap: 32px; padding-bottom: 32px; }
  .footer-tagline { max-width: 100%; }
  .footer-bottom { flex-direction: column; text-align: center; gap: 6px; }

  .btn-primary { padding: 14px 32px; font-size: 10px; }
}

/* ═══════════════════════════════════════
   RESPONSIVE — VERY SMALL (≤ 380px)
═══════════════════════════════════════ */
@media (max-width: 380px) {
  .hero-monogram { font-size: 90px; }
  .stats-grid { grid-template-columns: 1fr; }
  .tags { gap: 8px; }
  .tag { font-size: 9.5px; padding: 6px 12px; }
}
</style>
</head>
<body>

<!-- ─── ANNOUNCE ─── -->
<div class="announce">
  Candidature &nbsp;·&nbsp; Directeur Commercial France &nbsp;·&nbsp; <em>Terence Richard</em>
</div>

<!-- ─── STICKY HEADER ─── -->
<div class="sticky-header">
  <!-- TOP BAR (desktop only) -->
  <div class="topbar">
    <div class="topbar-langs">
      <span class="active">FR</span><span class="sep">·</span><span>EN</span>
    </div>
    <a href="#contact" class="topbar-item">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
      Contact
    </a>
    <a href="#" class="topbar-item">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6z"/><rect x="2" y="9" width="4" height="12"/><circle cx="4" cy="4" r="2"/></svg>
      LinkedIn
    </a>
  </div>

  <!-- NAVBAR -->
  <nav class="navbar" id="navbar">
    <!-- Desktop left nav -->
    <div class="nav-left">
      <div class="nav-item" id="item-vision">
        <button class="nav-link" onclick="toggleMenu('vision')">Vision stratégique</button>
      </div>
      <div class="nav-item" id="item-marche">
        <button class="nav-link" onclick="toggleMenu('marche')">Le Marché</button>
      </div>
      <div class="nav-item" id="item-plan">
        <button class="nav-link" onclick="toggleMenu('plan')">Plan d'action</button>
      </div>
    </div>

    <!-- Mobile hamburger (left) -->
    <button class="hamburger" id="hamburger" onclick="toggleDrawer()" aria-label="Menu">
      <span></span><span></span><span></span>
    </button>

    <!-- Logo center -->
    <a href="#hero" class="logo" style="text-align:center;">TR</a>

    <!-- Desktop right nav -->
    <div class="nav-right">
      <div class="nav-item" id="item-profil">
        <button class="nav-link" onclick="toggleMenu('profil')">Mon Profil</button>
      </div>
      <div class="nav-item" id="item-apropos">
        <button class="nav-link" onclick="toggleMenu('apropos')">À Propos</button>
      </div>
      <a href="#contact" class="icon-btn" title="Contact">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
      </a>
    </div>

    <!-- Desktop mega menus -->
    <div class="mega-wrapper">

      <!-- Vision -->
      <div class="mega-menu" id="mega-vision">
        <div class="mega-inner" style="grid-template-columns:repeat(3,1fr);gap:0;">
          <div style="border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">Axes principaux</div>
            <ul class="mega-col-links">
              <li><a href="#strategie" onclick="closeAllMenus()">Activation de l'écosystème</a></li>
              <li><a href="#strategie" onclick="closeAllMenus()">Développement de partenariats</a></li>
              <li><a href="#strategie" onclick="closeAllMenus()">Renforcement de la visibilité</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">Segments cibles</div>
            <ul class="mega-col-links">
              <li><a href="#marche" onclick="closeAllMenus()">Hospitality & Hôtellerie</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Architectes & Designers</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Retail premium</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Corporate gifting</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;">
            <div class="mega-col-title">Vision à moyen terme</div>
            <ul class="mega-col-links">
              <li><a href="#vision" onclick="closeAllMenus()">Référence hospitality France</a></li>
              <li><a href="#vision" onclick="closeAllMenus()">Réseau de prescripteurs</a></li>
              <li><a href="#vision" onclick="closeAllMenus()">Présence retail premium</a></li>
            </ul>
            <a href="#strategie" class="mega-see-all" onclick="closeAllMenus()">Voir la stratégie complète</a>
          </div>
        </div>
      </div>

      <!-- Marché -->
      <div class="mega-menu" id="mega-marche">
        <div class="mega-inner" style="grid-template-columns:200px 1fr 1fr;gap:0 44px;">
          <div style="background:var(--cream-dark);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:10px;padding:28px;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:58px;color:var(--sand);opacity:0.5;line-height:1;">FR</div>
            <div style="font-size:10px;letter-spacing:0.18em;text-transform:uppercase;color:var(--ink-muted);text-align:center;">Marché Français</div>
          </div>
          <div>
            <div class="mega-col-title">Écosystèmes clés</div>
            <ul class="mega-col-links">
              <li><a href="#marche" onclick="closeAllMenus()">Gastronomie & Restauration</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Hôtellerie de luxe</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Architecture & Design</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Lifestyle premium</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Réseaux prioritaires</div>
            <ul class="mega-col-links">
              <li><a href="#marche" onclick="closeAllMenus()">Architectes d'intérieur</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Groupes hôteliers</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Concept stores design</a></li>
              <li><a href="#marche" onclick="closeAllMenus()">Promoteurs immobiliers</a></li>
            </ul>
          </div>
        </div>
      </div>

      <!-- Plan -->
      <div class="mega-menu" id="mega-plan">
        <div class="mega-inner" style="grid-template-columns:repeat(3,1fr);gap:0;">
          <div style="border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">0 – 30 jours</div>
            <ul class="mega-col-links">
              <li><a href="#plan" onclick="closeAllMenus()">Phase d'écoute</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Analyse de l'équipe</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Comptes clés existants</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;border-right:1px solid var(--sand-light);padding-right:44px;">
            <div class="mega-col-title">30 – 60 jours</div>
            <ul class="mega-col-links">
              <li><a href="#plan" onclick="closeAllMenus()">Identification des priorités</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Comptes stratégiques</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Activation quick wins</a></li>
            </ul>
          </div>
          <div style="padding-left:44px;">
            <div class="mega-col-title">60 – 90 jours</div>
            <ul class="mega-col-links">
              <li><a href="#plan" onclick="closeAllMenus()">Feuille de route</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Lancement des initiatives</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">KPIs & objectifs</a></li>
            </ul>
            <a href="#plan" class="mega-see-all" onclick="closeAllMenus()">Voir le plan complet</a>
          </div>
        </div>
      </div>

      <!-- Profil -->
      <div class="mega-menu" id="mega-profil">
        <div class="mega-inner" style="grid-template-columns:200px 1fr 1fr;gap:0 44px;">
          <div style="background:var(--cream-dark);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:10px;padding:28px;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:52px;color:var(--sand);font-weight:300;line-height:1;">20+</div>
            <div style="width:28px;height:1px;background:var(--sand);"></div>
            <div style="font-size:10px;letter-spacing:0.16em;text-transform:uppercase;color:var(--ink-muted);text-align:center;line-height:1.6;">Années d'exp.<br>B2B</div>
          </div>
          <div>
            <div class="mega-col-title">Expériences</div>
            <ul class="mega-col-links">
              <li><a href="#profil" onclick="closeAllMenus()">Management commercial</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Pilotage de P&L</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Comptes stratégiques</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Distribution premium</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Atouts clés</div>
            <ul class="mega-col-links">
              <li><a href="#profil" onclick="closeAllMenus()">Structuration de marchés</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Activation d'écosystèmes</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Réseau prescripteurs</a></li>
            </ul>
            <a href="#profil" class="mega-see-all" onclick="closeAllMenus()">Voir le profil complet</a>
          </div>
        </div>
      </div>

      <!-- À propos -->
      <div class="mega-menu" id="mega-apropos">
        <div class="mega-inner" style="grid-template-columns:200px 1fr 1fr;gap:0 44px;">
          <div style="background:var(--ink);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:12px;padding:28px;">
            <div style="font-family:'Cormorant Garamond',serif;font-size:26px;color:var(--cream);font-weight:400;letter-spacing:0.06em;text-align:center;line-height:1.3;">Terence<br>Richard</div>
            <div style="width:28px;height:1px;background:var(--sand);"></div>
            <div style="font-size:10px;letter-spacing:0.16em;text-transform:uppercase;color:var(--sand);">Dir. Commercial</div>
          </div>
          <div>
            <div class="mega-col-title">Candidature</div>
            <ul class="mega-col-links">
              <li><a href="#hero" onclick="closeAllMenus()">Introduction</a></li>
              <li><a href="#profil" onclick="closeAllMenus()">Mon profil</a></li>
              <li><a href="#strategie" onclick="closeAllMenus()">Vision stratégique</a></li>
              <li><a href="#plan" onclick="closeAllMenus()">Plan 90 jours</a></li>
            </ul>
          </div>
          <div>
            <div class="mega-col-title">Contact</div>
            <ul class="mega-col-links">
              <li><a href="#contact" onclick="closeAllMenus()">Coordonnées</a></li>
              <li><a href="#" onclick="closeAllMenus()">LinkedIn</a></li>
              <li><a href="#contact" onclick="closeAllMenus()">Envoyer un message</a></li>
            </ul>
            <a href="#contact" class="mega-see-all" onclick="closeAllMenus()">Prendre contact</a>
          </div>
        </div>
      </div>

    </div><!-- /mega-wrapper -->
  </nav>
</div>

<!-- Desktop backdrop -->
<div class="menu-overlay" id="overlay" onclick="closeAllMenus()"></div>

<!-- ─── MOBILE DRAWER ─── -->
<div class="drawer-overlay" id="drawerOverlay" onclick="toggleDrawer()"></div>
<div class="mobile-drawer" id="mobileDrawer">
  <div class="drawer-header">
    <span class="drawer-logo">TR</span>
    <button class="drawer-close" onclick="toggleDrawer()">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><line x1="18" y1="6" x2="6" y2="18"/><line x1="6" y1="6" x2="18" y2="18"/></svg>
    </button>
  </div>
  <nav class="drawer-nav">
    <!-- Vision -->
    <div class="drawer-section">
      <button class="drawer-item" onclick="toggleDrawerSub('sub-vision',this)">
        Vision stratégique
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="drawer-sub" id="sub-vision">
        <div class="drawer-sub-title">Axes</div>
        <a href="#strategie" onclick="closeDrawer()">Activation de l'écosystème</a>
        <a href="#strategie" onclick="closeDrawer()">Développement de partenariats</a>
        <a href="#strategie" onclick="closeDrawer()">Renforcement de la visibilité</a>
        <div class="drawer-sub-title">Objectifs</div>
        <a href="#vision" onclick="closeDrawer()">Référence hospitality France</a>
        <a href="#vision" onclick="closeDrawer()">Réseau de prescripteurs</a>
      </div>
    </div>
    <!-- Marché -->
    <div class="drawer-section">
      <button class="drawer-item" onclick="toggleDrawerSub('sub-marche',this)">
        Le Marché
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="drawer-sub" id="sub-marche">
        <div class="drawer-sub-title">Écosystèmes</div>
        <a href="#marche" onclick="closeDrawer()">Gastronomie & Restauration</a>
        <a href="#marche" onclick="closeDrawer()">Hôtellerie de luxe</a>
        <a href="#marche" onclick="closeDrawer()">Architecture & Design</a>
        <div class="drawer-sub-title">Réseaux</div>
        <a href="#marche" onclick="closeDrawer()">Architectes d'intérieur</a>
        <a href="#marche" onclick="closeDrawer()">Groupes hôteliers</a>
        <a href="#marche" onclick="closeDrawer()">Concept stores design</a>
      </div>
    </div>
    <!-- Plan -->
    <div class="drawer-section">
      <button class="drawer-item" onclick="toggleDrawerSub('sub-plan',this)">
        Plan d'action
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="drawer-sub" id="sub-plan">
        <a href="#plan" onclick="closeDrawer()">0–30 jours : Écoute & Analyse</a>
        <a href="#plan" onclick="closeDrawer()">30–60 jours : Priorisation</a>
        <a href="#plan" onclick="closeDrawer()">60–90 jours : Lancement</a>
      </div>
    </div>
    <!-- Profil -->
    <div class="drawer-section">
      <button class="drawer-item" onclick="toggleDrawerSub('sub-profil',this)">
        Mon Profil
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="drawer-sub" id="sub-profil">
        <a href="#profil" onclick="closeDrawer()">Expérience & compétences</a>
        <a href="#leadership" onclick="closeDrawer()">Approche de leadership</a>
        <a href="#profil" onclick="closeDrawer()">Atouts différenciants</a>
      </div>
    </div>
    <!-- À propos -->
    <div class="drawer-section">
      <button class="drawer-item" onclick="toggleDrawerSub('sub-apropos',this)">
        À Propos
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><polyline points="6 9 12 15 18 9"/></svg>
      </button>
      <div class="drawer-sub" id="sub-apropos">
        <a href="#hero" onclick="closeDrawer()">Introduction</a>
        <a href="#strategie" onclick="closeDrawer()">Vision stratégique</a>
        <a href="#contact" onclick="closeDrawer()">Contact</a>
      </div>
    </div>
  </nav>
  <div class="drawer-footer">
    <a href="#" >LinkedIn</a>
    <a href="#contact" class="primary" onclick="closeDrawer()">Contact</a>
  </div>
</div>

<!-- ═══════════════════════════════════════
     HERO
════════════════════════════════════════ -->
<section class="hero" id="hero">
  <div class="hero-visual">
    <div class="hero-pattern"></div>
    <div class="hero-monogram">TR</div>
    <div class="hero-label">Vision Stratégique · France · 2025</div>
  </div>
  <div class="hero-content">
    <span class="hero-eyebrow">Candidature — Directeur Commercial France</span>
    <h1 class="hero-title">Développement<br><em>de Serax</em><br>en France</h1>
    <p class="hero-subtitle">Terence Richard</p>
    <div class="hero-divider"></div>
    <p class="hero-intro">Serax occupe une position unique à l'intersection du design, de l'hospitality et du lifestyle premium. La France représente l'un des marchés les plus influents en Europe — un écosystème riche à structurer et à activer.</p>
    <a href="#profil" class="hero-cta">Découvrir la vision <span class="hero-cta-line"></span></a>
  </div>
</section>

<!-- ═══════════════════════════════════════
     PROFIL
════════════════════════════════════════ -->
<section class="section profil-section" id="profil">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-tag">Mon Profil</span>
      <h2 class="section-title">Dirigeant commercial<br><em>& développeur de marchés</em></h2>
    </div>
    <div class="profil-grid reveal">
      <div>
        <div class="profil-text">
          <p>Dirigeant commercial avec plus de vingt ans d'expérience en développement et structuration de marchés B2B en France et à l'international.</p>
          <p>Plus récemment, création et structuration d'une plateforme de distribution dans l'univers du mobilier premium avec activation d'un réseau d'architectes et de prescripteurs.</p>
        </div>
        <div class="tags">
          <span class="tag">Management commercial</span>
          <span class="tag">Pilotage P&L</span>
          <span class="tag">Comptes stratégiques</span>
          <span class="tag">Marchés premium</span>
          <span class="tag">Prescription</span>
          <span class="tag">Distribution sélective</span>
        </div>
      </div>
      <div class="profil-div-v"></div>
      <div>
        <div class="stats-grid">
          <div class="stat-card"><div class="stat-num">20<sup>+</sup></div><div class="stat-label">Années d'expérience B2B</div></div>
          <div class="stat-card"><div class="stat-num">3</div><div class="stat-label">Axes stratégiques France</div></div>
          <div class="stat-card"><div class="stat-num">90</div><div class="stat-label">Jours pour un plan concret</div></div>
          <div class="stat-card"><div class="stat-num">5</div><div class="stat-label">Segments à activer</div></div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     MARCHÉ
════════════════════════════════════════ -->
<section class="section marche-section" id="marche">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-tag">Le Marché Français</span>
      <h2 class="section-title">Un écosystème premium<br><em>à fort potentiel</em></h2>
    </div>
    <div class="marche-grid reveal">
      <div class="marche-card">
        <div class="marche-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M3 9l9-7 9 7v11a2 2 0 01-2 2H5a2 2 0 01-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg></div>
        <div class="marche-card-title">Hospitality</div>
        <div class="marche-card-text">Un secteur en plein essor, moteur de croissance pour Serax en France.</div>
        <ul class="marche-list">
          <li>Hôtels & palaces</li>
          <li>Restaurants & chefs étoilés</li>
          <li>Groupes de restauration</li>
        </ul>
      </div>
      <div class="marche-card">
        <div class="marche-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="10"/><path d="M12 2a14.5 14.5 0 000 20 14.5 14.5 0 000-20"/><line x1="2" y1="12" x2="22" y2="12"/></svg></div>
        <div class="marche-card-title">Prescription</div>
        <div class="marche-card-text">Les architectes et designers sont des relais d'influence essentiels.</div>
        <ul class="marche-list">
          <li>Architectes d'intérieur</li>
          <li>Studios de design</li>
          <li>Promoteurs immobiliers</li>
        </ul>
      </div>
      <div class="marche-card">
        <div class="marche-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M6 2L3 6v14a2 2 0 002 2h14a2 2 0 002-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 01-8 0"/></svg></div>
        <div class="marche-card-title">Retail Premium</div>
        <div class="marche-card-text">Une distribution sélective cohérente avec le positionnement Serax.</div>
        <ul class="marche-list">
          <li>Concept stores design</li>
          <li>Showrooms sélectifs</li>
          <li>Corners dédiés premium</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     STRATÉGIE
════════════════════════════════════════ -->
<section class="section strategie-section" id="strategie">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-tag">Stratégie de Développement</span>
      <h2 class="section-title">Trois axes<br><em>pour s'imposer</em></h2>
    </div>
    <div class="axes-grid reveal">
      <div class="axe-card">
        <span class="axe-num">01</span>
        <span class="axe-tag">Axe 1</span>
        <div class="axe-title">Activation de l'écosystème</div>
        <div class="axe-text">Identifier et activer tous les acteurs clés du marché français autour de Serax.</div>
        <ul class="axe-list">
          <li>Architectes & designers</li>
          <li>Hospitality & restaurants</li>
          <li>Retail premium</li>
          <li>Projets immobiliers</li>
        </ul>
      </div>
      <div class="axe-card">
        <span class="axe-num">02</span>
        <span class="axe-tag">Axe 2</span>
        <div class="axe-title">Développement de partenariats</div>
        <div class="axe-text">Construire des partenariats durables avec les acteurs premium du marché.</div>
        <ul class="axe-list">
          <li>Groupes hôteliers</li>
          <li>Restaurateurs & chefs</li>
          <li>Concept stores</li>
          <li>Promoteurs immobiliers</li>
        </ul>
      </div>
      <div class="axe-card">
        <span class="axe-num">03</span>
        <span class="axe-tag">Axe 3</span>
        <div class="axe-title">Renforcement de la visibilité</div>
        <div class="axe-text">Affirmer la présence de Serax dans l'univers créatif et professionnel français.</div>
        <ul class="axe-list">
          <li>Événements & salons</li>
          <li>Collaborations chefs & designers</li>
          <li>Réseaux professionnels</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     PLAN 90 JOURS
════════════════════════════════════════ -->
<section class="section plan-section" id="plan">
  <div class="section-inner">
    <div class="section-header reveal">
      <span class="section-tag">Plan d'Action</span>
      <h2 class="section-title">Les premiers<br><em>90 jours</em></h2>
    </div>
    <div class="plan-timeline reveal">
      <div class="plan-phase">
        <div class="plan-dot">1</div>
        <div class="plan-period">0 — 30 jours</div>
        <div class="plan-phase-title">Écoute & Analyse</div>
        <ul class="plan-items">
          <li>Phase d'écoute approfondie</li>
          <li>Analyse de l'équipe en place</li>
          <li>Audit des comptes clés</li>
          <li>Compréhension de la distribution et des partenaires existants</li>
        </ul>
      </div>
      <div class="plan-phase">
        <div class="plan-dot">2</div>
        <div class="plan-period">30 — 60 jours</div>
        <div class="plan-phase-title">Priorisation</div>
        <ul class="plan-items">
          <li>Identification des priorités stratégiques</li>
          <li>Sélection des comptes stratégiques</li>
          <li>Identification et activation des quick wins</li>
        </ul>
      </div>
      <div class="plan-phase">
        <div class="plan-dot">3</div>
        <div class="plan-period">60 — 90 jours</div>
        <div class="plan-phase-title">Lancement</div>
        <ul class="plan-items">
          <li>Construction d'une feuille de route structurée</li>
          <li>Lancement des initiatives prioritaires</li>
          <li>Mise en place des KPIs</li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     VISION QUOTE
════════════════════════════════════════ -->
<section class="vision-section" id="vision">
  <div class="vision-inner">
    <blockquote class="vision-quote reveal">
      Positionner Serax comme une référence incontournable dans l'univers hospitality et design en France.
    </blockquote>
    <div class="vision-divider"></div>
    <div class="vision-author">Terence Richard — Vision à moyen terme</div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     LEADERSHIP
════════════════════════════════════════ -->
<section class="section leadership-section" id="leadership">
  <div class="section-inner">
    <div class="section-header reveal" style="text-align:center;">
      <span class="section-tag" style="display:block;text-align:center;">Approche de Leadership</span>
      <h2 class="section-title" style="text-align:center;">Un management<br><em>orienté terrain</em></h2>
    </div>
    <div class="lead-grid reveal">
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><circle cx="12" cy="12" r="10"/><polyline points="12 6 12 12 16 14"/></svg></div>
        <div>
          <div class="lead-title">Clarté des objectifs</div>
          <div class="lead-text">Définir des priorités claires, mesurables et alignées avec la stratégie globale Serax.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M17 21v-2a4 4 0 00-4-4H5a4 4 0 00-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M23 21v-2a4 4 0 00-3-3.87"/><path d="M16 3.13a4 4 0 010 7.75"/></svg></div>
        <div>
          <div class="lead-title">Responsabilisation</div>
          <div class="lead-text">Accompagner l'équipe existante dans une culture de l'autonomie et de la performance.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg></div>
        <div>
          <div class="lead-title">Proximité terrain</div>
          <div class="lead-text">Un management ancré dans la réalité du marché, au contact direct des clients et partenaires.</div>
        </div>
      </div>
      <div class="lead-card">
        <div class="lead-icon"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor"><path d="M21 15a2 2 0 01-2 2H7l-4 4V5a2 2 0 012-2h14a2 2 0 012 2z"/></svg></div>
        <div>
          <div class="lead-title">Communication directe</div>
          <div class="lead-text">Favoriser la collaboration ouverte et la transparence à tous les niveaux de l'organisation.</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- ═══════════════════════════════════════
     CONTACT
════════════════════════════════════════ -->
<section class="contact-section" id="contact">
  <div class="contact-inner reveal">
    <h2 class="contact-title">Prenons contact</h2>
    <p class="contact-sub">Je suis disponible pour échanger sur cette opportunité et approfondir ensemble la vision stratégique pour Serax en France.</p>
    <div class="contact-info">
      <div class="contact-item">
        <div class="contact-item-label">Nom</div>
        <div class="contact-item-value">Terence Richard</div>
      </div>
      <div class="contact-item">
        <div class="contact-item-label">Poste visé</div>
        <div class="contact-item-value">Directeur Commercial France</div>
      </div>
      <div class="contact-item">
        <div class="contact-item-label">Disponibilité</div>
        <div class="contact-item-value">Sur demande</div>
      </div>
    </div>
    <a href="mailto:" class="btn-primary">Envoyer un message</a>
  </div>
</section>

<!-- ═══════════════════════════════════════
     FOOTER
════════════════════════════════════════ -->
<footer class="footer">
  <div class="footer-grid">
    <div>
      <span class="footer-logo">TR</span>
      <p class="footer-tagline">Vision stratégique pour le développement de Serax en France — Terence Richard, Directeur Commercial.</p>
    </div>
    <div>
      <div class="footer-col-title">Vision</div>
      <ul class="footer-links">
        <li><a href="#strategie">Stratégie</a></li>
        <li><a href="#marche">Marché français</a></li>
        <li><a href="#plan">Plan 90 jours</a></li>
        <li><a href="#vision">Objectifs</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Profil</div>
      <ul class="footer-links">
        <li><a href="#profil">Expérience</a></li>
        <li><a href="#leadership">Leadership</a></li>
        <li><a href="#profil">Compétences</a></li>
      </ul>
    </div>
    <div>
      <div class="footer-col-title">Contact</div>
      <ul class="footer-links">
        <li><a href="#contact">Message direct</a></li>
        <li><a href="#">LinkedIn</a></li>
      </ul>
    </div>
  </div>
  <div class="footer-bottom">
    <span class="footer-copy">© Terence Richard — Candidature Serax France</span>
    <span class="footer-year">2025</span>
  </div>
</footer>

<script>
/* ─── DESKTOP MEGA MENUS ─── */
const menuMap = {
  vision:  { item: 'item-vision',  mega: 'mega-vision'  },
  marche:  { item: 'item-marche',  mega: 'mega-marche'  },
  plan:    { item: 'item-plan',    mega: 'mega-plan'    },
  profil:  { item: 'item-profil',  mega: 'mega-profil'  },
  apropos: { item: 'item-apropos', mega: 'mega-apropos' },
};
let openMenu = null;

function toggleMenu(key) {
  if (openMenu === key) { closeAllMenus(); return; }
  closeAllMenus(false);
  openMenu = key;
  document.getElementById(menuMap[key].item).classList.add('open');
  document.getElementById(menuMap[key].mega).classList.add('active');
  document.getElementById('overlay').classList.add('active');
}
function closeAllMenus(reset = true) {
  Object.values(menuMap).forEach(({ item, mega }) => {
    document.getElementById(item).classList.remove('open');
    document.getElementById(mega).classList.remove('active');
  });
  document.getElementById('overlay').classList.remove('active');
  if (reset) openMenu = null;
}
document.addEventListener('keydown', e => { if (e.key === 'Escape') { closeAllMenus(); closeDrawer(); } });

/* ─── MOBILE DRAWER ─── */
let drawerOpen = false;
function toggleDrawer() {
  drawerOpen = !drawerOpen;
  document.getElementById('mobileDrawer').classList.toggle('open', drawerOpen);
  document.getElementById('drawerOverlay').classList.toggle('open', drawerOpen);
  document.getElementById('hamburger').classList.toggle('open', drawerOpen);
  document.body.style.overflow = drawerOpen ? 'hidden' : '';
}
function closeDrawer() {
  drawerOpen = false;
  document.getElementById('mobileDrawer').classList.remove('open');
  document.getElementById('drawerOverlay').classList.remove('open');
  document.getElementById('hamburger').classList.remove('open');
  document.body.style.overflow = '';
}

let openSub = null;
function toggleDrawerSub(id, btn) {
  const sub = document.getElementById(id);
  if (openSub && openSub !== id) {
    const prev = document.getElementById(openSub);
    if (prev) prev.classList.remove('open');
    const prevBtn = prev && prev.previousElementSibling;
    if (prevBtn) prevBtn.classList.remove('expanded');
  }
  const isOpen = sub.classList.toggle('open');
  btn.classList.toggle('expanded', isOpen);
  openSub = isOpen ? id : null;
}

/* ─── STICKY NAVBAR ─── */
const navbar = document.getElementById('navbar');
window.addEventListener('scroll', () => {
  navbar.classList.toggle('scrolled', window.scrollY > 20);
  if (openMenu) closeAllMenus();
}, { passive: true });

/* ─── SCROLL REVEAL ─── */
const observer = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
}, { threshold: 0.1 });
document.querySelectorAll('.reveal').forEach(el => observer.observe(el));
</script>
</body>
</html>
