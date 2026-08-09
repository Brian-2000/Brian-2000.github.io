<!--
  NOTE FOR BRIAN — READ BEFORE YOU EMBED THIS IN README.md:
  GitHub strips <style> and <script> tags out of README.md files for security reasons.
  That's the real cause of the "squeezed margins" you're seeing — none of this CSS is
  actually being applied on github.com, so the browser falls back to plain, unstyled
  HTML inside GitHub's narrow markdown-body column.
  Best fix: host this file for free on GitHub Pages (or Vercel/Netlify), then in your
  README.md just link/embed it, e.g.:
    ### 🌐 [View my full portfolio →](https://your-username.github.io/portfolio/)
  That keeps every animation, gradient and the SVG illustration below intact.
-->
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Brian Muchere — Full-Stack Engineer · Systems Integration · Nairobi</title>
<meta name="description" content="Brian Muchere is a full-stack engineer building pension, HR, procurement and ERP systems for enterprise clients. Available for freelance and contract work.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=Inter:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap" rel="stylesheet">
<style>
:root{
  --paper:#0c1a2b;
  --paper-alt:#122542;
  --panel:#152a49;
  --line:#24405f;
  --line-bright:#3fa9e8;
  --amber:#e8a33f;
  --ink:#eef4fb;
  --ink-soft:#93a8c4;
  --radius:0px;
  --mono:'IBM Plex Mono',monospace;
  --display:'Space Grotesk',sans-serif;
  --body:'Inter',sans-serif;
  /* fluid spacing tokens — this is what keeps margins sane on every screen,
     including narrow embeds like a GitHub README column */
  /* --gutter:clamp(16px, 5vw, 24px);
  --section-y:clamp(48px, 9vw, 96px); */
}
*{margin:0;padding:0;box-sizing:border-box;}
html{scroll-behavior:smooth;}
body{
  background:
    linear-gradient(var(--paper),var(--paper)) fixed,
    repeating-linear-gradient(0deg, rgba(63,169,232,0.045) 0px, rgba(63,169,232,0.045) 1px, transparent 1px, transparent 48px),
    repeating-linear-gradient(90deg, rgba(63,169,232,0.045) 0px, rgba(63,169,232,0.045) 1px, transparent 1px, transparent 48px),
    var(--paper);
  color:var(--ink);
  font-family:var(--body);
  line-height:1.6;
  -webkit-font-smoothing:antialiased;
  overflow-x:hidden; /* guards against any stray element causing horizontal scroll on mobile */
}
a{color:inherit;}
img,svg{max-width:100%;display:block;}
.wrap{max-width:1180px;margin:0 auto;padding:0 var(--gutter);}
.eyebrow{
  font-family:var(--mono);
  font-size:0.72rem;
  letter-spacing:0.16em;
  text-transform:uppercase;
  color:var(--line-bright);
  display:flex;align-items:center;gap:10px;
  margin-bottom:14px;
}
.eyebrow::before{content:"";width:22px;height:1px;background:var(--line-bright);display:inline-block;}
h1,h2,h3,h4{font-family:var(--display);font-weight:600;color:var(--ink);letter-spacing:-0.01em;}
h2.section-title{font-size:clamp(1.5rem,3vw,2.3rem);margin-bottom:10px;}
.section-sub{color:var(--ink-soft);max-width:640px;font-size:1rem;margin-bottom:clamp(28px,5vw,44px);}
section{padding:var(--section-y) 0;position:relative;border-top:1px solid var(--line);}
section:first-of-type{border-top:none;}

/* ---------- Title block (signature component) ---------- */
.title-block{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(130px,1fr));
  border:1px solid var(--line);
  border-radius:10px;
  overflow:hidden;
  font-family:var(--mono);
  font-size:0.72rem;
  background:rgba(18,37,66,0.6);
}
.title-block > div{
  padding:12px 16px;
  border-left:1px solid var(--line);
  border-top:1px solid var(--line);
}
.title-block > div:first-child,
.title-block > div:nth-child(-n+2){border-top:none;}
.title-block dt{color:var(--ink-soft);text-transform:uppercase;letter-spacing:0.08em;font-size:0.65rem;margin-bottom:4px;}
.title-block dd{color:var(--ink);font-weight:500;word-break:break-word;}

/* ---------- Nav ---------- */
.nav{
  position:sticky;top:0;z-index:100;
  background:rgba(12,26,43,0.9);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--line);
}
.nav-inner{
  max-width:1180px;margin:0 auto;padding:14px var(--gutter);
  display:flex;align-items:center;justify-content:space-between;
  gap:12px;
}
.nav-brand{font-family:var(--mono);font-size:0.82rem;letter-spacing:0.05em;display:flex;align-items:center;gap:8px;white-space:nowrap;}
.nav-brand .dot{width:8px;height:8px;border-radius:50%;background:var(--amber);box-shadow:0 0 0 3px rgba(232,163,63,0.18);flex-shrink:0;}
.nav-links{display:flex;gap:24px;list-style:none;font-family:var(--mono);font-size:0.75rem;letter-spacing:0.04em;text-transform:uppercase;flex-wrap:wrap;}
.nav-links a{text-decoration:none;color:var(--ink-soft);transition:color .2s;padding:4px 0;border-bottom:1px solid transparent;}
.nav-links a:hover, .nav-links a.active{color:var(--line-bright);border-color:var(--line-bright);}
.nav-cta{
  font-family:var(--mono);font-size:0.75rem;text-transform:uppercase;letter-spacing:0.04em;
  border:1px solid var(--amber);color:var(--amber);padding:8px 16px;border-radius:30px;text-decoration:none;
  transition:.2s;white-space:nowrap;flex-shrink:0;
}
.nav-cta:hover{background:var(--amber);color:var(--paper);}
.nav-toggle{display:none;background:none;border:1px solid var(--line);color:var(--ink);border-radius:8px;padding:8px 10px;font-size:1rem;line-height:1;cursor:pointer;}

