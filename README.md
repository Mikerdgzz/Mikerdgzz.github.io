# Mikerdgzz.github.io
Viaje Albania
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Albania 2026 — Mike & Lucía</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
:root {
  --ink: #1a1208;
  --paper: #f5f0e8;
  --cream: #ede8dc;
  --gold: #c8922a;
  --gold-light: #e8c068;
  --teal: #1a7a6e;
  --teal-light: #2da898;
  --rust: #c05a2a;
  --slate: #4a5568;
  --muted: #8a8070;
  --border: rgba(26,18,8,0.12);
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{
  background:var(--paper);
  color:var(--ink);
  font-family:'DM Sans',sans-serif;
  font-size:15px;
  line-height:1.6;
}

/* ── COVER ── */
.cover{
  position:relative;
  min-height:100vh;
  display:flex;
  flex-direction:column;
  justify-content:flex-end;
  padding:4rem 5%;
  overflow:hidden;
  background:#0d1a1f;
}
.cover-bg{
  position:absolute;inset:0;
  background:
    radial-gradient(ellipse 80% 60% at 70% 40%, rgba(29,110,98,0.35) 0%, transparent 60%),
    radial-gradient(ellipse 50% 80% at 20% 80%, rgba(200,146,42,0.2) 0%, transparent 50%),
    linear-gradient(160deg, #0d1a1f 0%, #152a24 40%, #0d1a1f 100%);
}
.cover-grid{
  position:absolute;inset:0;
  background-image:
    linear-gradient(rgba(245,240,232,0.04) 1px, transparent 1px),
    linear-gradient(90deg, rgba(245,240,232,0.04) 1px, transparent 1px);
  background-size:60px 60px;
}
.cover-noise{
  position:absolute;inset:0;
  opacity:.025;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.85' numOctaves='4'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)'/%3E%3C/svg%3E");
  background-size:200px 200px;
}
.cover-content{position:relative;z-index:2;max-width:900px}
.cover-eyebrow{
  font-family:'DM Mono',monospace;
  font-size:11px;letter-spacing:3px;
  color:var(--gold-light);
  text-transform:uppercase;
  margin-bottom:1.5rem;
  display:flex;align-items:center;gap:12px;
}
.cover-eyebrow::before{content:'';display:block;width:32px;height:1px;background:var(--gold)}
.cover-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(4rem,9vw,8rem);
  font-weight:900;
  line-height:.92;
  color:#f5f0e8;
  letter-spacing:-2px;
  margin-bottom:1.5rem;
}
.cover-title em{
  font-style:italic;
  color:var(--gold-light);
}
.cover-sub{
  font-size:15px;
  color:rgba(245,240,232,0.55);
  margin-bottom:3rem;
  max-width:480px;
  line-height:1.7;
}
.cover-stats{
  display:flex;gap:0;
  border:1px solid rgba(245,240,232,0.12);
  border-radius:2px;
  overflow:hidden;
  width:fit-content;
  margin-bottom:2rem;
}
.cover-stat{
  padding:14px 24px;
  border-right:1px solid rgba(245,240,232,0.12);
  background:rgba(245,240,232,0.04);
}
.cover-stat:last-child{border-right:none}
.cs-val{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:#f5f0e8;display:block}
.cs-lbl{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:2px;color:rgba(245,240,232,0.4);text-transform:uppercase}
.cover-scroll{
  display:flex;align-items:center;gap:8px;
  font-family:'DM Mono',monospace;font-size:10px;
  color:rgba(245,240,232,0.3);letter-spacing:2px;
  text-transform:uppercase;
}
.scroll-line{width:40px;height:1px;background:rgba(245,240,232,0.2)}

/* ── NAV TABS ── */
.sticky-nav{
  position:sticky;top:0;z-index:100;
  background:rgba(245,240,232,0.95);
  backdrop-filter:blur(12px);
  border-bottom:1px solid var(--border);
  padding:0 5%;
  display:flex;align-items:center;gap:0;
}
.nav-tab{
  padding:16px 20px;
  font-family:'DM Mono',monospace;
  font-size:11px;letter-spacing:1.5px;
  text-transform:uppercase;
  color:var(--muted);
  cursor:pointer;
  border:none;background:none;
  border-bottom:2px solid transparent;
  transition:all .2s;
  white-space:nowrap;
}
.nav-tab.active,.nav-tab:hover{color:var(--ink);border-bottom-color:var(--gold)}
.nav-brand{
  font-family:'Playfair Display',serif;
  font-size:16px;font-weight:700;
  color:var(--ink);
  margin-right:auto;
  padding:16px 0;
}

/* ── SECTIONS ── */
.section{display:none;padding:5% 5% 6%}
.section.active{display:block}
.section-header{margin-bottom:3rem}
.section-label{
  font-family:'DM Mono',monospace;
  font-size:10px;letter-spacing:3px;text-transform:uppercase;
  color:var(--gold);display:flex;align-items:center;gap:10px;
  margin-bottom:.75rem;
}
.section-label::after{content:'';flex:1;height:1px;background:var(--border)}
.section-title{
  font-family:'Playfair Display',serif;
  font-size:clamp(2rem,4vw,3.5rem);
  font-weight:700;line-height:1.1;
  color:var(--ink);
}
.section-title em{font-style:italic;color:var(--teal)}

/* ── DAYS GRID ── */
.days-grid{display:flex;flex-direction:column;gap:2px}
.day-row{
  display:grid;
  grid-template-columns:80px 1fr;
  border:1px solid var(--border);
  border-radius:3px;
  overflow:hidden;
  transition:transform .2s,box-shadow .2s;
  background:#fff;
}
.day-row:hover{transform:translateX(4px);box-shadow:inset 3px 0 0 var(--gold)}
.day-num{
  background:var(--ink);
  display:flex;flex-direction:column;
  align-items:center;justify-content:center;
  gap:2px;padding:1.5rem .5rem;
}
.day-num-n{
  font-family:'Playfair Display',serif;
  font-size:2.5rem;font-weight:900;
  color:var(--gold-light);line-height:1;
}
.day-num-l{
  font-family:'DM Mono',monospace;
  font-size:9px;letter-spacing:2px;
  color:rgba(245,240,232,0.4);text-transform:uppercase;
}
.day-body{padding:1.5rem 1.75rem}
.day-name{
  font-family:'Playfair Display',serif;
  font-size:1.25rem;font-weight:700;
  color:var(--ink);margin-bottom:2px;
}
.day-date{
  font-family:'DM Mono',monospace;font-size:10px;
  letter-spacing:1.5px;color:var(--muted);
  text-transform:uppercase;margin-bottom:1rem;
}
.day-slots{display:grid;grid-template-columns:repeat(3,1fr);gap:10px;margin-bottom:12px}
.slot{background:var(--cream);padding:10px 12px;border-radius:2px}
.slot-time{
  font-family:'DM Mono',monospace;font-size:9px;
  letter-spacing:1.5px;color:var(--gold);
  text-transform:uppercase;margin-bottom:5px;
}
.slot-text{font-size:12.5px;color:var(--slate);line-height:1.5}
.day-tags{display:flex;flex-wrap:wrap;gap:5px;margin-bottom:10px}
.dtag{
  padding:3px 10px;border-radius:1px;
  font-family:'DM Mono',monospace;font-size:9px;
  letter-spacing:1px;text-transform:uppercase;font-weight:500;
}
.dtag-trek{background:#e8f3e0;color:#2d6b11}
.dtag-beach{background:#dff0ef;color:#0f6e5a}
.dtag-city{background:#e8e4f8;color:#3c2d89}
.dtag-drive{background:#f5ede0;color:#7a3a12}
.dtag-log{background:#f0ece0;color:#5a4a20}
.dtag-special{background:#fef3d8;color:#7a5010;border:1px solid #e8c068}
.day-tip{
  border-left:2px solid var(--gold);
  padding:8px 12px;
  font-size:12.5px;
  color:var(--slate);
  background:rgba(200,146,42,0.05);
  line-height:1.6;
  border-radius:0 2px 2px 0;
}
.day-warn{
  border-left:2px solid var(--rust);
  padding:8px 12px;
  font-size:12.5px;
  color:#7a3a12;
  background:rgba(192,90,42,0.06);
  line-height:1.6;
  border-radius:0 2px 2px 0;
}
/* BOVILLA SPECIAL */
.bovilla-badge{
  display:inline-flex;align-items:center;gap:6px;
  background:linear-gradient(135deg,#1a7a6e,#2da898);
  color:#fff;padding:3px 10px;border-radius:1px;
  font-family:'DM Mono',monospace;font-size:9px;letter-spacing:1px;text-transform:uppercase;
  margin-bottom:6px;
}

/* ── FLIGHTS ── */
.flights-grid{display:grid;grid-template-columns:1fr 1fr;gap:1.5rem;margin-bottom:2rem}
.flight-card{
  background:#fff;border:1px solid var(--border);
  border-radius:3px;padding:1.75rem;
  position:relative;overflow:hidden;
}
.flight-card::before{
  content:'';position:absolute;top:0;left:0;right:0;height:3px;
  background:var(--teal);
}
.flight-card.return::before{background:var(--gold)}
.flight-airline{
  font-family:'DM Mono',monospace;font-size:10px;
  letter-spacing:2px;text-transform:uppercase;
  color:var(--muted);margin-bottom:1rem;
  display:flex;align-items:center;gap:8px;
}
.flight-arrow{color:var(--muted);font-size:11px}
.f-row{display:flex;align-items:center;gap:1.5rem;margin-bottom:.75rem}
.f-apt{font-family:'Playfair Display',serif;font-size:2rem;font-weight:700;color:var(--ink);line-height:1}
.f-time{font-size:12px;color:var(--muted);margin-top:2px}
.f-sep{flex:1;display:flex;align-items:center;gap:8px}
.f-line{flex:1;height:1px;background:var(--border)}
.f-plane{font-size:16px;color:var(--teal)}
.f-price{
  font-family:'Playfair Display',serif;
  font-size:1.4rem;font-weight:700;
  color:var(--teal);
}
.f-note{font-size:12px;color:var(--muted);margin-top:2px}
.confirmed-badge{
  display:inline-flex;align-items:center;gap:5px;
  background:#e8f3e0;color:#2d6b11;
  padding:3px 10px;border-radius:1px;
  font-family:'DM Mono',monospace;font-size:9px;letter-spacing:1px;text-transform:uppercase;
  margin-top:8px;
}
.confirmed-badge::before{content:'✓';font-size:10px}
.car-card{
  background:var(--ink);border-radius:3px;
  padding:2rem 2.5rem;
  display:grid;grid-template-columns:1fr auto;
  align-items:center;gap:2rem;
}
.car-info h3{
  font-family:'Playfair Display',serif;
  font-size:1.4rem;color:#f5f0e8;
  margin-bottom:.5rem;
}
.car-info p{font-size:13px;color:rgba(245,240,232,0.5);line-height:1.7}
.car-stats{display:flex;gap:2rem}
.car-stat{text-align:right}
.car-stat-val{
  font-family:'Playfair Display',serif;
  font-size:1.75rem;font-weight:700;
  color:var(--gold-light);display:block;line-height:1;
}
.car-stat-lbl{
  font-family:'DM Mono',monospace;font-size:9px;
  letter-spacing:1.5px;text-transform:uppercase;
  color:rgba(245,240,232,0.35);margin-top:3px;display:block;
}

/* ── ROUTES ── */
.routes-list{display:flex;flex-direction:column;gap:10px}
.route-item{
  display:grid;grid-template-columns:auto 1fr auto;
  align-items:center;gap:1.5rem;
  background:#fff;border:1px solid var(--border);
  border-radius:3px;padding:1.25rem 1.5rem;
  transition:border-color .2s;
}
.route-item:hover{border-color:var(--teal)}
.route-day-badge{
  background:var(--ink);color:var(--gold-light);
  width:40px;height:40px;border-radius:2px;
  display:flex;align-items:center;justify-content:center;
  font-family:'Playfair Display',serif;font-size:1.1rem;font-weight:700;
  flex-shrink:0;
}
.route-body{}
.route-name{font-weight:500;font-size:14px;color:var(--ink);margin-bottom:3px}
.route-detail{font-family:'DM Mono',monospace;font-size:10px;letter-spacing:1px;color:var(--muted)}
.route-links{display:flex;gap:6px}
.rlink{
  display:inline-flex;align-items:center;gap:4px;
  padding:6px 12px;
  border:1px solid var(--border);border-radius:1px;
  font-family:'DM Mono',monospace;font-size:10px;letter-spacing:1px;text-transform:uppercase;
  color:var(--teal);text-decoration:none;
  transition:all .15s;white-space:nowrap;
}
.rlink:hover{background:var(--teal);color:#fff;border-color:var(--teal)}
.route-special{border-left:3px solid var(--teal-light)}

/* ── BUDGET ── */
.budget-layout{display:grid;grid-template-columns:1fr 360px;gap:2rem;align-items:start}
.budget-table{background:#fff;border:1px solid var(--border);border-radius:3px;overflow:hidden}
.bt-head{
  background:var(--ink);padding:1rem 1.5rem;
  display:grid;grid-template-columns:1fr auto;
}
.bt-head-l,.bt-head-r{
  font-family:'DM Mono',monospace;font-size:9px;
  letter-spacing:2px;text-transform:uppercase;
  color:rgba(245,240,232,0.4);
}
.bt-row{
  display:grid;grid-template-columns:1fr auto;
  padding:12px 1.5rem;
  border-bottom:1px solid var(--border);
  align-items:start;
}
.bt-row:last-child{border:none}
.bt-row.confirmed .bt-right{color:var(--teal)}
.bt-row.total{
  background:var(--cream);
  padding:16px 1.5rem;
  border-top:2px solid var(--border);
}
.bt-left{font-size:13.5px;color:var(--ink)}
.bt-left small{display:block;font-size:11px;color:var(--muted);margin-top:2px}
.bt-right{
  font-family:'Playfair Display',serif;
  font-size:1.1rem;font-weight:700;
  color:var(--ink);white-space:nowrap;
}
.bt-row.total .bt-left{font-weight:500;font-size:14px}
.bt-row.total .bt-right{font-size:1.5rem;color:var(--teal)}
.budget-sidebar{display:flex;flex-direction:column;gap:1.25rem}
.bs-card{
  background:#fff;border:1px solid var(--border);
  border-radius:3px;padding:1.5rem;
}
.bs-card-title{
  font-family:'DM Mono',monospace;font-size:10px;
  letter-spacing:2px;text-transform:uppercase;
  color:var(--gold);margin-bottom:1rem;
  display:flex;align-items:center;gap:8px;
}
.bs-card-title::after{content:'';flex:1;height:1px;background:var(--border)}
.big-stat{
  text-align:center;padding:1rem 0;
}
.big-stat-val{
  font-family:'Playfair Display',serif;
  font-size:3.5rem;font-weight:900;
  color:var(--teal);line-height:1;display:block;
}
.big-stat-lbl{font-size:12px;color:var(--muted);margin-top:4px}
.range-bar{
  display:flex;align-items:center;gap:8px;
  margin-top:1rem;font-size:11px;color:var(--muted);
  font-family:'DM Mono',monospace;letter-spacing:.5px;
}
.rb-track{flex:1;height:4px;background:var(--cream);border-radius:2px;overflow:hidden}
.rb-fill{height:100%;width:60%;background:linear-gradient(90deg,var(--teal),var(--gold));border-radius:2px}
.paid-row{display:flex;justify-content:space-between;padding:6px 0;font-size:13px;border-bottom:1px solid var(--border)}
.paid-row:last-child{border:none;padding-top:10px;font-weight:500}
.paid-check{color:var(--teal)}

/* ── INFO ── */
.info-masonry{display:grid;grid-template-columns:1fr 1fr;gap:1.25rem}
.info-block{background:#fff;border:1px solid var(--border);border-radius:3px;overflow:hidden}
.ib-head{background:var(--ink);padding:12px 1.25rem}
.ib-title{
  font-family:'Playfair Display',serif;
  font-size:1rem;font-weight:700;
  color:var(--gold-light);
}
.ib-body{padding:1.25rem}
.ib-item{
  display:flex;align-items:baseline;gap:8px;
  padding:6px 0;border-bottom:1px solid var(--border);
  font-size:13px;
}
.ib-item:last-child{border:none}
.ib-dot{
  width:5px;height:5px;border-radius:50%;
  background:var(--gold);flex-shrink:0;
  margin-top:5px;
}
.ib-text{color:var(--slate);line-height:1.5}
.food-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.food-item{
  background:var(--cream);padding:10px 12px;border-radius:2px;
}
.food-name{font-weight:500;font-size:13px;color:var(--ink);margin-bottom:2px}
.food-desc{font-size:11px;color:var(--muted)}
.photo-list{display:flex;flex-direction:column;gap:0}
.photo-item{
  display:flex;align-items:center;gap:12px;
  padding:9px 0;border-bottom:1px solid var(--border);
  font-size:13px;
}
.photo-item:last-child{border:none}
.photo-num{
  font-family:'Playfair Display',serif;
  font-size:1.4rem;font-weight:900;
  color:var(--cream);line-height:1;
  width:32px;flex-shrink:0;text-align:center;
  text-shadow:0 0 0 transparent;
  color:var(--gold-light);
  opacity:.4;
}
.photo-text{color:var(--slate)}
.dict-grid{display:grid;grid-template-columns:1fr 1fr;gap:8px}
.dict-item{
  display:flex;flex-direction:column;gap:2px;
  padding:8px 0;border-bottom:1px solid var(--border);
}
.dict-item:nth-last-child(-n+2){border:none}
.dict-al{font-family:'Playfair Display',serif;font-style:italic;font-size:14px;color:var(--ink);font-weight:700}
.dict-es{font-size:12px;color:var(--muted)}

/* ── BOVILLA HIGHLIGHT ── */
.bovilla-section{
  background:linear-gradient(135deg,#0f2a26 0%,#1a4a40 50%,#0f2a26 100%);
  border-radius:3px;
  padding:2.5rem;
  margin:2rem 0;
  position:relative;overflow:hidden;
  border:1px solid rgba(45,168,152,0.3);
}
.bovilla-section::before{
  content:'';position:absolute;
  top:-40%;right:-10%;
  width:400px;height:400px;
  border-radius:50%;
  background:radial-gradient(circle,rgba(45,168,152,0.15) 0%,transparent 70%);
}
.bovilla-label{
  font-family:'DM Mono',monospace;font-size:10px;
  letter-spacing:3px;text-transform:uppercase;
  color:var(--teal-light);
  display:flex;align-items:center;gap:10px;
  margin-bottom:1rem;
}
.bovilla-label::after{content:'';flex:1;height:1px;background:rgba(45,168,152,0.3)}
.bovilla-title{
  font-family:'Playfair Display',serif;
  font-size:2rem;font-weight:700;
  color:#f5f0e8;margin-bottom:.5rem;
}
.bovilla-title em{font-style:italic;color:var(--gold-light)}
.bovilla-body{
  display:grid;grid-template-columns:1fr 1fr;
  gap:2rem;margin-top:1.5rem;
  position:relative;
}
.bovilla-fact{
  display:flex;gap:12px;align-items:flex-start;
  padding:10px 0;border-bottom:1px solid rgba(245,240,232,0.08);
}
.bovilla-fact:last-child{border:none}
.bf-dot{width:6px;height:6px;background:var(--teal-light);border-radius:50%;flex-shrink:0;margin-top:6px}
.bf-text{font-size:13px;color:rgba(245,240,232,0.7);line-height:1.6}
.bf-text strong{color:#f5f0e8;font-weight:500}
.bovilla-why{
  background:rgba(45,168,152,0.1);
  border:1px solid rgba(45,168,152,0.25);
  border-radius:2px;padding:1.25rem;
  font-size:13px;color:rgba(245,240,232,0.75);
  line-height:1.7;
}
.bovilla-why strong{color:var(--gold-light)}

/* ── RESPONSIVE ── */
@media(max-width:700px){
  .day-slots{grid-template-columns:1fr}
  .flights-grid{grid-template-columns:1fr}
  .budget-layout{grid-template-columns:1fr}
  .info-masonry{grid-template-columns:1fr}
  .bovilla-body{grid-template-columns:1fr}
  .car-card{grid-template-columns:1fr}
  .car-stats{justify-content:flex-start}
  .cover-title{font-size:3.5rem;letter-spacing:-1px}
  .route-item{grid-template-columns:auto 1fr;grid-template-rows:auto auto}
  .route-links{grid-column:1/-1}
  .dict-grid,.food-grid{grid-template-columns:1fr}
}
@media(max-width:480px){
  .cover-stats{flex-wrap:wrap}
  .sticky-nav{overflow-x:auto;padding:0 3%}
  .section{padding:6% 4% 8%}
}
</style>
</head>
<body>

<!-- COVER -->
<div class="cover">
  <div class="cover-bg"></div>
  <div class="cover-grid"></div>
  <div class="cover-noise"></div>
  <div class="cover-content">
    <div class="cover-eyebrow">Viaje de aventura</div>
    <h1 class="cover-title">Al<em>ba</em>nia<br>2026</h1>
    <p class="cover-sub">Mike & Lucía · De los Alpes albaneses a la Riviera del Jónico. Siete días para descubrir el país más salvaje de Europa.</p>
    <div class="cover-stats">
      <div class="cover-stat"><span class="cs-val">7</span><span class="cs-lbl">Días</span></div>
      <div class="cover-stat"><span class="cs-val">28 May</span><span class="cs-lbl">Salida</span></div>
      <div class="cover-stat"><span class="cs-val">6 Noches</span><span class="cs-lbl">Alojamiento</span></div>
      <div class="cover-stat"><span class="cs-val">~1.300€</span><span class="cs-lbl">Presupuesto</span></div>
    </div>
    <div class="cover-scroll"><div class="scroll-line"></div> Desplazar para explorar</div>
  </div>
</div>

<!-- NAV -->
<nav class="sticky-nav">
  <span class="nav-brand">ALB '26</span>
  <button class="nav-tab active" onclick="show('itinerario',this)">Itinerario</button>
  <button class="nav-tab" onclick="show('vuelos',this)">Vuelos & Coche</button>
  <button class="nav-tab" onclick="show('rutas',this)">Rutas</button>
  <button class="nav-tab" onclick="show('presupuesto',this)">Presupuesto</button>
  <button class="nav-tab" onclick="show('info',this)">Guía</button>
</nav>

<!-- ITINERARIO -->
<div id="itinerario" class="section active">
  <div class="section-header">
    <div class="section-label">28 mayo — 4 junio</div>
    <h2 class="section-title">El <em>itinerario</em></h2>
  </div>

  <div class="days-grid">

    <!-- DÍA 1 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">1</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Aterrizaje → Shkodër</div>
        <div class="day-date">Jue 28 mayo noche · Vie 29 mayo</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Madrugada</div><div class="slot-text">Llegada 01:50. Coche → Shkodër (1h). Check-in 24h en el alojamiento.</div></div>
          <div class="slot"><div class="slot-time">Tarde 16:00–19:00</div><div class="slot-text">Castillo de Rozafa al atardecer. Paseo peatonal Rruga Kolë Idromeno.</div></div>
          <div class="slot"><div class="slot-time">Noche</div><div class="slot-text">Cena en Tradita o Mesnata. Sacar efectivo LEK (Credins Bank o OTP).</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-city">Ciudad</span><span class="dtag dtag-log">Logística</span></div>
        <div class="day-tip">Dormir hasta tarde para recuperar horas. Gestionar parking del coche con el host (2–5€/día). Dejar maletas grandes en el maletero, preparar mochila de montaña.</div>
      </div>
    </div>

    <!-- DÍA 2 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">2</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Shkodër → Theth</div>
        <div class="day-date">Sábado 30 mayo</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana 07:30</div><div class="slot-text">Furgon desde alojamiento. 1.200 LEK (~12€) por persona. 2.5–3h por el Paso Thore (1.600m).</div></div>
          <div class="slot"><div class="slot-time">Tarde</div><div class="slot-text">Iglesia de Theth + Torre Kulla (historia del Kanun). Cascada de Grunas (45 min). Cañón adyacente.</div></div>
          <div class="slot"><div class="slot-time">Noche</div><div class="slot-text">Cena en guesthouse (comida casera). Pedir picnic para mañana (5–7€). Preparar mochila: 2L agua mínimo.</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-trek">Montaña</span><span class="dtag dtag-city">Cultura</span></div>
        <div class="day-tip">No hacer el Blue Eye hoy para conservar las piernas. Confirmar el furgon del Día 3 → Valbona con el host de la guesthouse.</div>
      </div>
    </div>

    <!-- DÍA 3 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">3</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Travesía Theth → Valbona</div>
        <div class="day-date">Domingo 31 mayo · El día grande</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana 07:30</div><div class="slot-text">Inicio trekking. Marcas roja/blanca en rocas. Café Simoni Kafe (último punto con agua potable antes del paso). Llenar botellas aquí.</div></div>
          <div class="slot"><div class="slot-time">Mediodía</div><div class="slot-text">Valbona Pass (1.795m). Sendero secundario a la izquierda: 5 min extra al mirador sin árboles. Vistas tipo National Geographic.</div></div>
          <div class="slot"><div class="slot-time">Tarde/Noche</div><div class="slot-text">Descenso técnico (pedrera + lecho de río seco). Llegada guesthouse Valbona. Cordero asado + Flija. Reservar furgon para Día 4.</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-trek">Trekking</span></div>
        <div class="day-warn">17 km · +1.050m desnivel · 6.5–8h. Bastones muy recomendados para el descenso. El tramo final (lecho del río) es psicológicamente duro: queda más de lo que parece.</div>
      </div>
    </div>

    <!-- DÍA 4 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">4</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Ferry Lago Koman → Sur</div>
        <div class="day-date">Lunes 1 junio</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana 10:30</div><div class="slot-text">Furgon → Fierzë (embarcadero). 13:00 ferry Lago Koman. Ir en cubierta. 2.5–3h de "fiordo albanés".</div></div>
          <div class="slot"><div class="slot-time">Tarde 16:00</div><div class="slot-text">Desembarque en Koman. Furgon → Shkodër. 18:00 recoger el coche. Inicio ruta hacia el sur.</div></div>
          <div class="slot"><div class="slot-time">Noche</div><div class="slot-text">Opción B recomendada: Berat o Vlorë (3–3.5h). Más sensato que los 6h a Sarandë de noche.</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-log">Transporte</span><span class="dtag dtag-drive">Coche</span></div>
        <div class="day-tip">El lago Koman es uno de los trayectos en barco más espectaculares de Europa. Cubierta superior es obligatoria.</div>
      </div>
    </div>

    <!-- DÍA 5 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">5</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Ksamil y Sarandë</div>
        <div class="day-date">Martes 2 junio</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana 08:30</div><div class="slot-text">Ksamil temprano. Kayak o barca a las islas (10–15€). Único modo de tener el agua azul sin aglomeraciones.</div></div>
          <div class="slot"><div class="slot-time">Mediodía</div><div class="slot-text">Comida en el Castillo de Lëkurësi. Vistas 360° de la bahía y Corfú en el horizonte.</div></div>
          <div class="slot"><div class="slot-time">Tarde/Noche</div><div class="slot-text">Pulëbardha Beach o Mirror Beach para snorkel bajo acantilados. Cena en Sarandë: Saganaki + mejillones de Butrinto.</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-beach">Playa</span><span class="dtag dtag-city">Gastronomía</span></div>
        <div class="day-tip">Llegar a Ksamil antes de las 09:00 para aparcar. No quedarse en la orilla: la playa principal está saturada de sombrillas.</div>
      </div>
    </div>

    <!-- DÍA 6 -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">6</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Riviera Albanesa — Himarë</div>
        <div class="day-date">Miércoles 3 junio</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana</div><div class="slot-text">Ruta SH8 desde Sarandë. Parada en Castillo de Porto Palermo: fortaleza en península rodeada de mar cristalino.</div></div>
          <div class="slot"><div class="slot-time">Mediodía</div><div class="slot-text">Himarë: pescado fresco a la brasa (precio por peso). Más encanto local que Sarandë.</div></div>
          <div class="slot"><div class="slot-time">Tarde/Noche</div><div class="slot-text">Gjipe Beach (cañón, 20 min a pie) o Livadhi. Atardecer en Himarë Fshat. Cena de despedida. Souvenirs: aceite de oliva y miel de montaña.</div></div>
        </div>
        <div class="day-tags"><span class="dtag dtag-beach">Playa</span><span class="dtag dtag-drive">Conducción</span></div>
        <div class="day-tip">Escarpines imprescindibles: playas de piedra gorda. Mide siempre en tiempo: en la Riviera, 20 km = 40 min de curvas.</div>
      </div>
    </div>

    <!-- DÍA 7 CON BOVILLA -->
    <div class="day-row">
      <div class="day-num"><div class="day-num-n">7</div><div class="day-num-l">DÍA</div></div>
      <div class="day-body">
        <div class="day-name">Riviera → Bovilla Lake → Tirana → Vuelo</div>
        <div class="day-date">Jueves 4 junio · Día de regreso</div>
        <div class="day-slots">
          <div class="slot"><div class="slot-time">Mañana 08:00</div><div class="slot-text">Salida obligatoria. Llogara Pass (últimas vistas de la costa). 3.5–4h hasta Tirana.</div></div>
          <div class="slot">
            <div class="slot-time">Mediodía 12:00–13:30</div>
            <div class="bovilla-badge">★ Parada estrella</div>
            <div class="slot-text">Lago Bovilla (30 min desde Tirana). Vistas espectaculares desde la presa. Ideal antes de entrar en la ciudad.</div>
          </div>
          <div class="slot"><div class="slot-time">Tarde 14:00–18:20</div><div class="slot-text">Tirana Express (1.5h): Plaza Skanderbeg, Pirámide, Pazari i Ri. 15:30 salir. 16:15 gasolinera Kastrati. 16:30 devolver coche. 18:20 vuelo.</div></div>
        </div>
        <div class="day-tags">
          <span class="dtag dtag-special">★ Bovilla Lake</span>
          <span class="dtag dtag-city">Tirana</span>
          <span class="dtag dtag-log">Aeropuerto</span>
        </div>
        <div class="day-warn">Tráfico crítico: si el GPS marca rojo en Durrës, abortar Tirana y comer cerca del aeropuerto. Aspirar arena del coche antes de entregar. Check-in online hecho.</div>
      </div>
    </div>

  </div>

  <!-- BOVILLA HIGHLIGHT -->
  <div class="bovilla-section">
    <div class="bovilla-label">Parada especial · Día 7</div>
    <div class="bovilla-title">Lago <em>Bovilla</em> — La joya escondida junto a Tirana</div>
    <div class="bovilla-body">
      <div>
        <div class="bovilla-fact"><div class="bf-dot"></div><div class="bf-text"><strong>Por qué aquí y no antes:</strong> Está a solo 30 min de Tirana por la carretera de montaña. Es la parada más rentable del viaje: de paso obligado en el Día 7, sin desvío.</div></div>
        <div class="bovilla-fact"><div class="bf-dot"></div><div class="bf-text"><strong>Qué esperar:</strong> Un embalse de montaña de color turquesa intenso rodeado de picos de más de 1.800m. La combinación agua + roca + cielo es brutalmente fotogénica.</div></div>
        <div class="bovilla-fact"><div class="bf-dot"></div><div class="bf-text"><strong>Mejor vista:</strong> Desde la presa (Dam de Bovilla). Se llega en coche por la carretera SH56 que sube desde Tirana. 25 km desde el centro.</div></div>
        <div class="bovilla-fact"><div class="bf-dot"></div><div class="bf-text"><strong>Tiempo estimado:</strong> 1–1.5h en el sitio (conducción + parada + fotos). Encaja perfectamente entre llegar a Tirana (12:00) y empezar el "Tirana Express" (13:30–14:00).</div></div>
      </div>
      <div>
        <div class="bovilla-why">
          <strong>Estrategia del Día 7 con Bovilla:</strong><br><br>
          08:00 Salida desde Riviera<br>
          11:30–12:00 Llegada zona Tirana<br>
          12:00 → Desvío Bovilla (30 min coche)<br>
          12:30–13:30 Presa + fotos + respiro<br>
          13:30 → Regreso a Tirana centro<br>
          14:00–15:30 Tirana Express<br>
          15:30 Salida parking Skanderbeg<br>
          16:15 Gasolinera Kastrati<br>
          16:30 Entrega coche<br>
          18:20 Vuelo de vuelta ✈
        </div>
        <a class="rlink" href="https://www.google.com/maps/place/Bovilla+Reservoir,+Albania" target="_blank" style="margin-top:12px;display:inline-flex">Ver en Maps ↗</a>
      </div>
    </div>
  </div>

</div>

<!-- VUELOS Y COCHE -->
<div id="vuelos" class="section">
  <div class="section-header">
    <div class="section-label">Transporte confirmado</div>
    <h2 class="section-title">Vuelos <em>& coche</em></h2>
  </div>
  <div class="flights-grid">
    <div class="flight-card">
      <div class="flight-airline">WizzAir <span class="flight-arrow">·</span> Ida</div>
      <div class="f-row">
        <div><div class="f-apt">MAD</div><div class="f-time">Jue 28 mayo · 22:40</div></div>
        <div class="f-sep"><div class="f-line"></div><div class="f-plane">✈</div><div class="f-line"></div></div>
        <div><div class="f-apt">TIA</div><div class="f-time">Vie 29 mayo · 01:50</div></div>
      </div>
      <div class="f-price">50€ <span style="font-size:.85rem;color:var(--muted)">/ persona</span></div>
      <div class="f-note">Mochila 8 kg incluida · Maleta 20 kg: +28€</div>
      <div class="confirmed-badge">Confirmado</div><br>
      <a class="rlink" href="https://www.wizzair.com/es-es/check-in" target="_blank" style="margin-top:10px">Check-in WizzAir ↗</a>
    </div>
    <div class="flight-card return">
      <div class="flight-airline">WizzAir <span class="flight-arrow">·</span> Vuelta</div>
      <div class="f-row">
        <div><div class="f-apt">TIA</div><div class="f-time">Jue 4 junio · 18:20</div></div>
        <div class="f-sep"><div class="f-line"></div><div class="f-plane">✈</div><div class="f-line"></div></div>
        <div><div class="f-apt">MAD</div><div class="f-time">Jue 4 junio · 21:55</div></div>
      </div>
      <div class="f-price">40€ <span style="font-size:.85rem;color:var(--muted)">/ persona</span></div>
      <div class="f-note">Mochila 8 kg incluida · Maleta 20 kg: +28€</div>
      <div class="confirmed-badge">Confirmado</div><br>
      <a class="rlink" href="https://www.wizzair.com/es-es/check-in" target="_blank" style="margin-top:10px">Check-in WizzAir ↗</a>
    </div>
  </div>
  <div class="car-card">
    <div class="car-info">
      <h3>Coche de alquiler — Rinas (TIA)</h3>
      <p>28 mayo 02:00 AM — 4 junio 17:00 PM · 8 días completos<br>
      Días sin coche (Días 2–4): aparcado en Shkodër (4–5€/día)<br>
      Devolver con depósito lleno: gasolinera Kastrati junto al aeropuerto<br>
      Depósito de seguridad 1.500€ reembolsable · Revisar daños antes de entregar</p>
    </div>
    <div class="car-stats">
      <div class="car-stat"><span class="car-stat-val">99,74€</span><span class="car-stat-lbl">Alquiler total</span></div>
      <div class="car-stat"><span class="car-stat-val">~1.000 km</span><span class="car-stat-lbl">Distancia</span></div>
    </div>
  </div>
</div>

<!-- RUTAS -->
<div id="rutas" class="section">
  <div class="section-header">
    <div class="section-label">Google Maps · AllTrails</div>
    <h2 class="section-title">Rutas <em>& enlaces</em></h2>
  </div>
  <div class="routes-list">
    <div class="route-item">
      <div class="route-day-badge">1</div>
      <div class="route-body">
        <div class="route-name">Aeropuerto Tirana (TIA) → Shkodër</div>
        <div class="route-detail">~1h · 100 km · Autovía SH1 norte · Sin tráfico de madrugada</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://maps.app.goo.gl/YdkQLzEWiNJ2Ni1i9" target="_blank">Maps ↗</a>
        <a class="rlink" href="https://www.google.com/maps/dir/Tirana+International+Airport/Shkodër,+Albania" target="_blank">Ruta ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">4</div>
      <div class="route-body">
        <div class="route-name">Shkodër → Berat (escala recomendada)</div>
        <div class="route-detail">~3.5h · 200 km · Vía Lezhë y Durrës · Más sensato que conducir 6h a Sarandë</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.google.com/maps/dir/Shkodër,+Albania/Berat,+Albania" target="_blank">Ruta ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">5</div>
      <div class="route-body">
        <div class="route-name">Berat → Ksamil (llegada al sur)</div>
        <div class="route-detail">~2.5h · 160 km · Vía Fier y Vlorë · Paisaje costero en la última hora</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.google.com/maps/dir/Berat,+Albania/Ksamil,+Albania" target="_blank">Ruta ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">6</div>
      <div class="route-body">
        <div class="route-name">Sarandë → Himarë (Ruta SH8)</div>
        <div class="route-detail">~1.5h · 50 km · La carretera más espectacular de Albania · Parada en Porto Palermo</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.google.com/maps/dir/Sarandë,+Albania/Himarë,+Albania" target="_blank">Ruta costera ↗</a>
      </div>
    </div>
    <div class="route-item route-special">
      <div class="route-day-badge">7</div>
      <div class="route-body">
        <div class="route-name">★ Himarë → Lago Bovilla → Tirana</div>
        <div class="route-detail">~4h total · Llogara Pass + SH56 a Bovilla · Desvío de solo 30 min desde Tirana · Embalse turquesa a 1.000m de altitud</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.google.com/maps/place/Bovilla+Reservoir,+Albania" target="_blank">Bovilla ↗</a>
        <a class="rlink" href="https://www.google.com/maps/dir/Himarë,+Albania/Tirana,+Albania" target="_blank">Ruta ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">3</div>
      <div class="route-body">
        <div class="route-name">Trekking Theth → Valbona Pass</div>
        <div class="route-detail">17 km · +1.050m · 6.5–8h · Marcas roja/blanca · Descargar offline antes de salir</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.alltrails.com/trail/albania/diber/theth-valbona-pass" target="_blank">AllTrails ↗</a>
        <a class="rlink" href="https://maps.me" target="_blank">Maps.me ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">4</div>
      <div class="route-body">
        <div class="route-name">Ferry Lago Koman (Fierzë → Koman)</div>
        <div class="route-detail">Salida 13:00 · 2.5–3h · Cubierta obligatoria · Uno de los mejores trayectos en barco de Europa</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.komandoferry.com" target="_blank">Reserva ↗</a>
      </div>
    </div>
    <div class="route-item">
      <div class="route-day-badge">5</div>
      <div class="route-body">
        <div class="route-name">Gjipe Beach — La playa del cañón</div>
        <div class="route-detail">20 min caminando desde parking · Cañón que desemboca en playa virgen · Llevar efectivo LEK para parking</div>
      </div>
      <div class="route-links">
        <a class="rlink" href="https://www.google.com/maps/place/Gjipe+Beach,+Albania" target="_blank">Ubicación ↗</a>
      </div>
    </div>
  </div>
</div>

<!-- PRESUPUESTO -->
<div id="presupuesto" class="section">
  <div class="section-header">
    <div class="section-label">Estimación rigurosa</div>
    <h2 class="section-title">Presu<em>puesto</em></h2>
  </div>
  <div class="budget-layout">
    <div class="budget-table">
      <div class="bt-head">
        <div class="bt-head-l">Concepto</div>
        <div class="bt-head-r" style="text-align:right">Importe</div>
      </div>
      <div class="bt-row confirmed">
        <div class="bt-left">Vuelos ida + vuelta (2 personas)<small>50€ pp ida · 40€ pp vuelta · ya comprados ✓</small></div>
        <div class="bt-right" style="color:var(--teal)">180 €</div>
      </div>
      <div class="bt-row confirmed">
        <div class="bt-left">Coche de alquiler (8 días)<small>99,74€ · ya reservado ✓</small></div>
        <div class="bt-right" style="color:var(--teal)">100 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Gasolina<small>900–1.000 km estimados</small></div>
        <div class="bt-right">110 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Alojamiento (6 noches)<small>Guesthouses norte + apartamento sur</small></div>
        <div class="bt-right">400 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Comida (7 días · 2 personas)<small>20–30€/persona/día</small></div>
        <div class="bt-right">300 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Ferry Lago Koman (2 personas)<small>~14–20€ pp sin coche</small></div>
        <div class="bt-right">40 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Furgones montaña (Días 2 y 4)<small>Shkodër→Theth + Valbona→Fierzë</small></div>
        <div class="bt-right">50 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Actividades<small>Kayak Ksamil, entradas castillos, Bovilla</small></div>
        <div class="bt-right">60 €</div>
      </div>
      <div class="bt-row">
        <div class="bt-left">Extras<small>Parkings, cafés, SIM Vodafone Albania (20–30€)</small></div>
        <div class="bt-right">60 €</div>
      </div>
      <div class="bt-row total">
        <div class="bt-left">Total estimado (pareja)<small>Rango: 1.160€ – 1.440€</small></div>
        <div class="bt-right">~1.300 €</div>
      </div>
    </div>

    <div class="budget-sidebar">
      <div class="bs-card">
        <div class="bs-card-title">Por persona</div>
        <div class="big-stat">
          <span class="big-stat-val">~650€</span>
          <div class="big-stat-lbl">estimación central</div>
        </div>
        <div class="range-bar">
          <span>580€</span>
          <div class="rb-track"><div class="rb-fill"></div></div>
          <span>700€</span>
        </div>
      </div>

      <div class="bs-card">
        <div class="bs-card-title">Ya confirmado</div>
        <div class="paid-row"><span>Vuelo ida (2 pax)</span><span class="paid-check">100€ ✓</span></div>
        <div class="paid-row"><span>Vuelo vuelta (2 pax)</span><span class="paid-check">80€ ✓</span></div>
        <div class="paid-row"><span>Coche 8 días</span><span class="paid-check">99,74€ ✓</span></div>
        <div class="paid-row"><span style="font-weight:500">Total pagado</span><span class="paid-check" style="font-size:1.1rem">~280€</span></div>
        <div style="font-size:11.5px;color:var(--muted);margin-top:8px;padding-top:8px;border-top:1px solid var(--border)">Pendiente en destino: ~1.020€ en efectivo/tarjeta</div>
      </div>

      <div class="bs-card">
        <div class="bs-card-title">Tips de dinero</div>
        <div class="ib-item" style="padding:6px 0;border-bottom:1px solid var(--border)"><div class="ib-dot"></div><div class="ib-text" style="font-size:12.5px">1€ ≈ 100 LEK albaneses</div></div>
        <div class="ib-item" style="padding:6px 0;border-bottom:1px solid var(--border)"><div class="ib-dot"></div><div class="ib-text" style="font-size:12.5px">Sacar mucho efectivo en Shkodër (Credins Bank / OTP)</div></div>
        <div class="ib-item" style="padding:6px 0;border-bottom:1px solid var(--border)"><div class="ib-dot"></div><div class="ib-text" style="font-size:12.5px">Theth y Valbona: cero cajeros, solo LEK</div></div>
        <div class="ib-item" style="padding:6px 0"><div class="ib-dot"></div><div class="ib-text" style="font-size:12.5px">Restaurante local: 10–15€ · Cerveza: 2–3€</div></div>
      </div>
    </div>
  </div>
</div>

<!-- GUÍA -->
<div id="info" class="section">
  <div class="section-header">
    <div class="section-label">Survival guide</div>
    <h2 class="section-title">Guía <em>práctica</em></h2>
  </div>
  <div class="info-masonry">

    <div class="info-block">
      <div class="ib-head"><div class="ib-title">Logística esencial</div></div>
      <div class="ib-body">
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">Albania NO es UE: sin roaming gratuito español</div></div>
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">SIM Vodafone Albania en el aeropuerto TIA. 20–30€ por muchos GB</div></div>
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">Shkodër y Tirana: agua embotellada siempre</div></div>
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">Theth y Valbona: fuentes de montaña puras y deliciosas</div></div>
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">Apps: Maps.me (offline Albania), AllTrails, Google Maps</div></div>
        <div class="ib-item"><div class="ib-dot"></div><div class="ib-text">Depósito coche: 1.500€ (reembolsable). Revisar cobertura del seguro</div></div>
      </div>
    </div>

    <div class="info-block">
      <div class="ib-head"><div class="ib-title">Gastronomía — qué pedir</div></div>
      <div class="ib-body">
        <div class="food-grid">
          <div class="food-item"><div class="food-name">Tavë Kosi</div><div class="food-desc">Cordero al horno con yogur. Plato nacional.</div></div>
          <div class="food-item"><div class="food-name">Flija</div><div class="food-desc">Pastel de capas de masa y crema. Norte.</div></div>
          <div class="food-item"><div class="food-name">Byrek</div><div class="food-desc">Hojaldre relleno. El desayuno de campeones.</div></div>
          <div class="food-item"><div class="food-name">Qofte</div><div class="food-desc">Albóndigas alargadas a la brasa.</div></div>
          <div class="food-item"><div class="food-name">Fërgesë</div><div class="food-desc">Pimientos, tomates y feta caliente.</div></div>
          <div class="food-item"><div class="food-name">Raki</div><div class="food-desc">Aguardiente local. Cuidado: muy fuerte.</div></div>
        </div>
      </div>
    </div>

    <div class="info-block">
      <div class="ib-head"><div class="ib-title">Spots fotográficos</div></div>
      <div class="ib-body">
        <div class="photo-list">
          <div class="photo-item"><div class="photo-num">01</div><div class="photo-text">Castillo de Rozafa — atardecer con lago y Alpes</div></div>
          <div class="photo-item"><div class="photo-num">02</div><div class="photo-text">Iglesia de Theth — estampa clásica con montañas</div></div>
          <div class="photo-item"><div class="photo-num">03</div><div class="photo-text">Valbona Pass (1.795m) — mirador secreto 5 min a la izquierda</div></div>
          <div class="photo-item"><div class="photo-num">04</div><div class="photo-text">Ferry Lago Koman — el "fiordo albanés" desde cubierta</div></div>
          <div class="photo-item"><div class="photo-num">05</div><div class="photo-text">Islas de Ksamil — solo desde kayak o barca</div></div>
          <div class="photo-item"><div class="photo-num" style="color:var(--teal-light)">06</div><div class="photo-text"><strong>★ Lago Bovilla</strong> — embalse turquesa junto a Tirana</div></div>
          <div class="photo-item"><div class="photo-num">07</div><div class="photo-text">Llogara Pass — primera vista del mar desde la montaña</div></div>
          <div class="photo-item"><div class="photo-num">08</div><div class="photo-text">La Pirámide de Tirana — skyline desde las escaleras</div></div>
        </div>
      </div>
    </div>

    <div class="info-block">
      <div class="ib-head"><div class="ib-title">Diccionario de supervivencia</div></div>
      <div class="ib-body">
        <div class="dict-grid">
          <div class="dict-item"><div class="dict-al">Përshëndetje</div><div class="dict-es">Hola</div></div>
          <div class="dict-item"><div class="dict-al">Faleminderit</div><div class="dict-es">Gracias</div></div>
          <div class="dict-item"><div class="dict-al">Po / Jo</div><div class="dict-es">Sí / No</div></div>
          <div class="dict-item"><div class="dict-al">Gëzuar!</div><div class="dict-es">¡Salud!</div></div>
          <div class="dict-item" style="grid-column:1/-1"><div class="dict-al">Faturën, ju lutem</div><div class="dict-es">La cuenta, por favor</div></div>
        </div>
      </div>
    </div>

  </div>
</div>

<script>
function show(id, btn) {
  document.querySelectorAll('.section').forEach(s => s.classList.remove('active'));
  document.querySelectorAll('.nav-tab').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  btn.classList.add('active');
}
</script>
</body>
</html>
