<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Ritesh Gangurde — Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300;400;500;600;700&family=Syne:wght@700;800&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

:root {
  --bg: #05060e;
  --glass: rgba(255,255,255,0.04);
  --glass-border: rgba(255,255,255,0.10);
  --glass-hover: rgba(255,255,255,0.07);
  --text: #e2e8f4;
  --muted: #4e576b;
  --va: #a78bfa;
  --vb: #60a5fa;
  --vc: #34d399;
  --vd: #f472b6;
  --ve: #fb923c;
}

html { scroll-behavior: smooth; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Space Grotesk', sans-serif;
  min-height: 100vh;
  overflow-x: hidden;
  line-height: 1.65;
}

/* ═══════════════════════════════
   STARFIELD CANVAS
═══════════════════════════════ */
#starfield {
  position: fixed;
  inset: 0;
  z-index: 0;
  pointer-events: none;
}

/* aurora blobs behind stars */
.aurora {
  position: fixed;
  inset: 0;
  z-index: 0;
  pointer-events: none;
  overflow: hidden;
}
.aurora-blob {
  position: absolute;
  border-radius: 50%;
  filter: blur(120px);
  opacity: 0.55;
}
.ab1 {
  width: 700px; height: 700px;
  top: -250px; left: -200px;
  background: radial-gradient(circle, rgba(109,40,217,0.30) 0%, transparent 70%);
  animation: ab1 22s ease-in-out infinite alternate;
}
.ab2 {
  width: 550px; height: 550px;
  top: 20%; right: -180px;
  background: radial-gradient(circle, rgba(37,99,235,0.22) 0%, transparent 70%);
  animation: ab2 28s ease-in-out infinite alternate;
}
.ab3 {
  width: 480px; height: 480px;
  bottom: -100px; left: 10%;
  background: radial-gradient(circle, rgba(5,150,105,0.16) 0%, transparent 70%);
  animation: ab3 32s ease-in-out infinite alternate;
}

@keyframes ab1 { 0%{transform:translate(0,0) scale(1)} 100%{transform:translate(60px,40px) scale(1.08)} }
@keyframes ab2 { 0%{transform:translate(0,0) scale(1)} 100%{transform:translate(-60px,50px) scale(1.1)} }
@keyframes ab3 { 0%{transform:translate(0,0) scale(1)} 100%{transform:translate(40px,-50px) scale(1.07)} }

/* ═══════════════════════════════
   LAYOUT
═══════════════════════════════ */
.container {
  position: relative;
  z-index: 2;
  max-width: 900px;
  margin: 0 auto;
  padding: 2.5rem 1.5rem 6rem;
}

/* ═══════════════════════════════
   HERO
═══════════════════════════════ */
.hero {
  text-align: center;
  padding: 5rem 1rem 3rem;
  animation: fadeUp 1s cubic-bezier(.16,1,.3,1) both;
}

/* ── Avatar ── */
.avatar-wrap {
  width: 136px;
  height: 136px;
  margin: 0 auto 2rem;
  position: relative;
  flex-shrink: 0;
}

/* outer halo */
.av-halo {
  position: absolute;
  inset: -20px;
  border-radius: 50%;
  background: conic-gradient(from 0deg, rgba(167,139,250,0.3), rgba(96,165,250,0.2), rgba(52,211,153,0.15), rgba(244,114,182,0.2), rgba(167,139,250,0.3));
  filter: blur(16px);
  animation: haloPulse 4s ease-in-out infinite;
}

