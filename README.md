<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Raju Bahardar — Profile</title>
<style>
  @import url('https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Syne:wght@400;600;700;800&display=swap');
 
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
 
  :root {
    --bg: #020510;
    --surface: #080e1f;
    --card: #0c1428;
    --border: #1a2a4a;
    --accent: #00d4ff;
    --accent2: #7c3aed;
    --accent3: #f59e0b;
    --text: #e2e8f0;
    --muted: #64748b;
    --glow: rgba(0,212,255,0.15);
  }
 
  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'Syne', sans-serif;
    min-height: 100vh;
    overflow-x: hidden;
    cursor: default;
  }
 
  /* Animated grid background */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(0,212,255,0.03) 1px, transparent 1px),
      linear-gradient(90deg, rgba(0,212,255,0.03) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }
 
  /* Radial glow */
  body::after {
    content: '';
    position: fixed;
    top: -20%;
    left: 50%;
    transform: translateX(-50%);
    width: 800px;
    height: 600px;
    background: radial-gradient(ellipse, rgba(124,58,237,0.12) 0%, transparent 70%);
    pointer-events: none;
    z-index: 0;
  }
 
  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 40px 24px 80px;
    position: relative;
    z-index: 1;
  }
 
  /* ─── HERO ─── */
  .hero {
    border: 1px solid var(--border);
    background: linear-gradient(135deg, #0c1428 0%, #0a1020 50%, #0d0c1e 100%);
    border-radius: 2px;
    padding: 48px 40px 40px;
    position: relative;
    overflow: hidden;
    margin-bottom: 2px;
    animation: fadeSlideIn 0.8s ease both;
  }
 
  .hero::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, transparent, var(--accent), var(--accent2), transparent);
  }
 
  .hero::after {
    content: 'IOE // PULCHOWK';
    position: absolute;
    bottom: 20px; right: 28px;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.2em;
    color: var(--muted);
    opacity: 0.5;
  }
 
  .hero-tag {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    letter-spacing: 0.25em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .hero-tag::before {
    content: '';
    width: 24px; height: 1px;
    background: var(--accent);
  }
 
  .hero h1 {
    font-size: clamp(2rem, 5vw, 3.2rem);
    font-weight: 800;
    line-height: 1.05;
    letter-spacing: -0.02em;
    margin-bottom: 6px;
  }
  .hero h1 .name-first { color: var(--text); }
  .hero h1 .name-last {
    color: transparent;
    -webkit-text-stroke: 1.5px var(--accent);
    display: block;
  }
 
  .hero-subtitle {
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: var(--accent2);
    letter-spacing: 0.1em;
    margin-bottom: 24px;
  }
 
  .hero-desc {
    max-width: 560px;
    font-size: 15px;
    line-height: 1.7;
    color: #94a3b8;
    margin-bottom: 28px;
  }
 
  .hero-desc strong {
    color: var(--accent);
    font-weight: 600;
  }
 
  .hero-links {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
  }
 
  .btn {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    letter-spacing: 0.1em;
    padding: 10px 20px;
    border: 1px solid;
    text-decoration: none;
    transition: all 0.2s;
    display: inline-flex;
    align-items: center;
    gap: 8px;
  }
  .btn-primary {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0,212,255,0.05);
  }
  .btn-primary:hover {
    background: rgba(0,212,255,0.12);
    box-shadow: 0 0 20px rgba(0,212,255,0.2);
  }
  .btn-secondary {
    border-color: var(--border);
    color: var(--muted);
  }
  .btn-secondary:hover {
    border-color: var(--accent2);
    color: var(--accent2);
  }
 
  /* Floating badge */
  .badge-3rd {
    position: absolute;
    top: 36px; right: 36px;
    width: 72px; height: 72px;
    border: 1px solid var(--accent3);
    border-radius: 50%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    background: rgba(245,158,11,0.05);
    animation: spin-slow 12s linear infinite;
  }
  .badge-3rd span:first-child {
    font-size: 20px;
    font-weight: 800;
    color: var(--accent3);
    line-height: 1;
  }
  .badge-3rd span:last-child {
    font-family: 'Space Mono', monospace;
    font-size: 7px;
    color: var(--accent3);
    letter-spacing: 0.1em;
    opacity: 0.8;
  }
  @keyframes spin-slow {
    from { transform: rotate(0deg); }
    to { transform: rotate(360deg); }
  }
 
  /* ─── SECTION LAYOUT ─── */
  .grid-2 {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    margin-bottom: 2px;
  }
 
  .section-card {
    background: var(--card);
    border: 1px solid var(--border);
    padding: 28px;
    position: relative;
    animation: fadeSlideIn 0.8s ease both;
  }
  .section-card:nth-child(2) { animation-delay: 0.1s; }
  .section-card:nth-child(3) { animation-delay: 0.15s; }
  .section-card:nth-child(4) { animation-delay: 0.2s; }
 
  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 9px;
    letter-spacing: 0.3em;
    color: var(--accent);
    text-transform: uppercase;
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 8px;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }
 
  /* ─── SKILLS GRID ─── */
  .skills-row {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  .skill-pill {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    padding: 5px 12px;
    border: 1px solid var(--border);
    color: var(--muted);
    letter-spacing: 0.05em;
    transition: all 0.2s;
    cursor: default;
  }
  .skill-pill:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(0,212,255,0.05);
  }
  .skill-pill.hot {
    border-color: rgba(124,58,237,0.4);
    color: #a78bfa;
  }
  .skill-pill.hot:hover {
    border-color: var(--accent2);
    background: rgba(124,58,237,0.08);
  }
 
  /* ─── FOCUS AREAS ─── */
  .focus-list { list-style: none; }
  .focus-list li {
    padding: 10px 0;
    border-bottom: 1px solid var(--border);
    font-size: 13px;
    color: #94a3b8;
    display: flex;
    align-items: flex-start;
    gap: 10px;
    line-height: 1.5;
  }
  .focus-list li:last-child { border-bottom: none; }
  .focus-list li::before {
    content: '→';
    color: var(--accent);
    font-family: 'Space Mono', monospace;
    flex-shrink: 0;
    margin-top: 1px;
  }
  .focus-list li strong { color: var(--text); font-weight: 600; }
 
  /* ─── STATS CARD ─── */
  .stats-wide {
    grid-column: 1 / -1;
    background: var(--card);
    border: 1px solid var(--border);
    padding: 28px;
  }
 
  .stats-img-row {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
    margin-top: 12px;
  }
  .stats-img-row img {
    border: 1px solid var(--border);
    border-radius: 2px;
    max-width: 100%;
    flex: 1 1 200px;
    height: auto;
    filter: saturate(0.8);
    transition: filter 0.2s;
  }
  .stats-img-row img:hover { filter: saturate(1.1); }
 
  /* ─── TROPHIES ─── */
  .trophies-card {
    background: var(--card);
    border: 1px solid var(--border);
    padding: 28px;
    margin-bottom: 2px;
    animation: fadeSlideIn 0.8s 0.25s ease both;
  }
  .trophies-card img {
    width: 100%;
    height: auto;
    border: 1px solid var(--border);
    filter: saturate(0.7);
    transition: filter 0.2s;
  }
  .trophies-card img:hover { filter: saturate(1); }
 
  /* ─── FOOTER ─── */
  .footer-strip {
    background: var(--surface);
    border: 1px solid var(--border);
    padding: 16px 28px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 12px;
    animation: fadeSlideIn 0.8s 0.3s ease both;
  }
  .footer-strip .mono {
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.1em;
  }
  .footer-strip .mono span { color: var(--accent); }
 
  .visit-badge {
    display: flex;
    align-items: center;
    gap: 8px;
    font-family: 'Space Mono', monospace;
    font-size: 10px;
    color: var(--muted);
  }
  .visit-dot {
    width: 6px; height: 6px;
    background: #22c55e;
    border-radius: 50%;
    animation: pulse-dot 2s infinite;
  }
  @keyframes pulse-dot {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(1.4); }
  }
 
  /* ─── ANIMATIONS ─── */
  @keyframes fadeSlideIn {
    from { opacity: 0; transform: translateY(16px); }
    to { opacity: 1; transform: translateY(0); }
  }
 
  /* ─── RESPONSIVE ─── */
  @media (max-width: 580px) {
    .grid-2 { grid-template-columns: 1fr; }
    .badge-3rd { display: none; }
    .hero { padding: 32px 24px 32px; }
  }
