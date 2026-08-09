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
  --radius:14px;
  --mono:'IBM Plex Mono',monospace;
  --display:'Space Grotesk',sans-serif;
  --body:'Inter',sans-serif;
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
}
a{color:inherit;}
img{max-width:100%;display:block;}
.wrap{max-width:1180px;margin:0 auto;padding:0 24px;}
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
h2.section-title{font-size:clamp(1.6rem,3vw,2.3rem);margin-bottom:10px;}
.section-sub{color:var(--ink-soft);max-width:640px;font-size:1rem;margin-bottom:44px;}
section{padding:96px 0;position:relative;border-top:1px solid var(--line);}
section:first-of-type{border-top:none;}

/* ---------- Title block (signature component) ---------- */
.title-block{
  display:grid;
  grid-template-columns:repeat(auto-fit,minmax(140px,1fr));
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
}
.title-block > div:first-child{border-left:none;}
.title-block dt{color:var(--ink-soft);text-transform:uppercase;letter-spacing:0.08em;font-size:0.65rem;margin-bottom:4px;}
.title-block dd{color:var(--ink);font-weight:500;}

/* ---------- Nav ---------- */
.nav{
  position:sticky;top:0;z-index:100;
  background:rgba(12,26,43,0.88);
  backdrop-filter:blur(10px);
  border-bottom:1px solid var(--line);
}
.nav-inner{
  max-width:1180px;margin:0 auto;padding:16px 24px;
  display:flex;align-items:center;justify-content:space-between;
}
.nav-brand{font-family:var(--mono);font-size:0.85rem;letter-spacing:0.05em;display:flex;align-items:center;gap:8px;}
.nav-brand .dot{width:8px;height:8px;border-radius:50%;background:var(--amber);box-shadow:0 0 0 3px rgba(232,163,63,0.18);}
.nav-links{display:flex;gap:28px;list-style:none;font-family:var(--mono);font-size:0.76rem;letter-spacing:0.04em;text-transform:uppercase;}
.nav-links a{text-decoration:none;color:var(--ink-soft);transition:color .2s;padding:4px 0;border-bottom:1px solid transparent;}
.nav-links a:hover, .nav-links a.active{color:var(--line-bright);border-color:var(--line-bright);}
.nav-cta{
  font-family:var(--mono);font-size:0.76rem;text-transform:uppercase;letter-spacing:0.04em;
  border:1px solid var(--amber);color:var(--amber);padding:8px 16px;border-radius:30px;text-decoration:none;
  transition:.2s;white-space:nowrap;
}
.nav-cta:hover{background:var(--amber);color:var(--paper);}
.nav-toggle{display:none;background:none;border:1px solid var(--line);color:var(--ink);border-radius:8px;padding:8px 10px;font-size:1rem;}