/* ---------- Hero ---------- */
.hero{padding:clamp(40px,8vw,72px) 0 clamp(36px,6vw,60px);border-top:none;}
.hero-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:clamp(28px,5vw,48px);align-items:center;}
.hero h1{font-size:clamp(1.5rem,4vw,2.1rem);line-height:1.15;margin-bottom:18px;}
.hero h1 span{color:var(--line-bright);}
.hero p.lead{font-size:clamp(0.95rem,2vw,1.12rem);color:var(--ink-soft);max-width:520px;margin-bottom:28px;}
.btn-row{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:clamp(28px,5vw,44px);}
.btn{
  font-family:var(--mono);font-size:0.8rem;text-transform:uppercase;letter-spacing:0.05em;
  padding:13px 24px;border-radius:30px;text-decoration:none;transition:.2s;display:inline-flex;align-items:center;gap:8px;
}
.btn-primary{background:var(--line-bright);color:#06101c;font-weight:600;}
.btn-primary:hover{background:#63bcf0;}
.btn-ghost{border:1px solid var(--line);color:var(--ink);}
.btn-ghost:hover{border-color:var(--line-bright);color:var(--line-bright);}

/* hero services wheel — a self-contained inline SVG (no external image file,
   no extra folder, nothing to host). Six services orbit a central hub, each
   with its own hand-drawn icon. Numbering 01–06 mirrors the same order used
   in the Services section below, so it's a real index, not decoration. */
.hero-art{position:relative;width:100%;max-width:440px;margin:0 auto;}
.hero-wheel svg{width:100%;height:auto;}
.wheel-orbit{
  transform-box:fill-box;transform-origin:center;
  animation:orbitSpin 90s linear infinite;
}
@keyframes orbitSpin{to{transform:rotate(360deg);}}
.illus-caption{
  font-family:var(--mono);font-size:0.66rem;text-transform:uppercase;letter-spacing:0.1em;
  color:var(--ink-soft);text-align:center;margin-top:14px;
}

@media (prefers-reduced-motion: reduce){
  .wheel-orbit{animation:none;}
  *{scroll-behavior:auto !important;}
}

/* ---------- About stats ---------- */
.about-grid{
  display:grid;
  grid-template-columns:1.2fr 0.8fr;
  gap:clamp(28px,5vw,56px);
  align-items:start;
}
.about-grid p{color:var(--ink-soft);margin-bottom:16px;max-width:600px;}
.stat-list{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.stat-card{border:1px solid var(--line);border-radius:var(--radius);padding:20px;background:rgba(18,37,66,0.4);}
.stat-card .num{font-family:var(--display);font-size:1.8rem;color:var(--line-bright);}
.stat-card .lbl{font-family:var(--mono);font-size:0.7rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--ink-soft);margin-top:4px;}

/* ---------- Services ---------- */
.svc-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(340px,1fr));gap:20px;}
.svc-card{border:1px solid var(--line);border-radius:var(--radius);padding:24px;background:rgba(18,37,66,0.35);transition:.2s;}
.svc-card:hover{border-color:var(--line-bright);transform:translateY(-3px);}
.svc-card .idx{font-family:var(--mono);color:var(--amber);font-size:0.75rem;margin-bottom:10px;}
.svc-card h3{font-size:1.05rem;margin-bottom:10px;}
.svc-card ul{list-style:none;color:var(--ink-soft);font-size:0.88rem;}
.svc-card li{padding-left:16px;position:relative;margin-bottom:6px;}
.svc-card li::before{content:"—";position:absolute;left:0;color:var(--line);}

/* ---------- Skills ---------- */
.skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px;}
.skill-card{border:1px solid var(--line);border-radius:var(--radius);padding:20px;background:rgba(18,37,66,0.3);}
.skill-card h4{font-size:0.95rem;margin-bottom:12px;display:flex;align-items:center;gap:8px;color:var(--ink);}
.skill-card h4 .sw{width:6px;height:6px;background:var(--line-bright);border-radius:1px;transform:rotate(45deg);display:inline-block;flex-shrink:0;}
.tagset{display:flex;flex-wrap:wrap;gap:6px;}
.tag{
  font-family:var(--mono);font-size:0.7rem;color:var(--ink-soft);
  border:1px solid var(--line);padding:4px 10px;border-radius:20px;
}

/* ---------- Experience timeline ---------- */
.timeline{position:relative;padding-left:28px;}
.timeline::before{content:"";position:absolute;left:5px;top:6px;bottom:6px;width:1px;background:var(--line);}
.tl-item{position:relative;padding-bottom:40px;}
.tl-item:last-child{padding-bottom:0;}
.tl-item::before{
  content:"";position:absolute;left:-28px;top:4px;width:11px;height:11px;border-radius:50%;
  background:var(--paper);border:2px solid var(--line-bright);
}
.tl-head{display:flex;flex-wrap:wrap;justify-content:space-between;gap:8px;align-items:baseline;margin-bottom:6px;}
.tl-role{font-family:var(--display);font-size:1.1rem;color:var(--ink);}
.tl-date{font-family:var(--mono);font-size:0.72rem;color:var(--amber);text-transform:uppercase;letter-spacing:0.04em;}
.tl-org{color:var(--line-bright);font-size:0.9rem;margin-bottom:10px;}
.tl-item ul{color:var(--ink-soft);font-size:0.92rem;list-style:none;}
.tl-item li{padding-left:18px;position:relative;margin-bottom:6px;}
.tl-item li::before{content:"›";position:absolute;left:0;color:var(--line-bright);}

/* ---------- Projects ---------- */
.proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(280px,1fr));gap:20px;}
.proj-card{border:1px solid var(--line);border-radius:var(--radius);background:rgba(18,37,66,0.35);overflow:hidden;display:flex;flex-direction:column;transition:.2s;}
.proj-card:hover{border-color:var(--line-bright);transform:translateY(-3px);}
.proj-top{padding:22px 22px 0;flex:1;}
.proj-top h3{font-size:1.08rem;margin-bottom:8px;}
.proj-top p{color:var(--ink-soft);font-size:0.9rem;margin-bottom:14px;}
.proj-tags{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:20px;}
.proj-foot{
  font-family:var(--mono);font-size:0.66rem;text-transform:uppercase;letter-spacing:0.03em;
  display:grid;grid-template-columns:1fr 1fr;border-top:1px solid var(--line);
}
.proj-foot div{padding:10px 22px;border-left:1px solid var(--line);}
.proj-foot div:first-child{border-left:none;}
.proj-foot dt{color:var(--ink-soft);}
.proj-foot dd{color:var(--ink);margin-top:2px;}

