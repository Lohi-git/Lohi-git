<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="M Lohitth — Data Science and Cyber Security student at Karunya University. Python, Data Analytics, Web Development, Web Scraping and Cyber Security.">
  <title>M Lohitth — Data Science & Cyber Security</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Fira+Code:wght@400;500;600&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #070a13;
      --bg2: #0d1222;
      --card: rgba(255,255,255,.025);
      --green: #10b981;
      --green2: #34d399;
      --blue: #6366f1;
      --purple: #8b5cf6;
      --text: #f3f4f6;
      --muted: rgba(243,244,246,.65);
      --faint: rgba(243,244,246,.35);
      --border: rgba(255,255,255,.09);
      --border2: rgba(255,255,255,.16);
      --mono: "Fira Code", monospace;
      --head: "Space Grotesk", sans-serif;
    }

    * { margin:0; padding:0; box-sizing:border-box; }
    html { scroll-behavior:smooth; }
    body {
      background:var(--bg);
      color:var(--text);
      font-family:var(--head);
      overflow-x:hidden;
    }

    body::before {
      content:"";
      position:fixed;
      inset:0;
      pointer-events:none;
      z-index:-2;
      background:
        radial-gradient(circle at 15% 15%, rgba(99,102,241,.13), transparent 28%),
        radial-gradient(circle at 85% 80%, rgba(16,185,129,.10), transparent 30%);
    }

    body::after {
      content:"";
      position:fixed;
      inset:0;
      pointer-events:none;
      z-index:-1;
      opacity:.12;
      background-image:
        linear-gradient(rgba(255,255,255,.04) 1px, transparent 1px),
        linear-gradient(90deg, rgba(255,255,255,.04) 1px, transparent 1px);
      background-size:55px 55px;
      mask-image:linear-gradient(to bottom, black, transparent 85%);
    }

    ::selection { background:rgba(16,185,129,.25); color:white; }

    .progress {
      position:fixed;
      top:0;
      left:0;
      height:3px;
      width:0;
      background:linear-gradient(90deg,var(--green),var(--blue),var(--purple));
      z-index:9999;
    }

    nav {
      position:fixed;
      top:0;
      left:0;
      right:0;
      z-index:1000;
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px 6%;
      background:rgba(7,10,19,.72);
      backdrop-filter:blur(18px);
      border-bottom:1px solid var(--border);
    }

    .logo {
      font-family:var(--mono);
      color:var(--green2);
      font-size:14px;
      letter-spacing:1px;
    }

    .logo span { color:var(--faint); }

    .nav-links {
      display:flex;
      gap:28px;
      list-style:none;
    }

    .nav-links a {
      color:var(--muted);
      text-decoration:none;
      font-family:var(--mono);
      font-size:11px;
      text-transform:uppercase;
      letter-spacing:1.5px;
      transition:.25s;
    }

    .nav-links a:hover { color:var(--green2); }

    .status {
      display:flex;
      align-items:center;
      gap:8px;
      color:var(--green2);
      border:1px solid var(--border2);
      padding:8px 13px;
      font-family:var(--mono);
      font-size:10px;
      letter-spacing:1px;
      text-transform:uppercase;
    }

    .status-dot {
      width:7px;
      height:7px;
      border-radius:50%;
      background:var(--green);
      box-shadow:0 0 12px var(--green);
      animation:pulse 1.8s infinite;
    }

    @keyframes pulse {
      50% { opacity:.4; transform:scale(.7); }
    }

    section { position:relative; }

    .hero {
      min-height:100vh;
      display:grid;
      grid-template-columns:1.15fr .85fr;
      align-items:center;
      max-width:1250px;
      margin:auto;
      padding:120px 6% 70px;
      gap:50px;
    }

    .eyebrow {
      color:var(--green2);
      font-family:var(--mono);
      font-size:11px;
      text-transform:uppercase;
      letter-spacing:3px;
      margin-bottom:22px;
    }

    .eyebrow::before {
      content:"";
      display:inline-block;
      width:30px;
      height:1px;
      background:var(--green);
      vertical-align:middle;
      margin-right:12px;
    }

    h1 {
      font-size:clamp(52px,8vw,100px);
      line-height:.9;
      letter-spacing:-3px;
      margin-bottom:25px;
    }

    h1 .accent {
      color:var(--green2);
      text-shadow:0 0 45px rgba(16,185,129,.35);
    }

    .role {
      display:flex;
      flex-wrap:wrap;
      gap:0;
      border-top:1px solid var(--border);
      border-bottom:1px solid var(--border);
      margin-bottom:28px;
    }

    .role span {
      padding:12px 18px;
      border-right:1px solid var(--border);
      font-family:var(--mono);
      font-size:11px;
      color:var(--muted);
      letter-spacing:1.3px;
      text-transform:uppercase;
    }

    .role span:first-child { padding-left:0; }
    .role span:last-child { border-right:0; }

    .hero-text {
      max-width:620px;
      color:var(--muted);
      font-size:16px;
      line-height:1.8;
      margin-bottom:34px;
    }

    .buttons { display:flex; gap:12px; flex-wrap:wrap; }

    .btn {
      text-decoration:none;
      padding:13px 23px;
      font-family:var(--mono);
      font-size:10px;
      letter-spacing:1.5px;
      text-transform:uppercase;
      transition:.25s;
    }

    .btn-primary {
      color:#02100b;
      background:var(--green);
      font-weight:600;
    }

    .btn-primary:hover {
      background:var(--green2);
      box-shadow:0 0 28px rgba(16,185,129,.3);
      transform:translateY(-2px);
    }

    .btn-outline {
      color:var(--green2);
      border:1px solid var(--border2);
    }

    .btn-outline:hover {
      border-color:var(--green);
      background:rgba(16,185,129,.05);
    }

    .socials {
      display:flex;
      gap:10px;
      margin-top:30px;
    }

    .socials a {
      color:var(--faint);
      text-decoration:none;
      border:1px solid var(--border);
      padding:8px 12px;
      font-family:var(--mono);
      font-size:10px;
      transition:.2s;
    }

    .socials a:hover { color:var(--green2); border-color:var(--green); }

    .hero-visual {
      min-height:520px;
      display:flex;
      justify-content:center;
      align-items:center;
      position:relative;
    }

    .orb {
      width:min(420px,75vw);
      aspect-ratio:1;
      border:1px solid rgba(16,185,129,.35);
      border-radius:50%;
      position:relative;
      box-shadow:0 0 80px rgba(16,185,129,.08), inset 0 0 80px rgba(99,102,241,.08);
      animation:float 6s ease-in-out infinite;
    }

    .orb::before,
    .orb::after {
      content:"";
      position:absolute;
      border-radius:50%;
      inset:13%;
      border:1px dashed rgba(99,102,241,.45);
      animation:spin 18s linear infinite;
    }

    .orb::after {
      inset:27%;
      border-color:rgba(16,185,129,.5);
      animation-direction:reverse;
      animation-duration:12s;
    }

    @keyframes spin { to { transform:rotate(360deg); } }
    @keyframes float {
      50% { transform:translateY(-14px); }
    }

    .orb-center {
      position:absolute;
      inset:35%;
      border-radius:50%;
      display:flex;
      align-items:center;
      justify-content:center;
      background:linear-gradient(145deg,rgba(16,185,129,.15),rgba(99,102,241,.12));
      border:1px solid var(--border2);
      box-shadow:0 0 45px rgba(16,185,129,.15);
      font-family:var(--mono);
      font-size:42px;
      font-weight:600;
      color:var(--green2);
    }

    .orb-label {
      position:absolute;
      font-family:var(--mono);
      font-size:9px;
      letter-spacing:2px;
      color:var(--faint);
      text-transform:uppercase;
    }

    .label1 { top:12%; left:5%; }
    .label2 { right:3%; top:42%; }
    .label3 { bottom:12%; left:10%; }

    .ticker {
      border-top:1px solid var(--border);
      border-bottom:1px solid var(--border);
      padding:14px 0;
      overflow:hidden;
      background:rgba(255,255,255,.01);
    }

    .ticker-track {
      display:flex;
      width:max-content;
      animation:marquee 25s linear infinite;
    }

    .ticker-item {
      white-space:nowrap;
      padding:0 30px;
      font-family:var(--mono);
      font-size:10px;
      color:var(--faint);
      letter-spacing:2px;
      text-transform:uppercase;
    }

    .ticker-item b { color:var(--green2); }

    @keyframes marquee {
      to { transform:translateX(-50%); }
    }

    .wrap {
      max-width:1250px;
      margin:auto;
      padding:110px 6%;
    }

    .section-head {
      display:flex;
      align-items:center;
      gap:18px;
      margin-bottom:60px;
    }

    .section-number {
      font-family:var(--mono);
      color:var(--green2);
      font-size:11px;
      letter-spacing:2px;
    }

    .section-title {
      font-size:clamp(40px,5vw,68px);
      letter-spacing:-2px;
    }

    .line { height:1px; background:var(--border); flex:1; }

    .about {
      background:var(--bg2);
      border-top:1px solid var(--border);
      border-bottom:1px solid var(--border);
    }

    .about-grid {
      display:grid;
      grid-template-columns:.75fr 1.25fr;
      gap:70px;
    }

    .profile-card {
      min-height:390px;
      border:1px solid var(--border2);
      background:
        radial-gradient(circle at 50% 20%,rgba(16,185,129,.1),transparent 40%),
        rgba(255,255,255,.015);
      display:flex;
      align-items:center;
      justify-content:center;
      position:relative;
      overflow:hidden;
    }

    .profile-initial {
      font-size:150px;
      font-weight:700;
      color:rgba(16,185,129,.08);
      line-height:1;
    }

    .profile-card::before,
    .profile-card::after {
      content:"";
      position:absolute;
      width:45px;
      height:45px;
      border-color:var(--green);
    }

    .profile-card::before {
      top:0; left:0;
      border-top:2px solid;
      border-left:2px solid;
    }

    .profile-card::after {
      bottom:0; right:0;
      border-bottom:2px solid;
      border-right:2px solid;
    }

    .profile-info {
      position:absolute;
      bottom:20px;
      left:20px;
      right:20px;
      display:flex;
      justify-content:space-between;
      font-family:var(--mono);
      font-size:9px;
      color:var(--faint);
      letter-spacing:1px;
      text-transform:uppercase;
    }

    .about-lead {
      font-size:25px;
      line-height:1.55;
      font-weight:300;
      margin-bottom:22px;
    }

    .about-lead strong { color:var(--green2); font-weight:500; }

    .about-text {
      color:var(--muted);
      line-height:1.85;
      font-size:14px;
      margin-bottom:30px;
    }

    .facts {
      display:grid;
      grid-template-columns:1fr 1fr;
      border:1px solid var(--border);
    }

    .fact {
      padding:17px 20px;
      border-right:1px solid var(--border);
      border-bottom:1px solid var(--border);
    }

    .fact:nth-child(even) { border-right:0; }
    .fact:nth-last-child(-n+2) { border-bottom:0; }

    .fact small {
      display:block;
      font-family:var(--mono);
      color:var(--green2);
      font-size:9px;
      letter-spacing:2px;
      text-transform:uppercase;
      margin-bottom:5px;
    }

    .fact span { font-size:13px; color:var(--text); }

    .achievement {
      margin-top:25px;
      border:1px solid rgba(16,185,129,.25);
      padding:22px;
      background:rgba(16,185,129,.035);
    }

    .achievement-label {
      font-family:var(--mono);
      color:var(--green2);
      font-size:9px;
      letter-spacing:2px;
      text-transform:uppercase;
      margin-bottom:8px;
    }

    .achievement h3 { font-size:20px; margin-bottom:7px; }
    .achievement p { color:var(--muted); font-size:13px; line-height:1.6; }

    .skills-grid {
      display:grid;
      grid-template-columns:repeat(3,1fr);
      gap:18px;
    }

    .skill-card {
      border:1px solid var(--border);
      padding:28px;
      background:var(--card);
      transition:.3s;
    }

    .skill-card:hover {
      border-color:var(--blue);
      transform:translateY(-4px);
      box-shadow:0 15px 35px rgba(0,0,0,.25);
    }

    .skill-card h3 {
      color:var(--green2);
      font-family:var(--mono);
      font-size:11px;
      letter-spacing:2px;
      text-transform:uppercase;
      margin-bottom:18px;
    }

    .pills {
      display:flex;
      flex-wrap:wrap;
      gap:7px;
    }

    .pill {
      border:1px solid var(--border);
      color:var(--muted);
      padding:7px 11px;
      font-family:var(--mono);
      font-size:10px;
      transition:.2s;
    }

    .pill:hover { border-color:var(--green); color:var(--green2); }

    .projects {
      background:var(--bg2);
      border-top:1px solid var(--border);
      border-bottom:1px solid var(--border);
    }

    .project-list {
      display:grid;
      gap:16px;
    }

    .project {
      display:grid;
      grid-template-columns:70px 1fr auto;
      gap:25px;
      align-items:center;
      border:1px solid var(--border);
      padding:28px;
      background:rgba(255,255,255,.015);
      transition:.3s;
    }

    .project:hover {
      border-color:var(--blue);
      transform:translateX(5px);
    }

    .project-number {
      color:var(--blue);
      font-family:var(--mono);
      font-size:11px;
    }

    .project h3 {
      font-size:25px;
      margin-bottom:6px;
    }

    .project p {
      color:var(--muted);
      font-size:13px;
      line-height:1.7;
      max-width:750px;
    }

    .project-tags {
      display:flex;
      flex-wrap:wrap;
      gap:6px;
      margin-top:12px;
    }

    .project-tag {
      color:var(--green2);
      border:1px solid rgba(16,185,129,.22);
      padding:4px 8px;
      font-family:var(--mono);
      font-size:8px;
      letter-spacing:1px;
    }

    .project-link {
      color:var(--green2);
      text-decoration:none;
      font-family:var(--mono);
      font-size:10px;
      letter-spacing:1px;
      white-space:nowrap;
    }

    .project-link:hover { color:white; }

    .build {
      border:1px solid rgba(99,102,241,.3);
      background:linear-gradient(120deg,rgba(99,102,241,.08),rgba(16,185,129,.04));
      padding:35px;
      display:grid;
      grid-template-columns:1fr auto;
      align-items:center;
      gap:30px;
    }

    .build-label {
      color:#a5b4fc;
      font-family:var(--mono);
      font-size:9px;
      letter-spacing:2px;
      text-transform:uppercase;
      margin-bottom:10px;
    }

    .build h3 { font-size:32px; margin-bottom:10px; }
    .build p { color:var(--muted); font-size:14px; line-height:1.7; }

    .contact {
      background:var(--bg2);
      border-top:1px solid var(--border);
    }

    .contact-grid {
      display:grid;
      grid-template-columns:1fr 1fr;
      gap:70px;
    }

    .contact h2 {
      font-size:clamp(42px,5vw,70px);
      letter-spacing:-2px;
      line-height:.95;
      margin-bottom:25px;
    }

    .contact-intro {
      color:var(--muted);
      line-height:1.8;
      max-width:520px;
      font-size:14px;
    }

    .contact-links {
      border:1px solid var(--border);
    }

    .contact-link {
      display:flex;
      justify-content:space-between;
      align-items:center;
      padding:20px;
      border-bottom:1px solid var(--border);
      color:var(--text);
      text-decoration:none;
      transition:.2s;
    }

    .contact-link:last-child { border-bottom:0; }

    .contact-link:hover {
      background:rgba(16,185,129,.04);
      color:var(--green2);
    }

    .contact-label {
      font-family:var(--mono);
      color:var(--green2);
      font-size:9px;
      letter-spacing:2px;
      text-transform:uppercase;
      margin-bottom:4px;
    }

    .contact-value { font-size:13px; }

    footer {
      padding:25px 6%;
      display:flex;
      justify-content:space-between;
      gap:15px;
      border-top:1px solid var(--border);
      color:var(--faint);
      font-family:var(--mono);
      font-size:9px;
      letter-spacing:1px;
    }

    @media(max-width:900px) {
      .nav-links { display:none; }
      .status { display:none; }
      .hero, .about-grid, .contact-grid { grid-template-columns:1fr; }
      .hero { padding-top:130px; }
      .hero-visual { min-height:400px; }
      .skills-grid { grid-template-columns:1fr 1fr; }
      .project { grid-template-columns:45px 1fr; }
      .project-link { grid-column:2; }
      .build { grid-template-columns:1fr; }
    }

    @media(max-width:600px) {
      nav { padding:17px 5%; }
      .wrap { padding:80px 5%; }
      .hero { padding:115px 5% 60px; }
      h1 { font-size:58px; }
      .role span { border-right:0; padding-left:0; padding-right:12px; }
      .hero-text { font-size:14px; }
      .skills-grid { grid-template-columns:1fr; }
      .facts { grid-template-columns:1fr; }
      .fact { border-right:0; }
      .fact:nth-last-child(-n+2) { border-bottom:1px solid var(--border); }
      .fact:last-child { border-bottom:0; }
      .project { padding:22px; }
      .project h3 { font-size:21px; }
      .orb { width:310px; }
      footer { flex-direction:column; }
    }
  </style>
