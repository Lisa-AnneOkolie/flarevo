<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Flarevo — Strategic Management Services</title>
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display:ital@0;1&family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;1,9..40,300&display=swap" rel="stylesheet" />
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  :root {
    --orange: #F97316;
    --pink: #E8357A;
    --purple: #7C3AED;
    --purple-dark: #2D1B69;
    --ink: #1A1033;
    --ink-muted: #6B7280;
    --surface: #FAF9FC;
    --white: #FFFFFF;
    --grad: linear-gradient(135deg, #F97316 0%, #E8357A 50%, #7C3AED 100%);
    --grad-soft: linear-gradient(135deg, rgba(249,115,22,0.10) 0%, rgba(232,53,122,0.10) 50%, rgba(124,58,237,0.10) 100%);
    --border: rgba(124,58,237,0.12);
    --border-strong: rgba(124,58,237,0.25);
    --serif: 'DM Serif Display', Georgia, serif;
    --sans: 'DM Sans', system-ui, sans-serif;
  }
  html { scroll-behavior: smooth; }
  body { font-family: var(--sans); background: var(--surface); color: var(--ink); font-size: 16px; line-height: 1.7; -webkit-font-smoothing: antialiased; }

  /* NAV */
  nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; display: flex; align-items: center; justify-content: space-between; padding: 1rem 5vw; background: rgba(250,249,252,0.93); backdrop-filter: blur(12px); border-bottom: 1px solid var(--border); }
  .nav-logo { display: flex; align-items: center; text-decoration: none; }
  .nav-logo img { height: 48px; width: auto; }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a { font-size: 0.875rem; color: var(--ink-muted); text-decoration: none; transition: color 0.2s; }
  .nav-links a:hover { color: var(--purple); }
  .nav-cta { font-size: 0.875rem; font-weight: 500; background: var(--grad); color: var(--white); border: none; padding: 0.6rem 1.5rem; cursor: pointer; text-decoration: none; border-radius: 2px; transition: opacity 0.2s; }
  .nav-cta:hover { opacity: 0.88; }

  /* HERO */
  .hero { min-height: 100vh; display: flex; flex-direction: column; justify-content: center; padding: 8rem 5vw 5rem; max-width: 1100px; margin: 0 auto; }
  .hero-eyebrow { display: inline-flex; align-items: center; font-size: 0.75rem; font-weight: 500; letter-spacing: 0.14em; text-transform: uppercase; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; margin-bottom: 1.75rem; }
  .hero h1 { font-family: var(--serif); font-size: clamp(3rem, 7vw, 5.5rem); line-height: 1.05; letter-spacing: -0.02em; color: var(--ink); max-width: 780px; margin-bottom: 1.5rem; }
  .hero h1 em { font-style: italic; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
  .hero-sub { font-size: 1.1rem; color: var(--ink-muted); max-width: 520px; margin-bottom: 2.5rem; font-weight: 300; line-height: 1.8; }
  .hero-actions { display: flex; align-items: center; gap: 1.5rem; flex-wrap: wrap; }
  .btn-primary { background: var(--grad); color: var(--white); padding: 0.9rem 2.2rem; font-size: 0.9rem; font-weight: 500; font-family: var(--sans); border: none; cursor: pointer; text-decoration: none; border-radius: 2px; transition: opacity 0.2s; display: inline-block; }
  .btn-primary:hover { opacity: 0.88; }
  .btn-ghost { color: var(--purple); font-size: 0.9rem; font-weight: 400; text-decoration: none; border-bottom: 1px solid var(--border-strong); padding-bottom: 2px; transition: color 0.2s; }
  .btn-ghost:hover { color: var(--pink); }
  .hero-stripe { margin-top: 5rem; display: flex; align-items: center; gap: 2.5rem; flex-wrap: wrap; }
  .stripe-item { display: flex; flex-direction: column; gap: 2px; }
  .stripe-num { font-family: var(--serif); font-size: 1.6rem; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; line-height: 1; }
  .stripe-label { font-size: 0.8rem; color: var(--ink-muted); letter-spacing: 0.04em; }
  .stripe-div { width: 1px; height: 44px; background: var(--border-strong); }

  /* SECTION LABEL */
  .section-label { font-size: 0.7rem; font-weight: 500; letter-spacing: 0.16em; text-transform: uppercase; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; margin-bottom: 1rem; display: inline-block; }
  section { padding: 5rem 5vw; max-width: 1100px; margin: 0 auto; }

  /* ABOUT */
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: center; }
  .about-grid h2 { font-family: var(--serif); font-size: clamp(2rem, 3.5vw, 2.8rem); line-height: 1.15; letter-spacing: -0.015em; margin-bottom: 1.25rem; }
  .about-grid p { color: var(--ink-muted); font-weight: 300; margin-bottom: 1rem; }
  .about-visual { background: var(--grad-soft); padding: 2.5rem; border: 1px solid var(--border); border-radius: 4px; }
  .about-tag { font-family: var(--serif); font-size: 1.05rem; font-style: italic; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; border-bottom: 1px solid var(--border); padding-bottom: 1rem; margin-bottom: 1rem; }
  .about-list { list-style: none; }
  .about-list li { font-size: 0.875rem; color: var(--ink-muted); padding: 0.55rem 0; border-bottom: 0.5px solid var(--border); display: flex; align-items: center; gap: 0.75rem; }
  .about-list li::before { content: ''; display: block; width: 6px; height: 6px; background: var(--grad); border-radius: 50%; flex-shrink: 0; }

  /* SOCIAL LINKS */
  .social-bar { display: flex; gap: 1.25rem; margin-top: 1.5rem; flex-wrap: wrap; }
  .social-link { display: inline-flex; align-items: center; gap: 0.45rem; font-size: 0.8rem; font-weight: 500; color: var(--purple); text-decoration: none; border: 1px solid var(--border-strong); padding: 0.35rem 0.85rem; border-radius: 20px; transition: all 0.2s; letter-spacing: 0.02em; }
  .social-link:hover { background: var(--grad); color: var(--white); border-color: transparent; }

  /* SERVICES */
  .services-bg { background: var(--ink); padding: 5rem 5vw; }
  .services-inner { max-width: 1100px; margin: 0 auto; }
  .services-bg .section-label { background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
  .services-bg h2 { font-family: var(--serif); font-size: clamp(2rem, 3.5vw, 2.8rem); color: var(--white); margin-bottom: 3rem; line-height: 1.15; letter-spacing: -0.015em; }
  .services-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 1px; background: rgba(255,255,255,0.08); border: 1px solid rgba(255,255,255,0.08); }
  .service-card { background: var(--ink); padding: 2rem 1.75rem; transition: background 0.2s; }
  .service-card:hover { background: #231545; }
  .service-num { font-size: 0.7rem; letter-spacing: 0.12em; font-weight: 500; margin-bottom: 1.25rem; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
  .service-title { font-family: var(--serif); font-size: 1.3rem; color: var(--white); margin-bottom: 0.75rem; line-height: 1.25; }
  .service-desc { font-size: 0.875rem; color: rgba(255,255,255,0.5); font-weight: 300; line-height: 1.7; }
  .service-tags { margin-top: 1.25rem; display: flex; flex-wrap: wrap; gap: 0.4rem; }
  .service-tag { font-size: 0.7rem; letter-spacing: 0.08em; color: #E8357A; border: 0.5px solid rgba(232,53,122,0.35); padding: 0.25rem 0.6rem; border-radius: 2px; }

  /* PROCESS */
  .process-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); }
  .process-step { padding: 2rem 2rem 2rem 0; border-right: 1px solid var(--border); }
  .process-step:last-child { border-right: none; }
  .process-step:not(:first-child) { padding-left: 2rem; }
  .process-n { font-family: var(--serif); font-size: 2.5rem; color: #ddd; line-height: 1; margin-bottom: 0.75rem; }
  .process-title { font-weight: 500; font-size: 1rem; color: var(--ink); margin-bottom: 0.5rem; }
  .process-desc { font-size: 0.875rem; color: var(--ink-muted); font-weight: 300; line-height: 1.6; }

  /* PACKAGES */
  .packages-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); gap: 1.5rem; margin-top: 2.5rem; }
  .package-card { border: 1px solid var(--border); padding: 2rem; background: var(--white); position: relative; transition: border-color 0.2s, transform 0.2s; border-radius: 4px; }
  .package-card:hover { border-color: var(--pink); transform: translateY(-3px); }
  .package-card.featured { border-color: var(--purple); background: var(--grad-soft); }
  .pkg-badge { position: absolute; top: -1px; left: 2rem; background: var(--grad); color: var(--white); font-size: 0.65rem; font-weight: 500; letter-spacing: 0.1em; text-transform: uppercase; padding: 0.25rem 0.75rem; border-radius: 0 0 4px 4px; }
  .pkg-name { font-family: var(--serif); font-size: 1.4rem; color: var(--ink); margin-bottom: 0.4rem; margin-top: 0.5rem; }
  .pkg-sub { font-size: 0.8rem; color: var(--ink-muted); margin-bottom: 1.25rem; font-weight: 300; }
  .pkg-price { font-family: var(--serif); font-size: 2rem; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; margin-bottom: 1.25rem; line-height: 1; }
  .pkg-price span { font-size: 0.9rem; color: var(--ink-muted); font-family: var(--sans); -webkit-text-fill-color: var(--ink-muted); }
  .pkg-features { list-style: none; margin-bottom: 1.75rem; }
  .pkg-features li { font-size: 0.875rem; color: var(--ink-muted); padding: 0.4rem 0; border-bottom: 0.5px solid var(--border); display: flex; align-items: flex-start; gap: 0.6rem; font-weight: 300; }
  .pkg-features li::before { content: '✓'; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; font-weight: 700; flex-shrink: 0; }
  .pkg-cta { display: block; width: 100%; text-align: center; padding: 0.75rem; font-family: var(--sans); font-size: 0.875rem; font-weight: 500; letter-spacing: 0.04em; border: 1px solid var(--purple); background: transparent; color: var(--purple); cursor: pointer; text-decoration: none; border-radius: 2px; transition: all 0.2s; }
  .pkg-cta:hover { background: var(--grad); color: var(--white); border-color: transparent; }
  .package-card.featured .pkg-cta { background: var(--grad); color: var(--white); border-color: transparent; }

  /* TESTIMONIALS */
  .testi-bg { background: var(--ink); padding: 5rem 5vw; }
  .testi-inner { max-width: 1100px; margin: 0 auto; }
  .testi-bg .section-label { background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; }
  .testi-bg h2 { font-family: var(--serif); font-size: clamp(2rem, 3.5vw, 2.8rem); color: var(--white); margin-bottom: 3rem; line-height: 1.15; }
  .testi-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 1.5rem; }
  .testi-card { background: rgba(255,255,255,0.04); border: 1px solid rgba(255,255,255,0.08); padding: 2rem; border-radius: 4px; transition: border-color 0.2s; }
  .testi-card:hover { border-color: rgba(232,53,122,0.4); }
  .testi-quote { font-family: var(--serif); font-size: 1.05rem; font-style: italic; color: rgba(255,255,255,0.85); line-height: 1.7; margin-bottom: 1.5rem; }
  .testi-quote::before { content: '\201C'; font-size: 2rem; background: var(--grad); -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; line-height: 0; vertical-align: -0.5rem; margin-right: 0.2rem; }
  .testi-author { display: flex; align-items: center; gap: 0.75rem; }
  .testi-avatar { width: 40px; height: 40px; border-radius: 50%; background: var(--grad); display: flex; align-items: center; justify-content: center; font-family: var(--serif); font-size: 1rem; color: white; flex-shrink: 0; }
  .testi-name { font-size: 0.875rem; font-weight: 500; color: var(--white); }
  .testi-role { font-size: 0.78rem; color: rgba(255,255,255,0.45); }
  .testi-stars { color: #F97316; font-size: 0.8rem; letter-spacing: 0.1em; margin-bottom: 1rem; }

  /* CTA BANNER */
  .cta-banner { background: var(--grad); padding: 5rem 5vw; text-align: center; }
  .cta-banner h2 { font-family: var(--serif); font-size: clamp(1.8rem, 3vw, 2.5rem); color: var(--white); margin-bottom: 0.75rem; }
  .cta-banner p { color: rgba(255,255,255,0.85); font-weight: 300; margin-bottom: 2rem; font-size: 1.05rem; }
  .btn-white { background: var(--white); color: var(--purple-dark); padding: 0.9rem 2.2rem; font-size: 0.9rem; font-weight: 600; font-family: var(--sans); border: none; cursor: pointer; text-decoration: none; border-radius: 2px; transition: opacity 0.2s; display: inline-block; }
  .btn-white:hover { opacity: 0.92; }
  .btn-outline-white { color: var(--white); font-size: 0.9rem; text-decoration: none; border-bottom: 1px solid rgba(255,255,255,0.5); padding-bottom: 2px; margin-left: 1.5rem; }

  /* WHATSAPP */
  .wa-float { position: fixed; bottom: 2rem; right: 2rem; z-index: 999; background: #25D366; color: #fff; width: 56px; height: 56px; border-radius: 50%; display: flex; align-items: center; justify-content: center; box-shadow: 0 4px 16px rgba(37,211,102,0.4); text-decoration: none; transition: transform 0.2s; }
  .wa-float:hover { transform: scale(1.08); }
  .wa-tooltip { position: absolute; right: 68px; top: 50%; transform: translateY(-50%); background: var(--ink); color: #fff; font-size: 0.78rem; white-space: nowrap; padding: 0.35rem 0.75rem; border-radius: 2px; pointer-events: none; opacity: 0; transition: opacity 0.2s; }
  .wa-float:hover .wa-tooltip { opacity: 1; }

  /* FORM */
  .form-section { background: var(--white); border-top: 1px solid var(--border); padding: 5rem 5vw; }
  .form-inner { max-width: 680px; margin: 0 auto; }
  .form-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-top: 2rem; }
  .form-group { display: flex; flex-direction: column; gap: 0.4rem; }
  .form-group.full { grid-column: 1 / -1; }
  .form-group label { font-size: 0.78rem; font-weight: 500; letter-spacing: 0.06em; text-transform: uppercase; color: var(--ink-muted); }
  .form-group input, .form-group select, .form-group textarea { font-family: var(--sans); font-size: 0.95rem; padding: 0.75rem 1rem; border: 1px solid var(--border); background: var(--surface); color: var(--ink); outline: none; transition: border-color 0.2s; resize: vertical; border-radius: 2px; }
  .form-group input:focus, .form-group select:focus, .form-group textarea:focus { border-color: var(--purple); }
  .form-submit { margin-top: 1.25rem; width: 100%; padding: 0.9rem; background: var(--grad); color: var(--white); border: none; font-family: var(--sans); font-size: 0.95rem; font-weight: 500; cursor: pointer; border-radius: 2px; transition: opacity 0.2s; }
  .form-submit:hover { opacity: 0.88; }
  .form-submit:disabled { opacity: 0.5; cursor: not-allowed; }
  .form-success { display: none; background: #f0faf4; border: 1px solid #25D366; padding: 1.25rem; margin-top: 1rem; border-radius: 2px; font-size: 0.9rem; color: #0a7a3a; text-align: center; }

  /* FOOTER */
  footer { background: var(--ink); padding: 3rem 5vw 2rem; }
  .footer-top { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 2rem; margin-bottom: 2rem; padding-bottom: 2rem; border-bottom: 1px solid rgba(255,255,255,0.08); }
  .footer-logo img { height: 40px; width: auto; margin-bottom: 0.75rem; }
  .footer-tagline { font-size: 0.82rem; color: rgba(255,255,255,0.4); max-width: 220px; }
  .footer-socials { display: flex; gap: 1rem; flex-wrap: wrap; }
  .footer-social { font-size: 0.8rem; color: rgba(255,255,255,0.5); text-decoration: none; border: 1px solid rgba(255,255,255,0.12); padding: 0.3rem 0.8rem; border-radius: 20px; transition: all 0.2s; }
  .footer-social:hover { background: var(--grad); color: white; border-color: transparent; }
  .footer-bottom { display: flex; justify-content: space-between; flex-wrap: wrap; gap: 0.5rem; }
  .footer-bottom p { font-size: 0.78rem; color: rgba(255,255,255,0.3); }

  @media (max-width: 768px) {
    .about-grid { grid-template-columns: 1fr; gap: 2rem; }
    .nav-links { display: none; }
    .hero-stripe { gap: 1.5rem; }
    .process-grid { grid-template-columns: 1fr; }
    .process-step { border-right: none; border-bottom: 1px solid var(--border); padding: 1.5rem 0; }
    .process-step:not(:first-child) { padding-left: 0; }
    .form-grid { grid-template-columns: 1fr; }
    .footer-top { flex-direction: column; }
  }
</style>
</head>
<body>

<nav>
  <a href="#" class="nav-logo"><img src="flarevo-logo.png" alt="Flarevo" /></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#packages">Packages</a></li>
    <li><a href="#contact-form">Contact</a></li>
  </ul>
  <a href="#contact-form" class="nav-cta">Work with us</a>
</nav>

<div style="max-width:1100px; margin:0 auto; padding: 0 5vw;">
  <div class="hero">
    <div class="hero-eyebrow">Strategic Management Services</div>
    <h1>Your brand, built<br>with <em>intention.</em></h1>
    <p class="hero-sub">Flarevo helps businesses and personal brands grow through sharp strategy, distinctive content, and brand direction that actually converts.</p>
    <div class="hero-actions">
      <a href="#contact-form" class="btn-primary">Start a project</a>
      <a href="#services" class="btn-ghost">See what we do</a>
    </div>
    <div class="hero-stripe">
      <div class="stripe-item"><span class="stripe-num">Done for you</span><span class="stripe-label">Full execution</span></div>
      <div class="stripe-div"></div>
      <div class="stripe-item"><span class="stripe-num">Consulting</span><span class="stripe-label">Strategy and guidance</span></div>
      <div class="stripe-div"></div>
      <div class="stripe-item"><span class="stripe-num">Lagos, NG</span><span class="stripe-label">Serving clients globally</span></div>
    </div>
  </div>
</div>

<section id="about">
  <div class="about-grid">
    <div>
      <div class="section-label">About Flarevo</div>
      <h2>Strategy that moves the needle.</h2>
      <p>Flarevo is a strategic management firm founded to help businesses stop guessing and start growing. We combine brand audits, creative direction, and content strategy into one cohesive approach.</p>
      <p>Whether you are a startup building from scratch or an established brand that needs a reset, we come in, assess what is working, and build what is not.</p>
      <div class="social-bar">
        <a href="https://instagram.com/flarevo" target="_blank" class="social-link">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
          @flarevo
        </a>
        <a href="https://twitter.com/flarevo" target="_blank" class="social-link">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-4.714-6.231-5.401 6.231H2.744l7.73-8.835L1.254 2.25H8.08l4.253 5.622zm-1.161 17.52h1.833L7.084 4.126H5.117z"/></svg>
          @flarevo
        </a>
        <a href="https://linkedin.com/company/flarevo" target="_blank" class="social-link">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
          flarevo
        </a>
        <a href="mailto:flarevostudio@gmail.com" class="social-link">
          <svg width="14" height="14" viewBox="0 0 24 24" fill="currentColor"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.91 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
          flarevostudio@gmail.com
        </a>
      </div>
    </div>
    <div class="about-visual">
      <div class="about-tag">"We don't just manage your brand, we engineer its direction."</div>
      <ul class="about-list">
        <li>Mid-range pricing, professional quality, accessible investment</li>
        <li>Both done for you and consulting models available</li>
        <li>Small businesses, personal brands, and corporate clients</li>
        <li>Founded by Lisa-Anne Okolie, strategist and brand director</li>
      </ul>
    </div>
  </div>
</section>

<div class="services-bg" id="services">
  <div class="services-inner">
    <div class="section-label">What we do</div>
    <h2>Six ways we grow<br>your brand.</h2>
    <div class="services-grid">
      <div class="service-card"><div class="service-num">01</div><div class="service-title">Brand Audit</div><p class="service-desc">A full diagnostic of your brand's current position, identity, messaging, digital presence, and competitive gap analysis.</p><div class="service-tags"><span class="service-tag">Audit</span><span class="service-tag">Analysis</span><span class="service-tag">Report</span></div></div>
      <div class="service-card"><div class="service-num">02</div><div class="service-title">Social Media Management</div><p class="service-desc">End to end management of your social presence including content creation, scheduling, community engagement, and performance reporting.</p><div class="service-tags"><span class="service-tag">Instagram</span><span class="service-tag">Meta Ads</span><span class="service-tag">Strategy</span></div></div>
      <div class="service-card"><div class="service-num">03</div><div class="service-title">Content Strategy</div><p class="service-desc">A content roadmap aligned to your business goals including content pillars, editorial calendars, and channel specific direction.</p><div class="service-tags"><span class="service-tag">Planning</span><span class="service-tag">Direction</span><span class="service-tag">Calendars</span></div></div>
      <div class="service-card"><div class="service-num">04</div><div class="service-title">Brand Strategy</div><p class="service-desc">Positioning, voice, visual identity direction, and messaging frameworks that make your brand instantly recognisable and trusted.</p><div class="service-tags"><span class="service-tag">Positioning</span><span class="service-tag">Voice</span><span class="service-tag">Identity</span></div></div>
      <div class="service-card"><div class="service-num">05</div><div class="service-title">Growth Strategy</div><p class="service-desc">Data informed growth planning including paid and organic channel strategy, audience development, and conversion optimisation.</p><div class="service-tags"><span class="service-tag">Google Ads</span><span class="service-tag">Meta Ads</span><span class="service-tag">Growth</span></div></div>
      <div class="service-card"><div class="service-num">06</div><div class="service-title">Strategy Consulting</div><p class="service-desc">Advisory engagements for founders and teams who need an outside strategic mind, including workshops, planning sessions, and ongoing guidance.</p><div class="service-tags"><span class="service-tag">Advisory</span><span class="service-tag">Workshops</span><span class="service-tag">Consulting</span></div></div>
    </div>
  </div>
</div>

<section>
  <div class="section-label">How it works</div>
  <h2 style="font-family:var(--serif);font-size:clamp(1.8rem,3vw,2.4rem);letter-spacing:-0.015em;margin-bottom:2.5rem;line-height:1.2;">Simple. Focused. Effective.</h2>
  <div class="process-grid">
    <div class="process-step"><div class="process-n">1</div><div class="process-title">Discovery call</div><p class="process-desc">We learn about your business, goals, and what is not working. No fluff, just clarity.</p></div>
    <div class="process-step"><div class="process-n">2</div><div class="process-title">Audit and proposal</div><p class="process-desc">We audit your current presence and deliver a tailored proposal with scope, timeline, and pricing.</p></div>
    <div class="process-step"><div class="process-n">3</div><div class="process-title">Strategy build</div><p class="process-desc">We develop your strategy, content direction, and brand frameworks ready for execution.</p></div>
    <div class="process-step"><div class="process-n">4</div><div class="process-title">Execute and grow</div><p class="process-desc">We execute, monitor, and refine with regular check ins and performance reporting.</p></div>
  </div>
</section>

<section id="packages">
  <div class="section-label">Packages</div>
  <h2 style="font-family:var(--serif);font-size:clamp(1.8rem,3vw,2.4rem);letter-spacing:-0.015em;line-height:1.2;">Choose your engagement.</h2>
  <p style="color:var(--ink-muted);font-weight:300;margin-top:0.5rem;">All prices are starting points. Custom scopes available on request.</p>
  <div class="packages-grid">
    <div class="package-card">
      <div class="pkg-name">Starter</div>
      <div class="pkg-sub">For new brands and small businesses</div>
      <div class="pkg-price">₦100,000 <span>/ month</span></div>
      <ul class="pkg-features">
        <li>Social media management (2 platforms)</li>
        <li>12 posts per month</li>
        <li>Basic content strategy</li>
        <li>Monthly performance report</li>
        <li>1 strategy session per month</li>
      </ul>
      <a href="#" class="pkg-cta" onclick="openWA('starter'); return false;">Get started</a>
    </div>
    <div class="package-card featured">
      <div class="pkg-badge">Most popular</div>
      <div class="pkg-name">Growth</div>
      <div class="pkg-sub">For brands ready to scale</div>
      <div class="pkg-price">₦150,000 <span>/ month</span></div>
      <ul class="pkg-features">
        <li>Social media management (3 platforms)</li>
        <li>20 posts and stories per month</li>
        <li>Full content and brand strategy</li>
        <li>Paid ads management (Meta and Google)</li>
        <li>Brand audit included</li>
        <li>Bi-weekly strategy sessions</li>
        <li>Performance dashboard</li>
      </ul>
      <a href="#" class="pkg-cta" onclick="openWA('growth'); return false;">Get started</a>
    </div>
    <div class="package-card">
      <div class="pkg-name">Advisory</div>
      <div class="pkg-sub">Consulting and strategy only</div>
      <div class="pkg-price">₦50,000 <span>/ session</span></div>
      <ul class="pkg-features">
        <li>90 minute strategy session</li>
        <li>Brand or content audit</li>
        <li>Written strategy document</li>
        <li>30 day follow up support</li>
        <li>Retainer available on request</li>
      </ul>
      <a href="#" class="pkg-cta" onclick="openWA('advisory'); return false;">Book a session</a>
    </div>
  </div>
</section>

<div class="testi-bg" id="testimonials">
  <div class="testi-inner">
    <div class="section-label">Testimonials</div>
    <h2>What our clients say.</h2>
    <div class="testi-grid">
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-quote">Flarevo completely transformed how we show up online. Our engagement tripled within the first two months and we finally have a brand that feels like us.</p>
        <div class="testi-author">
          <div class="testi-avatar">A</div>
          <div><div class="testi-name">Adaeze Nwosu</div><div class="testi-role">Founder, Bloom Skincare</div></div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-quote">The strategy session alone was worth every kobo. Lisa-Anne gave us clarity we had been chasing for months. We walked out with a real plan.</p>
        <div class="testi-author">
          <div class="testi-avatar">K</div>
          <div><div class="testi-name">Kelechi Eze</div><div class="testi-role">CEO, TechBridge Lagos</div></div>
        </div>
      </div>
      <div class="testi-card">
        <div class="testi-stars">★★★★★</div>
        <p class="testi-quote">Working with Flarevo felt like having a full marketing team in our corner. Professional, creative, and genuinely invested in our growth.</p>
        <div class="testi-author">
          <div class="testi-avatar">T</div>
          <div><div class="testi-name">Temi Adeyemo</div><div class="testi-role">Personal Brand Coach</div></div>
        </div>
      </div>
    </div>
  </div>
</div>

<div class="cta-banner" id="contact">
  <h2>Ready to build something real?</h2>
  <p>Let's have a conversation about where your brand is and where it needs to go.</p>
  <a href="#contact-form" class="btn-white">Fill in the contact form</a>
  <a href="https://wa.me/2348148873623?text=Hi%20Flarevo%2C%20I%27d%20like%20to%20discuss%20a%20project" target="_blank" class="btn-outline-white">or chat on WhatsApp</a>
</div>

<a href="https://wa.me/2348148873623?text=Hi%20Flarevo%2C%20I%27d%20like%20to%20discuss%20a%20project" target="_blank" class="wa-float" aria-label="Chat on WhatsApp">
  <span class="wa-tooltip">Chat on WhatsApp</span>
  <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/></svg>
</a>

<div class="form-section" id="contact-form">
  <div class="form-inner">
    <div class="section-label">Get in touch</div>
    <h2 style="font-family:var(--serif);font-size:clamp(1.8rem,3vw,2.4rem);letter-spacing:-0.015em;line-height:1.2;margin-bottom:0.5rem;">Let's talk about your brand.</h2>
    <p style="color:var(--ink-muted);font-weight:300;font-size:1rem;">Fill in the form and we will get back to you within 24 hours.</p>
    <form id="contactForm" class="form-grid" onsubmit="handleSubmit(event)">
      <div class="form-group"><label>Your name</label><input type="text" id="fname" placeholder="e.g. Amaka Obi" required /></div>
      <div class="form-group"><label>Email address</label><input type="email" id="femail" placeholder="you@example.com" required /></div>
      <div class="form-group"><label>WhatsApp / Phone</label><input type="tel" id="fphone" placeholder="08XXXXXXXXX" /></div>
      <div class="form-group"><label>Service interested in</label>
        <select id="fservice" required>
          <option value="" disabled selected>Select a service</option>
          <option>Social Media Management</option>
          <option>Brand Audit</option>
          <option>Content Strategy</option>
          <option>Brand Strategy</option>
          <option>Growth Strategy</option>
          <option>Strategy Consulting</option>
          <option>Not sure yet, let's talk</option>
        </select>
      </div>
      <div class="form-group full"><label>Tell us about your project</label><textarea id="fmsg" rows="4" placeholder="What is your brand, what are you trying to achieve, and what is not working right now?" required></textarea></div>
      <div class="form-group full">
        <button type="submit" class="form-submit" id="submitBtn">Send enquiry</button>
        <div class="form-success" id="formSuccess">Message sent! We will be in touch within 24 hours. You can also reach us directly on WhatsApp.</div>
      </div>
    </form>
  </div>
</div>

<footer>
  <div class="footer-top">
    <div>
      <img src="flarevo-logo.png" alt="Flarevo" style="height:44px;width:auto;margin-bottom:0.75rem;" />
      <p class="footer-tagline">Strategic Management Services. Lagos, Nigeria. Serving clients globally.</p>
    </div>
    <div>
      <p style="font-size:0.78rem;color:rgba(255,255,255,0.4);margin-bottom:0.75rem;letter-spacing:0.06em;text-transform:uppercase;">Follow us</p>
      <div class="footer-socials">
        <a href="https://instagram.com/flarevo" target="_blank" class="footer-social">Instagram</a>
        <a href="https://twitter.com/theflarevo" target="_blank" class="footer-social">Twitter</a>
        <a href="https://linkedin.com/company/flarevo" target="_blank" class="footer-social">LinkedIn</a>
        <a href="mailto:flarevostudio@gmail.com" class="footer-social">Email us</a>
      </div>
    </div>
  </div>
  <div class="footer-bottom">
    <p>© 2026 Flarevo. All rights reserved.</p>
    <p>flarevostudio@gmail.com</p>
  </div>
</footer>

<script>
var waMessages = {
  starter: "Hi Flarevo! I am interested in the Starter Package (₦100,000/month).\n\nCould you share more details and let me know how we can get started?",
  growth: "Hi Flarevo! I am interested in the Growth Package (₦150,000/month).\n\nI am looking to scale my brand and would love to discuss next steps. When can we talk?",
  advisory: "Hi Flarevo! I would like to book an Advisory Session (₦50,000/session).\n\nCould you let me know your available dates so we can schedule a call?"
};

function openWA(pkg) {
  var msg = encodeURIComponent(waMessages[pkg]);
  window.open('https://wa.me/2348148873623?text=' + msg, '_blank');
}

function handleSubmit(e) {
  e.preventDefault();
  var btn = document.getElementById('submitBtn');
  var success = document.getElementById('formSuccess');
  var form = document.getElementById('contactForm');
  var name = document.getElementById('fname').value;
  var email = document.getElementById('femail').value;
  var phone = document.getElementById('fphone').value;
  var service = document.getElementById('fservice').value;
  var message = document.getElementById('fmsg').value;
  btn.disabled = true;
  btn.textContent = 'Sending...';
  var waMsg = encodeURIComponent("New enquiry from Flarevo website:\n\nName: " + name + "\nEmail: " + email + "\nPhone: " + (phone || 'Not provided') + "\nService: " + service + "\n\nMessage:\n" + message);
  setTimeout(function() {
    form.style.display = 'none';
    success.style.display = 'block';
    window.open('https://wa.me/2348148873623?text=' + waMsg, '_blank');
  }, 800);
}
</script>
</body>
</html>
