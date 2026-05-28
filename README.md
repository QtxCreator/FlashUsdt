<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;900&family=Noto+Sans+SC:wght@300;400;500;700;900&family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&display=swap" rel="stylesheet">
    <title>ByteNexx Flash Token Service Promo</title>
    <style>
        :root {
  /* 60% ground */
  --c-bg: #11100f;
  --c-bg-rgb: 17,16,15;
  /* 30% structure */
  --c-mid: #373429;
  --c-mid-rgb: 55,52,41;
  /* 10% emphasis */
  --c-accent: #506cbf;
  --c-accent-rgb: 80,108,191;
  /* Typography */
  --c-text: #efefee;
  --c-muted: #838076;
  /* Surfaces */
  --c-surface: rgba(255,255,255,0.03);
}
        
@page {
  size: 720px 960px;
  margin: 0;
}
:root {
  --font-sans: 'Inter', 'Noto Sans SC', 'Helvetica Neue', 'Apple Color Emoji', 'Segoe UI Emoji', sans-serif;
  --font-serif: 'Playfair Display', 'Noto Serif SC', 'Cormorant Garamond', 'Apple Color Emoji', serif;
  --font-mono: 'SF Mono', 'Consolas', 'Apple Color Emoji', monospace;

  /* Typographic Scale — 6-level fluid type system (Modular Scale) */
  --text-scale-6: clamp(64px, 12vw, 150px);   /* Hero / Display — oversized, single word or short phrase */
  --text-scale-5: clamp(48px, 8vw, 96px);      /* Primary Title — poster headline */
  --text-scale-4: clamp(32px, 5vw, 56px);      /* Subheadline — chapter opener or key quote */
  --text-scale-3: clamp(20px, 3vw, 32px);      /* Lead Paragraph — slightly larger than body */
  --text-scale-2: 16px;                         /* Body — standard body text */
  --text-scale-1: 12px;                         /* Meta / Caption — minimum readable size */
}
html, body {
  margin: 0; padding: 0;
  background: var(--c-bg);
  color: var(--c-text);
  font-family: 'Inter', 'Noto Sans SC', 'Helvetica Neue', sans-serif;
  -webkit-font-smoothing: antialiased;
}
/* Browser preview: scale poster to fit viewport & center on matching background */
@media screen {
  html {
    height: auto;
    display: flex;
    justify-content: center;
    align-items: flex-start;
    min-height: 100vh;
    background: var(--c-bg);
  }
  body {
    transform-origin: top center;
    margin: 0 auto;
    box-shadow: 0 0 60px rgba(0,0,0,0.3);
    /* scale injected by override_css with concrete canvas dimensions */
  }
}
.canvas {
  width: var(--canvas-w, 720px);
  min-height: var(--canvas-h, 960px);
  position: relative;
  overflow: hidden;
  box-sizing: border-box;
  page-break-after: always;
}
/* ═══ Continuous Canvas Mode (multi-page as one seamless surface) ═══ */
.continuous-canvas {
  width: var(--canvas-w, 720px);
  position: relative;
  overflow: hidden;
  box-sizing: border-box;
  /* height is set inline: canvas_h * total_pages */
}
.continuous-canvas .bg-layer-full {
  position: absolute;
  inset: 0;
  z-index: 1;
  pointer-events: none;
}
.continuous-canvas .bg-layer-full svg {
  width: 100%;
  height: 100%;
}
.continuous-canvas .page-section {
  position: absolute;
  left: 0;
  width: 100%;
  box-sizing: border-box;
  overflow: visible;
  /* top and height set inline per page */
}
.continuous-canvas .page-section .safe-zone {
  position: absolute;
  inset: 10% 12%;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(12, minmax(0, auto));
  align-content: start;
}
.continuous-canvas .page-section .page-ghost {
  position: absolute;
  bottom: -5%;
  right: 5%;
  font-size: 240px;
  font-weight: 900;
  color: var(--c-mid);
  opacity: 0.05;
  pointer-events: none;
  z-index: 0;
}
/* 12% Breathing Margin Enforcer (balanced: enough air without wasting space) */
.safe-zone {
  position: absolute;
  inset: 10% 12%;
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(12, minmax(0, auto));
  align-content: start;
  /* gap is injected dynamically by compile_blueprint via inline style */
}
/* Grid-item wrapper — every component gets one */
.grid-item {
  display: flex;
  min-width: 0;
  min-height: 0;
  overflow: visible;
}
/* Global content-overflow protection — prevents ANY text/block from breaking out of its container */
.grid-item * {
  max-width: 100%;
  box-sizing: border-box;
}
.grid-item p, .grid-item li, .grid-item span, .grid-item h1, .grid-item h2, .grid-item h3, .grid-item h4, .grid-item td, .grid-item th, .grid-item div {
  overflow-wrap: break-word;
  word-break: break-word;
}
/* CJK-safe text wrapping: prefer keeping CJK word groups intact, but allow break when necessary */
.hero-type, .hero-sub, .glass-canvas, .shaped-content, .stat-label, .delta-metric, .delta-label {
  text-wrap: balance;
  overflow-wrap: break-word;
  word-break: normal;
  line-break: strict;
}