/* ---------- Client work (live freelance sites) ---------- */
.client-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px;}
.client-card{
  border:1px solid var(--line);border-radius:var(--radius);overflow:hidden;
  background:rgba(18,37,66,0.35);transition:.2s;display:flex;flex-direction:column;
}
.client-card:hover{border-color:var(--line-bright);transform:translateY(-3px);}
.browser-frame{background:var(--paper-alt);border-bottom:1px solid var(--line);}
.browser-bar{display:flex;align-items:center;gap:8px;padding:10px 14px;border-bottom:1px solid var(--line);}
.browser-dots{display:flex;gap:5px;}
.browser-dots span{width:8px;height:8px;border-radius:50%;background:var(--line);display:inline-block;}
.browser-url{
  font-family:var(--mono);font-size:0.68rem;color:var(--ink-soft);
  background:rgba(12,26,43,0.6);border:1px solid var(--line);border-radius:20px;
  padding:3px 12px;flex:1;overflow:hidden;text-overflow:ellipsis;white-space:nowrap;
}
.browser-preview{
  height:110px;position:relative;overflow:hidden;
  display:flex;align-items:center;justify-content:center;
}
.browser-preview .glyph{font-family:var(--display);font-size:2.2rem;color:rgba(238,244,251,0.15);letter-spacing:0.02em;}
.client-top{padding:20px 22px;flex:1;}
.client-top h3{font-size:1.02rem;margin-bottom:6px;}
.client-top p{color:var(--ink-soft);font-size:0.86rem;margin-bottom:12px;}
.client-tags{display:flex;flex-wrap:wrap;gap:6px;}
.client-foot{border-top:1px solid var(--line);padding:12px 22px;}
.client-foot a{
  font-family:var(--mono);font-size:0.72rem;text-transform:uppercase;letter-spacing:0.04em;
  color:var(--line-bright);text-decoration:none;
}
.client-foot a:hover{text-decoration:underline;}

/* ---------- Case study ---------- */
.case{
  border:1px solid var(--line-bright);
  border-radius:18px;
  padding:clamp(24px,5vw,44px);
  background:linear-gradient(160deg,rgba(63,169,232,0.08),rgba(18,37,66,0.5));
  position:relative;
}
.case::before, .case::after{
  content:"";position:absolute;width:14px;height:14px;border:1px solid var(--line-bright);opacity:0.6;
}
.case::before{top:14px;left:14px;border-right:none;border-bottom:none;}
.case::after{bottom:14px;right:14px;border-left:none;border-top:none;}
.case-head{display:flex;flex-wrap:wrap;justify-content:space-between;gap:20px;margin-bottom:28px;}
.case-head h3{font-size:clamp(1.25rem,3vw,1.6rem);max-width:520px;}
.case-badge{font-family:var(--mono);font-size:0.7rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--amber);border:1px solid var(--amber);border-radius:30px;padding:6px 14px;height:fit-content;}
.case-cols{display:grid;grid-template-columns:1fr 1fr;gap:32px;margin-top:32px;}
.case-cols h4{font-size:0.85rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--line-bright);font-family:var(--mono);margin-bottom:14px;}
.pillar-list{list-style:none;}
.pillar-list li{padding:10px 0;border-bottom:1px solid var(--line);font-size:0.9rem;color:var(--ink-soft);display:flex;justify-content:space-between;gap:10px;flex-wrap:wrap;}
.pillar-list li:last-child{border-bottom:none;}
.pillar-list b{color:var(--ink);font-weight:500;}
.req-tag{font-family:var(--mono);font-size:0.62rem;text-transform:uppercase;padding:2px 8px;border-radius:10px;white-space:nowrap;height:fit-content;}
.req-mandatory{background:rgba(232,163,63,0.14);color:var(--amber);border:1px solid rgba(232,163,63,0.4);}
.req-optional{background:rgba(147,168,196,0.1);color:var(--ink-soft);border:1px solid var(--line);}

/* ---------- Education ---------- */
.edu-grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;}
.edu-card{border:1px solid var(--line);border-radius:var(--radius);padding:22px;background:rgba(18,37,66,0.3);}
.edu-card .k{font-family:var(--mono);font-size:0.68rem;color:var(--line-bright);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:8px;}
.edu-card h4{font-size:1rem;margin-bottom:4px;}
.edu-card .org{color:var(--ink-soft);font-size:0.86rem;margin-bottom:10px;}
.edu-card .date{font-family:var(--mono);font-size:0.72rem;color:var(--amber);}

/* ---------- Referees ---------- */
.ref-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:20px;}
.ref-card{border:1px solid var(--line);border-radius:var(--radius);padding:20px;background:rgba(18,37,66,0.3);}
.ref-card h4{font-size:1rem;margin-bottom:4px;}
.ref-card .role{color:var(--line-bright);font-size:0.82rem;margin-bottom:10px;}
.ref-card .org{color:var(--ink-soft);font-size:0.82rem;}
.ref-note{font-family:var(--mono);font-size:0.78rem;color:var(--ink-soft);margin-top:24px;}

/* ---------- Footer / contact ---------- */
.contact{text-align:center;}
.contact h2{font-size:clamp(1.7rem,5vw,3rem);max-width:700px;margin:0 auto 20px;}
.contact p{color:var(--ink-soft);max-width:520px;margin:0 auto 32px;}
.contact-links{display:flex;justify-content:center;gap:14px;flex-wrap:wrap;margin-bottom:48px;}
footer{border-top:1px solid var(--line);padding:28px 0;}
.foot-inner{display:flex;flex-wrap:wrap;justify-content:space-between;gap:12px;font-family:var(--mono);font-size:0.74rem;color:var(--ink-soft);}
.foot-inner a{color:var(--ink-soft);text-decoration:none;}
.foot-inner a:hover{color:var(--line-bright);}

/* ---------- Reveal animation ---------- */
.reveal{opacity:0;transform:translateY(18px);transition:opacity .6s ease, transform .6s ease;}
.reveal.in{opacity:1;transform:translateY(0);}

