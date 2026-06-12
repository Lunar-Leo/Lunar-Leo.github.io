<html lang="de">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Schreinerei Toni Audino – Nürnberg</title>
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400&family=Inter:wght@300;400;500;600&display=swap" rel="stylesheet" />
  <style>
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

    :root {
      --oak:     #8B6F47;
      --oak-dark:#5C4530;
      --cream:   #F7F3EE;
      --warm-white: #FDFAF7;
      --charcoal: #1E1A16;
      --mid:     #6B6057;
      --light:   #E8E0D5;
      --accent:  #C4873A;
    }

    html { scroll-behavior: smooth; }
    body {
      font-family: 'Inter', sans-serif;
      background: var(--warm-white);
      color: var(--charcoal);
      font-size: 16px;
      line-height: 1.65;
    }

    /* ── NAV ── */
    nav {
      position: fixed; top: 0; left: 0; right: 0; z-index: 100;
      display: flex; align-items: center; justify-content: space-between;
      padding: 1.2rem 5vw;
      background: rgba(253,250,247,0.92);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid var(--light);
    }
    .nav-logo {
      font-family: 'Playfair Display', serif;
      font-size: 1.15rem;
      color: var(--oak-dark);
      letter-spacing: 0.02em;
      text-decoration: none;
    }
    .nav-logo span { color: var(--accent); }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      text-decoration: none;
      color: var(--mid);
      font-size: 0.85rem;
      font-weight: 500;
      letter-spacing: 0.06em;
      text-transform: uppercase;
      transition: color 0.2s;
    }
    .nav-links a:hover { color: var(--oak); }
    .nav-cta {
      background: var(--oak);
      color: #fff !important;
      padding: 0.5rem 1.2rem;
      border-radius: 2px;
    }
    .nav-cta:hover { background: var(--oak-dark) !important; color: #fff !important; }

    /* ── HERO ── */
    #hero {
      min-height: 100vh;
      display: grid;
      grid-template-columns: 1fr 1fr;
      padding-top: 72px;
    }
    .hero-text {
      display: flex; flex-direction: column; justify-content: center;
      padding: 6vw 5vw 6vw 8vw;
    }
    .hero-eyebrow {
      font-size: 0.75rem; font-weight: 600;
      letter-spacing: 0.18em; text-transform: uppercase;
      color: var(--accent); margin-bottom: 1.4rem;
    }
    .hero-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(2.2rem, 4vw, 3.6rem);
      line-height: 1.12;
      color: var(--charcoal);
      margin-bottom: 1.5rem;
    }
    .hero-title em { font-style: italic; color: var(--oak); }
    .hero-sub {
      font-size: 1.05rem; color: var(--mid);
      max-width: 420px; margin-bottom: 2.5rem;
      font-weight: 300;
    }
    .hero-actions { display: flex; gap: 1rem; flex-wrap: wrap; }
    .btn-primary {
      background: var(--oak);
      color: #fff; text-decoration: none;
      padding: 0.85rem 2rem; font-size: 0.9rem;
      font-weight: 600; letter-spacing: 0.04em;
      border-radius: 2px; transition: background 0.2s;
    }
    .btn-primary:hover { background: var(--oak-dark); }
    .btn-ghost {
      border: 1.5px solid var(--oak);
      color: var(--oak); text-decoration: none;
      padding: 0.85rem 2rem; font-size: 0.9rem;
      font-weight: 600; letter-spacing: 0.04em;
      border-radius: 2px; transition: all 0.2s;
    }
    .btn-ghost:hover { background: var(--oak); color: #fff; }

    .hero-image {
      position: relative; overflow: hidden;
    }
    .hero-image img {
      width: 100%; height: 100%; object-fit: cover;
    }
    .hero-image-overlay {
      position: absolute; inset: 0;
      background: linear-gradient(135deg, rgba(92,69,48,0.15) 0%, transparent 60%);
    }
    .hero-badge {
      position: absolute; bottom: 2.5rem; left: 2rem;
      background: rgba(253,250,247,0.95);
      backdrop-filter: blur(8px);
      padding: 1rem 1.4rem;
      border-left: 3px solid var(--accent);
    }
    .hero-badge-num {
      font-family: 'Playfair Display', serif;
      font-size: 2rem; color: var(--oak-dark); line-height: 1;
    }
    .hero-badge-label {
      font-size: 0.72rem; font-weight: 600;
      text-transform: uppercase; letter-spacing: 0.1em;
      color: var(--mid); margin-top: 0.25rem;
    }

    /* ── LEISTUNGEN ── */
    #leistungen {
      background: var(--cream);
      padding: 6rem 8vw;
    }
    .section-header {
      display: flex; align-items: flex-end;
      justify-content: space-between;
      margin-bottom: 3rem;
      gap: 2rem;
    }
    .section-eyebrow {
      font-size: 0.72rem; font-weight: 600;
      letter-spacing: 0.18em; text-transform: uppercase;
      color: var(--accent); margin-bottom: 0.6rem;
    }
    .section-title {
      font-family: 'Playfair Display', serif;
      font-size: clamp(1.8rem, 3vw, 2.6rem);
      color: var(--charcoal);
    }

    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1.5px;
      background: var(--light);
    }
    .service-card {
      background: var(--warm-white);
      padding: 2.2rem 2rem;
      transition: background 0.2s;
      cursor: default;
    }
    .service-card:hover { background: var(--oak-dark); }
    .service-icon {
      width: 40px; height: 40px; margin-bottom: 1.2rem;
      color: var(--accent);
    }
    .service-card:hover .service-icon { color: var(--light); }
    .service-name {
      font-family: 'Playfair Display', serif;
      font-size: 1.15rem; margin-bottom: 0.6rem;
      color: var(--charcoal);
    }
    .service-card:hover .service-name { color: #fff; }
    .service-desc {
      font-size: 0.88rem; color: var(--mid); line-height: 1.6;
    }
    .service-card:hover .service-desc { color: var(--light); }

    /* ── ÜBER UNS ── */
    #ueber {
      display: grid; grid-template-columns: 1fr 1fr;
      min-height: 560px;
    }
    .ueber-image { position: relative; overflow: hidden; }
    .ueber-image img { width: 100%; height: 100%; object-fit: cover; }
    .wood-strip {
      position: absolute; top: 0; bottom: 0; right: 0;
      width: 6px;
      background: linear-gradient(to bottom, var(--accent), var(--oak-dark));
    }
    .ueber-text {
      padding: 5rem 6vw;
      background: var(--charcoal);
      color: var(--cream);
      display: flex; flex-direction: column; justify-content: center;
    }
    .ueber-text .section-eyebrow { color: var(--accent); }
    .ueber-text .section-title { color: #fff; margin-bottom: 1.5rem; }
    .ueber-text p { color: var(--light); font-weight: 300; margin-bottom: 1.2rem; font-size: 0.97rem; }
    .stats-row { display: flex; gap: 2.5rem; margin-top: 2rem; }
    .stat-num {
      font-family: 'Playfair Display', serif;
      font-size: 2.4rem; color: var(--accent); line-height: 1;
    }
    .stat-label {
      font-size: 0.72rem; font-weight: 600;
      text-transform: uppercase; letter-spacing: 0.1em;
      color: var(--mid); margin-top: 0.3rem;
    }

    /* ── GALERIE ── */
    #galerie { padding: 6rem 8vw; }
    .gallery-grid {
      display: grid;
      grid-template-columns: 2fr 1fr 1fr;
      grid-template-rows: 240px 240px;
      gap: 6px;
      margin-top: 3rem;
    }
    .gallery-item {
      overflow: hidden; position: relative;
      background: var(--light);
    }
    .gallery-item:first-child { grid-row: 1 / 3; }
    .gallery-item img {
      width: 100%; height: 100%;
      object-fit: cover;
      transition: transform 0.5s ease;
      filter: saturate(0.85);
    }
    .gallery-item:hover img { transform: scale(1.05); filter: saturate(1); }
    .gallery-label {
      position: absolute; bottom: 0; left: 0; right: 0;
      background: linear-gradient(transparent, rgba(30,26,22,0.75));
      color: #fff; font-size: 0.78rem; font-weight: 600;
      letter-spacing: 0.08em; text-transform: uppercase;
      padding: 1.5rem 1rem 0.8rem;
      opacity: 0; transition: opacity 0.3s;
    }
    .gallery-item:hover .gallery-label { opacity: 1; }

    /* ── KUNDENSTIMMEN ── */
    #kundenstimmen {
      background: var(--cream);
      padding: 6rem 8vw;
    }
    .reviews-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
      gap: 1.5rem;
      margin-top: 3rem;
    }
    .review-card {
      background: var(--warm-white);
      padding: 2rem;
      border-top: 3px solid var(--accent);
    }
    .stars { color: var(--accent); font-size: 0.9rem; margin-bottom: 0.8rem; }
    .review-text {
      font-size: 0.93rem; color: var(--charcoal);
      font-style: italic; margin-bottom: 1.2rem;
      line-height: 1.7;
    }
    .review-author { font-size: 0.78rem; font-weight: 600; color: var(--mid); text-transform: uppercase; letter-spacing: 0.06em; }

    /* ── KONTAKT ── */
    #kontakt {
      display: grid; grid-template-columns: 1fr 1fr;
    }
    .kontakt-info {
      background: var(--oak-dark);
      padding: 5rem 6vw;
      color: var(--cream);
    }
    .kontakt-info .section-eyebrow { color: var(--accent); }
    .kontakt-info .section-title { color: #fff; margin-bottom: 2rem; }
    .kontakt-detail {
      display: flex; gap: 1rem;
      margin-bottom: 1.5rem; align-items: flex-start;
    }
    .kontakt-detail-icon { color: var(--accent); margin-top: 2px; flex-shrink: 0; }
    .kontakt-detail-label {
      font-size: 0.7rem; font-weight: 600;
      text-transform: uppercase; letter-spacing: 0.12em;
      color: var(--accent); margin-bottom: 0.2rem;
    }
    .kontakt-detail-val { color: var(--light); font-size: 0.95rem; }
    .kontakt-form-area {
      background: var(--warm-white);
      padding: 5rem 6vw;
    }
    .kontakt-form-area .section-title { margin-bottom: 2rem; }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; margin-bottom: 1rem; }
    .form-group { display: flex; flex-direction: column; }
    .form-group.full { grid-column: 1 / -1; }
    label {
      font-size: 0.72rem; font-weight: 600;
      text-transform: uppercase; letter-spacing: 0.1em;
      color: var(--mid); margin-bottom: 0.4rem;
    }
    input, textarea, select {
      border: 1.5px solid var(--light);
      background: var(--cream);
      padding: 0.75rem 1rem;
      font-family: 'Inter', sans-serif;
      font-size: 0.9rem; color: var(--charcoal);
      border-radius: 2px;
      outline: none; transition: border-color 0.2s;
    }
    input:focus, textarea:focus, select:focus { border-color: var(--oak); }
    textarea { resize: vertical; min-height: 110px; }
    .form-submit {
      margin-top: 1.2rem;
      background: var(--oak);
      color: #fff; border: none; cursor: pointer;
      padding: 0.9rem 2.2rem; font-size: 0.9rem;
      font-weight: 600; letter-spacing: 0.04em;
      border-radius: 2px; transition: background 0.2s;
    }
    .form-submit:hover { background: var(--oak-dark); }

    /* ── FOOTER ── */
    footer {
      background: var(--charcoal);
      padding: 2rem 8vw;
      display: flex; align-items: center; justify-content: space-between;
      gap: 1rem; flex-wrap: wrap;
    }
    .footer-logo {
      font-family: 'Playfair Display', serif;
      color: var(--cream); font-size: 1rem;
    }
    .footer-logo span { color: var(--accent); }
    .footer-links { display: flex; gap: 2rem; }
    .footer-links a {
      color: var(--mid); text-decoration: none;
      font-size: 0.78rem; transition: color 0.2s;
    }
    .footer-links a:hover { color: var(--cream); }
    .footer-copy { font-size: 0.75rem; color: var(--mid); }

    /* ── RESPONSIVE ── */
    @media (max-width: 860px) {
      #hero { grid-template-columns: 1fr; }
      .hero-text { padding: 4rem 6vw 3rem; }
      .hero-image { min-height: 380px; }
      #ueber { grid-template-columns: 1fr; }
      .ueber-image { min-height: 320px; }
      #kontakt { grid-template-columns: 1fr; }
      .gallery-grid { grid-template-columns: 1fr 1fr; grid-template-rows: auto; }
      .gallery-item:first-child { grid-row: auto; grid-column: 1 / -1; height: 260px; }
      .gallery-item { height: 180px; }
      nav { padding: 1rem 4vw; }
      .nav-links { display: none; }
      .form-row { grid-template-columns: 1fr; }
    }

    /* ── SCROLL ANIMATION ── */
    .reveal { opacity: 0; transform: translateY(24px); transition: opacity 0.6s ease, transform 0.6s ease; }
    .reveal.visible { opacity: 1; transform: none; }
  </style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">Schreinerei <span>Audino</span></a>
  <ul class="nav-links">
    <li><a href="#leistungen">Leistungen</a></li>
    <li><a href="#ueber">Über uns</a></li>
    <li><a href="#galerie">Galerie</a></li>
    <li><a href="#kundenstimmen">Referenzen</a></li>
    <li><a href="#kontakt" class="nav-cta">Kontakt</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-text">
    <p class="hero-eyebrow">Schreinermeister · Nürnberg seit 2000</p>
    <h1 class="hero-title">
      Holz, das<br/>
      <em>Geschichten</em><br/>
      erzählt.
    </h1>
    <p class="hero-sub">Maßgefertigter Innenausbau für Küchen, Bäder, Wohnzimmer und mehr – handwerkliche Qualität aus Nürnberg.</p>
    <div class="hero-actions">
      <a href="#kontakt" class="btn-primary">Kostenlos anfragen</a>
      <a href="#galerie" class="btn-ghost">Galerie ansehen</a>
    </div>
  </div>
  <div class="hero-image">
    <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=900&q=80" alt="Holzküche Innenausbau" />
    <div class="hero-image-overlay"></div>
    <div class="hero-badge">
      <div class="hero-badge-num">20+</div>
      <div class="hero-badge-label">Jahre Erfahrung</div>
    </div>
  </div>