/* ═══ Micro-Typography: Computational Typesetting ═══ */
p, .glass-canvas, .shaped-content, li {
  /* Algorithmic justification — eliminates white rivers between words */
  text-align: justify;
  hyphens: auto;
  word-spacing: -0.05em;
  /* Hanging punctuation — visually aligned optical edges */
  hanging-punctuation: first last;
  /* Kill orphans & widows — force min 3 lines carried across page breaks */
  orphans: 3;
  widows: 3;
}
.grid-item table {
  width: 100%;
  table-layout: fixed;
  overflow: hidden;
}
.grid-item img {
  max-width: 100%;
  height: auto;
}

/* --- Archetype Layouts --- */
/* All archetypes share the 12×12 grid via .safe-zone.
   Archetype classes may override alignment defaults on the canvas level. */
.archetype-cover_hero .safe-zone {
  align-content: start;
  inset: 12% 14%;
}
/* Cover hero typography scale: larger text for covers */
.archetype-cover_hero .hero-type {
  font-size: clamp(42px, 8vw, 72px);
  line-height: 1.15;
}
.archetype-cover_hero .hero-sub {
  font-size: clamp(22px, 4vw, 32px);
  line-height: 1.3;
  opacity: 0.85;
}
.archetype-cover_hero .floating-meta {
  font-size: clamp(16px, 2.5vw, 22px);
}
.archetype-split_vertical { display: grid; grid-template-columns: 1fr 1fr; min-height: 960px; }
.archetype-split_vertical .safe-zone { position: relative; inset: auto; padding: 10%; display: grid; grid-template-columns: repeat(12, 1fr); grid-template-rows: repeat(12, 1fr); align-content: center; }
.archetype-split_vertical.single-column { grid-template-columns: 1fr; }
.archetype-editorial_flow .safe-zone { align-content: center; }
.archetype-scattered_canvas .safe-zone { /* same 12×12 grid — scattered effect via grid_area placement */ }
.archetype-data_dashboard .safe-zone { /* same 12×12 grid — dashboard tiles via grid_area placement */ }
.archetype-shaped_editorial .safe-zone { align-content: center; }

/* Continuous canvas archetype overrides (page-section inherits archetype class) */
.continuous-canvas .page-section.archetype-cover_hero .safe-zone { align-content: start; inset: 12% 14%; }
.continuous-canvas .page-section.archetype-cover_hero .hero-type { font-size: clamp(42px, 8vw, 72px); line-height: 1.15; }
.continuous-canvas .page-section.archetype-cover_hero .hero-sub { font-size: clamp(22px, 4vw, 32px); line-height: 1.3; opacity: 0.85; }
.continuous-canvas .page-section.archetype-cover_hero .floating-meta { font-size: clamp(16px, 2.5vw, 22px); }
.continuous-canvas .page-section.archetype-editorial_flow .safe-zone { align-content: center; }
.continuous-canvas .page-section.archetype-shaped_editorial .safe-zone { align-content: center; inset: 5% 6%; }

/* --- Components --- */
.hero-type {
  font-size: clamp(48px, 10vw, 110px);
  line-height: 0.88;
  letter-spacing: -0.03em;
  margin: 0;
  overflow-wrap: break-word;
  word-break: break-word;
  position: relative;
  z-index: 10;
}
.hero-type.weight-black { font-weight: 900; }
.hero-type.weight-thin { font-weight: 100; letter-spacing: 0.05em; font-family: 'Playfair Display', 'Noto Serif SC', serif; }
.hero-sub {
  margin: 8px 0 0 0;
  font-size: var(--text-scale-2);
  line-height: 1.3;
  opacity: 0.8;
}
/* Hero container needs vertical stacking */
.grid-item:has(.hero-type) {
  flex-direction: column;
  justify-content: center;
}
.hero-type, .hero-sub {
  width: 100%;
}
.hero-type {
  color: var(--c-text);
}

