<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Goli Pranay Kumar — AI Engineer</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Clash+Display:wght@400;500;600;700&family=Syne:wght@400;700;800&display=swap" rel="stylesheet"/>
<style>
  :root {
    --cyan: #00C2FF;
    --cyan-dim: #0099CC;
    --neon-green: #00FF94;
    --purple: #7B2FFF;
    --pink: #FF2D9B;
    --bg: #03070F;
    --bg2: #060D1A;
    --bg3: #091525;
    --card: rgba(0,194,255,0.04);
    --border: rgba(0,194,255,0.12);
    --text: #E8F4FF;
    --muted: #6B8FA8;
    --mono: 'Space Mono', monospace;
    --display: 'Syne', sans-serif;
  }

  * { margin:0; padding:0; box-sizing:border-box; }

  html { scroll-behavior: smooth; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: var(--mono);
    overflow-x: hidden;
    cursor: none;
  }

  /* CUSTOM CURSOR */
  #cursor {
    width: 12px; height: 12px;
    background: var(--cyan);
    border-radius: 50%;
    position: fixed; pointer-events: none; z-index: 9999;
    transform: translate(-50%,-50%);
    transition: transform 0.08s, width 0.2s, height 0.2s, background 0.2s;
    mix-blend-mode: screen;
  }
  #cursor-ring {
    width: 36px; height: 36px;
    border: 1.5px solid rgba(0,194,255,0.5);
    border-radius: 50%;
    position: fixed; pointer-events: none; z-index: 9998;
    transform: translate(-50%,-50%);
    transition: transform 0.18s ease-out, width 0.2s, height 0.2s;
  }
  body:hover #cursor { opacity: 1; }

  /* GRID BACKGROUND */
  body::before {
    content:'';
    position: fixed; inset:0; z-index:0;
    background-image:
      linear-gradient(rgba(0,194,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,194,255,0.03) 1px, transparent 1px);
    background-size: 60px 60px;
    pointer-events: none;
  }

  /* NOISE OVERLAY */
  body::after {
    content:'';
    position: fixed; inset:0; z-index:1;
    background-image: url("data:image/svg+xml,%3Csvg viewBox='0 0 256 256' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='0.9' numOctaves='4' stitchTiles='stitch'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='0.03'/%3E%3C/svg%3E");
    pointer-events: none; opacity:0.4;
  }

  .wrap { position:relative; z-index:2; }

  /* ====== HERO ====== */
  .hero {
    min-height: 100vh;
    display: flex; flex-direction:column; align-items:center; justify-content:center;
    text-align:center; padding: 80px 24px 60px;
    position:relative; overflow:hidden;
  }

  .hero-orbs {
    position:absolute; inset:0; pointer-events:none;
  }
  .orb {
    position:absolute; border-radius:50%; filter:blur(80px); opacity:0.18;
    animation: drift 12s ease-in-out infinite;
  }
  .orb1 { width:500px;height:500px; background:var(--cyan); top:-100px; left:-100px; animation-delay:0s;}
  .orb2 { width:400px;height:400px; background:var(--purple); bottom:-80px; right:-80px; animation-delay:-4s;}
  .orb3 { width:300px;height:300px; background:var(--neon-green); top:50%; left:60%; animation-delay:-8s; opacity:0.1;}

  @keyframes drift {
    0%,100% { transform: translate(0,0) scale(1); }
    50% { transform: translate(30px,-20px) scale(1.05); }
  }

  .hero-badge {
    display:inline-flex; align-items:center; gap:8px;
    background:rgba(0,194,255,0.08); border:1px solid var(--border);
    border-radius:100px; padding:6px 16px; font-size:11px; letter-spacing:2px;
    color:var(--cyan); text-transform:uppercase; margin-bottom:32px;
    animation: fadeUp 0.6s ease both;
  }
  .hero-badge span { width:6px;height:6px; background:var(--neon-green); border-radius:50%; animation: pulse 2s infinite;}

  @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:0.4;transform:scale(0.8)} }

  .hero-name {
    font-family: var(--display);
    font-size: clamp(48px, 9vw, 110px);
    font-weight: 800;
    line-height: 0.95;
    letter-spacing: -2px;
    animation: fadeUp 0.6s 0.1s ease both;
  }
  .hero-name .line1 { display:block; color:var(--text); }
  .hero-name .line2 {
    display:block;
    background: linear-gradient(135deg, var(--cyan) 0%, var(--neon-green) 100%);
    -webkit-background-clip: text; -webkit-text-fill-color: transparent;
  }

  .hero-role {
    margin-top:24px; font-size:14px; letter-spacing:3px;
    color:var(--muted); text-transform:uppercase;
    animation: fadeUp 0.6s 0.2s ease both;
  }

  .hero-desc {
    margin-top:20px; font-size:13px; line-height:1.8;
    color: rgba(232,244,255,0.6); max-width:520px;
    animation: fadeUp 0.6s 0.3s ease both;
  }

  .hero-cta {
    margin-top:40px; display:flex; gap:16px; flex-wrap:wrap; justify-content:center;
    animation: fadeUp 0.6s 0.4s ease both;
  }
  .btn {
    display:inline-flex; align-items:center; gap:8px;
    padding:12px 28px; border-radius:6px; font-family:var(--mono);
    font-size:12px; letter-spacing:1.5px; text-transform:uppercase;
    text-decoration:none; cursor:none; transition:all 0.2s;
    position:relative; overflow:hidden;
  }
  .btn-primary {
    background: var(--cyan); color: var(--bg);
    font-weight:700; border:none;
  }
  .btn-primary:hover { background: var(--neon-green); transform:translateY(-2px); box-shadow:0 8px 30px rgba(0,194,255,0.3); }
  .btn-outline {
    background:transparent; color:var(--cyan);
    border:1px solid rgba(0,194,255,0.4);
  }
  .btn-outline:hover { border-color:var(--cyan); background:rgba(0,194,255,0.08); transform:translateY(-2px);}

  .scroll-hint {
    position:absolute; bottom:32px; left:50%; transform:translateX(-50%);
    display:flex; flex-direction:column; align-items:center; gap:8px;
    color:var(--muted); font-size:10px; letter-spacing:2px;
    animation: fadeUp 1s 1s ease both;
  }
  .scroll-line { width:1px; height:40px; background:linear-gradient(var(--cyan),transparent); animation: scrollPulse 2s infinite;}
  @keyframes scrollPulse { 0%,100%{opacity:0.3} 50%{opacity:1} }

  @keyframes fadeUp { from{opacity:0;transform:translateY(20px)} to{opacity:1;transform:translateY(0)} }

  /* ====== SECTIONS ====== */
  section { padding: 80px 24px; max-width:1100px; margin:0 auto; }

  .section-label {
    font-size:10px; letter-spacing:4px; color:var(--cyan);
    text-transform:uppercase; margin-bottom:12px;
    display:flex; align-items:center; gap:12px;
  }
  .section-label::after { content:''; flex:1; height:1px; background:var(--border); }

  .section-title {
    font-family:var(--display); font-size:clamp(32px,5vw,56px);
    font-weight:800; line-height:1.1; margin-bottom:48px;
  }

  /* ====== ABOUT ====== */
  .about-grid {
    display:grid; grid-template-columns:1fr 1fr; gap:48px; align-items:start;
  }
  @media(max-width:700px){.about-grid{grid-template-columns:1fr;}}

  .about-text p { font-size:14px; line-height:2; color:rgba(232,244,255,0.7); margin-bottom:16px; }

  .about-stats {
    display:grid; grid-template-columns:1fr 1fr; gap:16px;
  }
  .stat-card {
    background:var(--card); border:1px solid var(--border); border-radius:12px;
    padding:24px; position:relative; overflow:hidden; transition:border-color 0.2s, transform 0.2s;
  }
  .stat-card:hover { border-color:var(--cyan); transform:translateY(-4px); }
  .stat-card::before {
    content:''; position:absolute; inset:0;
    background:linear-gradient(135deg, rgba(0,194,255,0.05), transparent);
    opacity:0; transition:opacity 0.2s;
  }
  .stat-card:hover::before { opacity:1; }
  .stat-num { font-family:var(--display); font-size:40px; font-weight:800; color:var(--cyan); line-height:1; }
  .stat-label { font-size:11px; color:var(--muted); margin-top:6px; letter-spacing:1px; }

  /* ====== SKILLS ====== */
  .skills-section { background:var(--bg2); margin:0; max-width:100%; border-top:1px solid var(--border); border-bottom:1px solid var(--border); }
  .skills-inner { max-width:1100px; margin:0 auto; padding:80px 24px; }

  .skill-categories { display:flex; flex-direction:column; gap:40px; }
  .skill-cat-title { font-size:10px; letter-spacing:3px; color:var(--muted); text-transform:uppercase; margin-bottom:16px;}

  .skill-pills { display:flex; flex-wrap:wrap; gap:12px; }
  .pill {
    display:inline-flex; align-items:center; gap:8px;
    padding:10px 18px; border-radius:8px;
    background:rgba(255,255,255,0.03); border:1px solid var(--border);
    font-size:12px; letter-spacing:1px; transition:all 0.2s; cursor:none;
  }
  .pill:hover { background:rgba(0,194,255,0.08); border-color:var(--cyan); transform:translateY(-2px); color:var(--cyan);}
  .pill-icon { font-size:16px; }
  .pill.featured { border-color:rgba(0,194,255,0.3); background:rgba(0,194,255,0.06); color:var(--cyan);}

  /* Skill bar animation */
  .skill-bar-row { display:flex; flex-direction:column; gap:12px; }
  .skill-bar-item { display:flex; flex-direction:column; gap:6px; }
  .skill-bar-header { display:flex; justify-content:space-between; font-size:12px; }
  .skill-bar-name { color:var(--text); }
  .skill-bar-pct { color:var(--cyan); }
  .skill-bar-track { height:4px; background:rgba(255,255,255,0.06); border-radius:4px; overflow:hidden; }
  .skill-bar-fill {
    height:100%; border-radius:4px;
    background:linear-gradient(90deg,var(--cyan),var(--neon-green));
    width:0%; transition: width 1.2s cubic-bezier(0.16,1,0.3,1);
  }

  /* ====== PROJECTS ====== */
  .projects-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(300px,1fr)); gap:24px; }

  .project-card {
    background:var(--card); border:1px solid var(--border); border-radius:16px;
    padding:32px; position:relative; overflow:hidden; transition:all 0.3s;
    cursor:none;
  }
  .project-card:hover { border-color:rgba(0,194,255,0.4); transform:translateY(-6px); box-shadow:0 20px 60px rgba(0,0,0,0.4), 0 0 40px rgba(0,194,255,0.06);}
  .project-card::after {
    content:''; position:absolute; top:0; left:0; right:0; height:2px;
    background:linear-gradient(90deg, var(--cyan), var(--neon-green));
    opacity:0; transition:opacity 0.3s;
  }
  .project-card:hover::after { opacity:1; }

  .project-icon { font-size:32px; margin-bottom:16px; }
  .project-name { font-family:var(--display); font-size:22px; font-weight:700; margin-bottom:12px; }
  .project-desc { font-size:13px; line-height:1.8; color:rgba(232,244,255,0.6); margin-bottom:20px; }
  .project-tags { display:flex; flex-wrap:wrap; gap:8px; margin-bottom:24px; }
  .tag {
    padding:4px 10px; background:rgba(0,194,255,0.08); border:1px solid rgba(0,194,255,0.2);
    border-radius:4px; font-size:10px; color:var(--cyan); letter-spacing:1px;
  }
  .project-link {
    display:inline-flex; align-items:center; gap:6px;
    font-size:11px; letter-spacing:2px; text-transform:uppercase;
    color:var(--cyan); text-decoration:none; transition:gap 0.2s;
  }
  .project-link:hover { gap:10px; }
  .project-link svg { transition:transform 0.2s; }
  .project-link:hover svg { transform:translateX(4px); }

  .project-card.featured {
    grid-column: span 2;
    background:linear-gradient(135deg, rgba(0,194,255,0.06), rgba(0,255,148,0.03));
    border-color:rgba(0,194,255,0.2);
  }
  @media(max-width:700px){.project-card.featured{grid-column:span 1;}}

  /* ====== GOALS ====== */
  .goals-section { background:var(--bg2); margin:0; max-width:100%; border-top:1px solid var(--border);}
  .goals-inner { max-width:1100px; margin:0 auto; padding:80px 24px; }
  .goals-grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:20px; }
  .goal-item {
    border:1px solid var(--border); border-radius:12px; padding:28px;
    background:rgba(255,255,255,0.02); transition:all 0.2s;
  }
  .goal-item:hover { border-color:var(--neon-green); background:rgba(0,255,148,0.04); transform:translateY(-4px);}
  .goal-icon { font-size:28px; margin-bottom:12px; }
  .goal-text { font-size:13px; line-height:1.7; color:rgba(232,244,255,0.75); }

  /* ====== CONNECT ====== */
  .connect-section { text-align:center; }
  .connect-links { display:flex; gap:16px; justify-content:center; flex-wrap:wrap; margin-top:40px; }
  .connect-btn {
    display:inline-flex; align-items:center; gap:10px;
    padding:14px 28px; border-radius:8px; text-decoration:none;
    font-family:var(--mono); font-size:12px; letter-spacing:1.5px; text-transform:uppercase;
    border:1px solid var(--border); color:var(--text); cursor:none; transition:all 0.2s;
    background:rgba(255,255,255,0.02);
  }
  .connect-btn:hover { transform:translateY(-4px); box-shadow:0 10px 30px rgba(0,0,0,0.3); }
  .cb-linkedin:hover { border-color:#0077B5; color:#0077B5; background:rgba(0,119,181,0.08);}
  .cb-gmail:hover { border-color:#D14836; color:#D14836; background:rgba(209,72,54,0.08);}
  .cb-leetcode:hover { border-color:#FFA116; color:#FFA116; background:rgba(255,161,22,0.08);}
  .cb-github:hover { border-color:#fff; color:#fff; background:rgba(255,255,255,0.05);}

  /* ====== FOOTER ====== */
  footer {
    border-top:1px solid var(--border); padding:40px 24px; text-align:center;
    color:var(--muted); font-size:11px; letter-spacing:2px;
  }
  footer span { color:var(--cyan); }

  /* ====== SCANLINE EFFECT ====== */
  .hero::before {
    content:'';
    position:absolute; inset:0; pointer-events:none;
    background:repeating-linear-gradient(0deg, transparent, transparent 2px, rgba(0,0,0,0.05) 2px, rgba(0,0,0,0.05) 4px);
    z-index:1;
  }

  /* ====== MARQUEE ====== */
  .marquee-wrap { overflow:hidden; border-top:1px solid var(--border); border-bottom:1px solid var(--border); padding:14px 0; background:var(--bg2);}
  .marquee-inner { display:flex; gap:48px; white-space:nowrap; animation:marquee 20s linear infinite; width:max-content;}
  .marquee-item { font-size:11px; letter-spacing:3px; text-transform:uppercase; color:var(--muted); display:flex; align-items:center; gap:16px;}
  .marquee-item::after { content:'◆'; color:var(--cyan); font-size:8px; }
  @keyframes marquee { from{transform:translateX(0)} to{transform:translateX(-50%)} }

  /* ====== GLITCH EFFECT ====== */
  .glitch { position:relative; }
  .glitch::before, .glitch::after {
    content:attr(data-text); position:absolute; top:0; left:0; width:100%;
    background:var(--bg); clip-path:inset(0);
  }
  .glitch::before { left:2px; text-shadow:-2px 0 var(--pink); animation:glitch1 3s infinite; }
  .glitch::after { left:-2px; text-shadow:2px 0 var(--cyan); animation:glitch2 3s infinite; }
  @keyframes glitch1 {
    0%,90%,100%{clip-path:inset(50% 0 50% 0)} 92%{clip-path:inset(20% 0 60% 0)} 94%{clip-path:inset(70% 0 10% 0)} 96%{clip-path:inset(40% 0 30% 0)}
  }
  @keyframes glitch2 {
    0%,88%,100%{clip-path:inset(50% 0 50% 0)} 90%{clip-path:inset(10% 0 80% 0)} 93%{clip-path:inset(60% 0 20% 0)} 97%{clip-path:inset(30% 0 50% 0)}
  }

  /* ====== ANIMATED COUNTER ====== */
  .counter { display:inline-block; }

  /* ====== TYPEWRITER ====== */
  .typewriter { display:inline; border-right:2px solid var(--cyan); padding-right:4px; animation:blink 1s step-end infinite; }
  @keyframes blink { 0%,100%{border-color:var(--cyan)} 50%{border-color:transparent} }

  /* ====== RESPONSIVE ====== */
  @media(max-width:600px){
    .hero-name { font-size:clamp(36px,12vw,60px); }
    .connect-links { flex-direction:column; align-items:center;}
    .projects-grid { grid-template-columns:1fr; }
    .about-stats { grid-template-columns:1fr 1fr; }
  }
</style>
</head>
<body>

<!-- Custom Cursor -->
<div id="cursor"></div>
<div id="cursor-ring"></div>

<div class="wrap">

  <!-- ====== HERO ====== -->
  <section class="hero">
    <div class="hero-orbs">
      <div class="orb orb1"></div>
      <div class="orb orb2"></div>
      <div class="orb orb3"></div>
    </div>

    <div class="hero-badge"><span></span> Open to Opportunities</div>

    <h1 class="hero-name">
      <span class="line1">Goli Pranay</span>
      <span class="line2 glitch" data-text="Kumar">Kumar</span>
    </h1>

    <p class="hero-role">AI &amp; Data Science Engineer</p>
    <p class="hero-desc">
      B.Tech student building at the intersection of AI, data, and thoughtful software design. Vignan Institute of Technology &amp; Science • 2023–2027
    </p>

    <div class="hero-cta">
      <a href="https://github.com/GoliPranayKumar" class="btn btn-primary">View GitHub →</a>
      <a href="mailto:golipranaykumar@gmail.com" class="btn btn-outline">Say Hello</a>
    </div>

    <div class="scroll-hint">
      <div class="scroll-line"></div>
      <span>Scroll</span>
    </div>
  </section>

  <!-- ====== MARQUEE ====== -->
  <div class="marquee-wrap">
    <div class="marquee-inner" id="marqueeInner">
      <span class="marquee-item">Python</span>
      <span class="marquee-item">TensorFlow</span>
      <span class="marquee-item">React</span>
      <span class="marquee-item">Node.js</span>
      <span class="marquee-item">Deep Learning</span>
      <span class="marquee-item">Java</span>
      <span class="marquee-item">MongoDB</span>
      <span class="marquee-item">OpenCV</span>
      <span class="marquee-item">DSA</span>
      <span class="marquee-item">Next.js</span>
      <span class="marquee-item">MySQL</span>
      <span class="marquee-item">PyTorch</span>
      <span class="marquee-item">Python</span>
      <span class="marquee-item">TensorFlow</span>
      <span class="marquee-item">React</span>
      <span class="marquee-item">Node.js</span>
      <span class="marquee-item">Deep Learning</span>
      <span class="marquee-item">Java</span>
      <span class="marquee-item">MongoDB</span>
      <span class="marquee-item">OpenCV</span>
      <span class="marquee-item">DSA</span>
      <span class="marquee-item">Next.js</span>
      <span class="marquee-item">MySQL</span>
      <span class="marquee-item">PyTorch</span>
    </div>
  </div>

  <!-- ====== ABOUT ====== -->
  <section>
    <div class="section-label">// 001 — About</div>
    <h2 class="section-title">Who I Am</h2>
    <div class="about-grid">
      <div class="about-text">
        <p>I'm a passionate AI &amp; Data Science student who loves turning complex problems into elegant software solutions. From training neural networks to shipping full-stack apps — I build things that matter.</p>
        <p>My journey started with curiosity about how machines learn. Today I'm working on AI-powered applications, exploring DSA patterns, and contributing to open-source projects.</p>
        <p>When I'm not coding: <strong>strategy games 🎮 &nbsp;UI/UX design 🎨 &nbsp;video editing 🎬 &nbsp;exploring AI tools 🤖</strong></p>
      </div>
      <div class="about-stats">
        <div class="stat-card">
          <div class="stat-num counter" data-target="4">0</div>
          <div class="stat-label">Projects Built</div>
        </div>
        <div class="stat-card">
          <div class="stat-num counter" data-target="500">0</div>
          <div class="stat-label">LeetCode Goal</div>
        </div>
        <div class="stat-card">
          <div class="stat-num counter" data-target="6">0</div>
          <div class="stat-label">Languages</div>
        </div>
        <div class="stat-card">
          <div class="stat-num counter" data-target="2027">0</div>
          <div class="stat-label">Graduation Year</div>
        </div>
      </div>
    </div>
  </section>

  <!-- ====== SKILLS ====== -->
  <div class="skills-section">
    <div class="skills-inner">
      <div class="section-label">// 002 — Skills</div>
      <h2 class="section-title">Tech Stack</h2>

      <div class="skill-categories">

        <div>
          <div class="skill-cat-title">Languages</div>
          <div class="skill-pills">
            <div class="pill featured"><span class="pill-icon">🐍</span> Python</div>
            <div class="pill featured"><span class="pill-icon">☕</span> Java</div>
            <div class="pill"><span class="pill-icon">⚡</span> C</div>
            <div class="pill"><span class="pill-icon">🌐</span> HTML/CSS</div>
            <div class="pill"><span class="pill-icon">📜</span> JavaScript</div>
          </div>
        </div>

        <div>
          <div class="skill-cat-title">Frameworks &amp; Tools</div>
          <div class="skill-pills">
            <div class="pill featured"><span class="pill-icon">⚛️</span> React</div>
            <div class="pill"><span class="pill-icon">🟢</span> Node.js</div>
            <div class="pill"><span class="pill-icon">▲</span> Next.js</div>
            <div class="pill featured"><span class="pill-icon">🧠</span> TensorFlow</div>
            <div class="pill featured"><span class="pill-icon">🔥</span> PyTorch</div>
            <div class="pill"><span class="pill-icon">👁️</span> OpenCV</div>
            <div class="pill"><span class="pill-icon">💨</span> TailwindCSS</div>
            <div class="pill"><span class="pill-icon">🎞️</span> Framer Motion</div>
          </div>
        </div>

        <div>
          <div class="skill-cat-title">Proficiency</div>
          <div class="skill-bar-row">
            <div class="skill-bar-item">
              <div class="skill-bar-header"><span class="skill-bar-name">Python / AI/ML</span><span class="skill-bar-pct">88%</span></div>
              <div class="skill-bar-track"><div class="skill-bar-fill" data-pct="88"></div></div>
            </div>
            <div class="skill-bar-item">
              <div class="skill-bar-header"><span class="skill-bar-name">Data Structures &amp; Algorithms</span><span class="skill-bar-pct">80%</span></div>
              <div class="skill-bar-track"><div class="skill-bar-fill" data-pct="80"></div></div>
            </div>
            <div class="skill-bar-item">
              <div class="skill-bar-header"><span class="skill-bar-name">React / Full Stack</span><span class="skill-bar-pct">75%</span></div>
              <div class="skill-bar-track"><div class="skill-bar-fill" data-pct="75"></div></div>
            </div>
            <div class="skill-bar-item">
              <div class="skill-bar-header"><span class="skill-bar-name">Java</span><span class="skill-bar-pct">72%</span></div>
              <div class="skill-bar-track"><div class="skill-bar-fill" data-pct="72"></div></div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </div>

  <!-- ====== PROJECTS ====== -->
  <section>
    <div class="section-label">// 003 — Projects</div>
    <h2 class="section-title">Featured Work</h2>
    <div class="projects-grid">

      <div class="project-card featured">
        <div class="project-icon">🧠</div>
        <div class="project-name">MediScannerAI</div>
        <div class="project-desc">AI-powered deep learning system that detects abnormalities in Chest X-rays with high diagnostic accuracy. Combines computer vision with clinical intuition.</div>
        <div class="project-tags">
          <span class="tag">Python</span>
          <span class="tag">TensorFlow</span>
          <span class="tag">PyTorch</span>
          <span class="tag">React</span>
          <span class="tag">OpenCV</span>
        </div>
        <a href="https://github.com/GoliPranayKumar/MediScannerAi" class="project-link">
          View Project
          <svg width="14" height="14" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
      </div>

      <div class="project-card">
        <div class="project-icon">⚔️</div>
        <div class="project-name">Yuddha Bhumi</div>
        <div class="project-desc">Strategy-based battlefield simulation game with real-time game state management and complex AI-driven opponents.</div>
        <div class="project-tags">
          <span class="tag">React</span>
          <span class="tag">Node.js</span>
          <span class="tag">Game Algorithms</span>
        </div>
        <a href="https://github.com/GoliPranayKumar/YuddhaBhumi" class="project-link">
          View Project
          <svg width="14" height="14" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
      </div>

      <div class="project-card">
        <div class="project-icon">📊</div>
        <div class="project-name">Credovia</div>
        <div class="project-desc">Full-stack credibility score platform with real-time calculations, smooth animations, and a polished dashboard experience.</div>
        <div class="project-tags">
          <span class="tag">Next.js</span>
          <span class="tag">TailwindCSS</span>
          <span class="tag">Appwrite</span>
          <span class="tag">Framer Motion</span>
        </div>
        <a href="https://github.com/GoliPranayKumar/Credovia" class="project-link">
          View Project
          <svg width="14" height="14" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
      </div>

      <div class="project-card">
        <div class="project-icon">📚</div>
        <div class="project-name">DSA in Java</div>
        <div class="project-desc">Complete implementation of core Data Structures &amp; Algorithms in Java — Arrays, Stacks, Queues, Trees, Graphs and more.</div>
        <div class="project-tags">
          <span class="tag">Java</span>
          <span class="tag">DSA</span>
          <span class="tag">Algorithms</span>
        </div>
        <a href="https://github.com/GoliPranayKumar/DataStructures" class="project-link">
          View Project
          <svg width="14" height="14" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24"><path d="M5 12h14M12 5l7 7-7 7"/></svg>
        </a>
      </div>

    </div>
  </section>

  <!-- ====== GOALS ====== -->
  <div class="goals-section">
    <div class="goals-inner">
      <div class="section-label">// 004 — Goals</div>
      <h2 class="section-title">Current Mission</h2>
      <div class="goals-grid">
        <div class="goal-item">
          <div class="goal-icon">🎯</div>
          <div class="goal-text">Solve <strong>500+ LeetCode</strong> problems to master competitive programming</div>
        </div>
        <div class="goal-item">
          <div class="goal-icon">🧮</div>
          <div class="goal-text">Master <strong>Advanced DSA</strong> — graphs, DP, segment trees, and beyond</div>
        </div>
        <div class="goal-item">
          <div class="goal-icon">🚀</div>
          <div class="goal-text">Build a <strong>production AI SaaS</strong> with real users and revenue</div>
        </div>
        <div class="goal-item">
          <div class="goal-icon">🌍</div>
          <div class="goal-text">Make meaningful contributions to <strong>Open Source</strong> AI projects</div>
        </div>
      </div>
    </div>
  </div>

  <!-- ====== CONNECT ====== -->
  <section class="connect-section">
    <div class="section-label" style="justify-content:center;">// 005 — Connect</div>
    <h2 class="section-title">Let's Build Together</h2>
    <p style="color:rgba(232,244,255,0.6);font-size:13px;max-width:480px;margin:0 auto;line-height:1.9;">
      Always open to collaborating on interesting AI projects, discussing DSA, or just saying hi. Reach out anytime.
    </p>
    <div class="connect-links">
      <a href="https://www.linkedin.com/in/golipranaykumar/" class="connect-btn cb-linkedin">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a href="mailto:golipranaykumar@gmail.com" class="connect-btn cb-gmail">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M24 5.457v13.909c0 .904-.732 1.636-1.636 1.636h-3.819V11.73L12 16.64l-6.545-4.91v9.273H1.636A1.636 1.636 0 0 1 0 19.366V5.457c0-2.023 2.309-3.178 3.927-1.964L5.455 4.64 12 9.548l6.545-4.908 1.528-1.145C21.69 2.28 24 3.434 24 5.457z"/></svg>
        Gmail
      </a>
      <a href="https://leetcode.com/u/golipranaykumar/" class="connect-btn cb-leetcode">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.545 2.545 0 0 1 .619-1.164L9.13 8.114c1.058-1.134 3.204-1.27 4.43-.278l3.501 2.831c.593.48 1.461.387 1.94-.207a1.384 1.384 0 0 0-.207-1.943l-3.5-2.831c-.8-.647-1.766-1.045-2.774-1.202l2.015-2.158A1.384 1.384 0 0 0 13.483 0zm-2.866 12.815a1.38 1.38 0 0 0-1.38 1.382 1.38 1.38 0 0 0 1.38 1.382H20.79a1.38 1.38 0 0 0 1.38-1.382 1.38 1.38 0 0 0-1.38-1.382z"/></svg>
        LeetCode
      </a>
      <a href="https://github.com/GoliPranayKumar" class="connect-btn cb-github">
        <svg width="16" height="16" fill="currentColor" viewBox="0 0 24 24"><path d="M12 .297c-6.63 0-12 5.373-12 12 0 5.303 3.438 9.8 8.205 11.385.6.113.82-.258.82-.577 0-.285-.01-1.04-.015-2.04-3.338.724-4.042-1.61-4.042-1.61C4.422 18.07 3.633 17.7 3.633 17.7c-1.087-.744.084-.729.084-.729 1.205.084 1.838 1.236 1.838 1.236 1.07 1.835 2.809 1.305 3.495.998.108-.776.417-1.305.76-1.605-2.665-.3-5.466-1.332-5.466-5.93 0-1.31.465-2.38 1.235-3.22-.135-.303-.54-1.523.105-3.176 0 0 1.005-.322 3.3 1.23.96-.267 1.98-.399 3-.405 1.02.006 2.04.138 3 .405 2.28-1.552 3.285-1.23 3.285-1.23.645 1.653.24 2.873.12 3.176.765.84 1.23 1.91 1.23 3.22 0 4.61-2.805 5.625-5.475 5.92.42.36.81 1.096.81 2.22 0 1.606-.015 2.896-.015 3.286 0 .315.21.69.825.57C20.565 22.092 24 17.592 24 12.297c0-6.627-5.373-12-12-12"/></svg>
        GitHub
      </a>
    </div>
  </section>

  <!-- ====== FOOTER ====== -->
  <footer>
    <p>Designed &amp; built by <span>Goli Pranay Kumar</span> &nbsp;•&nbsp; B.Tech AI &amp; Data Science &nbsp;•&nbsp; Vignan Institute of Technology and Science</p>
    <p style="margin-top:8px;font-size:10px;opacity:0.5;">© 2024 — Always Learning 🚀</p>
  </footer>

</div>

<script>
// Custom Cursor
const cursor = document.getElementById('cursor');
const ring = document.getElementById('cursor-ring');
let mx=0,my=0,rx=0,ry=0;
document.addEventListener('mousemove',e=>{
  mx=e.clientX; my=e.clientY;
  cursor.style.left=mx+'px'; cursor.style.top=my+'px';
});
function animRing(){
  rx+=(mx-rx)*0.12; ry+=(my-ry)*0.12;
  ring.style.left=rx+'px'; ring.style.top=ry+'px';
  requestAnimationFrame(animRing);
}
animRing();
document.querySelectorAll('a,button,.pill,.project-card,.stat-card,.goal-item').forEach(el=>{
  el.addEventListener('mouseenter',()=>{ cursor.style.width='20px'; cursor.style.height='20px'; ring.style.width='52px'; ring.style.height='52px'; });
  el.addEventListener('mouseleave',()=>{ cursor.style.width='12px'; cursor.style.height='12px'; ring.style.width='36px'; ring.style.height='36px'; });
});

// Animated Counters
const counters = document.querySelectorAll('.counter');
const counterObserver = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      const el=e.target; const target=+el.dataset.target;
      const dur=1500; const step=dur/60;
      let current=0; const inc=target/60;
      const timer=setInterval(()=>{
        current=Math.min(current+inc,target);
        el.textContent=Math.floor(current)+(target>=100?'+':'');
        if(current>=target)clearInterval(timer);
      },step);
      counterObserver.unobserve(el);
    }
  });
},{threshold:0.5});
counters.forEach(c=>counterObserver.observe(c));