/* ================= RESPONSIVE ================= */
/* Tablet / narrow-desktop */
@media (max-width:900px){
  .hero-grid{grid-template-columns:1fr;}
  .hero-art{order:-1;max-width:320px;}
  .about-grid{grid-template-columns:1fr;}
  .case-cols{grid-template-columns:1fr;}
  .edu-grid{grid-template-columns:1fr;}
}
/* Phones */
@media (max-width:720px){
  .nav-links, .nav-cta{display:none;}
  .nav-toggle{display:block;}
  .nav.open .nav-links{
    display:flex;flex-direction:column;position:absolute;top:100%;left:0;right:0;
    background:var(--paper-alt);padding:20px var(--gutter);border-bottom:1px solid var(--line);gap:16px;
  }
  .nav.open .nav-cta{display:inline-flex;margin-top:4px;}
  .stat-list{grid-template-columns:1fr 1fr;}
  .title-block{grid-template-columns:1fr 1fr;}
  .case-head{flex-direction:column;}
  .contact-links{flex-direction:column;align-items:stretch;}
  .contact-links .btn{justify-content:center;}
}
/* Very small phones */
@media (max-width:400px){
  .stat-list, .title-block{grid-template-columns:1fr;}
  .btn-row{flex-direction:column;align-items:stretch;}
  .btn-row .btn{justify-content:center;}
}

.section-h {
  margin-top: 20px;
}
</style>
</head>
<body>

<nav class="nav" id="nav">
  <div class="nav-inner">
    <!-- <div class="nav-brand"><span class="dot"></span> BRIAN MUCHERE</div> -->
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#work">Work</a></li>
      <li><a href="#clients">Clients</a></li>
      <li><a href="#case-study">Case Study</a></li>
      <li><a href="#credentials">Credentials</a></li>
    </ul>
    <a class="nav-cta" href="mailto:mucherebrian@gmail.com">Start a project</a>
    <button class="nav-toggle" id="navToggle" aria-label="Toggle menu">☰</button>
  </div>
</nav>