.glass-canvas {
  background: var(--c-surface);
  border: 1px solid rgba(128, 128, 128, 0.08);
  border-radius: 2px;
  padding: 36px;
  font-size: 16px;
  line-height: 1.6;
  z-index: 5;
  position: relative;
  overflow-wrap: break-word;
  word-break: break-word;
}

.floating-meta {
  display: flex;
  flex-direction: column;
  font-size: 12px;
  font-family: 'SF Mono', 'Consolas', monospace, sans-serif;
  letter-spacing: 0.1em;
  color: var(--c-muted);
  opacity: 0.6;
  z-index: 20;
  overflow: hidden;
  text-overflow: ellipsis;
  /* Positioned via grid_area in .grid-item wrapper — no absolute needed */
}
/* Legacy position helpers (kept for backwards compat with old blueprints) */
.pos-top-left { align-self: start; justify-self: start; }
.pos-top-right { align-self: start; justify-self: end; text-align: right; }
.pos-bottom-left { align-self: end; justify-self: start; }
.pos-bottom-right { align-self: end; justify-self: end; text-align: right; }

.stat-block { display: flex; flex-direction: column; margin-bottom: 24px; }
.stat-num { font-size: clamp(32px, 5vw, 56px); font-weight: 900; line-height: 0.9; color: var(--c-text); }
.stat-unit { font-size: clamp(14px, 2vw, 20px); font-weight: 300; color: var(--c-muted); margin-left: 4px; display: inline;}
.stat-label { font-size: 12px; letter-spacing: 0.15em; color: var(--c-accent); margin-top: 8px; text-transform: uppercase; }

.hairline { border: none; border-top: 0.5px solid var(--c-muted); opacity: 0.3; margin: 8px 0; width: 100%; }
.hairline.style-accent { border-top-color: var(--c-accent); width: 30%; margin-left: 0; opacity: 0.8;}

.page-ghost {
  position: absolute; bottom: -5%; right: 5%;
  font-size: 240px; font-weight: 900; color: var(--c-mid);
  opacity: 0.05; pointer-events: none; z-index: 0;
}

.bg-layer { position: absolute; inset: 0; z-index: 1; pointer-events: none; }
.bg-layer svg { width: 100%; height: 100%; }

/* --- Shaped_Canvas (Semantic Shape-Wrapping) --- */
.shaped-canvas {
  position: relative;
  padding: 24px;
  font-size: 16px;
  line-height: 1.7;
  z-index: 5;
  overflow-wrap: break-word;
  word-break: break-word;
}
.shape-float {
  float: left;
  margin: 0;
  padding: 0;
}
.shape-circle   { shape-outside: circle(45% at 50% 50%);   width: 40%; height: 90%; }
.shape-wave     { shape-outside: polygon(0 0, 80% 0, 60% 25%, 80% 50%, 60% 75%, 80% 100%, 0 100%); width: 45%; height: 100%; }
.shape-diagonal_slash { shape-outside: polygon(0 0, 100% 0, 0 100%); width: 50%; height: 100%; }
.shape-diamond  { shape-outside: polygon(50% 0, 100% 50%, 50% 100%, 0 50%); width: 45%; height: 90%; }
.shape-wedge_right { shape-outside: polygon(0 0, 60% 0, 100% 50%, 60% 100%, 0 100%); width: 50%; height: 100%; }

/* --- Archetype: shaped_editorial --- */
.archetype-shaped_editorial .safe-zone {
  inset: 5% 6%;
  /* Inherits 12×12 grid from .safe-zone */
  align-content: center;
}

/* ═══ Tufte Marginalia System ═══ */
/* 30% sidenote rail for report/long-form archetypes */
.archetype-tufte_report .safe-zone {
  display: grid;
  grid-template-columns: 1fr 280px;
  gap: 40px;
  align-content: start;
}
.archetype-tufte_report .main-column {
  display: grid;
  grid-template-columns: repeat(12, 1fr);
  grid-template-rows: repeat(12, 1fr);
  gap: inherit;
}
.archetype-tufte_report .side-rail {
  display: flex;
  flex-direction: column;
  gap: 24px;
  padding-top: 8px;
}
.sidenote {
  font-size: 13px;
  line-height: 1.5;
  color: var(--c-muted);
  border-left: 2px solid var(--c-accent);
  padding-left: 12px;
  opacity: 0.85;
}
.sidenote .sidenote-label {
  font-weight: 700;
  font-size: 12px;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  color: var(--c-accent);
  display: block;
  margin-bottom: 4px;
}

