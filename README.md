<!DOCTYPE html><html lang="en"><head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rakib Hasan | Cyber Developer Portfolio</title>
  <style>
    :root {
      --bg-main: #020617;
      --bg-card: rgba(15, 23, 42, 0.9);
      --accent-neon: #22f7ff;
      --accent-neon-2: #ff00ff;
      --accent-gold: #ffd700;
      --text-main: #e5e7eb;
      --text-muted: #9ca3af;
      --border-glow: 0 0 20px rgba(34, 247, 255, 0.5);
      --radius-xl: 18px;
    }* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  scroll-behavior: smooth;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
}

body {
  background: radial-gradient(circle at top, #0f172a 0, #020617 45%, #000 100%);
  color: var(--text-main);
  min-height: 100vh;
}

/* Neon background orbs */
.bg-orb {
  position: fixed;
  border-radius: 999px;
  filter: blur(80px);
  opacity: 0.35;
  z-index: -1;
}

.bg-orb.orb-1 {
  width: 320px;
  height: 320px;
  background: #22f7ff;
  top: -40px;
  left: -40px;
}

.bg-orb.orb-2 {
  width: 380px;
  height: 380px;
  background: #ff00ff;
  bottom: -60px;
  right: -40px;
}

header {
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(16px);
  background: linear-gradient(to right, rgba(15, 23, 42, 0.9), rgba(15, 23, 42, 0.4));
  border-bottom: 1px solid rgba(148, 163, 184, 0.2);
}

.nav-container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 0.8rem 1.25rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
}

.brand {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.brand-logo {
  width: 34px;
  height: 34px;
  border-radius: 999px;
  border: 2px solid var(--accent-neon);
  box-shadow: var(--border-glow);
  overflow: hidden;
}

.brand-logo img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.brand-text {
  display: flex;
  flex-direction: column;
  line-height: 1.1;
}

.brand-text span:first-child {
  font-size: 0.85rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--accent-neon);
}

.brand-text span:last-child {
  font-size: 1rem;
  font-weight: 700;
}

nav ul {
  list-style: none;
  display: flex;
  gap: 1.2rem;
  font-size: 0.9rem;
}

nav a {
  color: var(--text-muted);
  text-decoration: none;
  position: relative;
  padding-bottom: 2px;
}

nav a::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: 0;
  width: 0;
  height: 2px;
  background: linear-gradient(90deg, var(--accent-neon), var(--accent-neon-2));
  transition: width 0.2s ease-out;
}

nav a:hover {
  color: var(--text-main);
}

nav a:hover::after {
  width: 100%;
}

.btn-primary {
  padding: 0.5rem 1rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.6);
  background: radial-gradient(circle at top left, rgba(34, 247, 255, 0.25), rgba(15, 23, 42, 0.95));
  color: var(--text-main);
  font-size: 0.85rem;
  cursor: pointer;
  transition: all 0.15s ease-out;
  box-shadow: 0 0 0 rgba(34, 247, 255, 0.3);
}

.btn-primary:hover {
  transform: translateY(-1px);
  box-shadow: 0 0 18px rgba(34, 247, 255, 0.5);
  border-color: var(--accent-neon);
}

main {
  max-width: 1100px;
  margin: 0 auto;
  padding: 1.8rem 1.25rem 3rem;
}

/* HERO */
.hero {
  display: grid;
  grid-template-columns: minmax(0, 1.4fr) minmax(0, 1.1fr);
  gap: 2rem;
  align-items: center;
  padding: 1.8rem 1.2rem;
  margin-top: 0.5rem;
  border-radius: 24px;
  background: linear-gradient(135deg, rgba(15, 23, 42, 0.98), rgba(30, 64, 175, 0.95));
  box-shadow: 0 25px 60px rgba(15, 23, 42, 0.8);
  border: 1px solid rgba(148, 163, 184, 0.35);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: "CYBER";
  position: absolute;
  right: -10px;
  bottom: -40px;
  font-size: 5rem;
  font-weight: 800;
  letter-spacing: 0.2em;
  color: rgba(15, 23, 42, 0.7);
}