<!-- HERO -->
<section class="hero wrap">
  <div class="hero-grid">
    <div>
      <div class="eyebrow reveal in">Technology Solutions · Software · Connectivity · IT · Training</div>
      <h1 class="reveal in">Building <span>technology that connects, automates &amp; empowers</span> people and businesses.</h1>
      <p class="lead reveal in">I'm Brian Muchere, a Full-Stack Software Engineer and Technology Solutions Specialist with 5+ years of
          experience delivering custom software, enterprise and business systems, internet &amp; Wi-Fi solutions, IT hardware and infrastructure, data
          &amp; AI solutions, and practical technology training. From powering businesses with reliable connectivity
          and digital systems to training the next generation of technology professionals, I turn technology into practical, scalable solutions.
      </p>
      <div class="btn-row reveal in">
        <a class="btn btn-primary" href="#work">View the work</a>
        <a class="btn btn-ghost" href="mailto:mucherebrian@gmail.com">Start a project →</a>
      </div>
      <dl class="title-block reveal in">
        <div><dt>Location</dt><dd>Nairobi, KE</dd></div>
        <div><dt>Experience</dt><dd>5+ years</dd></div>
        <div><dt>Status</dt><dd>Open to projects</dd></div>
        <div><dt>Core stack</dt><dd>Python · Django · React · TypeScript</dd></div>
      </dl>
    </div>

    <!-- Hero visual: the six services as a circular diagram, drawn entirely
         as inline SVG. No image file, no external link, nothing to host —
         it's just markup, so it survives copy/paste into a README exactly
         as well as it renders here. -->
    <div class="hero-art reveal in hero-wheel" aria-hidden="true">
      <svg viewBox="0 0 520 580" xmlns="http://www.w3.org/2000/svg">
        <rect x="0" y="0" width="520" height="580" fill="#0c1a2b"/>

        <g stroke="#24405f" stroke-width="1" opacity="0.35">
          <line x1="0" y1="90" x2="520" y2="90"/>
          <line x1="0" y1="470" x2="520" y2="470"/>
          <line x1="95" y1="0" x2="95" y2="580"/>
          <line x1="425" y1="0" x2="425" y2="580"/>
        </g>

        <circle class="wheel-orbit" cx="260" cy="280" r="190" fill="none" stroke="#24405f" stroke-width="1.4" stroke-dasharray="3 7" opacity="0.6"/>

        <g stroke="#3fa9e8" stroke-width="1.6" opacity="0.55">
          <line x1="260" y1="280" x2="260" y2="90"/>
          <line x1="260" y1="280" x2="425" y2="185"/>
          <line x1="260" y1="280" x2="425" y2="375"/>
          <line x1="260" y1="280" x2="260" y2="470"/>
          <line x1="260" y1="280" x2="95" y2="375"/>
          <line x1="260" y1="280" x2="95" y2="185"/>
        </g>

        <!-- 01 Custom Software -->
        <g transform="translate(260,90)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text y="-70" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">01</text>
          <g stroke="#eef4fb" stroke-width="2.4" fill="none" stroke-linecap="round" stroke-linejoin="round">
            <path d="M-8,-11 L-17,0 L-8,11"/>
            <path d="M8,-11 L17,0 L8,11"/>
            <path d="M3,-13 L-3,13"/>
          </g>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Custom Software</text>
        </g>

        <!-- 02 Enterprise Systems -->
        <g transform="translate(425,185)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text x="30" y="-58" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">02</text>
          <g>
            <rect x="-13" y="-16" width="26" height="32" rx="2" fill="none" stroke="#eef4fb" stroke-width="2.1"/>
            <rect x="-9" y="-11" width="5" height="5" fill="#eef4fb"/>
            <rect x="1" y="-11" width="5" height="5" fill="#eef4fb"/>
            <rect x="-9" y="-2" width="5" height="5" fill="#eef4fb"/>
            <rect x="1" y="-2" width="5" height="5" fill="#eef4fb"/>
            <rect x="-4" y="8" width="8" height="8" fill="#eef4fb"/>
          </g>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Enterprise</text>
          <text y="102" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Systems</text>
        </g>

        <!-- 03 Sector Solutions -->
        <g transform="translate(425,375)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text x="30" y="-58" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">03</text>
          <g fill="#eef4fb">
            <rect x="-14" y="-14" width="11" height="11" rx="2"/>
            <rect x="3" y="-14" width="11" height="11" rx="2"/>
            <rect x="-14" y="3" width="11" height="11" rx="2"/>
            <rect x="3" y="3" width="11" height="11" rx="2"/>
          </g>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Sector</text>
          <text y="102" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Solutions</text>
        </g>

        <!-- 04 Data & AI -->
        <g transform="translate(260,470)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text y="-70" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">04</text>
          <g stroke="#eef4fb" stroke-width="2.1">
            <line x1="0" y1="-14" x2="-12" y2="10"/>
            <line x1="0" y1="-14" x2="12" y2="10"/>
            <line x1="-12" y1="10" x2="12" y2="10"/>
          </g>
          <g fill="#eef4fb">
            <circle cx="0" cy="-14" r="3.4"/>
            <circle cx="-12" cy="10" r="3.4"/>
            <circle cx="12" cy="10" r="3.4"/>
          </g>
          <circle cx="0" cy="1" r="3" fill="none" stroke="#e8a33f" stroke-width="2"/>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Data &amp; AI</text>
        </g>

        <!-- 05 Infrastructure -->
        <g transform="translate(95,375)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text x="-30" y="-58" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">05</text>
          <g stroke="#eef4fb" stroke-width="2.4" fill="none" stroke-linecap="round">
            <path d="M-15,-3 a21,21 0 0 1 30,0"/>
            <path d="M-9,5 a12,12 0 0 1 18,0"/>
          </g>
          <circle cx="0" cy="13" r="2.6" fill="#eef4fb"/>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Infrastructure</text>
        </g>

        <!-- 06 Tech Training -->
        <g transform="translate(95,185)">
          <circle r="54" fill="#152a49" stroke="#3fa9e8" stroke-width="1.6"/>
          <text x="-30" y="-58" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="11" letter-spacing="1" fill="#e8a33f">06</text>
          <path d="M-16,-4 L0,-12 L16,-4 L0,4 Z" fill="#0c1a2b" stroke="#eef4fb" stroke-width="2" stroke-linejoin="round"/>
          <path d="M-8,0 L-8,8 Q0,14 8,8 L8,0" fill="none" stroke="#eef4fb" stroke-width="2" stroke-linecap="round"/>
          <line x1="12" y1="-2" x2="12" y2="9" stroke="#eef4fb" stroke-width="2" stroke-linecap="round"/>
          <circle cx="12" cy="10" r="1.8" fill="#e8a33f"/>
          <text y="86" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="13.5" letter-spacing="0.5" fill="#eef4fb">Tech Training</text>
        </g>

        <!-- hub -->
        <circle cx="260" cy="280" r="70" fill="#122542" stroke="#e8a33f" stroke-width="1.8"/>
        <circle class="wheel-orbit" cx="260" cy="280" r="58" fill="none" stroke="#e8a33f" stroke-width="1" stroke-dasharray="2 5" opacity="0.6"/>
        <text x="260" y="272" text-anchor="middle" font-family="'Space Grotesk','Segoe UI',sans-serif" font-size="17" font-weight="600" fill="#eef4fb">BRIAN</text>
        <text x="260" y="289" text-anchor="middle" font-family="'IBM Plex Mono','Courier New',monospace" font-size="9.5" letter-spacing="1.5" fill="#93a8c4">6 CORE SERVICES</text>
      </svg>
      <p class="illus-caption">// six services, one core</p>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about" class="wrap section-h">
  <div class="eyebrow reveal">About</div>
  <div class="about-grid">
    <div class="reveal">
      <h2 class="section-title">I connect the systems institutions run on.</h2>
      <p>Results-driven full-stack developer with 5+ years building scalable web applications, REST APIs and enterprise platforms with Python, Django, React, JavaScript, TypeScript, Tailwind CSS, Bootstrap and Firebase. Most of that work sits inside HR, pension, recruitment and procurement systems for enterprise clients, so I'm used to messy integration requirements, audit trails, and the kind of edge cases that only show up once real money and real people are on the line.</p>
      <p>Outside the core stack I bring machine learning into products where it earns its place — predictive analytics, NLP and anomaly detection with scikit-learn, TensorFlow and PyTorch — and a networking background (CCNA, structured LAN builds, core-banking systems like T24) that makes me comfortable owning a project end-to-end, from the server room to the browser.</p>
      <p>That networking side extends into ISP-style connectivity work too — internet and Wi-Fi installation, fiber and wireless setup, router/access-point configuration, and network maintenance for homes, offices, schools and organizations that just need reliable connectivity in place.</p>
    </div>
    <div class="stat-list reveal">
      <div class="stat-card"><div class="num">5+</div><div class="lbl">Years shipping production systems</div></div>
      <div class="stat-card"><div class="num">8+</div><div class="lbl">Enterprise platforms delivered</div></div>
      <div class="stat-card"><div class="num">4</div><div class="lbl">Domains: pension, HR, procurement, recruitment</div></div>
      <div class="stat-card"><div class="num">4</div><div class="lbl">Live freelance client sites shipped</div></div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="wrap section-h">
  <div class="eyebrow reveal section-h">Freelance services</div>
  <h2 class="section-title reveal">Work with me on your next build</h2>
  <p class="section-sub reveal">I take on freelance and contract engagements — from a single integration to a full platform build. Here's where I add the most value.</p>
  <div class="svc-grid">
    <div class="svc-card reveal">
      <div class="idx">01 · Software</div>
      <h3>Custom web &amp; software development</h3>
      <ul>
        <li>Business websites &amp; web apps</li>
        <li>Mobile apps &amp; customer portals</li>
        <li>Management dashboards</li>
        <li>System integrations &amp; APIs</li>
      </ul>
    </div>
    <div class="svc-card reveal">
      <div class="idx">02 · Enterprise systems</div>
      <h3>Business &amp; organization platforms</h3>
      <ul>
        <li>HR, payroll &amp; employee management</li>
        <li>Procurement &amp; workflow automation</li>
        <li>Pension &amp; provident fund systems</li>
        <li>Document management &amp; dashboards</li>
      </ul>
    </div>
    <div class="svc-card reveal">
      <div class="idx">03 · Sector solutions</div>
      <h3>POS, health &amp; education systems</h3>
      <ul>
        <li>POS &amp; SME inventory/sales systems</li>
        <li>Hospital management (HMIS)</li>
        <li>School management &amp; CBC assessment tools</li>
        <li>Fee, billing &amp; reporting modules</li>
      </ul>
    </div>
    <div class="svc-card reveal">
      <div class="idx">04 · Data &amp; AI</div>
      <h3>Data, automation &amp; ML</h3>
      <ul>
        <li>Predictive analytics &amp; anomaly detection</li>
        <li>NLP &amp; document/ID processing (OCR)</li>
        <li>Process automation with Python</li>
        <li>Reporting &amp; BI integrations</li>
      </ul>
    </div>
    <div class="svc-card reveal">
      <div class="idx">05 · Infrastructure</div>
      <h3>ISP, internet &amp; network solutions</h3>
      <ul>
        <li>Internet &amp; Wi-Fi installation (ISP-style setup)</li>
        <li>Fiber &amp; wireless connectivity, coverage optimization</li>
        <li>Router/access point &amp; switch configuration (Cisco)</li>
        <li>Network monitoring, maintenance &amp; troubleshooting</li>
      </ul>
    </div>
    <div class="svc-card reveal">
      <div class="idx">06 · Training</div>
      <h3>Technology training</h3>
      <ul>
        <li>Programming &amp; software development</li>
        <li>Data science &amp; analytics</li>
        <li>AI &amp; machine learning fundamentals</li>
        <li>Digital literacy &amp; productivity tools</li>
      </ul>
    </div>
  </div>
