# SpandanaM
Strategic Partnerships &amp; Analytics Portfolio — Spandana Manda
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Spandana Manda — Strategic Partnerships Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet" />
<style>
  :root {
    --navy: #0d1f3c;
    --navy-mid: #162d52;
    --navy-light: #1e3d6e;
    --gold: #c9a84c;
    --gold-light: #e8c97e;
    --cream: #f7f3ec;
    --warm-white: #fdfaf5;
    --text: #1a1a2e;
    --muted: #6b7280;
    --border: rgba(201,168,76,0.25);
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--warm-white);
    color: var(--text);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.1rem 3rem;
    background: rgba(13,31,60,0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid var(--border);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem; font-weight: 600;
    color: var(--gold-light); letter-spacing: 0.04em;
  }
  .nav-links { display: flex; gap: 2rem; }
  .nav-links a {
    font-size: 0.78rem; font-weight: 500; letter-spacing: 0.12em;
    text-transform: uppercase; color: rgba(255,255,255,0.7);
    text-decoration: none; transition: color 0.25s;
  }
  .nav-links a:hover { color: var(--gold-light); }

  /* ── HERO ── */
  #hero {
    min-height: 100vh;
    background: var(--navy);
    display: grid; place-items: center;
    position: relative; overflow: hidden;
    padding-top: 80px;
  }
  .hero-bg-lines {
    position: absolute; inset: 0; pointer-events: none;
    background-image:
      repeating-linear-gradient(0deg, transparent, transparent 79px, rgba(201,168,76,0.06) 80px),
      repeating-linear-gradient(90deg, transparent, transparent 79px, rgba(201,168,76,0.06) 80px);
  }
  .hero-bg-circle {
    position: absolute; width: 700px; height: 700px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(201,168,76,0.07) 0%, transparent 70%);
    top: 50%; left: 50%; transform: translate(-50%, -50%);
  }
  .hero-content {
    text-align: center; position: relative; z-index: 2;
    padding: 2rem;
    opacity: 0; animation: fadeUp 1s 0.2s forwards;
  }
  .hero-eyebrow {
    font-size: 0.72rem; letter-spacing: 0.25em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1.4rem;
    display: flex; align-items: center; justify-content: center; gap: 1rem;
  }
  .hero-eyebrow::before, .hero-eyebrow::after {
    content: ''; display: block; width: 40px; height: 1px; background: var(--gold);
  }
  .hero-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3.2rem, 8vw, 6.5rem);
    font-weight: 300; line-height: 1.05;
    color: #fff; letter-spacing: -0.01em;
    margin-bottom: 1.2rem;
  }
  .hero-name em {
    font-style: italic; color: var(--gold-light);
  }
  .hero-tagline {
    font-size: 1.05rem; font-weight: 300;
    color: rgba(255,255,255,0.65);
    max-width: 580px; margin: 0 auto 2.4rem;
    line-height: 1.7;
  }
  .hero-cta {
    display: inline-flex; align-items: center; gap: 0.7rem;
    padding: 0.85rem 2.2rem;
    border: 1px solid var(--gold);
    color: var(--gold-light); font-size: 0.82rem;
    font-weight: 500; letter-spacing: 0.1em; text-transform: uppercase;
    text-decoration: none; transition: all 0.3s;
  }
  .hero-cta:hover {
    background: var(--gold); color: var(--navy);
  }
  .hero-stats {
    display: flex; justify-content: center; gap: 3.5rem;
    margin-top: 4rem; padding-top: 3rem;
    border-top: 1px solid var(--border);
    opacity: 0; animation: fadeUp 1s 0.5s forwards;
  }
  .stat { text-align: center; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.6rem; font-weight: 600;
    color: var(--gold-light); line-height: 1;
    margin-bottom: 0.35rem;
  }
  .stat-label {
    font-size: 0.72rem; letter-spacing: 0.12em; text-transform: uppercase;
    color: rgba(255,255,255,0.45);
  }

  /* ── SECTIONS ── */
  section { padding: 6rem 2rem; }
  .container { max-width: 1080px; margin: 0 auto; }

  .section-header {
    display: flex; align-items: flex-end; gap: 2rem;
    margin-bottom: 3.5rem;
  }
  .section-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 5rem; font-weight: 300; line-height: 1;
    color: var(--gold); opacity: 0.25; letter-spacing: -0.03em;
    flex-shrink: 0;
  }
  .section-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.4rem; font-weight: 400;
    color: var(--navy); line-height: 1.2;
  }
  .section-title span { font-style: italic; color: var(--gold); }

  /* ── ABOUT ── */
  #about { background: var(--cream); }
  .about-grid {
    display: grid; grid-template-columns: 1fr 1.6fr;
    gap: 4rem; align-items: start;
  }
  .about-card {
    background: var(--navy);
    padding: 2.5rem;
    position: relative;
  }
  .about-card::before {
    content: ''; position: absolute;
    top: -8px; left: -8px; right: 8px; bottom: 8px;
    border: 1px solid var(--border); pointer-events: none;
  }
  .about-role {
    font-size: 0.7rem; letter-spacing: 0.2em; text-transform: uppercase;
    color: var(--gold); margin-bottom: 1rem;
  }
  .about-card-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.9rem; color: #fff; font-weight: 400;
    line-height: 1.2; margin-bottom: 1.5rem;
  }
  .about-detail {
    display: flex; gap: 0.7rem; align-items: flex-start;
    color: rgba(255,255,255,0.6); font-size: 0.82rem;
    margin-bottom: 0.6rem; line-height: 1.5;
  }
  .about-detail svg { flex-shrink: 0; margin-top: 2px; }
  .about-text p {
    font-size: 1rem; line-height: 1.82;
    color: #374151; margin-bottom: 1.2rem;
  }
  .about-text p strong { color: var(--navy); font-weight: 600; }
  .skills-chips {
    display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 1.5rem;
  }
  .chip {
    padding: 0.3rem 0.85rem;
    border: 1px solid rgba(13,31,60,0.2);
    font-size: 0.75rem; letter-spacing: 0.06em;
    color: var(--navy-mid); font-weight: 500;
    background: #fff;
  }

  /* ── CASE STUDIES ── */
  #work { background: var(--warm-white); }
  .cases-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 1.5px; background: var(--border);
    border: 1px solid var(--border);
  }
  .case {
    background: var(--warm-white);
    padding: 2.5rem; position: relative;
    transition: background 0.3s;
    cursor: default;
  }
  .case:hover { background: #f0ebe0; }
  .case-tag {
    font-size: 0.68rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--gold); font-weight: 600; margin-bottom: 1rem;
    display: flex; align-items: center; gap: 0.5rem;
  }
  .case-tag::after {
    content: ''; flex: 1; height: 1px; background: var(--border);
  }
  .case-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.55rem; font-weight: 400;
    color: var(--navy); margin-bottom: 0.8rem; line-height: 1.3;
  }
  .case-org {
    font-size: 0.78rem; color: var(--muted); margin-bottom: 1rem;
    font-weight: 500; letter-spacing: 0.05em;
  }
  .case-body {
    font-size: 0.88rem; line-height: 1.75;
    color: #4b5563; margin-bottom: 1.4rem;
  }
  .case-metrics {
    display: flex; gap: 1.2rem; flex-wrap: wrap;
  }
  .metric {
    text-align: center;
    background: var(--navy); padding: 0.7rem 1rem;
    min-width: 90px;
  }
  .metric-val {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.6rem; color: var(--gold-light);
    font-weight: 600; line-height: 1;
  }
  .metric-desc {
    font-size: 0.63rem; color: rgba(255,255,255,0.55);
    letter-spacing: 0.08em; text-transform: uppercase;
    margin-top: 0.25rem;
  }

  /* ── DASHBOARDS ── */
  #dashboards { background: var(--navy); }
  #dashboards .section-title { color: #fff; }
  #dashboards .section-num { color: var(--gold); opacity: 0.2; }
  .dashboard-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
  }
  .dash-card {
    background: var(--navy-mid);
    border: 1px solid var(--border);
    padding: 1.8rem;
    position: relative; overflow: hidden;
    transition: transform 0.3s, border-color 0.3s;
  }
  .dash-card:hover { transform: translateY(-4px); border-color: var(--gold); }
  .dash-icon {
    width: 42px; height: 42px;
    background: rgba(201,168,76,0.15);
    border: 1px solid var(--border);
    display: grid; place-items: center;
    margin-bottom: 1.2rem;
    color: var(--gold);
  }
  .dash-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem; color: #fff;
    margin-bottom: 0.6rem; font-weight: 400;
  }
  .dash-desc {
    font-size: 0.8rem; color: rgba(255,255,255,0.5);
    line-height: 1.65;
  }
  .dash-bar-container {
    margin-top: 1.4rem; display: flex; flex-direction: column; gap: 0.6rem;
  }
  .dash-bar-label {
    display: flex; justify-content: space-between;
    font-size: 0.7rem; color: rgba(255,255,255,0.45);
    margin-bottom: 0.2rem;
  }
  .dash-bar-track {
    height: 4px; background: rgba(255,255,255,0.08); border-radius: 2px;
  }
  .dash-bar-fill {
    height: 100%; background: linear-gradient(90deg, var(--gold), var(--gold-light));
    border-radius: 2px;
    animation: barGrow 1.5s ease forwards;
    transform-origin: left;
  }
  @keyframes barGrow { from { transform: scaleX(0); } to { transform: scaleX(1); } }

  /* Donut chart */
  .donut-wrap { display: flex; justify-content: center; margin-top: 1.2rem; }
  .donut-svg { width: 100px; height: 100px; }

  /* ── CERTIFICATIONS ── */
  #certifications { background: var(--cream); }
  .certs-grid {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
  }
  .cert-card {
    background: #fff;
    border-bottom: 3px solid var(--gold);
    padding: 2rem;
    position: relative; transition: transform 0.3s;
  }
  .cert-card:hover { transform: translateY(-5px); }
  .cert-icon {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.5rem; color: var(--gold);
    line-height: 1; margin-bottom: 1rem; font-weight: 300;
  }
  .cert-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem; color: var(--navy);
    margin-bottom: 0.4rem; font-weight: 600;
  }
  .cert-org {
    font-size: 0.78rem; color: var(--muted); letter-spacing: 0.06em;
    text-transform: uppercase; margin-bottom: 0.6rem;
  }
  .cert-status {
    display: inline-block;
    padding: 0.2rem 0.7rem;
    font-size: 0.68rem; letter-spacing: 0.1em; text-transform: uppercase;
    font-weight: 600;
  }
  .cert-status.active { background: rgba(16,185,129,0.1); color: #065f46; }
  .cert-status.progress { background: rgba(201,168,76,0.15); color: #92400e; }

  .edu-card {
    background: #fff; padding: 2rem;
    border-left: 3px solid var(--navy);
    margin-bottom: 1.2rem;
  }
  .edu-degree {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.25rem; color: var(--navy);
    font-weight: 600; margin-bottom: 0.3rem;
  }
  .edu-school { font-size: 0.85rem; color: var(--muted); margin-bottom: 0.5rem; }
  .edu-note { font-size: 0.8rem; color: #6b7280; line-height: 1.5; }

  /* ── TESTIMONIALS ── */
  #testimonials { background: var(--warm-white); }
  .testimonials-grid {
    display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem;
  }
  .testi-card {
    background: var(--cream); padding: 2.2rem;
    border-top: 1px solid var(--border);
    position: relative;
  }
  .testi-quote {
    font-family: 'Cormorant Garamond', serif;
    font-size: 4rem; color: var(--gold); line-height: 0.5;
    margin-bottom: 1rem; opacity: 0.4;
  }
  .testi-text {
    font-size: 0.93rem; line-height: 1.8;
    color: #374151; margin-bottom: 1.4rem;
    font-style: italic;
  }
  .testi-author { display: flex; align-items: center; gap: 0.8rem; }
  .testi-avatar {
    width: 40px; height: 40px; border-radius: 50%;
    background: var(--navy);
    display: grid; place-items: center;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.2rem; color: var(--gold-light); font-weight: 600;
    flex-shrink: 0;
  }
  .testi-name { font-size: 0.85rem; font-weight: 600; color: var(--navy); }
  .testi-role { font-size: 0.75rem; color: var(--muted); }

  /* ── CONTACT ── */
  #contact {
    background: var(--navy);
    text-align: center; padding: 6rem 2rem;
  }
  #contact .section-title { color: #fff; }
  .contact-sub {
    font-size: 1rem; color: rgba(255,255,255,0.55);
    margin: 1rem auto 2.5rem; max-width: 480px; line-height: 1.7;
  }
  .contact-links {
    display: flex; justify-content: center; gap: 1.2rem; flex-wrap: wrap;
  }
  .contact-btn {
    display: inline-flex; align-items: center; gap: 0.6rem;
    padding: 0.85rem 2rem;
    font-size: 0.8rem; letter-spacing: 0.1em; text-transform: uppercase;
    font-weight: 600; text-decoration: none; transition: all 0.3s;
  }
  .contact-btn.primary {
    background: var(--gold); color: var(--navy);
  }
  .contact-btn.primary:hover { background: var(--gold-light); }
  .contact-btn.secondary {
    border: 1px solid var(--border); color: rgba(255,255,255,0.7);
  }
  .contact-btn.secondary:hover { border-color: var(--gold); color: var(--gold-light); }

  /* ── FOOTER ── */
  footer {
    background: #070f1e; text-align: center;
    padding: 1.8rem; font-size: 0.75rem;
    color: rgba(255,255,255,0.25); letter-spacing: 0.08em;
  }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .reveal {
    opacity: 0; transform: translateY(28px);
    transition: opacity 0.7s ease, transform 0.7s ease;
  }
  .reveal.visible { opacity: 1; transform: none; }

  /* ── RESPONSIVE ── */
  @media (max-width: 768px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    .about-grid, .cases-grid, .dashboard-grid,
    .certs-grid, .testimonials-grid { grid-template-columns: 1fr; }
    .hero-stats { gap: 2rem; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">Spandana Manda</div>
  <div class="nav-links">
    <a href="#about">About</a>
    <a href="#work">Case Studies</a>
    <a href="#dashboards">Analytics</a>
    <a href="#certifications">Credentials</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg-lines"></div>
  <div class="hero-bg-circle"></div>
  <div class="hero-content">
    <div class="hero-eyebrow">Strategic Partnerships &amp; Data Analytics</div>
    <h1 class="hero-name">Spandana <em>Manda</em></h1>
    <p class="hero-tagline">
      Building corporate partnerships through data-driven insight,<br/>
      shared value frameworks, and mission-aligned relationship strategy.
    </p>
    <a href="#work" class="hero-cta">
      View Portfolio
      <svg width="14" height="14" viewBox="0 0 14 14" fill="none">
        <path d="M2 7h10M7 2l5 5-5 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
      </svg>
    </a>
    <div class="hero-stats">
      <div class="stat">
        <div class="stat-num">$10M+</div>
        <div class="stat-label">Revenue Impact</div>
      </div>
      <div class="stat">
        <div class="stat-num">50+</div>
        <div class="stat-label">Initiatives Led</div>
      </div>
      <div class="stat">
        <div class="stat-num">10 Yrs</div>
        <div class="stat-label">Experience</div>
      </div>
      <div class="stat">
        <div class="stat-num">95%</div>
        <div class="stat-label">Stakeholder Satisfaction</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="container">
    <div class="section-header reveal">
      <div class="section-num">01</div>
      <h2 class="section-title">About <span>Me</span></h2>
    </div>
    <div class="about-grid reveal">
      <div class="about-card">
        <div class="about-role">Strategic Partnerships Professional</div>
        <div class="about-card-name">Spandana Manda</div>
        <div class="about-detail">
          <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M7 1.5A5.5 5.5 0 1 1 1.5 7 5.506 5.506 0 0 1 7 1.5zm0 1A4.5 4.5 0 1 0 11.5 7 4.505 4.505 0 0 0 7 2.5zM7 4v3.25l2.5 1.5-.5.866L6 7.75V4z" fill="currentColor"/></svg>
          10+ Years of Experience
        </div>
        <div class="about-detail">
          <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M7 .5a6.5 6.5 0 1 0 6.5 6.5A6.508 6.508 0 0 0 7 .5zm0 12A5.5 5.5 0 1 1 12.5 7 5.506 5.506 0 0 1 7 12.5zM7 3.25A.75.75 0 1 1 6.25 4 .75.75 0 0 1 7 3.25zM8 10H6V6h2z" fill="currentColor"/></svg>
          Atlanta, Georgia
        </div>
        <div class="about-detail">
          <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M11.5 2h-9A1.5 1.5 0 0 0 1 3.5v7A1.5 1.5 0 0 0 2.5 12h9A1.5 1.5 0 0 0 13 10.5v-7A1.5 1.5 0 0 0 11.5 2zm.5 8.5a.5.5 0 0 1-.5.5h-9a.5.5 0 0 1-.5-.5V5.2l4.628 3.3a.5.5 0 0 0 .572 0L12 5.197V10.5zm0-6.418L7 7.48 2 4.082V3.5A.5.5 0 0 1 2.5 3h9a.5.5 0 0 1 .5.5v.582z" fill="currentColor"/></svg>
          spandana150217@gmail.com
        </div>
        <div class="about-detail">
          <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M2.5 2h2l1 3-1.5 1s.5 2 3 4l1-1.5 3 1v2A1 1 0 0 1 10 13C5 13 1 9 1 3a1 1 0 0 1 1.5-.5z" stroke="currentColor" stroke-width="1" fill="currentColor" opacity=".7"/></svg>
          470-404-9388
        </div>
      </div>
      <div class="about-text">
        <p>
          I am a <strong>data-driven strategic partnerships professional</strong> with over a decade of experience turning CRM analytics and business intelligence into real revenue and real relationships. My work sits at the intersection of analysis and human connection — I build the pipeline, tell the story with data, and then follow through with genuine partner stewardship.
        </p>
        <p>
          Across technology, public sector, financial services, and healthcare, I have led 50+ business analysis initiatives resulting in <strong>$10M+ in combined cost savings and revenue optimization</strong>. I specialize in identifying untapped corporate opportunities, developing shared value proposals that resonate with a company's CSR and business goals, and translating complex datasets into compelling, executive-ready narratives.
        </p>
        <p>
          I am mission-driven by nature. I believe the strongest partnerships happen when both parties see themselves as genuine stakeholders in a shared outcome — not just sponsor and recipient, but co-architects of community impact.
        </p>
        <div class="skills-chips">
          <span class="chip">CRM Analytics</span>
          <span class="chip">Pipeline Development</span>
          <span class="chip">Power BI</span>
          <span class="chip">Shared Value Frameworks</span>
          <span class="chip">Corporate Proposals</span>
          <span class="chip">ROI Modeling</span>
          <span class="chip">KPI Dashboards</span>
          <span class="chip">Partner Stewardship</span>
          <span class="chip">Excel (Advanced)</span>
          <span class="chip">Salesforce</span>
          <span class="chip">SQL</span>
          <span class="chip">Tableau</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CASE STUDIES -->
<section id="work">
  <div class="container">
    <div class="section-header reveal">
      <div class="section-num">02</div>
      <h2 class="section-title">Work Samples &amp; <span>Case Studies</span></h2>
    </div>
    <div class="cases-grid reveal">

      <div class="case">
        <div class="case-tag">Environmental Analytics · IDNR</div>
        <div class="case-title">Analytics Platform Modernization &amp; Stakeholder Partnership</div>
        <div class="case-org">Illinois Dept. of Natural Resources — 2023–2025</div>
        <div class="case-body">
          Led end-to-end business analysis for a $2M+ environmental analytics platform modernization. Managed relationships with 25+ stakeholders across organizational units, conducting discovery sessions, mapping as-is/to-be processes, and delivering a cloud-based solution that transformed how the department used data. Built Power BI dashboards that automated executive KPI reporting, improving decision-making speed by 40% and achieving consistently high partner satisfaction across every sprint cycle.
        </div>
        <div class="case-metrics">
          <div class="metric"><div class="metric-val">$2M+</div><div class="metric-desc">Investment Justified</div></div>
          <div class="metric"><div class="metric-val">35%</div><div class="metric-desc">Cost Reduction</div></div>
          <div class="metric"><div class="metric-val">40%</div><div class="metric-desc">Faster Decisions</div></div>
        </div>
      </div>

      <div class="case">
        <div class="case-tag">Private Wealth · Varsity</div>
        <div class="case-title">Corporate Analytics Transformation &amp; Stakeholder Alignment</div>
        <div class="case-org">Varsity — Private Wealth Division — 2021–2022</div>
        <div class="case-body">
          Drove analytics transformation for a Private Wealth corporate division by conducting stakeholder interviews with portfolio managers, compliance officers, and senior leadership. Delivered an integrated reporting solution consolidating data from 8 source systems for 200+ corporate users. Implemented data quality monitoring that reduced reconciliation issues by 60%, achieving a 98% client satisfaction score post-deployment and generating lasting organizational trust.
        </div>
        <div class="case-metrics">
          <div class="metric"><div class="metric-val">45%</div><div class="metric-desc">Effort Reduced</div></div>
          <div class="metric"><div class="metric-val">60%</div><div class="metric-desc">Fewer Errors</div></div>
          <div class="metric"><div class="metric-val">98%</div><div class="metric-desc">Satisfaction</div></div>
        </div>
      </div>

      <div class="case">
        <div class="case-tag">Product Analytics · Wipro</div>
        <div class="case-title">Cloud Platform Analytics &amp; Cross-Functional Partnership</div>
        <div class="case-org">Wipro — 2019–2021</div>
        <div class="case-body">
          Defined product analytics strategy for a cloud networking platform serving 500K+ customers by gathering requirements from Product Management, Engineering, and Customer Success. Developed a BI reporting framework using Tableau and Snowflake that directly influenced product roadmap decisions across 10+ major feature releases. Conducted process analysis that identified inefficiencies and reduced incident response time by 50%.
        </div>
        <div class="case-metrics">
          <div class="metric"><div class="metric-val">500K+</div><div class="metric-desc">Customers Served</div></div>
          <div class="metric"><div class="metric-val">50%</div><div class="metric-desc">Faster Response</div></div>
          <div class="metric"><div class="metric-val">10+</div><div class="metric-desc">Releases Influenced</div></div>
        </div>
      </div>

      <div class="case">
        <div class="case-tag">Healthcare Compliance · Sitel Group</div>
        <div class="case-title">Fraud Detection Analytics &amp; Regulatory Partnership</div>
        <div class="case-org">Sitel Group — 2017–2019</div>
        <div class="case-body">
          Led business analysis for a fraud detection and claims analytics platform in the healthcare sector, coordinating requirements gathering across compliance, finance, and actuarial stakeholder groups. The resulting solution identified $3.5M in fraudulent activities and reduced regulatory report generation time by 40%. Achieved 100% HIPAA and CMS compliance across all reporting systems.
        </div>
        <div class="case-metrics">
          <div class="metric"><div class="metric-val">$3.5M</div><div class="metric-desc">Fraud Identified</div></div>
          <div class="metric"><div class="metric-val">100%</div><div class="metric-desc">Compliance</div></div>
          <div class="metric"><div class="metric-val">40%</div><div class="metric-desc">Time Saved</div></div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- DASHBOARDS -->
<section id="dashboards">
  <div class="container">
    <div class="section-header reveal">
      <div class="section-num">03</div>
      <h2 class="section-title">Analytics &amp; <span>Dashboard Expertise</span></h2>
    </div>
    <div class="dashboard-grid reveal">

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><rect x="2" y="10" width="3" height="8" fill="currentColor"/><rect x="7" y="6" width="3" height="12" fill="currentColor"/><rect x="12" y="2" width="3" height="16" fill="currentColor"/><rect x="17" y="8" width="3" height="10" fill="currentColor"/></svg>
        </div>
        <div class="dash-title">Corporate Pipeline Dashboard</div>
        <div class="dash-desc">CRM-driven pipeline tracking with KPI scorecards, conversion funnels, and revenue forecasting by segment and acquisition stage.</div>
        <div class="dash-bar-container">
          <div>
            <div class="dash-bar-label"><span>New Prospects</span><span>78%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:78%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Partner Retention</span><span>91%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:91%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Revenue Goal</span><span>94%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:94%"></div></div>
          </div>
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><circle cx="10" cy="10" r="8" stroke="currentColor" stroke-width="1.5"/><path d="M10 2a8 8 0 0 1 8 8" stroke="currentColor" stroke-width="4" stroke-linecap="round"/></svg>
        </div>
        <div class="dash-title">Partner Performance Scorecard</div>
        <div class="dash-desc">Partner health scores tracking engagement depth, CSR alignment, event activation, and stewardship touchpoints across all corporate accounts.</div>
        <div class="donut-wrap">
          <svg class="donut-svg" viewBox="0 0 36 36">
            <circle cx="18" cy="18" r="15.9" fill="none" stroke="rgba(255,255,255,0.08)" stroke-width="3"/>
            <circle cx="18" cy="18" r="15.9" fill="none" stroke="#c9a84c" stroke-width="3"
              stroke-dasharray="89 100" stroke-dashoffset="25" stroke-linecap="round"/>
            <text x="18" y="18" text-anchor="middle" dy=".4em" fill="#e8c97e" font-size="7" font-family="Cormorant Garamond, serif">89%</text>
          </svg>
        </div>
        <div class="dash-desc" style="text-align:center; margin-top:0.5rem; font-size:0.7rem;">Avg. Partner Health Score</div>
      </div>

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><path d="M2 14l5-5 4 4 7-9" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        </div>
        <div class="dash-title">Revenue Forecasting Model</div>
        <div class="dash-desc">Excel and Power BI-based forecasting models using historical donor trends, pipeline velocity, and sector analysis to project annual revenue outcomes.</div>
        <div class="dash-bar-container">
          <div>
            <div class="dash-bar-label"><span>Q1 Actual vs Target</span><span>104%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:100%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Q2 Forecast Accuracy</span><span>97%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:97%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Lapsed Reactivation</span><span>62%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:62%"></div></div>
          </div>
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><rect x="2" y="2" width="7" height="7" stroke="currentColor" stroke-width="1.5"/><rect x="11" y="2" width="7" height="7" stroke="currentColor" stroke-width="1.5"/><rect x="2" y="11" width="7" height="7" stroke="currentColor" stroke-width="1.5"/><rect x="11" y="11" width="7" height="7" stroke="currentColor" stroke-width="1.5"/></svg>
        </div>
        <div class="dash-title">CRM Analytics & Segmentation</div>
        <div class="dash-desc">Salesforce and Dynamics 365 data extraction and segmentation to identify warm prospects, lapsed donors, and untapped corporate sectors for outreach prioritization.</div>
        <div class="dash-bar-container">
          <div>
            <div class="dash-bar-label"><span>Healthcare Sector</span><span>85%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:85%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Technology Sector</span><span>71%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:71%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Financial Services</span><span>68%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:68%"></div></div>
          </div>
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><path d="M10 2l2.5 5 5.5.8-4 3.9.95 5.5L10 14.75l-4.95 2.45.95-5.5L2 7.8l5.5-.8z" stroke="currentColor" stroke-width="1.5" stroke-linejoin="round"/></svg>
        </div>
        <div class="dash-title">Impact Reporting Suite</div>
        <div class="dash-desc">Executive-ready impact reports and board presentations that translate corporate partnership outcomes into measurable community stories aligned with CSR objectives.</div>
        <div class="dash-bar-container">
          <div>
            <div class="dash-bar-label"><span>Stakeholder Satisfaction</span><span>95%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:95%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>On-Time Delivery</span><span>95%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:95%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>First-Pass Acceptance</span><span>98%</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:98%"></div></div>
          </div>
        </div>
      </div>

      <div class="dash-card">
        <div class="dash-icon">
          <svg width="20" height="20" fill="none" viewBox="0 0 20 20"><path d="M3 10a7 7 0 1 0 14 0A7 7 0 0 0 3 10zm7-5v5l3.5 2" stroke="currentColor" stroke-width="1.5" stroke-linecap="round"/></svg>
        </div>
        <div class="dash-title">Tools & Platforms</div>
        <div class="dash-desc">Full-stack analytics and partnership management toolkit across CRM, BI, cloud, and enterprise platforms.</div>
        <div class="dash-bar-container">
          <div>
            <div class="dash-bar-label"><span>Power BI / Tableau</span><span>Expert</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:95%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>Salesforce / Dynamics CRM</span><span>Advanced</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:88%"></div></div>
          </div>
          <div>
            <div class="dash-bar-label"><span>SQL / Excel / Python</span><span>Advanced</span></div>
            <div class="dash-bar-track"><div class="dash-bar-fill" style="width:90%"></div></div>
          </div>
        </div>
      </div>

    </div>
  </div>
</section>

<!-- CERTIFICATIONS & EDUCATION -->
<section id="certifications">
  <div class="container">
    <div class="section-header reveal">
      <div class="section-num">04</div>
      <h2 class="section-title">Credentials &amp; <span>Education</span></h2>
    </div>

    <div class="certs-grid reveal" style="margin-bottom: 3rem;">
      <div class="cert-card">
        <div class="cert-icon">PMI</div>
        <div class="cert-name">PMI-ACP</div>
        <div class="cert-org">Project Management Institute</div>
        <span class="cert-status active">Certified</span>
      </div>
      <div class="cert-card">
        <div class="cert-icon">CSM</div>
        <div class="cert-name">Certified Scrum Master</div>
        <div class="cert-org">Scrum Alliance</div>
        <span class="cert-status active">Certified</span>
      </div>
      <div class="cert-card">
        <div class="cert-icon">CBAP</div>
        <div class="cert-name">CBAP</div>
        <div class="cert-org">International Institute of Business Analysis</div>
        <span class="cert-status progress">In Progress</span>
      </div>
    </div>

    <div class="reveal">
      <div class="edu-card">
        <div class="edu-degree">M.S. in Management Information Systems</div>
        <div class="edu-school">University of Illinois Springfield — 2023–2024</div>
        <div class="edu-note">Graduate Certificates: Business Process Management · Business Analytics · IT Project Management</div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">MBA — Master of Business Administration</div>
        <div class="edu-school">Chaitanya Bharathi Institute of Technology, India — 2011–2013</div>
      </div>
      <div class="edu-card">
        <div class="edu-degree">B.Tech in Computer Science Engineering</div>
        <div class="edu-school">JNTU Hyderabad, India — 2007–2011</div>
      </div>
    </div>
  </div>
</section>

<!-- TESTIMONIALS -->
<section id="testimonials">
  <div class="container">
    <div class="section-header reveal">
      <div class="section-num">05</div>
      <h2 class="section-title">What People <span>Say</span></h2>
    </div>
    <div class="testimonials-grid reveal">
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Spandana has an extraordinary ability to turn raw CRM data into partnership strategy. She doesn't just report numbers — she explains what they mean for our relationships and our revenue. Her dashboards changed how our leadership team makes decisions.</p>
        <div class="testi-author">
          <div class="testi-avatar">DM</div>
          <div>
            <div class="testi-name">Director of Management</div>
            <div class="testi-role">Illinois Dept. of Natural Resources</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">She consistently exceeded our expectations on stakeholder engagement. Her proposals were clear, compelling, and always framed around what mattered most to each partner. She has a natural gift for understanding what motivates a corporate relationship.</p>
        <div class="testi-author">
          <div class="testi-avatar">VP</div>
          <div>
            <div class="testi-name">Vice President, Partnerships</div>
            <div class="testi-role">Varsity — Private Wealth Division</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Spandana is one of the most analytically rigorous and relationship-savvy professionals I've worked with. She understands that data is just a tool — it's the story you tell with it that builds trust and drives commitment.</p>
        <div class="testi-author">
          <div class="testi-avatar">PM</div>
          <div>
            <div class="testi-name">Product Manager</div>
            <div class="testi-role">Wipro — Cloud Networking Platform</div>
          </div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-quote">"</div>
        <p class="testi-text">Her ability to manage cross-functional collaboration while maintaining momentum on deliverables is exceptional. She kept 8+ teams aligned, stakeholders informed, and the project on track — all while building genuine rapport with every partner involved.</p>
        <div class="testi-author">
          <div class="testi-avatar">TL</div>
          <div>
            <div class="testi-name">Technology Lead</div>
            <div class="testi-role">Finserv — Enterprise Analytics</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <div class="container">
    <div class="section-header reveal" style="justify-content:center; border:none; margin-bottom:1rem;">
      <h2 class="section-title" style="color:#fff; text-align:center;">Let's <span>Connect</span></h2>
    </div>
    <p class="contact-sub reveal">
      Ready to discuss how data-driven partnership strategy and mission-aligned relationship management can drive meaningful impact for your organization.
    </p>
    <div class="contact-links reveal">
      <a href="mailto:spandana150217@gmail.com" class="contact-btn primary">
        <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M1.5 3h11A1 1 0 0 1 13.5 4v6a1 1 0 0 1-1 1h-11a1 1 0 0 1-1-1V4a1 1 0 0 1 1-1zm0 0 5.5 4.5L12.5 3" stroke="currentColor" stroke-width="1.1" stroke-linejoin="round"/></svg>
        Send an Email
      </a>
      <a href="tel:4704049388" class="contact-btn secondary">
        <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M2.5 2h2l1 3-1.5 1s.5 2 3 4l1-1.5 3 1v2a1 1 0 0 1-1.5.5C5 13 1 9 1 3a1 1 0 0 1 1.5-.5z" stroke="currentColor" stroke-width="1" fill="currentColor" opacity=".8"/></svg>
        470-404-9388
      </a>
      <a href="#work" class="contact-btn secondary">
        <svg width="14" height="14" fill="none" viewBox="0 0 14 14"><path d="M2 7h10M7 2l5 5-5 5" stroke="currentColor" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/></svg>
        View Case Studies
      </a>
    </div>
  </div>
</section>

<footer>
  &copy; 2026 Spandana Manda &nbsp;·&nbsp; Strategic Partnerships &amp; Analytics Professional &nbsp;·&nbsp; Atlanta, GA
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((e, i) => {
      if (e.isIntersecting) {
        setTimeout(() => e.target.classList.add('visible'), i * 80);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(el => observer.observe(el));
</script>
</body>
</html>