.hero-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  padding: 0.25rem 0.7rem;
  border-radius: 999px;
  border: 1px solid rgba(56, 189, 248, 0.7);
  background: rgba(15, 23, 42, 0.7);
  font-size: 0.75rem;
  color: var(--accent-neon);
  margin-bottom: 0.8rem;
}

.hero-badge span {
  font-size: 0.8rem;
  color: var(--text-muted);
}

.hero-title {
  font-size: clamp(2.2rem, 4vw, 2.7rem);
  line-height: 1.1;
  margin-bottom: 0.5rem;
}

.hero-title span.highlight {
  background: linear-gradient(90deg, var(--accent-neon), var(--accent-gold));
  -webkit-background-clip: text;
  color: transparent;
}

.hero-subtitle {
  font-size: 1rem;
  color: var(--text-muted);
  margin-bottom: 1rem;
  max-width: 480px;
}

.hero-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.5rem;
  margin-bottom: 1.4rem;
}

.hero-tag {
  padding: 0.2rem 0.7rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.5);
  font-size: 0.75rem;
  color: var(--text-muted);
}

.hero-actions {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  align-items: center;
}

.btn-ghost {
  padding: 0.5rem 1rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.6);
  background: transparent;
  color: var(--text-main);
  font-size: 0.85rem;
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 0.4rem;
}

.btn-ghost span {
  font-size: 1rem;
}

.hero-right {
  position: relative;
}

.hero-card {
  border-radius: 20px;
  background: var(--bg-card);
  border: 1px solid rgba(148, 163, 184, 0.4);
  padding: 0.9rem;
  box-shadow: var(--border-glow);
}

.hero-banner {
  border-radius: 16px;
  overflow: hidden;
  margin-bottom: 0.75rem;
  border: 1px solid rgba(148, 163, 184, 0.4);
}

.hero-banner img {
  width: 100%;
  display: block;
}

.hero-meta {
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 0.8rem;
  color: var(--text-muted);
}

.status-dot {
  width: 8px;
  height: 8px;
  border-radius: 999px;
  background: #22c55e;
  box-shadow: 0 0 10px rgba(34, 197, 94, 0.8);
  display: inline-block;
  margin-right: 4px;
}

.floating-chip {
  position: absolute;
  right: 6px;
  top: -10px;
  padding: 0.4rem 0.7rem;
  font-size: 0.7rem;
  border-radius: 999px;
  background: linear-gradient(120deg, rgba(34, 247, 255, 0.95), rgba(59, 130, 246, 0.95));
  color: #020617;
  font-weight: 600;
  box-shadow: 0 15px 30px rgba(37, 99, 235, 0.8);
}

/* Sections */
section {
  margin-top: 3rem;
}

.section-title {
  font-size: 1.3rem;
  margin-bottom: 1.1rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.section-title span.icon {
  font-size: 1.3rem;
}

.section-sub {
  font-size: 0.9rem;
  color: var(--text-muted);
  margin-bottom: 1.4rem;
  max-width: 520px;
}

.grid-2 {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 1.5rem;
}

.card {
  background: var(--bg-card);
  border-radius: var(--radius-xl);
  padding: 1.2rem;
  border: 1px solid rgba(148, 163, 184, 0.3);
}

.card h3 {
  font-size: 1rem;
  margin-bottom: 0.5rem;
}

.card p {
  font-size: 0.85rem;
  color: var(--text-muted);
}

.pill-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin-top: 0.7rem;
}

.pill {
  padding: 0.25rem 0.65rem;
  border-radius: 999px;
  font-size: 0.75rem;
  border: 1px solid rgba(148, 163, 184, 0.45);
  color: var(--text-muted);
}

.skills-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 0.65rem;
  margin-top: 0.7rem;
}

.skill-box {
  padding: 0.55rem 0.65rem;
  border-radius: 12px;
  background: linear-gradient(135deg, rgba(15, 23, 42, 0.95), rgba(30, 64, 175, 0.9));
  border: 1px solid rgba(148, 163, 184, 0.4);
  font-size: 0.8rem;
}