/* ═══ Delta Widget — Data-to-Ink Ratio Component ═══ */
.delta-widget {
  text-align: center;
  padding: 16px 12px;
}
.delta-widget .delta-metric {
  font-size: 12px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--c-muted);
  margin-bottom: 4px;
}
.delta-widget .delta-value {
  font-size: 36px;
  font-weight: 900;
  color: var(--c-text);
  line-height: 1.1;
}
.delta-widget .delta-change {
  font-size: 14px;
  font-weight: 700;
  margin-top: 4px;
}
.delta-widget .delta-label {
  font-size: 12px;
  color: var(--c-muted);
  margin-top: 8px;
}

/* ═══ Polymorphic Process_List — Container Query Adaptive ═══ */
.process-list-container {
  container-type: inline-size;
  width: 100%;
  min-height: 100%;
}
/* Wide: horizontal timeline */
.process-list {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  gap: 8px;
  list-style: none;
  padding: 0;
  margin: 0;
  min-height: 100%;
}
.process-list .process-step {
  flex: 1;
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  position: relative;
  padding: 12px 4px;
}
.process-step .step-num {
  width: 32px; height: 32px; border-radius: 50%;
  background: var(--c-accent); color: #fff;
  display: flex; align-items: center; justify-content: center;
  font-weight: 800; font-size: 14px; margin-bottom: 8px;
  flex-shrink: 0;
}
.process-step .step-title { font-weight: 700; font-size: 13px; color: var(--c-text); }
.process-step .step-desc { font-size: 12px; color: var(--c-muted); margin-top: 4px; line-height: 1.4; }
/* Connector line between horizontal steps */
.process-step:not(:last-child)::after {
  content: ''; position: absolute; top: 28px; right: -6px;
  width: 12px; height: 2px; background: var(--c-accent); opacity: 0.5;
}
/* Narrow: vertical numbered list */
@container (max-width: 360px) {
  .process-list {
    flex-direction: column;
    gap: 12px;
  }
  .process-list .process-step {
    flex-direction: row;
    text-align: left;
    align-items: flex-start;
    gap: 12px;
    padding: 4px 0;
  }
  .process-step .step-num { margin-bottom: 0; }
  .process-step:not(:last-child)::after { display: none; }
}

        :root { --canvas-w: 720px; --canvas-h: 960px; }
@page { size: 720px 960px; margin: 0; }
html, body { width: 720px; min-height: 960px; }
@media screen { body { scale: min(1, calc(100vw / 720), calc(100vh / 960)); } }

    </style>
</head>
<body>

<div class="continuous-canvas" style="height: 1920px; background: var(--c-bg);">
  <div class="bg-layer-full"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 720 1920" width="720" height="1920">
  <defs>
    <linearGradient id="fg" x1="0" y1="0" x2="1" y2="1">
      <stop offset="0%" stop-color="#506cbf" stop-opacity="0.05"/>
      <stop offset="50%" stop-color="#506cbf" stop-opacity="0.075"/>
      <stop offset="100%" stop-color="#506cbf" stop-opacity="0.025"/>
    </linearGradient>
  </defs>
  <path d="M440,0 C530,247 642,340 86,640 C304,757 157,1063 230,1280 C19,1431 468,1711 201,1920" fill="none" stroke="url(#fg)" stroke-width="71" stroke-linecap="round" opacity="0.050"/>
  <path d="M411,0 C503,179 112,514 538,640 C242,770 70,1132 76,1280 C435,1553 525,1710 536,1920" fill="none" stroke="url(#fg)" stroke-width="109" stroke-linecap="round" opacity="0.060"/>
  <path d="M290,0 C620,227 507,332 390,640 C164,809 57,1009 550,1280 C73,1447 458,1675 428,1920" fill="none" stroke="url(#fg)" stroke-width="79" stroke-linecap="round" opacity="0.070"/>
  <path d="M193,0 C439,145 525,355 226,640 C273,949 461,1074 612,1280 C493,1560 559,1648 445,1920" fill="none" stroke="url(#fg)" stroke-width="62" stroke-linecap="round" opacity="0.080"/>