</style>
</head>
<body>
<div class="container">
 
  <!-- HERO -->
  <div class="hero">
    <div class="hero-tag">Engineering Student · AI/ML Engineer</div>
    <h1>
      <span class="name-first">Raju</span>
      <span class="name-last">Bahardar</span>
    </h1>
    <div class="hero-subtitle">3RD YEAR · IOE PULCHOWK CAMPUS</div>
    <p class="hero-desc">
      Building intelligent systems at the intersection of <strong>machine learning</strong> and <strong>power systems</strong>. I work with Python, Pandas, NumPy, and Scikit-learn to develop predictive models — currently exploring <strong>forecasting, optimization,</strong> and <strong>real-time automation</strong>.
    </p>
    <div class="hero-links">
      <a class="btn btn-primary" href="https://linkedin.com/in/raju-bahardar-876527334" target="_blank">
        ↗ LinkedIn
      </a>
      <a class="btn btn-secondary" href="mailto:rajubahardar7@gmail.com">
        ✉ rajubahardar7@gmail.com
      </a>
    </div>
    <div class="badge-3rd">
      <span>3rd</span>
      <span>YEAR</span>
    </div>
  </div>
 
  <!-- TWO COLUMN -->
  <div class="grid-2">
 
    <!-- TECH STACK -->
    <div class="section-card">
      <div class="section-label">Tech Stack</div>
      <div style="margin-bottom:14px;">
        <div style="font-family:'Space Mono',monospace;font-size:9px;letter-spacing:0.15em;color:var(--muted);margin-bottom:8px;">CORE</div>
        <div class="skills-row">
          <span class="skill-pill hot">Python</span>
          <span class="skill-pill hot">Scikit-learn</span>
          <span class="skill-pill hot">NumPy</span>
          <span class="skill-pill hot">Pandas</span>
          <span class="skill-pill hot">OpenCV</span>
        </div>
      </div>
      <div style="margin-bottom:14px;">
        <div style="font-family:'Space Mono',monospace;font-size:9px;letter-spacing:0.15em;color:var(--muted);margin-bottom:8px;">SYSTEMS</div>
        <div class="skills-row">
          <span class="skill-pill">C</span>
          <span class="skill-pill">C++</span>
          <span class="skill-pill">Arduino</span>
        </div>
      </div>
      <div>
        <div style="font-family:'Space Mono',monospace;font-size:9px;letter-spacing:0.15em;color:var(--muted);margin-bottom:8px;">WEB + TOOLS</div>
        <div class="skills-row">
          <span class="skill-pill">JavaScript</span>
          <span class="skill-pill">HTML5</span>
          <span class="skill-pill">Git</span>
          <span class="skill-pill">GitHub</span>
          <span class="skill-pill">Matplotlib</span>
        </div>
      </div>
    </div>
 
    <!-- FOCUS AREAS -->
    <div class="section-card">
      <div class="section-label">Current Focus</div>
      <ul class="focus-list">
        <li><strong>ML in Power Systems</strong> — forecasting load curves and grid behavior</li>
        <li><strong>Optimization</strong> — energy dispatch and intelligent control loops</li>
        <li><strong>Real-time Systems</strong> — predictive automation with embedded hardware</li>
        <li><strong>Data Analysis</strong> — building end-to-end ML pipelines from raw sensor data</li>
      </ul>
    </div>
 
    <!-- GITHUB STATS -->
    <div class="stats-wide">
      <div class="section-label">GitHub Activity</div>
      <div class="stats-img-row">
        <img src="https://github-readme-stats.vercel.app/api?username=Rajubahardar&theme=tokyonight&hide_border=true&include_all_commits=true&count_private=false" alt="GitHub Stats" />
        <img src="https://nirzak-streak-stats.vercel.app/?user=Rajubahardar&theme=tokyonight&hide_border=true" alt="Streak" />
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Rajubahardar&theme=tokyonight&hide_border=true&layout=compact" alt="Top Languages" />
      </div>
    </div>
 
  </div>
 
  <!-- TROPHIES -->
  <div class="trophies-card">
    <div class="section-label">GitHub Trophies</div>
    <img src="https://github-profile-trophy.vercel.app/?username=Rajubahardar&theme=radical&no-frame=true&no-bg=true&margin-w=4&row=1" alt="Trophies" />
  </div>
 
  <!-- FOOTER -->
  <div class="footer-strip">
    <div class="mono">
      <span>Raju Bahardar</span> · Always learning, building, improving.
    </div>
    <div class="visit-badge">
      <div class="visit-dot"></div>
      <span>Profile Active</span>
    </div>
  </div>
 
</div>
</body>
</html>