/* ---------- Hero ---------- */
.hero{padding:72px 0 60px;border-top:none;}
.hero-grid{display:grid;grid-template-columns:1.1fr 0.9fr;gap:48px;align-items:center;}
.hero h1{font-size:clamp(1.5rem,3vw,2.0rem);line-height:1.02;margin-bottom:18px;}
.hero h1 span{color:var(--line-bright);}
.hero p.lead{font-size:1.12rem;color:var(--ink-soft);max-width:520px;margin-bottom:32px;}
.btn-row{display:flex;gap:14px;flex-wrap:wrap;margin-bottom:44px;}
.btn{
  font-family:var(--mono);font-size:0.8rem;text-transform:uppercase;letter-spacing:0.05em;
  padding:13px 24px;border-radius:30px;text-decoration:none;transition:.2s;display:inline-flex;align-items:center;gap:8px;
}
.btn-primary{background:var(--line-bright);color:#06101c;font-weight:600;}
.btn-primary:hover{background:#63bcf0;}
.btn-ghost{border:1px solid var(--line);color:var(--ink);}
.btn-ghost:hover{border-color:var(--line-bright);color:var(--line-bright);}

.schema{position:relative;aspect-ratio:1/1;}
.schema svg{width:100%;height:100%;}
.schema-path{stroke:var(--line-bright);stroke-width:1.6;fill:none;opacity:0.75;}
.schema-pulse{stroke-dasharray:6 220;animation:dash 5.5s linear infinite;}
@keyframes dash{to{stroke-dashoffset:-450;}}
.schema-node rect{fill:var(--panel);stroke:var(--line);}
.schema-node text{font-family:var(--mono);font-size:9.5px;fill:var(--ink-soft);}
.schema-node.core rect{stroke:var(--amber);}
.schema-node.core text{fill:var(--amber);}

@media (prefers-reduced-motion: reduce){
  .schema-pulse{animation:none;}
  *{scroll-behavior:auto !important;}
}

/* ---------- About stats ---------- */
.about-grid{display:grid;grid-template-columns:1.2fr 0.8fr;gap:56px;align-items:start;}
.about-grid p{color:var(--ink-soft);margin-bottom:16px;max-width:600px;}
.stat-list{display:grid;grid-template-columns:1fr 1fr;gap:16px;}
.stat-card{border:1px solid var(--line);border-radius:var(--radius);padding:20px;background:rgba(18,37,66,0.4);}
.stat-card .num{font-family:var(--display);font-size:1.9rem;color:var(--line-bright);}
.stat-card .lbl{font-family:var(--mono);font-size:0.7rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--ink-soft);margin-top:4px;}

/* ---------- Services ---------- */
.svc-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(260px,1fr));gap:20px;}
.svc-card{border:1px solid var(--line);border-radius:var(--radius);padding:26px;background:rgba(18,37,66,0.35);transition:.2s;}
.svc-card:hover{border-color:var(--line-bright);transform:translateY(-3px);}
.svc-card .idx{font-family:var(--mono);color:var(--amber);font-size:0.75rem;margin-bottom:10px;}
.svc-card h3{font-size:1.08rem;margin-bottom:10px;}
.svc-card ul{list-style:none;color:var(--ink-soft);font-size:0.88rem;}
.svc-card li{padding-left:16px;position:relative;margin-bottom:6px;}
.svc-card li::before{content:"—";position:absolute;left:0;color:var(--line);}

/* ---------- Skills ---------- */
.skill-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:16px;}
.skill-card{border:1px solid var(--line);border-radius:var(--radius);padding:20px;background:rgba(18,37,66,0.3);}
.skill-card h4{font-size:0.95rem;margin-bottom:12px;display:flex;align-items:center;gap:8px;color:var(--ink);}
.skill-card h4 .sw{width:6px;height:6px;background:var(--line-bright);border-radius:1px;transform:rotate(45deg);display:inline-block;}
.tagset{display:flex;flex-wrap:wrap;gap:6px;}
.tag{
  font-family:var(--mono);font-size:0.7rem;color:var(--ink-soft);
  border:1px solid var(--line);padding:4px 10px;border-radius:20px;
}

/* ---------- Experience timeline ---------- */
.timeline{position:relative;padding-left:32px;}
.timeline::before{content:"";position:absolute;left:5px;top:6px;bottom:6px;width:1px;background:var(--line);}
.tl-item{position:relative;padding-bottom:44px;}
.tl-item:last-child{padding-bottom:0;}
.tl-item::before{
  content:"";position:absolute;left:-32px;top:4px;width:11px;height:11px;border-radius:50%;
  background:var(--paper);border:2px solid var(--line-bright);
}
.tl-head{display:flex;flex-wrap:wrap;justify-content:space-between;gap:8px;align-items:baseline;margin-bottom:6px;}
.tl-role{font-family:var(--display);font-size:1.15rem;color:var(--ink);}
.tl-date{font-family:var(--mono);font-size:0.72rem;color:var(--amber);text-transform:uppercase;letter-spacing:0.04em;}
.tl-org{color:var(--line-bright);font-size:0.9rem;margin-bottom:10px;}
.tl-item ul{color:var(--ink-soft);font-size:0.92rem;list-style:none;}
.tl-item li{padding-left:18px;position:relative;margin-bottom:6px;}
.tl-item li::before{content:"›";position:absolute;left:0;color:var(--line-bright);}