</section>

<!-- LEISTUNGEN -->
<section id="leistungen">
  <div class="section-header reveal">
    <div>
      <p class="section-eyebrow">Was wir tun</p>
      <h2 class="section-title">Unsere Leistungen</h2>
    </div>
  </div>
  <div class="services-grid reveal">
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 9h18M3 15h18M9 3v18M15 3v18"/></svg>
      <div class="service-name">Küchen</div>
      <p class="service-desc">Maßgefertigte Einbauküchen aus edlen Hölzern – funktional, elegant und auf Sie zugeschnitten.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><rect x="3" y="3" width="18" height="18" rx="1"/><path d="M9 3v18M3 9h6M3 15h6"/></svg>
      <div class="service-name">Wohnzimmer</div>
      <p class="service-desc">Einbauregale, Wandvertäfelungen und Möbel, die Ihren Wohnraum einzigartig machen.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M4 6h16M4 12h16M4 18h16"/></svg>
      <div class="service-name">Bäder & Holz</div>
      <p class="service-desc">Holz im Bad – mit der richtigen Behandlung dauerhaft schön: Waschtische, Regale, Verkleidungen.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/></svg>
      <div class="service-name">Holzböden & Parkett</div>
      <p class="service-desc">Fachgerechtes Verlegen von Parkett, Landhausdielen und Laminatböden aller Art.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 3h18v18H3zM3 9h18M9 3v18"/></svg>
      <div class="service-name">Holzdecken</div>
      <p class="service-desc">Verkleidungen und Kassettendecken aus Holz – ein Blickfang, der Räume verwandelt.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><circle cx="12" cy="12" r="10"/><path d="M12 8v4l3 3"/></svg>
      <div class="service-name">Altmöbel-Restaurierung</div>
      <p class="service-desc">Schäden repariert, Oberflächen erneuert – damit Ihre Lieblingsstücke noch Generationen überdauern.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 18l9-12 9 12H3z"/></svg>
      <div class="service-name">Holzterrassen</div>
      <p class="service-desc">Robuste und witterungsbeständige Holzterrassen für Ihren Außenbereich.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M9 3H5a2 2 0 00-2 2v14a2 2 0 002 2h14a2 2 0 002-2V9M9 3l6 6M9 3v6h6"/></svg>
      <div class="service-name">Beratung & Planung</div>
      <p class="service-desc">Vom ersten Entwurf bis zur Umsetzung – persönliche Beratung, die Ihre Ideen zur Wirklichkeit macht.</p>
    </div>
    <div class="service-card">
      <svg class="service-icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M3 7l4 4 4-4 4 4 4-4M3 13l4 4 4-4 4 4 4-4"/></svg>
      <div class="service-name">Kellerbars</div>
      <p class="service-desc">Stilvoller Innenausbau von Kellerbars und Hobbyräumen – Ihr persönlicher Rückzugsort.</p>
    </div>
  </div>