</head>

<body>

  <div class="progress" id="progress"></div>

  <nav>
    <div class="logo"><span>&lt;</span>LOHITTH<span>/&gt;</span></div>

    <ul class="nav-links">
      <li><a href="#about">01 About</a></li>
      <li><a href="#skills">02 Skills</a></li>
      <li><a href="#projects">03 Projects</a></li>
      <li><a href="#contact">04 Contact</a></li>
    </ul>

    <div class="status">
      <span class="status-dot"></span>
      Available
    </div>
  </nav>

  <main>

    <section class="hero" id="home">
      <div>
        <div class="eyebrow">Data Science × Cyber Security</div>

        <h1>M <span class="accent">LOHITTH</span></h1>

        <div class="role">
          <span>Data Science Student</span>
          <span>Cyber Security</span>
          <span>Developer</span>
        </div>

        <p class="hero-text">
          I build data-driven applications, interactive web experiences,
          and practical solutions using Python, data analytics, modern web
          technologies, and AI tools.
        </p>

        <div class="buttons">
          <a class="btn btn-primary" href="#projects">View Projects →</a>
          <a class="btn btn-outline" href="#contact">Let's Connect</a>
        </div>

        <div class="socials">
          <a href="https://www.linkedin.com/in/m-lohitth-1619b7378" target="_blank">LinkedIn</a>
          <a href="mailto:mlohitth@karunya.edu.in">Email</a>
        </div>
      </div>

      <div class="hero-visual">
        <div class="orb">
          <div class="orb-center">ML</div>
          <div class="orb-label label1">Python</div>
          <div class="orb-label label2">Cyber Security</div>
          <div class="orb-label label3">Data Analytics</div>
        </div>
      </div>
    </section>

    <div class="ticker">
      <div class="ticker-track">
        <div class="ticker-item"><b>PYTHON</b> • DATA ANALYTICS</div>
        <div class="ticker-item">WEB SCRAPING • REACT</div>
        <div class="ticker-item"><b>CYBER SECURITY</b> • AI TOOLS</div>
        <div class="ticker-item">TAILWIND CSS • JAVASCRIPT</div>
        <div class="ticker-item"><b>PYTHON</b> • DATA ANALYTICS</div>
        <div class="ticker-item">WEB SCRAPING • REACT</div>
        <div class="ticker-item"><b>CYBER SECURITY</b> • AI TOOLS</div>
        <div class="ticker-item">TAILWIND CSS • JAVASCRIPT</div>
      </div>
    </div>

    <section class="about" id="about">
      <div class="wrap">
        <div class="section-head">
          <span class="section-number">01</span>
          <h2 class="section-title">ABOUT</h2>
          <div class="line"></div>
        </div>

        <div class="about-grid">
          <div class="profile-card">
            <div class="profile-initial">ML</div>
            <div class="profile-info">
              <span>Tirunelveli, India</span>
              <span>Karunya University</span>
            </div>
          </div>

          <div>
            <p class="about-lead">
              I'm a <strong>Data Science & Cyber Security student</strong>
              focused on building useful software and exploring modern technology.
            </p>

            <p class="about-text">
              I am currently studying at Karunya University, Coimbatore.
              My main interests include Python, data analytics, interactive web
              development, AI tools, web scraping, and cybersecurity concepts.
              I enjoy taking ideas and turning them into practical applications.
            </p>

            <div class="facts">
              <div class="fact">
                <small>Education</small>
                <span>Data Science & Cyber Security</span>
              </div>
              <div class="fact">
                <small>University</small>
                <span>Karunya University</span>
              </div>
              <div class="fact">
                <small>Based In</small>
                <span>Tirunelveli, Tamil Nadu</span>
              </div>
              <div class="fact">
                <small>Focus</small>
                <span>Python & Data Analytics</span>
              </div>
            </div>

            <div class="achievement">
              <div class="achievement-label">Recent Achievement</div>
              <h3>🥈 2nd Prize — Mindkraft 2026</h3>
              <p>
                Bot Fest — built a comprehensive finance website and secured
                second place at Mindkraft 2026.
              </p>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section id="skills">
      <div class="wrap">
        <div class="section-head">
          <span class="section-number">02</span>
          <h2 class="section-title">SKILLS</h2>
          <div class="line"></div>
        </div>

        <div class="skills-grid">
          <div class="skill-card">
            <h3>Languages</h3>
            <div class="pills">
              <span class="pill">Python</span>
              <span class="pill">JavaScript</span>
              <span class="pill">HTML</span>
              <span class="pill">CSS</span>
            </div>
          </div>

          <div class="skill-card">
            <h3>Web & Frameworks</h3>
            <div class="pills">
              <span class="pill">React</span>
              <span class="pill">Tailwind CSS</span>
              <span class="pill">Interactive UI</span>
              <span class="pill">Web Development</span>
            </div>
          </div>

          <div class="skill-card">
            <h3>Core Focus</h3>
            <div class="pills">
              <span class="pill">Data Analytics</span>
              <span class="pill">Web Scraping</span>
              <span class="pill">Cyber Security</span>
              <span class="pill">AI Tools</span>
            </div>
          </div>
        </div>
      </div>
    </section>

    <section class="projects" id="projects">
      <div class="wrap">
        <div class="section-head">
          <span class="section-number">03</span>
          <h2 class="section-title">PROJECTS</h2>
          <div class="line"></div>
        </div>

        <div class="project-list">

          <article class="project">
            <div class="project-number">01</div>
            <div>
              <h3>Finance Website</h3>
              <p>
                A comprehensive finance-focused website built for Mindkraft 2026
                Bot Fest, where the project secured 2nd prize.
              </p>
              <div class="project-tags">
                <span class="project-tag">WEB</span>
                <span class="project-tag">FINANCE</span>
                <span class="project-tag">MINDKRAFT 2026</span>
              </div>
            </div>
            <a class="project-link" href="#contact">Details ↗</a>
          </article>

          <article class="project">
            <div class="project-number">02</div>
            <div>
              <h3>3D Interactive CV</h3>
              <p>
                A professional interactive CV currently being built with React
                and Tailwind CSS to present skills and experience in a more
                engaging format.
              </p>
              <div class="project-tags">
                <span class="project-tag">REACT</span>
                <span class="project-tag">TAILWIND</span>
                <span class="project-tag">3D UI</span>
              </div>
            </div>
            <a class="project-link" href="#contact">Building ↗</a>
          </article>

          <article class="project">
            <div class="project-number">03</div>
            <div>
              <h3>Data Analytics & Web Scraping</h3>
              <p>
                A project area focused on collecting useful web data,
                processing datasets with Python, and turning raw information
                into meaningful analysis.
              </p>
              <div class="project-tags">
                <span class="project-tag">PYTHON</span>
                <span class="project-tag">DATA</span>
                <span class="project-tag">SCRAPING</span>
              </div>
            </div>
            <a class="project-link" href="#contact">Explore ↗</a>
          </article>

        </div>
      </div>
    </section>

    <section>
      <div class="wrap">
        <div class="build">
          <div>
            <div class="build-label">Currently Building</div>
            <h3>3D Interactive CV</h3>
            <p>
              A professional interactive CV using React and Tailwind CSS,
              designed to present my skills and work beyond a traditional resume.
            </p>
          </div>
          <a class="btn btn-primary" href="#contact">Connect →</a>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="wrap">
        <div class="contact-grid">

          <div>
            <div class="section-number" style="margin-bottom:20px;">04 CONTACT</div>
            <h2>LET'S<br><span style="color:var(--green2)">CONNECT.</span></h2>
            <p class="contact-intro">
              I'm interested in web development, data analytics, web scraping,
              AI tools, and opportunities where I can build useful technology.
            </p>
          </div>

          <div class="contact-links">
            <a class="contact-link"
               href="mailto:mlohitth@karunya.edu.in">
              <div>
                <div class="contact-label">Email</div>
                <div class="contact-value">mlohitth@karunya.edu.in</div>
              </div>
              <span>↗</span>
            </a>

            <a class="contact-link"
               href="https://www.linkedin.com/in/m-lohitth-1619b7378"
               target="_blank">
              <div>
                <div class="contact-label">LinkedIn</div>
                <div class="contact-value">m-lohitth-1619b7378</div>
              </div>
              <span>↗</span>
            </a>

            <a class="contact-link" href="#home">
              <div>
                <div class="contact-label">Location</div>
                <div class="contact-value">Tirunelveli, Tamil Nadu, India</div>
              </div>
              <span>↑</span>
            </a>
          </div>

        </div>
      </div>
    </section>

  </main>

  <footer>
    <span>© 2026 M LOHITTH</span>
    <span>DATA SCIENCE × CYBER SECURITY</span>
  </footer>

  <script>
    // Scroll progress
    const progress = document.getElementById("progress");

    window.addEventListener("scroll", () => {
      const scrollTop = window.scrollY;
      const height = document.documentElement.scrollHeight - window.innerHeight;
      progress.style.width = (scrollTop / height) * 100 + "%";
    });

    // Small reveal animation
    const observer = new IntersectionObserver(
      entries => {
        entries.forEach(entry => {
          if (entry.isIntersecting) {
            entry.target.style.opacity = "1";
            entry.target.style.transform = "translateY(0)";
          }
        });
      },
      { threshold: 0.12 }
    );

    document.querySelectorAll(
      ".skill-card, .project, .achievement, .build, .profile-card"
    ).forEach(el => {
      el.style.opacity = "0";
      el.style.transform = "translateY(20px)";
      el.style.transition = "opacity .6s ease, transform .6s ease";
      observer.observe(el);
    });
  </script>

</body>
</html>