/* spinning ring */
.av-ring {
  position: absolute;
  inset: -3px;
  border-radius: 50%;
  padding: 3px;
  background: conic-gradient(from 0deg, #a78bfa, #60a5fa, #34d399, #f472b6, #fb923c, #a78bfa);
  animation: ringRotate 8s linear infinite;
}
.av-ring-inner {
  width: 100%; height: 100%;
  border-radius: 50%;
  background: #080912;
}

/* glass circle */
.av-face {
  position: absolute;
  inset: 4px;
  border-radius: 50%;
  background: linear-gradient(145deg, rgba(255,255,255,0.08), rgba(255,255,255,0.02));
  backdrop-filter: blur(20px);
  border: 1px solid rgba(255,255,255,0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 2;
}

.av-initials {
  font-family: 'Syne', sans-serif;
  font-size: 2rem;
  font-weight: 800;
  letter-spacing: -0.02em;
  background: linear-gradient(135deg, #c4b5fd 0%, #93c5fd 50%, #6ee7b7 100%);
  background-clip: text;
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  line-height: 1;
}

@keyframes haloPulse {
  0%,100%{transform:scale(1); opacity:0.6}
  50%{transform:scale(1.1); opacity:0.9}
}
@keyframes ringRotate { to{transform:rotate(360deg)} }

/* ── Name — FIXED: fluid sizing so it never gets clipped ── */
.hero-badge {
  display: inline-block;
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.7rem;
  letter-spacing: 0.2em;
  color: var(--va);
  background: rgba(167,139,250,0.08);
  border: 1px solid rgba(167,139,250,0.2);
  border-radius: 999px;
  padding: 0.28rem 0.9rem;
  margin-bottom: 1rem;
}

.hero-name {
  font-family: 'Syne', sans-serif;
  font-weight: 800;
  font-size: clamp(2rem, 7vw, 3.4rem);
  line-height: 1.1;
  letter-spacing: -0.04em;
  color: #fff;
  white-space: normal;
  word-break: break-word;
  overflow-wrap: anywhere;
  padding: 0 0.5rem;
  margin-bottom: 0.8rem;
}

.hero-tagline {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.9rem;
  color: var(--muted);
  height: 1.6rem;
  margin-bottom: 2rem;
}
.typed-cursor {
  display: inline-block;
  width: 2px; height: 0.9em;
  background: var(--vb);
  margin-left: 2px;
  vertical-align: middle;
  animation: blink 1.1s step-end infinite;
}

/* ── Social buttons — glassmorphism ── */
.social-row {
  display: flex;
  gap: 0.7rem;
  justify-content: center;
  flex-wrap: wrap;
}

.soc-btn {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.6rem 1.3rem;
  border-radius: 12px;
  font-size: 0.82rem;
  font-weight: 500;
  text-decoration: none;
  color: var(--text);
  background: var(--glass);
  border: 1px solid var(--glass-border);
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  transition: all 0.25s ease;
  position: relative;
  overflow: hidden;
}
.soc-btn::before {
  content: '';
  position: absolute;
  inset: 0;
  background: linear-gradient(135deg, rgba(255,255,255,0.06), transparent);
  pointer-events: none;
}
.soc-btn:hover {
  background: rgba(167,139,250,0.1);
  border-color: rgba(167,139,250,0.35);
  color: #c4b5fd;
  transform: translateY(-3px);
  box-shadow: 0 12px 30px rgba(0,0,0,0.4), 0 0 20px rgba(167,139,250,0.12);
}
.soc-btn svg { width: 16px; height: 16px; flex-shrink: 0; }

/* ═══════════════════════════════
   GLASS DIVIDER
═══════════════════════════════ */
.divider {
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(255,255,255,0.07), transparent);
  margin: 2.5rem 0;
}

/* ═══════════════════════════════
   SECTIONS
═══════════════════════════════ */
.section {
  margin: 2.8rem 0;
  opacity: 0;
  transform: translateY(24px);
  transition: opacity 0.7s ease, transform 0.7s ease;
}
.section.visible { opacity: 1; transform: none; }

.sec-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.66rem;
  letter-spacing: 0.22em;
  text-transform: uppercase;
  color: var(--va);
  margin-bottom: 1.3rem;
  display: flex;
  align-items: center;
  gap: 0.7rem;
}
.sec-label::before { content: '//'; opacity: 0.5; }
.sec-label::after {
  content: '';
  flex: 1;
  height: 1px;
  background: linear-gradient(to right, rgba(167,139,250,0.25), transparent);
}

/* ── Info cards — glass ── */
.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 0.85rem;
}

.glass-card {
  background: var(--glass);
  border: 1px solid var(--glass-border);
  border-radius: 16px;
  padding: 1.2rem 1.25rem;
  backdrop-filter: blur(20px);
  -webkit-backdrop-filter: blur(20px);
  position: relative;
  overflow: hidden;
  transition: all 0.28s ease;
}
.glass-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(255,255,255,0.18), transparent);
}
.glass-card::after {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 50% -20%, rgba(167,139,250,0.07), transparent 65%);
  opacity: 0;
  transition: opacity 0.3s;
}
.glass-card:hover {
  border-color: rgba(167,139,250,0.22);
  transform: translateY(-5px);
  box-shadow: 0 20px 50px rgba(0,0,0,0.5), 0 0 0 1px rgba(167,139,250,0.08);
}
.glass-card:hover::after { opacity: 1; }

