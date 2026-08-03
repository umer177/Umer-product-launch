# Umer-product-
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>StudySpark — Study Smarter, Not Harder.</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,600;9..144,700&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#fbf9f5;
    --surface:#ffffff;
    --ink:#1c1a2e;
    --ink-soft:#5c5878;
    --border:#e7e3f3;
    --primary:#4b3aa4;
    --primary-dark:#332468;
    --primary-soft:#efeafb;
    --accent:#ffb703;
    --accent-ink:#3a2a00;
    --radius:14px;
  }

  *{ box-sizing:border-box; }
  html{ scroll-behavior:smooth; }
  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ animation-duration:0.001ms !important; transition-duration:0.001ms !important; }
  }

  body{
    margin:0;
    background:var(--bg);
    color:var(--ink);
    font-family:"Inter", system-ui, sans-serif;
    line-height:1.65;
  }

  img{ max-width:100%; display:block; }

  a{ color:inherit; }
  a:focus-visible,
  button:focus-visible{
    outline:3px solid var(--primary);
    outline-offset:3px;
  }

  .skip-link{
    position:absolute;
    left:-999px;
    background:var(--ink);
    color:#fff;
    padding:0.75rem 1.25rem;
    border-radius:6px;
    z-index:100;
  }
  .skip-link:focus{ left:1rem; top:1rem; }

  .shell{
    max-width:1080px;
    margin:0 auto;
    padding:0 1.5rem;
  }

  h1, h2, h3{
    font-family:"Fraunces", Georgia, serif;
    font-weight:700;
    margin:0;
  }

  .eyebrow{
    display:inline-block;
    font-size:0.78rem;
    font-weight:700;
    letter-spacing:0.09em;
    text-transform:uppercase;
    color:var(--primary);
    background:var(--primary-soft);
    border-radius:999px;
    padding:0.35rem 0.9rem;
    margin-bottom:1rem;
  }

  /* ---------- TOP BAR ---------- */
  header.topbar{
    background:var(--bg);
    border-bottom:1px solid var(--border);
    position:sticky;
    top:0;
    z-index:10;
  }
  .topbar-inner{
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:1.1rem 0;
  }
  .brand{
    display:flex;
    align-items:center;
    gap:0.5rem;
    font-family:"Fraunces", Georgia, serif;
    font-weight:700;
    font-size:1.25rem;
  }
  .brand-mark{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    width:34px;
    height:34px;
    border-radius:9px;
    background:var(--primary);
    color:#fff;
    font-size:1.1rem;
  }
  header.topbar nav ul{
    list-style:none;
    display:flex;
    gap:1.75rem;
    margin:0;
    padding:0;
    font-size:0.92rem;
    font-weight:500;
  }
  header.topbar nav a{
    text-decoration:none;
    color:var(--ink-soft);
  }
  header.topbar nav a:hover{ color:var(--primary); }

  @media (max-width:640px){
    header.topbar nav{ display:none; }
  }

  /* ---------- BUTTONS ---------- */
  .btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:0.5rem;
    font-weight:600;
    font-size:0.98rem;
    padding:0.85rem 1.6rem;
    border-radius:999px;
    text-decoration:none;
    border:2px solid transparent;
    cursor:pointer;
    transition:transform 0.15s ease, box-shadow 0.15s ease;
  }
  .btn:hover{ transform:translateY(-2px); }
  .btn-primary{
    background:var(--accent);
    color:var(--accent-ink);
    box-shadow:0 8px 20px rgba(255,183,3,0.35);
  }
  .btn-ghost{
    background:transparent;
    color:var(--surface);
    border-color:rgba(255,255,255,0.55);
  }
  .btn-ghost:hover{ border-color:#fff; }

  /* ---------- HERO ---------- */
  .hero{
    background:radial-gradient(circle at 12% 18%, rgba(255,183,3,0.35), transparent 40%),
               linear-gradient(160deg, var(--primary) 0%, var(--primary-dark) 100%);
    color:#fff;
    padding:5rem 0 6rem;
    background-image:
      radial-gradient(rgba(255,255,255,0.14) 1.5px, transparent 1.5px),
      radial-gradient(circle at 12% 18%, rgba(255,183,3,0.35), transparent 40%),
      linear-gradient(160deg, var(--primary) 0%, var(--primary-dark) 100%);
    background-size: 22px 22px, auto, auto;
  }
  .hero-inner{
    max-width:640px;
  }
  .hero .eyebrow{
    background:rgba(255,255,255,0.14);
    color:#fff;
  }
  .hero h1{
    font-size:clamp(2.4rem, 6vw, 3.4rem);
    line-height:1.08;
    margin-bottom:1rem;
  }
  .hero .tagline{
    font-size:1.2rem;
    color:rgba(255,255,255,0.86);
    max-width:46ch;
    margin:0 0 2rem;
  }
  .hero-actions{
    display:flex;
    flex-wrap:wrap;
    gap:1rem;
  }

  /* ---------- SECTIONS ---------- */
  section{ padding:4.5rem 0; }

  .section-head{
    max-width:56ch;
    margin:0 0 2.5rem;
  }
  .section-head h2{
    font-size:1.9rem;
    margin-bottom:0.75rem;
  }
  .section-head p{
    color:var(--ink-soft);
    margin:0;
  }

  /* ---------- PROBLEM ---------- */
  .problem-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:1.5rem;
  }
  .problem-card{
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:var(--radius);
    padding:1.75rem;
  }
  .problem-card .glyph{
    font-size:1.6rem;
    margin-bottom:0.9rem;
  }
  .problem-card h3{
    font-size:1.1rem;
    margin-bottom:0.5rem;
  }
  .problem-card p{
    color:var(--ink-soft);
    margin:0;
    font-size:0.95rem;
  }

  @media (max-width:800px){
    .problem-grid{ grid-template-columns:1fr; }
  }

  /* ---------- FEATURES ---------- */
  .features{ background:var(--primary-soft); }
  .feature-grid{
    display:grid;
    grid-template-columns:repeat(3, 1fr);
    gap:1.5rem;
  }
  .feature-card{
    background:var(--surface);
    border-radius:var(--radius);
    padding:2rem 1.75rem;
    box-shadow:0 1px 2px rgba(28,26,46,0.04), 0 12px 28px rgba(28,26,46,0.06);
    transition:transform 0.2s ease, box-shadow 0.2s ease;
  }
  .feature-card:hover{
    transform:translateY(-4px);
    box-shadow:0 16px 32px rgba(28,26,46,0.1);
  }
  .feature-icon{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    width:48px;
    height:48px;
    border-radius:12px;
    background:var(--primary);
    color:#fff;
    font-size:1.35rem;
    margin-bottom:1.1rem;
  }
  .feature-card h3{
    font-size:1.15rem;
    margin-bottom:0.5rem;
  }
  .feature-card p{
    color:var(--ink-soft);
    margin:0;
    font-size:0.95rem;
  }

  @media (max-width:800px){
    .feature-grid{ grid-template-columns:1fr; }
  }

  /* ---------- SHOWCASE / IMAGE ---------- */
  .showcase-inner{
    display:grid;
    grid-template-columns:1.1fr 0.9fr;
    gap:3rem;
    align-items:center;
  }
  .mockup-frame{
    background:linear-gradient(160deg, var(--primary-soft), var(--surface));
    border:1px dashed var(--primary);
    border-radius:var(--radius);
    padding:1rem;
  }
  .mockup-frame img{
    width:100%;
    height:auto;
    min-height:260px;
    object-fit:cover;
    border-radius:calc(var(--radius) - 6px);
    background:var(--surface);
  }
  .mockup-caption{
    margin:0.75rem 0 0;
    font-size:0.85rem;
    color:var(--ink-soft);
    text-align:center;
  }
  .tag-list{
    list-style:none;
    display:flex;
    flex-wrap:wrap;
    gap:0.65rem;
    margin:0;
    padding:0;
  }
  .tag-list li{
    background:var(--surface);
    border:1px solid var(--border);
    border-radius:999px;
    padding:0.5rem 1rem;
    font-size:0.9rem;
    font-weight:500;
  }

  @media (max-width:800px){
    .showcase-inner{ grid-template-columns:1fr; }
  }

  /* ---------- WHO IT'S FOR ---------- */
  .audience{
    background:var(--primary-dark);
    color:#fff;
  }
  .audience .section-head p{
    color:rgba(255,255,255,0.82);
  }
  .audience .eyebrow{
    background:rgba(255,255,255,0.14);
    color:#fff;
  }
  .audience-pills{
    display:flex;
    flex-wrap:wrap;
    gap:0.75rem;
    margin-top:1.75rem;
  }
  .audience-pills li{
    list-style:none;
    border:1px solid rgba(255,255,255,0.35);
    border-radius:999px;
    padding:0.5rem 1.1rem;
    font-size:0.9rem;
  }

  /* ---------- CTA STRIP ---------- */
  .cta-strip{
    text-align:center;
    padding:4rem 0;
  }
  .cta-strip h2{
    font-size:1.8rem;
    margin-bottom:1rem;
  }
  .cta-strip p{
    color:var(--ink-soft);
    max-width:48ch;
    margin:0 auto 1.75rem;
  }

  /* ---------- FOOTER ---------- */
  footer.site-footer{
    background:var(--ink);
    color:rgba(255,255,255,0.75);
    padding:2.5rem 0;
    font-size:0.9rem;
  }
  .footer-inner{
    display:flex;
    flex-wrap:wrap;
    justify-content:space-between;
    align-items:center;
    gap:1rem;
  }
  footer.site-footer a{
    color:rgba(255,255,255,0.75);
    text-decoration:none;
  }
  footer.site-footer a:hover{ color:#fff; }
  .footer-links{
    list-style:none;
    display:flex;
    gap:1.5rem;
    margin:0;
    padding:0;
  }

  @media (max-width:600px){
    section{ padding:3.25rem 0; }
    .footer-inner{ flex-direction:column; align-items:flex-start; }
  }
</style>
</head>
<body>

<a class="skip-link" href="#main">Skip to main content</a>

<header class="topbar">
  <div class="shell topbar-inner">
    <a class="brand" href="#top" aria-label="StudySpark home">
      <span class="brand-mark" aria-hidden="true">⚡</span>
      StudySpark
    </a>
    <nav aria-label="Primary">
      <ul>
        <li><a href="#problem">Problem</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#showcase">Preview</a></li>
        <li><a href="#audience">Who it's for</a></li>
      </ul>
    </nav>
  </div>
</header>

<main id="main">

  <section class="hero" id="top">
    <div class="shell hero-inner">
      <p class="eyebrow">Now in early access</p>
      <h1>StudySpark</h1>
      <p class="tagline">Study Smarter, Not Harder.</p>
      <div class="hero-actions">
        <a class="btn btn-primary" href="#showcase">Get Demo</a>
        <a class="btn btn-ghost" href="#audience">Pre-order</a>
      </div>
    </div>
  </section>

  <section id="problem">
    <div class="shell">
      <div class="section-head">
        <p class="eyebrow">The Problem</p>
        <h2>Studying shouldn't feel this scattered</h2>
        <p>Most students aren't short on effort — they're short on a system that keeps up with them.</p>
      </div>
      <div class="problem-grid">
        <div class="problem-card">
          <div class="glyph" aria-hidden="true">🗓️</div>
          <h3>Forgotten tasks</h3>
          <p>Assignments and deadlines get lost across group chats, notebooks, and sticky notes.</p>
        </div>
        <div class="problem-card">
          <div class="glyph" aria-hidden="true">🗂️</div>
          <h3>Disorganized notes</h3>
          <p>Notes end up scattered across apps and papers, making revision harder than it needs to be.</p>
        </div>
        <div class="problem-card">
          <div class="glyph" aria-hidden="true">🌀</div>
          <h3>Lost focus</h3>
          <p>Without a clear plan, study sessions drift and momentum disappears before real progress is made.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="features" class="features">
    <div class="shell">
      <div class="section-head">
        <p class="eyebrow">Features</p>
        <h2>Everything your study routine was missing</h2>
        <p>StudySpark brings planning, memory, and momentum into one place.</p>
      </div>
      <div class="feature-grid">
        <div class="feature-card">
          <div class="feature-icon" aria-hidden="true">🤖</div>
          <h3>AI Study Planner</h3>
          <p>Get a personalized study schedule that adapts to your workload, deadlines, and energy levels.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon" aria-hidden="true">📝</div>
          <h3>Smart Flashcards</h3>
          <p>Turn your notes into flashcards automatically, then review them with spaced repetition that sticks.</p>
        </div>
        <div class="feature-card">
          <div class="feature-icon" aria-hidden="true">⏰</div>
          <h3>Homework Reminders</h3>
          <p>Never miss a deadline again with smart reminders that nudge you before it's too late, not after.</p>
        </div>
      </div>
    </div>
  </section>

  <section id="showcase">
    <div class="shell showcase-inner">
      <figure class="mockup-frame">
        <img src="image/Photo.png" alt="Placeholder for the StudySpark logo or app mockup — replace with your product screenshot.">
        <figcaption class="mockup-caption">Insert your StudySpark logo or app mockup here.</figcaption>
      </figure>
      <div>
        <p class="eyebrow">At a glance</p>
        <h2>One app, built around how you actually study</h2>
        <p style="color:var(--ink-soft); margin:0.75rem 0 1.75rem;">A quick look at what's inside StudySpark.</p>
        <ul class="tag-list">
          <li>🤖 AI-Powered</li>
          <li>📚 Study Planner</li>
          <li>📝 Smart Notes</li>
          <li>⚡ Flashcards</li>
          <li>📊 Progress Tracker</li>
          <li>🎯 Focus Mode</li>
        </ul>
      </div>
    </div>
  </section>

  <section id="audience" class="audience">
    <div class="shell">
      <div class="section-head">
        <p class="eyebrow">Who it's for</p>
        <h2>Built for students at every level</h2>
        <p>StudySpark is designed for O-Level, A-Level, high school, college, and university students who want to stay organized, manage their study time, and improve their academic performance with AI-powered learning tools.</p>
      </div>
      <ul class="audience-pills">
        <li>O-Level</li>
        <li>A-Level</li>
        <li>High School</li>
        <li>College</li>
        <li>University</li>
      </ul>
    </div>
  </section>

  <section class="cta-strip">
    <div class="shell">
      <h2>Ready to study smarter?</h2>
      <p>Join early access and be the first to try StudySpark when it launches.</p>
      <a class="btn btn-primary" href="#top">Pre-order StudySpark</a>
    </div>
  </section>

</main>

<footer class="site-footer">
  <div class="shell footer-inner">
    <span>© 2026 StudySpark. All rights reserved.</span>
    <ul class="footer-links">
      <li><a href="#problem">Problem</a></li>
      <li><a href="#features">Features</a></li>
      <li><a href="#audience">Who it's for</a></li>
    </ul>
  </div>
</footer>

</body>
</html>