.skill-box span {
  display: block;
  font-size: 0.7rem;
  color: var(--text-muted);
  margin-top: 2px;
}

.project-card {
  background: linear-gradient(135deg, rgba(15, 23, 42, 0.96), rgba(88, 28, 135, 0.98));
  border-radius: var(--radius-xl);
  padding: 1.2rem;
  border: 1px solid rgba(168, 85, 247, 0.8);
  box-shadow: 0 20px 40px rgba(88, 28, 135, 0.7);
}

.project-card h3 {
  font-size: 1rem;
  margin-bottom: 0.3rem;
}

.project-meta {
  font-size: 0.8rem;
  color: var(--text-muted);
  margin-bottom: 0.5rem;
}

.project-link {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  margin-top: 0.6rem;
  font-size: 0.8rem;
  color: var(--accent-neon);
  text-decoration: none;
}

.project-link:hover {
  text-decoration: underline;
}

.contact-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
  gap: 1.5rem;
  align-items: center;
}

.contact-list {
  list-style: none;
  font-size: 0.9rem;
}

.contact-list li {
  margin-bottom: 0.55rem;
  color: var(--text-muted);
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.3rem;
  font-size: 0.75rem;
  padding: 0.2rem 0.55rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.45);
  margin-top: 0.4rem;
}

.social-row {
  display: flex;
  flex-wrap: wrap;
  gap: 0.6rem;
  margin-top: 0.9rem;
}

.social-btn {
  padding: 0.45rem 0.9rem;
  border-radius: 999px;
  font-size: 0.8rem;
  border: 1px solid rgba(148, 163, 184, 0.6);
  text-decoration: none;
  color: var(--text-main);
  background: rgba(15, 23, 42, 0.9);
}

.social-btn span {
  opacity: 0.8;
  font-size: 0.85em;
}

.terminal-card {
  background: #020617;
  border-radius: 14px;
  border: 1px solid rgba(148, 163, 184, 0.6);
  overflow: hidden;
  font-family: "Fira Code", monospace;
  font-size: 0.78rem;
}

.terminal-top {
  display: flex;
  align-items: center;
  gap: 0.3rem;
  padding: 0.4rem 0.6rem;
  background: #020617;
  border-bottom: 1px solid rgba(148, 163, 184, 0.4);
}

.dot {
  width: 8px;
  height: 8px;
  border-radius: 999px;
}

.dot.red {
  background: #f97373;
}

.dot.yellow {
  background: #facc15;
}

.dot.green {
  background: #4ade80;
}

.terminal-body {
  padding: 0.75rem 0.9rem 0.85rem;
}

.terminal-line {
  margin-bottom: 0.25rem;
}

.prompt {
  color: #22f7ff;
}

footer {
  text-align: center;
  font-size: 0.8rem;
  color: var(--text-muted);
  padding: 1.5rem 1rem 2rem;
}

footer span.brand {
  background: linear-gradient(90deg, var(--accent-neon), var(--accent-gold));
  -webkit-background-clip: text;
  color: transparent;
  font-weight: 600;
}

/* Responsive */
@media (max-width: 900px) {
  .hero {
    grid-template-columns: minmax(0, 1fr);
  }

  .hero-right {
    order: -1;
  }

  .hero::before {
    display: none;
  }

  .grid-2,
  .contact-grid {
    grid-template-columns: minmax(0, 1fr);
  }

  nav ul {
    display: none;
  }
}