.gc-icon {
  font-size: 1.4rem;
  margin-bottom: 0.7rem;
  display: block;
  position: relative; z-index: 1;
}
.gc-title {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.64rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
  margin-bottom: 0.35rem;
  position: relative; z-index: 1;
}
.gc-text {
  font-size: 0.88rem;
  color: var(--text);
  line-height: 1.5;
  position: relative; z-index: 1;
}

/* ── Tech tags ── */
.tag-row-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.64rem;
  letter-spacing: 0.14em;
  text-transform: uppercase;
  color: var(--muted);
  margin: 1.1rem 0 0.6rem;
}
.tech-row { display: flex; flex-wrap: wrap; gap: 0.45rem; }

.tag {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.32rem 0.8rem;
  border-radius: 8px;
  font-size: 0.76rem;
  font-family: 'JetBrains Mono', monospace;
  font-weight: 500;
  border: 1px solid transparent;
  backdrop-filter: blur(10px);
  cursor: default;
  transition: all 0.2s ease;
  opacity: 0;
  animation: tagPop 0.4s ease forwards;
}
.tag:hover { transform: translateY(-2px) scale(1.06); }

.t-lang   { background:rgba(167,139,250,.08); color:#c4b5fd; border-color:rgba(167,139,250,.2); }
.t-frame  { background:rgba(96,165,250,.08);  color:#93c5fd; border-color:rgba(96,165,250,.2); }
.t-db     { background:rgba(251,146,60,.08);  color:#fdba74; border-color:rgba(251,146,60,.2); }
.t-design { background:rgba(244,114,182,.08); color:#f9a8d4; border-color:rgba(244,114,182,.2); }
.t-tools  { background:rgba(52,211,153,.08);  color:#6ee7b7; border-color:rgba(52,211,153,.2); }
.t-game   { background:rgba(248,113,113,.08); color:#fca5a5; border-color:rgba(248,113,113,.2); }

.tag:nth-child(1){animation-delay:.02s}.tag:nth-child(2){animation-delay:.04s}
.tag:nth-child(3){animation-delay:.06s}.tag:nth-child(4){animation-delay:.08s}
.tag:nth-child(5){animation-delay:.10s}.tag:nth-child(6){animation-delay:.12s}
.tag:nth-child(7){animation-delay:.14s}.tag:nth-child(8){animation-delay:.16s}
.tag:nth-child(n+9){animation-delay:.18s}

/* ── GitHub stats ── */
.stats-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(265px, 1fr));
  gap: 1rem;
}

.stat-card {
  background: var(--glass);
  border: 1px solid var(--glass-border);
  border-radius: 16px;
  overflow: hidden;
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  position: relative;
  transition: all 0.28s ease;
}
.stat-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0;
  height: 1px;
  background: linear-gradient(to right, transparent, rgba(255,255,255,0.14), transparent);
  z-index: 1;
}
.stat-card:hover {
  border-color: rgba(167,139,250,0.22);
  transform: translateY(-4px);
  box-shadow: 0 20px 50px rgba(0,0,0,0.55), 0 0 30px rgba(167,139,250,0.08);
}
.stat-card img {
  width: 100%;
  display: block;
  border-radius: 16px;
}

/* ── Stat counters ── */
.counters-row {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
  gap: 0.85rem;
  margin-bottom: 1.2rem;
}
.counter-card {
  background: var(--glass);
  border: 1px solid var(--glass-border);
  border-radius: 14px;
  padding: 1rem 1.1rem;
  backdrop-filter: blur(16px);
  text-align: center;
  transition: all 0.25s;
  position: relative;
  overflow: hidden;
}
.counter-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(to right, transparent, rgba(255,255,255,0.15), transparent);
}
.counter-card:hover { transform: translateY(-3px); border-color: rgba(255,255,255,0.16); }
.cc-num {
  font-family: 'Syne', sans-serif;
  font-size: 1.8rem;
  font-weight: 800;
  line-height: 1;
  margin-bottom: 0.3rem;
}
.cc-label {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.62rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--muted);
}

/* ── Fun fact ── */
.funfact-card {
  background: linear-gradient(120deg, rgba(167,139,250,0.06), rgba(96,165,250,0.05));
  border: 1px solid rgba(167,139,250,0.14);
  border-radius: 16px;
  padding: 1.5rem 1.8rem;
  backdrop-filter: blur(16px);
  position: relative;
  overflow: hidden;
}
.funfact-card::before {
  content: '';
  position: absolute;
  top: 0; left: 0; right: 0; height: 1px;
  background: linear-gradient(to right, transparent, rgba(167,139,250,0.3), transparent);
}
.funfact-card .ff-tag {
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.64rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: var(--vc);
  margin-bottom: 0.5rem;
}
.funfact-card p { font-size: 0.95rem; color: var(--text); }

/* ── Footer ── */
footer {
  text-align: center;
  margin-top: 4rem;
  padding-top: 2rem;
  border-top: 1px solid rgba(255,255,255,0.05);
  font-family: 'JetBrains Mono', monospace;
  font-size: 0.74rem;
  color: var(--muted);
}
footer span { color: var(--va); }

/* ═══════════════════════════════
   KEYFRAMES
═══════════════════════════════ */
@keyframes fadeUp {
  from{opacity:0;transform:translateY(30px)}
  to{opacity:1;transform:translateY(0)}
}
@keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }
@keyframes tagPop {
  from{opacity:0;transform:scale(0.82) translateY(5px)}
  to{opacity:1;transform:scale(1) translateY(0)}
}
</style>
</head>
<body>