/* ---------- Projects ---------- */
.proj-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(300px,1fr));gap:22px;}
.proj-card{border:1px solid var(--line);border-radius:var(--radius);background:rgba(18,37,66,0.35);overflow:hidden;display:flex;flex-direction:column;transition:.2s;}
.proj-card:hover{border-color:var(--line-bright);transform:translateY(-3px);}
.proj-top{padding:24px 24px 0;flex:1;}
.proj-top h3{font-size:1.12rem;margin-bottom:8px;}
.proj-top p{color:var(--ink-soft);font-size:0.9rem;margin-bottom:14px;}
.proj-tags{display:flex;flex-wrap:wrap;gap:6px;margin-bottom:20px;}
.proj-foot{
  font-family:var(--mono);font-size:0.68rem;text-transform:uppercase;letter-spacing:0.03em;
  display:grid;grid-template-columns:1fr 1fr;border-top:1px solid var(--line);
}
.proj-foot div{padding:10px 24px;border-left:1px solid var(--line);}
.proj-foot div:first-child{border-left:none;}
.proj-foot dt{color:var(--ink-soft);}
.proj-foot dd{color:var(--ink);margin-top:2px;}

/* ---------- Case study ---------- */
.case{
  border:1px solid var(--line-bright);
  border-radius:18px;
  padding:44px;
  background:linear-gradient(160deg,rgba(63,169,232,0.08),rgba(18,37,66,0.5));
  position:relative;
}
.case::before, .case::after{
  content:"";position:absolute;width:14px;height:14px;border:1px solid var(--line-bright);opacity:0.6;
}
.case::before{top:14px;left:14px;border-right:none;border-bottom:none;}
.case::after{bottom:14px;right:14px;border-left:none;border-top:none;}
.case-head{display:flex;flex-wrap:wrap;justify-content:space-between;gap:20px;margin-bottom:28px;}
.case-head h3{font-size:1.6rem;max-width:520px;}
.case-badge{font-family:var(--mono);font-size:0.7rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--amber);border:1px solid var(--amber);border-radius:30px;padding:6px 14px;height:fit-content;}
.case-cols{display:grid;grid-template-columns:1fr 1fr;gap:36px;margin-top:32px;}
.case-cols h4{font-size:0.85rem;text-transform:uppercase;letter-spacing:0.06em;color:var(--line-bright);font-family:var(--mono);margin-bottom:14px;}
.pillar-list{list-style:none;}
.pillar-list li{padding:10px 0;border-bottom:1px solid var(--line);font-size:0.9rem;color:var(--ink-soft);display:flex;justify-content:space-between;gap:10px;}
.pillar-list li:last-child{border-bottom:none;}
.pillar-list b{color:var(--ink);font-weight:500;}
.req-tag{font-family:var(--mono);font-size:0.62rem;text-transform:uppercase;padding:2px 8px;border-radius:10px;white-space:nowrap;height:fit-content;}
.req-mandatory{background:rgba(232,163,63,0.14);color:var(--amber);border:1px solid rgba(232,163,63,0.4);}
.req-optional{background:rgba(147,168,196,0.1);color:var(--ink-soft);border:1px solid var(--line);}

/* ---------- Education ---------- */
.edu-grid{display:grid;grid-template-columns:1fr 1fr;gap:22px;}
.edu-card{border:1px solid var(--line);border-radius:var(--radius);padding:24px;background:rgba(18,37,66,0.3);}
.edu-card .k{font-family:var(--mono);font-size:0.68rem;color:var(--line-bright);text-transform:uppercase;letter-spacing:0.06em;margin-bottom:8px;}
.edu-card h4{font-size:1.02rem;margin-bottom:4px;}
.edu-card .org{color:var(--ink-soft);font-size:0.86rem;margin-bottom:10px;}
.edu-card .date{font-family:var(--mono);font-size:0.72rem;color:var(--amber);}