</section>

<!-- ÜBER UNS -->
<section id="ueber">
  <div class="ueber-image">
    <img src="https://images.unsplash.com/photo-1504148455328-c376907d081c?w=800&q=80" alt="Handwerksarbeit in der Schreinerei" />
    <div class="wood-strip"></div>
  </div>
  <div class="ueber-text">
    <div class="reveal">
      <p class="section-eyebrow">Über uns</p>
      <h2 class="section-title">Handwerk mit Herz – seit über 20 Jahren</h2>
      <p>Toni Audino und sein Team stehen für exklusiven Holzinnenausbau in Nürnberg. Was 2000 als kleiner Handwerksbetrieb begann, ist heute eine feste Größe für alle, die Qualität und Individualität schätzen.</p>
      <p>Jedes Projekt ist ein Unikat. Wir hören zu, planen mit Ihnen, und setzen Ihre Wünsche mit dem besten Holz und präziser Handarbeit um – ohne Kompromisse.</p>
      <div class="stats-row">
        <div>
          <div class="stat-num">20+</div>
          <div class="stat-label">Jahre Erfahrung</div>
        </div>
        <div>
          <div class="stat-num">500+</div>
          <div class="stat-label">Projekte</div>
        </div>
        <div>
          <div class="stat-num">4.5★</div>
          <div class="stat-label">Google Bewertung</div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GALERIE -->