</svg></div>

  <div class="page-section archetype-cover_hero" style="top: 0px; height: 960px;">
    <div class="safe-zone" style="gap: 16px;">
      <div class="grid-item" style="grid-area: 1 / 1 / 4 / 13; align-items: start; justify-content: start;">
<div class="floating-meta pos-top-left"><span>FLASH TOKEN SERVICE</span><span>2026</span></div>
</div>
      <div class="grid-item" style="grid-area: 4 / 1 / 7 / 13; align-items: start; justify-content: start;">
<h1 class="hero-type weight-black">BYTE<br>NEXX</h1>
</div>
      <div class="grid-item" style="grid-area: 8 / 1 / 10 / 13; align-items: start; justify-content: start;">
<hr class="hairline style-accent">
</div>
      <div class="grid-item" style="grid-area: 10 / 1 / 13 / 13; align-items: start; justify-content: start;">
<div class="floating-meta pos-bottom-right"><span>DEMO IS FREE</span><span>CONTACT @BYTENEXX</span></div>
</div>
    </div>
  </div>

  <div class="page-section archetype-editorial_flow" style="top: 960px; height: 960px;">
    <div class="safe-zone" style="gap: 16px; inset: 8% 10%;">
      <div class="page-ghost">02</div>
      <div class="grid-item" style="grid-area: 1 / 1 / 4 / 13; align-items: start; justify-content: start;">
<h1 class="hero-type weight-thin" style="font-size: var(--text-scale-4)">WALLETS & NETWORKS</h1>
</div>
      <div class="grid-item" style="grid-area: 4 / 1 / 13 / 13; align-items: stretch; justify-content: start;">
<div class="glass-canvas" style="width:100%; min-height:100%; box-sizing:border-box;">
<h3 style="font-size:16px;font-weight:700;margin:20px 0 12px 0;color:var(--c-accent);text-transform:uppercase;letter-spacing:0.08em;">Supported Wallets</h3>
<ul style="margin:8px 0 16px 0;padding-left:20px;list-style-type:none;">
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>Trust Wallet</strong> &mdash; Binance ecosystem native</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>Binance Web3 Wallet</strong> &mdash; Seamless DeFi access</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>Safepal Wallet</strong> &mdash; Hardware-grade security</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>Metamask Wallet</strong> &mdash; Ethereum standard</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>OKX Wallet</strong> &mdash; Multi-chain powerhouse</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>Base Wallet</strong> &mdash; Coinbase L2 native</li>
</ul>
<hr class="hairline" style="margin:12px 0 16px 0;width:60%;opacity:0.3;">
<h3 style="font-size:16px;font-weight:700;margin:4px 0 12px 0;color:var(--c-accent);text-transform:uppercase;letter-spacing:0.08em;">Tokens & Networks</h3>
<ul style="margin:8px 0 16px 0;padding-left:20px;list-style-type:none;">
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>USDT / BTC / SOL / ETH</strong> &mdash; All major tokens</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>BNB Network</strong> &mdash; Fast &amp; low fees</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>TRC20 Network</strong> &mdash; Tron stablecoin standard</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>ETH Network</strong> &mdash; Ethereum mainnet</li>
<li style="margin:6px 0;line-height:1.7;font-size:15px;"><strong>SOL Network</strong> &mdash; Solana blazing speed</li>
</ul>
<hr class="hairline" style="margin:12px 0 16px 0;width:60%;opacity:0.3;">
<div style="text-align:center;padding:8px 0;">
<p style="margin:0 0 8px 0;font-size:18px;font-weight:900;color:var(--c-accent);letter-spacing:0.05em;">DEMO IS 100% FREE</p>
<p style="margin:0 0 8px 0;font-size:14px;color:var(--c-muted);line-height:1.5;">Try before you buy. No risk, no commitment.</p>
<p style="margin:12px 0 4px 0;font-size:15px;color:var(--c-text);"><strong>Contact:</strong> @bytenexx on Telegram</p>
<p style="margin:0;font-size:14px;color:var(--c-accent);"><strong>https://t.me/bytenexx</strong></p>
</div>
</div>
</div>
    </div>
  </div>
</div>
</body>
</html>