/* ---------- Referees ---------- */
.ref-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(240px,1fr));gap:20px;}
.ref-card{border:1px solid var(--line);border-radius:var(--radius);padding:22px;background:rgba(18,37,66,0.3);}
.ref-card h4{font-size:1rem;margin-bottom:4px;}
.ref-card .role{color:var(--line-bright);font-size:0.82rem;margin-bottom:10px;}
.ref-card .org{color:var(--ink-soft);font-size:0.82rem;}
.ref-note{font-family:var(--mono);font-size:0.78rem;color:var(--ink-soft);margin-top:28px;}

/* ---------- Footer / contact ---------- */
.contact{text-align:center;}
.contact h2{font-size:clamp(2rem,5vw,3rem);max-width:700px;margin:0 auto 20px;}
.contact p{color:var(--ink-soft);max-width:520px;margin:0 auto 36px;}
.contact-links{display:flex;justify-content:center;gap:16px;flex-wrap:wrap;margin-bottom:56px;}
footer{border-top:1px solid var(--line);padding:32px 0;}
.foot-inner{display:flex;flex-wrap:wrap;justify-content:space-between;gap:16px;font-family:var(--mono);font-size:0.75rem;color:var(--ink-soft);}
.foot-inner a{color:var(--ink-soft);text-decoration:none;}
.foot-inner a:hover{color:var(--line-bright);}

/* ---------- Reveal animation ---------- */
.reveal{opacity:0;transform:translateY(18px);transition:opacity .6s ease, transform .6s ease;}
.reveal.in{opacity:1;transform:translateY(0);}

/* ---------- Responsive ---------- */
@media (max-width:860px){
  .hero-grid{grid-template-columns:1fr;}
  .schema{max-width:420px;margin:0 auto;}
  .about-grid{grid-template-columns:1fr;}
  .case-cols{grid-template-columns:1fr;}
  .edu-grid{grid-template-columns:1fr;}
}
@media (max-width:720px){
  .nav-links, .nav-cta{display:none;}
  .nav-toggle{display:block;}
  .nav.open .nav-links{
    display:flex;flex-direction:column;position:absolute;top:100%;left:0;right:0;
    background:var(--paper-alt);padding:20px 24px;border-bottom:1px solid var(--line);gap:16px;
  }
  .nav.open .nav-cta{display:inline-flex;margin-top:4px;}
  section{padding:64px 0;}
}
</style>
</head>
<body>

<nav class="nav" id="nav">
  <div class="nav-inner">
    <div class="nav-brand"><span class="dot"></span> BRIAN MUCHERE</div>
    <ul class="nav-links">
      <li><a href="#about">About</a></li>
      <li><a href="#services">Services</a></li>
      <li><a href="#skills">Skills</a></li>
      <li><a href="#experience">Experience</a></li>
      <li><a href="#work">Work</a></li>
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
        <p class="lead reveal in">I'm Brian Muchere, a Nairobi-based Full-Stack Software Engineer and Technology Solutions Specialist with 5+ years of 
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
        <div><dt>Core stack</dt><dd>Python · PHP · React · ML</dd></div>
      </dl>
    </div>
    <div class="schema reveal in" aria-hidden="true">
      <svg viewBox="0 0 400 400">
        <path class="schema-path" d="M200 200 L90 90"/>
        <path class="schema-path" d="M200 200 L310 90"/>
        <path class="schema-path" d="M200 200 L90 310"/>
        <path class="schema-path" d="M200 200 L310 310"/>
        <path class="schema-path" d="M200 200 L200 60"/>
        <path class="schema-path schema-pulse" d="M200 200 L90 90"/>
        <path class="schema-path schema-pulse" d="M200 200 L310 310"/>
        <path class="schema-path schema-pulse" d="M200 200 L200 60"/>
        <g class="schema-node core"><rect x="160" y="172" width="80" height="56" rx="8"/><text x="200" y="196" text-anchor="middle">ERP /</text><text x="200" y="210" text-anchor="middle">CORE API</text></g>
        <g class="schema-node"><rect x="50" y="62" width="80" height="46" rx="8"/><text x="90" y="82" text-anchor="middle">PENSION</text><text x="90" y="94" text-anchor="middle">PORTAL</text></g>
        <g class="schema-node"><rect x="270" y="62" width="80" height="46" rx="8"/><text x="310" y="82" text-anchor="middle">HR &amp;</text><text x="310" y="94" text-anchor="middle">PAYROLL</text></g>
        <g class="schema-node"><rect x="50" y="288" width="80" height="46" rx="8"/><text x="90" y="308" text-anchor="middle">PROCURE-</text><text x="90" y="320" text-anchor="middle">MENT</text></g>
        <g class="schema-node"><rect x="270" y="288" width="80" height="46" rx="8"/><text x="310" y="308" text-anchor="middle">LIVENESS /</text><text x="310" y="320" text-anchor="middle">BIOMETRIC</text></g>
        <g class="schema-node"><rect x="160" y="20" width="80" height="42" rx="8"/><text x="200" y="38" text-anchor="middle">ANALYTICS</text><text x="200" y="50" text-anchor="middle">/ ML</text></g>
      </svg>
    </div>
  </div>