<!-- aurora -->
<div class="aurora">
  <div class="aurora-blob ab1"></div>
  <div class="aurora-blob ab2"></div>
  <div class="aurora-blob ab3"></div>
</div>

<!-- starfield -->
<canvas id="starfield"></canvas>

<div class="container">

  <!-- ─── HERO ─── -->
  <header class="hero">
    <div class="avatar-wrap">
      <div class="av-halo"></div>
      <div class="av-ring"><div class="av-ring-inner"></div></div>
      <div class="av-face"><div class="av-initials">RG</div></div>
    </div>

    <div class="hero-badge">// Hello, World!</div>
    <h1 class="hero-name">Ritesh Gangurde</h1>
    <p class="hero-tagline">
      <span id="typed"></span><span class="typed-cursor"></span>
    </p>

    <div class="social-row">
      <a class="soc-btn" href="https://discord.gg/Diablo6529" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.317 4.37a19.791 19.791 0 0 0-4.885-1.515.074.074 0 0 0-.079.037c-.21.375-.444.864-.608 1.25a18.27 18.27 0 0 0-5.487 0 12.64 12.64 0 0 0-.617-1.25.077.077 0 0 0-.079-.037A19.736 19.736 0 0 0 3.677 4.37a.07.07 0 0 0-.032.027C.533 9.046-.32 13.58.099 18.057c.002.022.015.043.032.055a19.9 19.9 0 0 0 5.993 3.03.078.078 0 0 0 .084-.028c.462-.63.874-1.295 1.226-1.994a.076.076 0 0 0-.041-.106 13.107 13.107 0 0 1-1.872-.892.077.077 0 0 1-.008-.128 10.2 10.2 0 0 0 .372-.292.074.074 0 0 1 .077-.01c3.928 1.793 8.18 1.793 12.062 0a.074.074 0 0 1 .078.01c.12.098.246.198.373.292a.077.077 0 0 1-.006.127 12.299 12.299 0 0 1-1.873.892.077.077 0 0 0-.041.107c.36.698.772 1.362 1.225 1.993a.076.076 0 0 0 .084.028 19.839 19.839 0 0 0 6.002-3.03.077.077 0 0 0 .032-.054c.5-5.177-.838-9.674-3.549-13.66a.061.061 0 0 0-.031-.03z"/></svg>
        Discord
      </a>
      <a class="soc-btn" href="https://linkedin.com/in/ritesh-gangurde-7b93b9227" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433a2.062 2.062 0 0 1-2.063-2.065 2.064 2.064 0 1 1 2.063 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/></svg>
        LinkedIn
      </a>
      <a class="soc-btn" href="https://github.com/RiteshGangurde" target="_blank">
        <svg viewBox="0 0 24 24" fill="currentColor"><path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0 1 12 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/></svg>
        GitHub
      </a>
    </div>
  </header>

  <div class="divider"></div>

  <!-- ─── ABOUT ─── -->
  <section class="section">
    <div class="sec-label">about.json</div>
    <div class="info-grid">
      <div class="glass-card"><span class="gc-icon">🛠</span><div class="gc-title">Currently Building</div><div class="gc-text">Cross-platform food ordering app with React Native</div></div>
      <div class="glass-card"><span class="gc-icon">🌱</span><div class="gc-title">Currently Learning</div><div class="gc-text">Advanced React Native &amp; cyber forensics</div></div>
      <div class="glass-card"><span class="gc-icon">🤝</span><div class="gc-title">Open to Collaborate</div><div class="gc-text">Front-end projects &amp; hackathon teams</div></div>
      <div class="glass-card"><span class="gc-icon">🧩</span><div class="gc-title">Seeking Help With</div><div class="gc-text">iOS development &amp; cyber forensics</div></div>
      <div class="glass-card"><span class="gc-icon">💬</span><div class="gc-title">Ask Me About</div><div class="gc-text">Front-end dev, Smart India Hackathon &amp; UI projects</div></div>
    </div>
  </section>

  <!-- ─── TECH STACK ─── -->
  <section class="section">
    <div class="sec-label">tech_stack</div>

    <div class="tag-row-label">Languages</div>
    <div class="tech-row">
      <span class="tag t-lang">C</span><span class="tag t-lang">C++</span><span class="tag t-lang">C#</span>
      <span class="tag t-lang">JavaScript</span><span class="tag t-lang">Java</span><span class="tag t-lang">Kotlin</span>
      <span class="tag t-lang">PHP</span><span class="tag t-lang">HTML5</span><span class="tag t-lang">CSS3</span><span class="tag t-lang">LaTeX</span>
    </div>

    <div class="tag-row-label">Frameworks &amp; Runtimes</div>
    <div class="tech-row">
      <span class="tag t-frame">React</span><span class="tag t-frame">React Native</span><span class="tag t-frame">Next.js</span>
      <span class="tag t-frame">Node.js</span><span class="tag t-frame">Flutter</span><span class="tag t-frame">Bootstrap</span>
      <span class="tag t-frame">TailwindCSS</span><span class="tag t-frame">Firebase</span>
    </div>

    <div class="tag-row-label">Databases</div>
    <div class="tech-row">
      <span class="tag t-db">MySQL</span><span class="tag t-db">MongoDB</span><span class="tag t-db">SQLite</span>
    </div>

    <div class="tag-row-label">Design &amp; Creative</div>
    <div class="tech-row">
      <span class="tag t-design">Figma</span><span class="tag t-design">Adobe XD</span><span class="tag t-design">Photoshop</span>
      <span class="tag t-design">Illustrator</span><span class="tag t-design">After Effects</span>
      <span class="tag t-design">Premiere Pro</span><span class="tag t-design">Blender</span><span class="tag t-design">Canva</span>
    </div>

    <div class="tag-row-label">Tools</div>
    <div class="tech-row">
      <span class="tag t-tools">Git</span><span class="tag t-tools">GitHub</span>
      <span class="tag t-tools">Apache</span><span class="tag t-tools">Anaconda</span>
    </div>

    <div class="tag-row-label">Gaming &amp; Engines</div>
    <div class="tech-row">
      <span class="tag t-game">Unity</span><span class="tag t-game">Unreal Engine</span><span class="tag t-game">OpenGL</span>
      <span class="tag t-game">Epic Games</span><span class="tag t-game">Riot Games</span><span class="tag t-game">nVidia</span>
    </div>
  </section>

  <!-- ─── GITHUB STATS ─── -->
  <section class="section">
    <div class="sec-label">github.stats()</div>

    <!-- Live counters pulled from GitHub API -->
    <div class="counters-row" id="counters">
      <div class="counter-card">
        <div class="cc-num" id="cnt-repos" style="color:var(--va)">—</div>
        <div class="cc-label">Public Repos</div>
      </div>
      <div class="counter-card">
        <div class="cc-num" id="cnt-followers" style="color:var(--vb)">—</div>
        <div class="cc-label">Followers</div>
      </div>
      <div class="counter-card">
        <div class="cc-num" id="cnt-following" style="color:var(--vc)">—</div>
        <div class="cc-label">Following</div>
      </div>
      <div class="counter-card">
        <div class="cc-num" id="cnt-stars" style="color:var(--vd)">—</div>
        <div class="cc-label">Stars Earned</div>
      </div>
    </div>

    <div class="stats-grid">
      <div class="stat-card">
        <img src="https://github-readme-stats.vercel.app/api?username=RiteshGangurde&show_icons=true&theme=transparent&hide_border=true&bg_color=00000000&title_color=a78bfa&text_color=94a3b8&icon_color=60a5fa&ring_color=a78bfa" alt="GitHub Stats" loading="lazy">
      </div>
      <div class="stat-card">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=RiteshGangurde&theme=transparent&hide_border=true&background=00000000&ring=a78bfa&fire=fb923c&currStreakLabel=60a5fa&sideLabels=94a3b8&dates=4e576b&stroke=1e293b" alt="Streak" loading="lazy">
      </div>
      <div class="stat-card">
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=RiteshGangurde&theme=transparent&hide_border=true&bg_color=00000000&title_color=a78bfa&text_color=94a3b8&layout=compact" alt="Top Langs" loading="lazy">
      </div>
      <div class="stat-card">
        <img src="https://github-contributor-stats.vercel.app/api?username=RiteshGangurde&limit=5&theme=dark&combine_all_yearly_contributions=true&hide_border=true&bg_color=00000000" alt="Top Repos" loading="lazy">
      </div>
    </div>
  </section>

  <!-- ─── FUN FACT ─── -->
  <section class="section">
    <div class="funfact-card">
      <div class="ff-tag">⚡ fun_fact</div>
      <p>Passionate about solving real-world problems through technology and innovation — turning bold ideas into impactful, elegant software.</p>
    </div>
  </section>

  <footer>crafted by <span>Ritesh Gangurde</span> &nbsp;·&nbsp; <span>@RiteshGangurde</span></footer>