@media (max-width: 640px) {
  main {
    padding-inline: 1rem;
  }

  .hero {
    padding: 1.3rem 1rem;
  }

  .skills-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

  </style>
</head><body>
  <div class="bg-orb orb-1"></div>
  <div class="bg-orb orb-2"></div>  <header>
    <div class="nav-container">
      <div class="brand">
        <div class="brand-logo">
          <img src="https://i.imgur.com/Q89m3ix.jpeg" alt="Rakib Logo" />
        </div>
        <div class="brand-text">
          <span>CYBER BRAND</span>
          <span>Rakib Hasan</span>
        </div>
      </div><nav>
    <ul>
      <li><a href="#about">About</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <button class="btn-primary" onclick="document.getElementById('contact').scrollIntoView({behavior: 'smooth'})">
    Hire / Collab →
  </button>
</div>

  </header>  <main>
    <!-- HERO -->
    <section class="hero" id="top">
      <div class="hero-left">
        <div class="hero-badge">
          <span>🛡 CYBER • LUXURY • PRO</span>
          <span>BD Developer</span>
        </div>
        <h1 class="hero-title">
          Hi, I'm <span class="highlight">Rakib Hasan</span><br />
          Frontend Developer & Digital Brand Designer
        </h1>
        <p class="hero-subtitle">
          I blend <strong>clean UI</strong>, <strong>neon cyber style</strong> and
          <strong>premium branding</strong> to create experiences that feel alive.
        </p>
        <div class="hero-tags">
          <span class="hero-tag">🚀 Frontend Developer</span>
          <span class="hero-tag">🧠 AI • Creative Mind</span>
          <span class="hero-tag">🛡 Cyber Bot Enthusiast</span>
          <span class="hero-tag">👑 Personal Brand Builder</span>
        </div>
        <div class="hero-actions">
          <button class="btn-primary" onclick="document.getElementById('projects').scrollIntoView({behavior: 'smooth'})">
            View Featured Project
          </button>
          <button class="btn-ghost" onclick="document.getElementById('about').scrollIntoView({behavior: 'smooth'})">
            <span>↓</span> More About Me
          </button>
        </div>
      </div><div class="hero-right">
    <div class="floating-chip">LIVE • NEON MODE</div>
    <div class="hero-card">
      <div class="hero-banner">
        <img src="https://i.imgur.com/Q89m3ix.jpeg" alt="Rakib Banner" />
      </div>
      <div class="hero-meta">
        <div>
          <span class="status-dot"></span> Available for collab
        </div>
        <div>From 🇧🇩 Bangladesh</div>
      </div>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <h2 class="section-title"><span class="icon">🧬</span> Digital Identity</h2>
  <p class="section-sub">
    I'm <strong>☆ NUR RAKIB ☆ HAFIZ</strong>, a Bangladeshi developer who
    believes code is not just logic – it's a way to express personality.
    I love mixing hacker vibes, luxury style and minimal pro design.
  </p>

  <div class="grid-2">
    <div class="card">
      <h3>Who am I?</h3>
      <p>
        • Frontend developer focused on <strong>modern UI</strong> &
        <strong>smooth UX</strong>.<br />
        • Passionate about <strong>cyber-themed interfaces</strong> and
        <strong>animated profiles</strong>.<br />
        • Always experimenting with new visual ideas and concepts.
      </p>
      <div class="pill-row">
        <span class="pill">Name: ☆ NUR RAKIB ☆ HAFIZ</span>
        <span class="pill">Religion: ISLAM</span>
        <span class="pill">Status: Complicated ❤️</span>
        <span class="pill">Education: STUDY</span>
      </div>
    </div>

    <div class="card">
      <h3>Mindset & Vision</h3>
      <p>
        I want to build a strong <strong>personal brand</strong> as a
        developer from Bangladesh, and create designs that feel
        <strong>global, premium and unique</strong>.
      </p>
      <div class="pill-row">
        <span class="pill">Never stop learning</span>
        <span class="pill">Quality over shortcuts</span>
        <span class="pill">Design + Code = Power</span>
      </div>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills">
  <h2 class="section-title"><span class="icon">💡</span> Skills & Tech Stack</h2>
  <p class="section-sub">
    Tools and technologies I use to craft neon, cyber and professional
    experiences on the web.
  </p>

  <div class="grid-2">
    <div class="card">
      <h3>Core Frontend</h3>
      <div class="skills-grid">
        <div class="skill-box">HTML5 <span>Semantic, SEO friendly</span></div>
        <div class="skill-box">CSS3 <span>Flex, Grid, Animation</span></div>
        <div class="skill-box">JavaScript <span>Interactive UI</span></div>
        <div class="skill-box">React (basic) <span>Modern SPA</span></div>
        <div class="skill-box">Tailwind CSS <span>Fast styling</span></div>
        <div class="skill-box">Bootstrap <span>Quick layouts</span></div>
      </div>
    </div>

    <div class="card">
      <h3>Tools & Focus</h3>
      <div class="skills-grid">
        <div class="skill-box">Git & GitHub <span>Code control</span></div>
        <div class="skill-box">VS Code <span>Main editor</span></div>
        <div class="skill-box">Figma (basic) <span>UI mockups</span></div>
        <div class="skill-box">Design Sense <span>Colors & layout</span></div>
        <div class="skill-box">Branding <span>Profile identity</span></div>
        <div class="skill-box">Cyber Style UI <span>Neon / Hacker vibe</span></div>
      </div>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="projects">
  <h2 class="section-title"><span class="icon">🚀</span> Featured Project</h2>
  <p class="section-sub">
    A highlight from my work that represents my cyber style and creative
    developer identity.
  </p>

  <div class="project-card">
    <h3>🤖 CYBER-BOT-RAKIB</h3>
    <p class="project-meta">
      A bot project with strong cyber feel, combining automation and
      personality.
    </p>
    <p>
      Focused on <strong>branding</strong>, <strong>visual identity</strong>
      and a cool hacker vibe. Built to look different from typical boring
      repos.
    </p>
    <div class="pill-row">
      <span class="pill">Bot / Automation</span>
      <span class="pill">Cyber Theme</span>
      <span class="pill">Unique README Design</span>
    </div>
    <a class="project-link" href="https://github.com/bdrakib123/cyber-bot-rakib" target="_blank" rel="noreferrer">
      → View CYBER-BOT-RAKIB on GitHub
    </a>
  </div>
</section>

<!-- CONTACT -->
<section id="contact">
  <h2 class="section-title"><span class="icon">📡</span> Contact & Social</h2>
  <p class="section-sub">
    Want to collab, design your GitHub profile, or build something cool?
    You can find me here:
  </p>

  <div class="contact-grid">
    <div>
      <ul class="contact-list">
        <li>📍 From: <strong>Bangladesh</strong></li>
        <li>🧑‍💻 Role: <strong>Frontend Developer</strong></li>
        <li>🛡 Brand: <strong>CYBER RAKIB</strong></li>
      </ul>
      <div class="badge">✨ Open for creative collaborations</div>
      <div class="social-row">
        <a class="social-btn" href="https://github.com/bdrakib123" target="_blank" rel="noreferrer">
          GitHub <span>@bdrakib123</span>
        </a>
        <a class="social-btn" href="https://www.facebook.com/hoon420" target="_blank" rel="noreferrer">
          Facebook <span>/hoon420</span>
        </a>
        <a class="social-btn" href="https://www.instagram.com/hoon420" target="_blank" rel="noreferrer">
          Instagram <span>@hoon420</span>
        </a>
      </div>
    </div>

    <div class="terminal-card">
      <div class="terminal-top">
        <div class="dot red"></div>
        <div class="dot yellow"></div>
        <div class="dot green"></div>
      </div>
      <div class="terminal-body">
        <div class="terminal-line"><span class="prompt">rakib@portfolio</span>:~$ brand status</div>
        <div class="terminal-line">▶ Name : RAKIB HASAN (☆ NUR RAKIB ☆)</div>
        <div class="terminal-line">▶ Mode : SUPER PREMIUM DEVELOPER PROFILE</div>
        <div class="terminal-line">▶ Style: NEON • HACKER • LUXURY • PRO</div>
        <div class="terminal-line">▶ Mission: Build a global digital identity</div>
      </div>
    </div>
  </div>
</section>

  </main>  <footer>
    <p>
      Designed with passion by <span class="brand">CYBER RAKIB</span> • Keep building, keep glowing.
    </p>
  </footer>
</body></html>