</section>

<!-- ABOUT -->
<section id="about" class="wrap">
  <div class="eyebrow reveal">About</div>
  <div class="about-grid">
    <div class="reveal">
      <h2 class="section-title">I connect the systems institutions run on.</h2>
      <p>Results-driven full-stack developer with 5+ years building scalable web applications, REST APIs and enterprise platforms with Python, Django, React, JavaScript, TypeScript and Firebase — plus Laravel and Vue on the PHP side. Most of that work sits inside HR, pension, recruitment and procurement systems for enterprise clients, so I'm used to messy integration requirements, audit trails, and the kind of edge cases that only show up once real money and real people are on the line.</p>
      <p>Outside the core stack I bring machine learning into products where it earns its place — predictive analytics, NLP and anomaly detection with scikit-learn, TensorFlow and PyTorch — and a networking background (CCNA, structured LAN builds, core-banking systems like T24) that makes me comfortable owning a project end-to-end, from the server room to the browser.</p>
      <p>That networking side extends into ISP-style connectivity work too — internet and Wi-Fi installation, fiber and wireless setup, router/access-point configuration, and network maintenance for homes, offices, schools and organizations that just need reliable connectivity in place.</p>
    </div>
    <div class="stat-list reveal">
      <div class="stat-card"><div class="num">5+</div><div class="lbl">Years shipping production systems</div></div>
      <div class="stat-card"><div class="num">8+</div><div class="lbl">Enterprise platforms delivered</div></div>
      <div class="stat-card"><div class="num">4</div><div class="lbl">Domains: pension, HR, procurement, recruitment</div></div>
      <div class="stat-card"><div class="num">2</div><div class="lbl">Full stacks fluent: Python/Django &amp; PHP/Laravel</div></div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section id="services" class="wrap">
  <div class="eyebrow reveal">Freelance services</div>
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
<section id="skills" class="wrap">
  <div class="eyebrow reveal">Technical skills</div>
  <h2 class="section-title reveal">The stack, in full</h2>
  <p class="section-sub reveal">Backend-first, comfortable across two full-stack ecosystems, and equipped to add ML where it's genuinely useful.</p>
  <div class="skill-grid">
    <div class="skill-card reveal"><h4><span class="sw"></span>Backend &amp; frameworks</h4><div class="tagset"><span class="tag">Python</span><span class="tag">Django</span><span class="tag">Flask</span><span class="tag">FastAPI</span><span class="tag">PHP</span><span class="tag">Laravel</span><span class="tag">Node.js</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Frontend</h4><div class="tagset"><span class="tag">React</span><span class="tag">Redux</span><span class="tag">Vue.js</span><span class="tag">TypeScript</span><span class="tag">Ant Design</span><span class="tag">Tailwind</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Data &amp; databases</h4><div class="tagset"><span class="tag">PostgreSQL</span><span class="tag">MySQL</span><span class="tag">SQL Server</span><span class="tag">SQLAlchemy</span><span class="tag">Advanced SQL</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Machine learning</h4><div class="tagset"><span class="tag">scikit-learn</span><span class="tag">TensorFlow</span><span class="tag">PyTorch</span><span class="tag">spaCy</span><span class="tag">NLP</span><span class="tag">Anomaly detection</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>DevOps &amp; cloud</h4><div class="tagset"><span class="tag">Docker</span><span class="tag">Git / CI-CD</span><span class="tag">HCIA Cloud</span><span class="tag">Deployment troubleshooting</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Networking</h4><div class="tagset"><span class="tag">CCNA</span><span class="tag">Cisco / D-Link</span><span class="tag">LAN design</span><span class="tag">T24 core banking</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Testing</h4><div class="tagset"><span class="tag">pytest</span><span class="tag">Jest</span></div></div>
    <div class="skill-card reveal"><h4><span class="sw"></span>Domain expertise</h4><div class="tagset"><span class="tag">AML / KYC / CFT</span><span class="tag">Pension systems</span><span class="tag">Asset management</span><span class="tag">API integration</span></div></div>
  </div>