</div>

<script>
/* ══════════════════════════════════════
   STARFIELD + METEORS
══════════════════════════════════════ */
const canvas = document.getElementById('starfield');
const ctx    = canvas.getContext('2d');
let W, H;

function resize() {
  W = canvas.width  = window.innerWidth;
  H = canvas.height = document.documentElement.scrollHeight;
}
resize();
window.addEventListener('resize', resize);

/* ── Stars ── */
const STAR_COUNT = 320;
const stars = Array.from({length: STAR_COUNT}, () => ({
  x: Math.random(),
  y: Math.random(),
  r: Math.random() * 1.4 + 0.3,
  alpha: Math.random() * 0.6 + 0.2,
  speed: Math.random() * 0.0004 + 0.0001,   // twinkle speed
  phase: Math.random() * Math.PI * 2
}));

/* ── Meteors / shooting stars ── */
class Meteor {
  constructor(immediate = false) {
    this.reset(immediate);
  }
  reset(immediate = false) {
    // start from top quarter, random x position
    this.x  = Math.random() * W * 1.4 - W * 0.2;
    this.y  = immediate ? Math.random() * H * 0.5 : -40;
    this.len = Math.random() * 180 + 80;
    this.speed = Math.random() * 7 + 5;
    this.angle = Math.PI / 5 + (Math.random() - 0.5) * 0.3; // ~36deg
    this.alpha = 0;
    this.life  = 0;
    this.maxLife = Math.random() * 60 + 50;
    this.color = Math.random() < 0.5 ? '#c4b5fd' : '#93c5fd';
    this.width = Math.random() * 1.5 + 0.5;
  }
  step() {
    this.life++;
    this.x += Math.cos(this.angle) * this.speed;
    this.y += Math.sin(this.angle) * this.speed;
    // fade in / out
    const p = this.life / this.maxLife;
    this.alpha = p < 0.2 ? p / 0.2 : p > 0.7 ? (1 - p) / 0.3 : 1;
    if (this.life >= this.maxLife || this.x > W + 200 || this.y > H + 200) this.reset();
  }
  draw() {
    const tx = this.x - Math.cos(this.angle) * this.len;
    const ty = this.y - Math.sin(this.angle) * this.len;
    const grad = ctx.createLinearGradient(tx, ty, this.x, this.y);
    grad.addColorStop(0, 'transparent');
    grad.addColorStop(0.6, this.color.replace(')', `,${this.alpha * 0.4})`).replace('rgb', 'rgba').replace('#', 'rgba(').replace(')', ''));
    grad.addColorStop(1, this.color + Math.round(this.alpha * 255).toString(16).padStart(2,'0'));
    ctx.save();
    ctx.beginPath();
    ctx.moveTo(tx, ty);
    ctx.lineTo(this.x, this.y);
    ctx.strokeStyle = grad;
    ctx.lineWidth = this.width;
    ctx.globalAlpha = this.alpha;
    ctx.shadowColor = this.color;
    ctx.shadowBlur = 6;
    ctx.stroke();
    // tiny bright head
    ctx.beginPath();
    ctx.arc(this.x, this.y, this.width * 1.2, 0, Math.PI * 2);
    ctx.fillStyle = '#fff';
    ctx.globalAlpha = this.alpha * 0.9;
    ctx.fill();
    ctx.restore();
  }
}