</section>

<!-- SKILLS -->
<section id="skills" class="wrap section-h">
  <div class="eyebrow reveal section-h">Technical skills</div>
  <h2 class="section-title reveal">The stack, in full</h2>
  <p class="section-sub reveal">Python/Django on the backend, a modern JavaScript/TypeScript frontend, and ML brought in where it's genuinely useful.</p>
  <div class="skill-grid">
    <div class="skill-card reveal"><h4><span class="sw"></span>Backend &amp; frameworks</h4><div class="tagset"><span class="tag">Python</span><span class="tag">Django</span><span class="tag">Flask</span><span class="tag">FastAPI</span><span class="tag">Node.js</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Frontend</h4><div class="tagset"><span class="tag">JavaScript</span><span class="tag">TypeScript</span><span class="tag">React</span><span class="tag">Redux</span><span class="tag">HTML5</span><span class="tag">CSS3</span><span class="tag">Tailwind CSS</span><span class="tag">Bootstrap</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Data &amp; databases</h4><div class="tagset"><span class="tag">PostgreSQL</span><span class="tag">MySQL</span><span class="tag">SQL Server</span><span class="tag">SQLAlchemy</span><span class="tag">Advanced SQL</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Machine learning</h4><div class="tagset"><span class="tag">scikit-learn</span><span class="tag">TensorFlow</span><span class="tag">PyTorch</span><span class="tag">spaCy</span><span class="tag">NLP</span><span class="tag">Anomaly detection</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>DevOps &amp; cloud</h4><div class="tagset"><span class="tag">Docker</span><span class="tag">Git / CI-CD</span><span class="tag">HCIA Cloud</span><span class="tag">Deployment troubleshooting</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Networking</h4><div class="tagset"><span class="tag">CCNA</span><span class="tag">Cisco / D-Link</span><span class="tag">LAN design</span><span class="tag">T24 core banking</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Testing</h4><div class="tagset"><span class="tag">pytest</span><span class="tag">Jest</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Domain expertise</h4><div class="tagset"><span class="tag">AML / KYC / CFT</span><span class="tag">Pension systems</span><span class="tag">Asset management</span><span class="tag">API integration</span></div></div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="wrap section-h">
  <div class="eyebrow reveal section-h">Experience</div>
  <h2 class="section-title reveal">Where the stack got built</h2>
  <div class="timeline">
    <div class="tl-item reveal">
      <div class="tl-head"><span class="tl-role">Full-Stack Software Developer</span><span class="tl-date">Jan 2024 — Present</span></div>
      <div class="tl-org">Deft Technologies Ltd · Nairobi, Kenya</div>
      <ul>
        <li>Designed and built enterprise platforms with Django, React and TypeScript — including pension, procurement and recruitment portals.</li>
        <li>Built secure REST APIs and integrated third-party systems across HR, procurement and finance workflows.</li>
        <li>Led automation initiatives that removed manual steps from internal software delivery.</li>
        <li>Ran sprint planning, retrospectives and client requirement analysis inside agile teams.</li>
      </ul>
    </div>
    <div class="tl-item reveal">
      <div class="tl-head"><span class="tl-role">Technical Support Intern — Digitalent</span><span class="tl-date">Dec 2022 — Dec 2023</span></div>
      <div class="tl-org">Kenya Revenue Authority (KRA), Presidential Digitalent Program</div>
      <ul>
        <li>Installed, configured and maintained KRA software and ICT infrastructure.</li>
        <li>Co-built an ICT Asset Management &amp; Inventory System and a LAN IP Sniffing System.</li>
        <li>Monitored the KRA Western Region network with NagVis; configured Cisco and D-Link routers/switches and structured cabling.</li>
      </ul>
    </div>
    <div class="tl-item reveal">
      <div class="tl-head"><span class="tl-role">Computer Studies Instructor</span><span class="tl-date">May 2022 — Aug 2022</span></div>
      <div class="tl-org">Royal Computer School</div>
      <ul>
        <li>Designed lesson plans and practical training materials.</li>
        <li>Ran group training sessions and ICT troubleshooting for staff.</li>
      </ul>
    </div>
    <div class="tl-item reveal">
      <div class="tl-head"><span class="tl-role">Business Development &amp; Social Media Intern</span><span class="tl-date">Dec 2021 — Jan 2022</span></div>
      <div class="tl-org">Funder Holdings</div>
      <ul>
        <li>Managed corporate social platforms and built a content calendar.</li>
        <li>Conducted market research to support growth strategy.</li>
      </ul>
    </div>
  </div>
</section>