</section>

<!-- EXPERIENCE -->
<section id="experience" class="wrap">
  <div class="eyebrow reveal">Experience</div>
  <h2 class="section-title reveal">Where the stack got built</h2>
  <div class="timeline">
    <div class="tl-item reveal">
      <div class="tl-head"><span class="tl-role">Full-Stack Software Developer</span><span class="tl-date">Jan 2024 — Present</span></div>
      <div class="tl-org">Deft Technologies Ltd · Nairobi, Kenya</div>
      <ul>
        <li>Designed and built enterprise platforms with Django, Laravel, Vue.js and React — including pension, procurement and recruitment portals.</li>
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
<section id="work" class="wrap">
  <div class="eyebrow reveal">Selected work</div>
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
        <div class="proj-tags"><span class="tag">Laravel</span><span class="tag">Vue.js</span><span class="tag">MySQL</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI · KQ PF</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Provident Fund E-Procurement Portal</h3>
        <p>Supplier management, approvals, requisitions, tender management and reporting dashboards for two institutional clients.</p>
        <div class="proj-tags"><span class="tag">Laravel</span><span class="tag">Vue.js</span><span class="tag">REST API</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI · KQ PF</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Employee Self-Service (ESS) Portal</h3>
        <p>Leave management, appraisals, profile management and secure payslip access for staff.</p>
        <div class="proj-tags"><span class="tag">Django</span><span class="tag">React</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>AKI</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>Pension Management System</h3>
        <p>Contribution tracking, claims processing, benefits management and reporting for a licensed insurance broker.</p>
        <div class="proj-tags"><span class="tag">Laravel</span><span class="tag">Vue.js</span><span class="tag">MySQL</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>QIJITO Insurance Brokers</dd></div><div><dt>Role</dt><dd>Full-stack dev</dd></div></dl>
    </div>

    <div class="proj-card reveal">
      <div class="proj-top">
        <h3>ICT Asset Management &amp; LAN IP Sniffing</h3>
        <p>Asset inventory system plus a network tool for identifying and tracking devices on the LAN.</p>
        <div class="proj-tags"><span class="tag">C# / .NET</span><span class="tag">Python</span><span class="tag">SQL Server</span></div>
      </div>
      <dl class="proj-foot"><div><dt>Client</dt><dd>Kenya Revenue Authority</dd></div><div><dt>Role</dt><dd>Contributor</dd></div></dl>
    </div>

  </div>
</section>

<!-- CASE STUDY -->
<section id="case-study" class="wrap">
  <div class="eyebrow reveal">Case study</div>
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
<section id="credentials" class="wrap">
  <div class="eyebrow reveal">Credentials</div>
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
<section id="referees" class="wrap">
  <div class="eyebrow reveal">References</div>
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
<section id="contact" class="wrap contact">
  <div class="eyebrow reveal" style="justify-content:center;">Get in touch</div>
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