const meteors = Array.from({length: 4}, () => new Meteor(true));
// stagger new meteors over time
let nextMeteorIn = 0;

function drawStars(t) {
  stars.forEach(s => {
    const tw = 0.5 + 0.5 * Math.sin(t * s.speed * 1000 + s.phase);
    ctx.beginPath();
    ctx.arc(s.x * W, s.y * H, s.r, 0, Math.PI * 2);
    ctx.fillStyle = `rgba(220,230,255,${s.alpha * tw})`;
    ctx.fill();
  });
}

function loop(t) {
  ctx.clearRect(0, 0, W, H);
  drawStars(t * 0.001);

  // spawn meteors periodically
  nextMeteorIn--;
  if (nextMeteorIn <= 0) {
    const idx = meteors.findIndex(m => m.life >= m.maxLife - 2);
    if (idx !== -1) meteors[idx].reset();
    nextMeteorIn = 60 + Math.random() * 120;
  }

  meteors.forEach(m => { m.step(); m.draw(); });
  requestAnimationFrame(loop);
}
requestAnimationFrame(loop);

/* ══════════════════════════════════════
   SCROLL REVEAL
══════════════════════════════════════ */
const obs = new IntersectionObserver(entries => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); }});
}, { threshold: 0.08 });
document.querySelectorAll('.section').forEach(s => obs.observe(s));