<section id="galerie">
  <div class="section-header reveal">
    <div>
      <p class="section-eyebrow">Unsere Arbeiten</p>
      <h2 class="section-title">Galerie</h2>
    </div>
    <a href="#kontakt" class="btn-ghost" style="white-space:nowrap">Projekt anfragen</a>
  </div>
  <div class="gallery-grid reveal">
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1556909114-f6e7ad7d3136?w=800&q=80" alt="Küche" />
      <div class="gallery-label">Küchen</div>
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1588854337115-1c67d9247e4d?w=500&q=80" alt="Wohnzimmer" />
      <div class="gallery-label">Wohnzimmer</div>
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1522771739844-6a9f6d5f14af?w=500&q=80" alt="Bad" />
      <div class="gallery-label">Bad</div>
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1567016376408-0226e4d0c1ea?w=500&q=80" alt="Parkett" />
      <div class="gallery-label">Parkett</div>
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?w=500&q=80" alt="Terrasse" />
      <div class="gallery-label">Terrassen</div>
    </div>
  </div>
</section>

<!-- KUNDENSTIMMEN -->
<section id="kundenstimmen">
  <div class="reveal">
    <p class="section-eyebrow">Was Kunden sagen</p>
    <h2 class="section-title">Kundenstimmen</h2>
  </div>
  <div class="reviews-grid reveal">
    <div class="review-card">
      <div class="stars">★★★★★</div>
      <p class="review-text">„Das Team hat meine Haustür schnell und kompetent repariert. Die Beratung war sehr freundlich und zielführend. Gerne wieder."</p>
      <div class="review-author">— Google Bewertung</div>
    </div>
    <div class="review-card">
      <div class="stars">★★★★★</div>
      <p class="review-text">„Alle unsere Wünsche wurden erfüllt. Wir sind äußerst zufrieden. Eine Leidenschaft für das Handwerk, die man sofort spürt."</p>
      <div class="review-author">— Google Bewertung</div>
    </div>
    <div class="review-card">
      <div class="stars">★★★★★</div>
      <p class="review-text">„Kompetente Beratung, schnelle Ausführung und ein Ergebnis, das alle meine Erwartungen übertroffen hat. Absolut empfehlenswert!"</p>
      <div class="review-author">— Google Bewertung</div>
    </div>
  </div>