// Skill Bars
const bars = document.querySelectorAll('.skill-bar-fill');
const barObserver = new IntersectionObserver((entries)=>{
  entries.forEach(e=>{
    if(e.isIntersecting){
      e.target.style.width = e.target.dataset.pct+'%';
      barObserver.unobserve(e.target);
    }
  });
},{threshold:0.3});
bars.forEach(b=>barObserver.observe(b));

// Typewriter for hero role (optional extra)
const roles = ['AI & Data Science Engineer','Full Stack Developer','DSA Enthusiast','Open Source Contributor'];
let ri=0,ci=0,deleting=false;
const roleEl = document.querySelector('.hero-role');
if(roleEl){
  function typeRole(){
    const full=roles[ri];
    if(!deleting){ roleEl.textContent=full.slice(0,ci+1); ci++; }
    else{ roleEl.textContent=full.slice(0,ci-1); ci--; }
    if(!deleting && ci===full.length){ setTimeout(()=>{deleting=true;},1800); setTimeout(typeRole,100); return; }
    if(deleting && ci===0){ deleting=false; ri=(ri+1)%roles.length; setTimeout(typeRole,300); return; }
    setTimeout(typeRole, deleting?40:80);
  }
  roleEl.textContent='';
  setTimeout(typeRole,800);
}
</script>
</body>
</html>