/* ══════════════════════════════════════
   TYPEWRITER
══════════════════════════════════════ */
const roles = ['Front-end Developer','React Native Builder','Hackathon Enthusiast','UI/UX Craftsman','Cyber Forensics Explorer'];
let ri=0, ci=0, del=false;
const el = document.getElementById('typed');
function type() {
  const cur = roles[ri];
  if (!del) { el.textContent = cur.slice(0, ++ci); if (ci === cur.length) { del = true; setTimeout(type, 1900); return; } }
  else { el.textContent = cur.slice(0, --ci); if (ci === 0) { del = false; ri = (ri+1) % roles.length; } }
  setTimeout(type, del ? 40 : 76);
}
type();

/* ══════════════════════════════════════
   LIVE GITHUB STATS via API
══════════════════════════════════════ */
async function fetchGitHubStats() {
  try {
    const user = await fetch('https://api.github.com/users/RiteshGangurde').then(r => r.json());
    const repos = await fetch('https://api.github.com/users/RiteshGangurde/repos?per_page=100').then(r => r.json());
    const stars = Array.isArray(repos) ? repos.reduce((s, r) => s + (r.stargazers_count || 0), 0) : 0;

    const animate = (el, target) => {
      let cur = 0;
      const step = Math.max(1, Math.ceil(target / 40));
      const t = setInterval(() => {
        cur = Math.min(cur + step, target);
        el.textContent = cur.toLocaleString();
        if (cur >= target) clearInterval(t);
      }, 35);
    };

    animate(document.getElementById('cnt-repos'),     user.public_repos || 0);
    animate(document.getElementById('cnt-followers'), user.followers || 0);
    animate(document.getElementById('cnt-following'), user.following || 0);
    animate(document.getElementById('cnt-stars'),     stars);
  } catch(e) {
    ['cnt-repos','cnt-followers','cnt-following','cnt-stars'].forEach(id => {
      document.getElementById(id).textContent = '—';
    });
  }
}
fetchGitHubStats();
</script>
</body>
</html>