<!-- PROJECTS -->
<section id="work" class="wrap section-h">
  <div class="eyebrow reveal section-h">Selected work</div>
  <h2 class="section-title reveal">Systems in production</h2>
  <p class="section-sub reveal">Platforms built for financial services, pension administration and government-adjacent institutions.</p>
  <div class="proj-grid">

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Kenya Airways Provident Fund Portal</h3>
        <p>Member-facing pension/provident fund portal — contributions, statements, secure authentication and reporting.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">React</span><span class="tag">PostgreSQL</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>Kenya Airways PF</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Provident Fund E-Recruitment Portal</h3>
        <p>Recruitment platform for AKI &amp; Kenya Airways Provident Fund with applicant tracking, vacancy management, interview workflows and notifications.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">TypeScript</span><span class="tag">Tailwind CSS</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI · KQ PF</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Provident Fund E-Procurement Portal</h3>
        <p>Supplier management, approvals, requisitions, tender management and reporting dashboards for two institutional clients.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">JavaScript</span><span class="tag">Bootstrap</span><span class="tag">REST API</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI · KQ PF</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Employee Self-Service (ESS) Portal</h3>
        <p>Leave management, appraisals, profile management and secure payslip access for staff.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">React</span><span class="tag">TypeScript</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Pension Management System</h3>
        <p>Contribution tracking, claims processing, benefits management and reporting for a licensed insurance broker.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">JavaScript</span><span class="tag">Bootstrap</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>QIJITO Insurance Brokers</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>ICT Asset Management &amp; LAN IP Sniffing</h3>
        <p>Asset inventory system plus a network tool for identifying and tracking devices on the LAN.</p>
        <div class="proj-tags"><span class="tag">Python</span><span class="tag">C# / .NET</span><span class="tag">SQL Server</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>Kenya Revenue Authority</dd></div><div><dt>Role</dt><dd>Contributor</dd></div></dl>
    </div>

  </div>
</section>

<!-- CLIENT WORK -->
<section id="clients" class="wrap section-h">
  <div class="eyebrow reveal section-h">Freelance client work</div>
  <h2 class="section-title reveal">Live sites I've built &amp; shipped</h2>
  <p class="section-sub reveal">Beyond enterprise systems, I design and build business websites end to end. Replace the placeholder preview blocks below with real screenshots of each site whenever you get a moment — that's the one thing I can't fetch for you automatically.</p>
  <div class="client-grid">

    <div class="client-card reveal">
      <div class="browser-frame">
        <div class="browser-bar">
          <div class="browser-dots"><span></span><span></span><span></span></div>
          <div class="browser-url">defttech.co.ke</div>
        </div>
        <!-- <div class="browser-preview"><span class="glyph">Deft</span></div> -->
      </div>
      <div class="client-top">
        <h3>Deft</h3>
        <p>Business website built and shipped end to end — structure, styling and content.</p>
        <div class="client-tags"><span class="tag">Next js</span><span class="tag">Typescript</span><span class="tag">Tailwind CSS</span></div>
      </div>
      <div class="client-foot"><a href="https://defttech.co.ke/" target="_blank" rel="noopener">Visit deft.co.ke →</a></div>
    </div>

    <div class="client-card reveal">
      <div class="browser-frame">
        <div class="browser-bar">
          <div class="browser-dots"><span></span><span></span><span></span></div>
          <div class="browser-url">noted.co.ke</div>
        </div>
        <!-- <div class="browser-preview"><span class="glyph">Noted</span></div> -->
      </div>
      <div class="client-top">
        <h3>Noted</h3>
        <p>Business website built and shipped end to end — structure, styling and content.</p>
        <div class="client-tags"><span class="tag">Django</span><span class="tag">JavaScript</span><span class="tag">Tailwind CSS</span></div>
      </div>
      <div class="client-foot"><a href="https://noted.co.ke/" target="_blank" rel="noopener">Visit noted.co.ke →</a></div>
    </div>

    <div class="client-card reveal">
      <div class="browser-frame">
        <div class="browser-bar">
          <div class="browser-dots"><span></span><span></span><span></span></div>
          <div class="browser-url">serenehomecare.co.ke</div>
        </div>
        <!-- <div class="browser-preview"><span class="glyph">Serene</span></div> -->
      </div>
      <div class="client-top">
        <h3>Serene Home Care</h3>
        <p>Home-care service website with service listings, contact and booking-style enquiry flows.</p>
        <div class="client-tags"><span class="tag">Django</span><span class="tag">HTML/CSS</span><span class="tag">Bootstrap</span></div>
      </div>
      <div class="client-foot"><a href="https://serenehomecare.co.ke/" target="_blank" rel="noopener">Visit serenehomecare.co.ke →</a></div>
    </div>

    <div class="client-card reveal">
      <div class="browser-frame">
        <div class="browser-bar">
          <div class="browser-dots"><span></span><span></span><span></span></div>
          <div class="browser-url">infrasoft.co.ke</div>
        </div>
        <!-- <div class="browser-preview"><span class="glyph">Infrasoft</span></div> -->
      </div>
      <div class="client-top">
        <h3>Infrasoft</h3>
        <p>Corporate technology/software company site — services, portfolio and lead-generation pages.</p>
        <div class="client-tags"><span class="tag">JavaScript</span><span class="tag">TypeScript</span><span class="tag">Tailwind CSS</span></div>
      </div>
      <div class="client-foot"><a href="https://infrasoft.co.ke/" target="_blank" rel="noopener">Visit infrasoft.co.ke →</a></div>
    </div>

    <div class="client-card reveal">
      <div class="browser-frame">
        <div class="browser-bar">
          <div class="browser-dots"><span></span><span></span><span></span></div>
          <div class="browser-url">nestapetroleum.com</div>
        </div>
        <!-- <div class="browser-preview"><span class="glyph">Nesta</span></div> -->
      </div>
      <div class="client-top">
        <h3>Nesta Petroleum</h3>
        <p>Corporate petroleum/energy company website — company profile, services and contact channels.</p>
        <div class="client-tags"><span class="tag">React Js</span><span class="tag">TailwindCss</span><span class="tag">JavaScript</span></div>
      </div>
      <div class="client-foot"><a href="https://nestapetroleum.com/" target="_blank" rel="noopener">Visit nestapetroleum.com →</a></div>
    </div>

  </div>
</section>