</section>

<!-- KONTAKT -->
<section id="kontakt">
  <div class="kontakt-info reveal">
    <p class="section-eyebrow">Jetzt anfragen</p>
    <h2 class="section-title">Kontakt</h2>
    <div class="kontakt-detail">
      <svg class="kontakt-detail-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0118 0z"/><circle cx="12" cy="10" r="3"/></svg>
      <div>
        <div class="kontakt-detail-label">Adresse</div>
        <div class="kontakt-detail-val">Ziegelsteinstraße 184<br/>90411 Nürnberg</div>
      </div>
    </div>
    <div class="kontakt-detail">
      <svg class="kontakt-detail-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><path d="M22 16.92v3a2 2 0 01-2.18 2 19.79 19.79 0 01-8.63-3.07A19.5 19.5 0 013.07 9.81a19.79 19.79 0 01-3.07-8.69A2 2 0 012 0h3a2 2 0 012 1.72c.127.96.361 1.903.7 2.81a2 2 0 01-.45 2.11L6.09 7.91a16 16 0 006 6l1.27-1.27a2 2 0 012.11-.45c.907.339 1.85.573 2.81.7A2 2 0 0122 14.92z"/></svg>
      <div>
        <div class="kontakt-detail-label">Telefon</div>
        <div class="kontakt-detail-val">+49 (0)911 524773</div>
      </div>
    </div>
    <div class="kontakt-detail">
      <svg class="kontakt-detail-icon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="10"/><polyline points="12,6 12,12 16,14"/></svg>
      <div>
        <div class="kontakt-detail-label">Öffnungszeiten</div>
        <div class="kontakt-detail-val">Mo–Fr: 7:00 – 18:00 Uhr<br/>Sa: 9:00 – 17:00 Uhr</div>
      </div>
    </div>
  </div>
  <div class="kontakt-form-area reveal">
    <h2 class="section-title">Schreiben Sie uns</h2>
    <form onsubmit="return false">
      <div class="form-row">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" placeholder="Max Mustermann" />
        </div>
        <div class="form-group">
          <label for="email">E-Mail</label>
          <input type="email" id="email" placeholder="max@email.de" />
        </div>
      </div>
      <div class="form-row">
        <div class="form-group">
          <label for="telefon">Telefon</label>
          <input type="tel" id="telefon" placeholder="+49 ..." />
        </div>
        <div class="form-group">
          <label for="leistung">Leistung</label>
          <select id="leistung">
            <option value="">Bitte wählen ...</option>
            <option>Küchen</option>
            <option>Wohnzimmer</option>
            <option>Bad</option>
            <option>Parkett / Böden</option>
            <option>Holzdecken</option>
            <option>Terrasse</option>
            <option>Altmöbel-Restaurierung</option>
            <option>Sonstiges</option>
          </select>
        </div>
      </div>
      <div class="form-row" style="grid-template-columns:1fr;">
        <div class="form-group full">
          <label for="nachricht">Nachricht</label>
          <textarea id="nachricht" placeholder="Beschreiben Sie kurz Ihr Projekt ..."></textarea>
        </div>
      </div>
      <button type="submit" class="form-submit">Anfrage senden →</button>
    </form>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">Schreinerei <span>Audino</span> · Nürnberg</div>
  <div class="footer-links">
    <a href="#">Impressum</a>
    <a href="#">Datenschutz</a>
    <a href="#">AGB</a>
  </div>
  <div class="footer-copy">© 2026 Schreinerei Toni Audino</div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => { if (e.isIntersecting) e.target.classList.add('visible'); });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));
</script>
</body>
</html>