<!-- CASE STUDY -->
<section id="case-study" class="wrap section-h">
  <div class="eyebrow reveal section-h">Case study</div>
  <div class="case reveal">
    <div class="case-head">
      <div>
        <h3>Liveness Certification / Proof of Life Module</h3>
        <p style="color:var(--ink-soft);max-width:560px;margin-top:10px;">A requirements-led design for a pension ERP module that verifies beneficiaries are alive before disbursement continues — cutting fraud and "ghost pensioner" payouts while giving pensioners a remote, accessible way to certify.</p>
      </div>
      <span class="case-badge">Requirements &amp; systems design</span>
    </div>

    <div class="case-cols">
      <div>
        <h4>What it solves</h4>
        <ul class="pillar-list">
          <li>Eliminate payments to deceased or "ghost" pensioners <span class="req-tag req-mandatory">Core goal</span></li>
          <li>Digital identity checks in place of manual, in-person proof-of-life visits <span class="req-tag req-mandatory">Core goal</span></li>
          <li>Real-time status feeding directly into pension disbursement control <span class="req-tag req-mandatory">Core goal</span></li>
          <li>Cross-verification against national ID / civil registry systems <span class="req-tag req-optional">Where permissible</span></li>
        </ul>
      </div>
      <div>
        <h4>Module pillars</h4>
        <ul class="pillar-list">
          <li><b>Pensioner portal</b> — MFA login, dashboard, self-initiated checks <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>Biometric verification</b> — facial recognition with anti-spoofing liveness detection <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>OCR &amp; ID matching</b> — national ID/passport validation against records <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>ERP integration</b> — auto-updates status, blocks payment if unverified <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>Assisted verification</b> — agent-supported option for low-connectivity pensioners <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>Notifications</b> — SMS/email/push reminders for pending certifications <span class="req-tag req-optional">Optional</span></li>
          <li><b>Audit &amp; compliance</b> — time-stamped, geo-tagged logs; encrypted biometric data <span class="req-tag req-mandatory">Mandatory</span></li>
          <li><b>Analytics</b> — compliance dashboards, fraud-prevention reporting <span class="req-tag req-optional">Optional</span></li>
        </ul>
      </div>
    </div>
  </div>
</section>

<!-- EDUCATION / CREDENTIALS -->
<section id="credentials" class="wrap section-h">
  <div class="eyebrow reveal section-h">Credentials</div>
  <h2 class="section-title reveal">Education &amp; certifications</h2>
  <div class="edu-grid">
    <div class="edu-card reveal">
      <div class="k">Degree</div>
      <h4>B.Sc. Computer Science</h4>
      <div class="org">University of Eldoret — Second Class Honours, Upper Division</div>
      <div class="date">Aug 2017 — Aug 2021</div>
    </div>
    <div class="edu-card reveal">
      <div class="k">Certification</div>
      <h4>Cisco Certified Network Associate (CCNA)</h4>
      <div class="org">Cisco Networking Academy</div>
      <div class="date">Jan 2023 — May 2023</div>
    </div>
    <div class="edu-card reveal">
      <div class="k">Certification</div>
      <h4>HCIA — Cloud Computing &amp; Data Storage</h4>
      <div class="org">PDTP &amp; Huawei Academy</div>
      <div class="date">Mar 2023 — May 2023</div>
    </div>
    <div class="edu-card reveal">
      <div class="k">Certification</div>
      <h4>CS50's Web Programming with Python &amp; JavaScript</h4>
      <div class="org">Harvard University (edX)</div>
      <div class="date">Jan 2023 — Aug 2023</div>
    </div>
    <div class="edu-card reveal">
      <div class="k">Certification</div>
      <h4>Automation with Python</h4>
      <div class="org">Google via Coursera</div>
      <div class="date">Apr 2023 — Jul 2023</div>
    </div>
  </div>
</section>

<!-- REFEREES -->
<section id="referees" class="wrap section-h">
  <div class="eyebrow reveal section-h">References</div>
  <h2 class="section-title reveal">People who've worked with me</h2>
  <div class="ref-grid">
    <div class="ref-card reveal">
      <h4>Fredrick Wabala</h4>
      <div class="role">Pension Administration &amp; Consulting</div>
      <div class="org">Enwealth Financial Services Limited</div>
    </div>
    <div class="ref-card reveal">
      <h4>Ezra Chirchir</h4>
      <div class="role">Technical Director</div>
      <div class="org">Deft Technologies Ltd</div>
    </div>
    <div class="ref-card reveal">
      <h4>Kelvin Koome Mwiti</h4>
      <div class="role">Functional Director</div>
      <div class="org">Deft Technologies Ltd</div>
    </div>
  </div>
  <p class="ref-note">Full contact details provided on request.</p>
</section>

<!-- CONTACT -->
<section id="contact" class="wrap contact section-h">
  <div class="eyebrow reveal section-h" style="justify-content:center;">Get in touch</div>
  <h2 class="reveal">Have a system that needs building — or fixing?</h2>
  <p class="reveal">I'm currently open to freelance and contract engagements, from a focused integration to a full platform build. Tell me what you're working on.</p>
  <div class="contact-links reveal">
    <a class="btn btn-primary" href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a>
    <a class="btn btn-ghost" href="tel:+254799737828">+254 799 737828</a>
    <a class="btn btn-ghost" href="https://github.com/Brian-2000/" target="_blank" rel="noopener">GitHub</a>
    <a class="btn btn-ghost" href="https://www.linkedin.com/in/brian-muchere/" target="_blank" rel="noopener">LinkedIn</a>
  </div>
</section>

<footer>
  <div class="wrap foot-inner">
    <span>© <span id="year"></span> Brian Muchere — full-stack engineer, Nairobi</span>
    <span>Built with Django, React &amp; a lot of title blocks</span>
  </div>
</footer>

<script>
document.getElementById('year').textContent = new Date().getFullYear();

// mobile nav toggle
const nav = document.getElementById('nav');
document.getElementById('navToggle').addEventListener('click', () => nav.classList.toggle('open'));
nav.querySelectorAll('.nav-links a').forEach(a => a.addEventListener('click', () => nav.classList.remove('open')));

// scroll reveal
const revealEls = document.querySelectorAll('.reveal');
const io = new IntersectionObserver((entries) => {
  entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('in'); io.unobserve(e.target); } });
}, { threshold: 0.12 });
revealEls.forEach(el => io.observe(el));

// active nav link on scroll
const sections = document.querySelectorAll('section[id]');
const navLinks = document.querySelectorAll('.nav-links a');
const spy = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    const link = document.querySelector(`.nav-links a[href="#${entry.target.id}"]`);
    if (!link) return;
    if (entry.isIntersecting) {
      navLinks.forEach(l => l.classList.remove('active'));
      link.classList.add('active');
    }
  });
}, { rootMargin: '-40% 0px -50% 0px' });
sections.forEach(s => spy.observe(s));
</script>

</body>
</html>