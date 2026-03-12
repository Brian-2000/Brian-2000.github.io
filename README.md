<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Brian Muchere · Full‑Stack Python Developer</title>
  <!-- Google Font & Font Awesome -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300..700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: "Inter", sans-serif;
      background: #f4f7fb;
      color: #1a2639;
      line-height: 1.5;
      padding: 2rem 1rem;
    }

    .container {
      max-width: 1200px;
      margin: 0 auto;
      background: white;
      border-radius: 2rem;
      box-shadow: 0 20px 35px -8px rgba(0,20,30,0.15);
      overflow: hidden;
      padding: 2.5rem 2rem;
    }

    /* headings */
    h1 {
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: -0.02em;
      color: #0b2b40;
      line-height: 1.2;
    }

    h2 {
      font-size: 1.8rem;
      font-weight: 600;
      letter-spacing: -0.01em;
      border-bottom: 4px solid #e6f0fa;
      padding-bottom: 0.5rem;
      margin: 2.2rem 0 1.5rem 0;
      color: #0f3b4f;
    }

    h3 {
      font-size: 1.3rem;
      font-weight: 600;
      margin-bottom: 0.3rem;
      color: #1e4a6b;
    }

    .subhead {
      font-size: 1.2rem;
      font-weight: 400;
      color: #2f5e7a;
      margin-top: -0.2rem;
      margin-bottom: 1.2rem;
    }

    /* contact bar */
    .contact-bar {
      background: #eef4fa;
      padding: 1rem 1.5rem;
      border-radius: 60px;
      display: flex;
      flex-wrap: wrap;
      gap: 1.8rem 2.5rem;
      margin: 1.8rem 0 0.8rem 0;
      font-size: 0.98rem;
    }

    .contact-item {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      color: #1a3b4f;
    }

    .contact-item i {
      width: 1.3rem;
      color: #006a8e;
      font-size: 1.2rem;
    }

    .contact-item a {
      color: #1a3b4f;
      text-decoration: none;
      border-bottom: 1px dotted transparent;
      transition: 0.2s;
    }

    .contact-item a:hover {
      border-bottom-color: #006a8e;
      color: #006a8e;
    }

    /* summary card */
    .summary-card {
      background: #f0f6fd;
      padding: 1.6rem 2rem;
      border-radius: 2rem;
      margin: 2rem 0 1.5rem 0;
      font-size: 1.05rem;
      border-left: 6px solid #1e6f9f;
      box-shadow: 0 4px 8px rgba(0,40,60,0.05);
    }

    /* skills grid */
    .skills-section {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 1.5rem;
      margin-top: 1rem;
    }

    .skill-category {
      background: #f9fcff;
      border-radius: 1.5rem;
      padding: 1.4rem 1.4rem 1.6rem;
      border: 1px solid #dde9f2;
      transition: 0.15s;
    }

    .skill-category:hover {
      border-color: #9bc2db;
    }

    .skill-category h4 {
      font-size: 1.2rem;
      font-weight: 600;
      margin-bottom: 1rem;
      color: #114e6f;
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }

    .skill-category h4 i {
      color: #2c7fb8;
      font-size: 1.3rem;
    }

    .skill-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    .skill-tag {
      background: white;
      border-radius: 40px;
      padding: 0.3rem 1rem;
      font-size: 0.9rem;
      font-weight: 500;
      color: #133e57;
      border: 1px solid #c1d9eb;
      box-shadow: 0 1px 3px rgba(0,0,0,0.02);
    }

    /* experience & project cards */
    .exp-card, .project-card {
      background: #ffffff;
      border: 1px solid #dde5ed;
      border-radius: 1.8rem;
      padding: 1.8rem 2rem;
      margin-bottom: 1.8rem;
      box-shadow: 0 8px 18px -8px rgba(0,40,60,0.08);
    }

    .exp-header {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: baseline;
      margin-bottom: 0.8rem;
    }

    .exp-title {
      font-size: 1.4rem;
      font-weight: 650;
      color: #0b3e57;
    }

    .exp-company {
      font-weight: 600;
      color: #256f94;
    }

    .exp-date {
      background: #e1eff9;
      padding: 0.3rem 1rem;
      border-radius: 40px;
      font-size: 0.9rem;
      font-weight: 500;
    }

    .exp-desc {
      margin-top: 1rem;
      padding-left: 0.2rem;
    }

    .exp-desc ul {
      list-style: none;
    }

    .exp-desc li {
      margin-bottom: 0.6rem;
      display: flex;
      gap: 0.8rem;
    }

    .exp-desc li i {
      color: #006a8e;
      font-size: 0.9rem;
      margin-top: 0.25rem;
      width: 1.2rem;
    }

    /* two col for edu+cert */
    .edu-cert-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 2rem;
      margin: 1rem 0;
    }

    .edu-item, .cert-item {
      background: #f7fafd;
      border-radius: 1.5rem;
      padding: 1.5rem;
      border-left: 4px solid #4682b4;
    }

    .edu-item strong, .cert-item strong {
      color: #0b4d6b;
      font-weight: 650;
    }

    .date-badge {
      font-size: 0.9rem;
      background: #dbeafe;
      padding: 0.2rem 0.8rem;
      border-radius: 30px;
      display: inline-block;
      margin-top: 0.5rem;
    }

    /* projects grid */
    .project-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
      gap: 1.5rem;
    }

    .project-card {
      padding: 1.5rem;
      margin-bottom: 0;
      display: flex;
      flex-direction: column;
    }

    .project-name {
      font-size: 1.3rem;
      font-weight: 650;
      color: #0d4e70;
    }

    .project-client {
      font-weight: 500;
      color: #3c6f94;
      margin-bottom: 0.8rem;
    }

    .project-desc {
      margin-top: 0.5rem;
      color: #2a4050;
    }

    /* referees */
    .referee-list {
      display: flex;
      flex-wrap: wrap;
      gap: 2rem;
      margin: 2rem 0 1rem;
      justify-content: space-between;
    }

    .referee-card {
      background: #f3f9ff;
      flex: 1 1 220px;
      padding: 1.5rem;
      border-radius: 2rem;
      border: 1px solid #cee2f0;
    }

    .referee-name {
      font-weight: 700;
      font-size: 1.2rem;
      color: #103f58;
    }

    .referee-title {
      font-size: 0.95rem;
      color: #336688;
      margin: 0.3rem 0 0.6rem;
    }

    .referee-contact {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      font-size: 0.95rem;
    }

    .referee-contact i {
      color: #006a8e;
      width: 1.2rem;
    }

    .referee-contact a {
      color: #1a4d6b;
      text-decoration: none;
    }

    .referee-contact a:hover {
      text-decoration: underline;
    }

    hr {
      border: none;
      height: 2px;
      background: linear-gradient(to right, #c3ddec, transparent);
      margin: 2rem 0 0.5rem;
    }

    .footer-note {
      text-align: center;
      font-size: 0.9rem;
      color: #6f8fa5;
      margin-top: 2.2rem;
    }

    @media (max-width: 650px) {
      h1 { font-size: 2.2rem; }
      .container { padding: 1.5rem; }
      .contact-bar { flex-direction: column; gap: 0.8rem; }
      .edu-cert-grid { grid-template-columns: 1fr; }
      .referee-list { flex-direction: column; }
    }
  </style>
</head>
<body>
<div class="container">
  
  <!-- HEADER -->
  <h1>BRIAN MUCHERE</h1>
  <div class="subhead">Full‑Stack Python & Web Developer · Business Intelligence & AI</div>
  
  <div class="contact-bar">
    <span class="contact-item"><i class="fas fa-map-marker-alt"></i> P.O Box 783-50102, Mumias</span>
    <span class="contact-item"><i class="fas fa-phone-alt"></i> +254 799 737828</span>
    <span class="contact-item"><i class="fas fa-envelope"></i> <a href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a></span>
    <span class="contact-item"><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank">brian-muchere</a></span>
    <span class="contact-item"><i class="fab fa-github"></i> <a href="https://github.com/Brian-2000/" target="_blank">Brian-2000</a></span>
  </div>

  <!-- SUMMARY -->
  <div class="summary-card">
    <i class="fas fa-bullseye" style="color: #1e6f9f; margin-right: 0.5rem;"></i>
    Results-driven Full-Stack Python & Web Developer with over 5 years of proven expertise in architecting, developing, and deploying enterprise-grade business intelligence and data analytics solutions. Skilled in designing scalable RESTful APIs with Python (Django, Flask, FastAPI), implementing asynchronous workflows with Celery, and engineering AI-driven pipelines for predictive analytics, NLP, and anomaly detection. Strong front-end development experience with React, Redux, Ant Design, Vuejs, styled-components, and LESS, delivering responsive, user-centric interfaces. Proficient in SQL, SQLAlchemy, and advanced database engineering, including secure credential management and optimized connection pooling. Experienced in Docker-based deployments, DevOps practices, and troubleshooting complex production environments. Adept at building comprehensive test suites (pytest, Jest) to ensure reliability and scalability. Passionate about transforming business needs into robust, maintainable technical solutions through cross-functional collaboration in agile environments.
  </div>

  <!-- CORE SKILLS (grouped) -->
  <h2>⚙️ Core technical skills</h2>
  <div class="skills-section">
    <div class="skill-category"><h4><i class="fas fa-code"></i> Languages & frameworks</h4><div class="skill-tags"><span class="skill-tag">Python</span><span class="skill-tag">Django</span><span class="skill-tag">Flask</span><span class="skill-tag">FastAPI</span><span class="skill-tag">Laravel</span><span class="skill-tag">Vue.js</span><span class="skill-tag">JavaScript</span><span class="skill-tag">PHP</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-database"></i> SQL & ORM</h4><div class="skill-tags"><span class="skill-tag">Advanced SQL</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">PostgreSQL</span><span class="skill-tag">MySQL</span><span class="skill-tag">Enterprise DB</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-cloud"></i> DevOps & cloud</h4><div class="skill-tags"><span class="skill-tag">Docker</span><span class="skill-tag">K8s (basics)</span><span class="skill-tag">CI/CD</span><span class="skill-tag">Git/GitHub</span><span class="skill-tag">HCIA Cloud</span><span class="skill-tag">Preventive maint.</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-robot"></i> AI / ML</h4><div class="skill-tags"><span class="skill-tag">Predictive analytics</span><span class="skill-tag">NLP (spaCy)</span><span class="skill-tag">Anomaly detection</span><span class="skill-tag">scikit-learn</span><span class="skill-tag">TensorFlow</span><span class="skill-tag">PyTorch</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-laptop-code"></i> Frontend & UI</h4><div class="skill-tags"><span class="skill-tag">React</span><span class="skill-tag">Redux</span><span class="skill-tag">Ant Design</span><span class="skill-tag">Vue.js</span><span class="skill-tag">styled-components</span><span class="skill-tag">LESS</span><span class="skill-tag">FluentUI</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-network-wired"></i> Networking & systems</h4><div class="skill-tags"><span class="skill-tag">CCNA</span><span class="skill-tag">CISCO/D-LINK</span><span class="skill-tag">LAN setup</span><span class="skill-tag">T24 Core Banking</span><span class="skill-tag">NagVis</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-shield-alt"></i> Specialised & compliance</h4><div class="skill-tags"><span class="skill-tag">AML/KYC/CFT</span><span class="skill-tag">API integration</span><span class="skill-tag">Asset management</span><span class="skill-tag">Connection pooling</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-check-circle"></i> Testing & practices</h4><div class="skill-tags"><span class="skill-tag">pytest</span><span class="skill-tag">Jest</span><span class="skill-tag">performance opt.</span><span class="skill-tag">documentation</span><span class="skill-tag">agile</span></div></div>
    <div class="skill-category"><h4><i class="fas fa-users"></i> Soft skills</h4><div class="skill-tags"><span class="skill-tag">Analytical thinking</span><span class="skill-tag">teamwork</span><span class="skill-tag">adaptability</span><span class="skill-tag">reporting</span><span class="skill-tag">mentoring</span></div></div>
  </div>

  <!-- WORK EXPERIENCE -->
  <h2>💼 Experience</h2>
  <div class="exp-card">
    <div class="exp-header"><span class="exp-title">Full‑Stack Software Developer</span> <span class="exp-date">Jan 2024 – Present</span></div>
    <div class="exp-company">Deft Technologies Ltd · Nairobi</div>
    <div class="exp-desc"><ul>
      <li><i class="fas fa-caret-right"></i> Designed and delivered enterprise systems for insurance: ESS Portal (AKI), Pension Management (QIJITO), Deft corporate website, EDMS.</li>
      <li><i class="fas fa-caret-right"></i> Full‑stack development with Django, Laravel, Vue.js, UI/UX design, database architecture, testing & deployment.</li>
      <li><i class="fas fa-caret-right"></i> Integrated third‑party APIs and built enterprise data exchange across HR, procurement, finance.</li>
      <li><i class="fas fa-caret-right"></i> Innovation lead – automated internal processes, improved delivery efficiency. Active in agile sprints & client analysis.</li>
    </ul></div>
  </div>

  <div class="exp-card">
    <div class="exp-header"><span class="exp-title">Technical Support Intern (Presidential Digitalent)</span> <span class="exp-date">Dec 2022 – Dec 2023</span></div>
    <div class="exp-company">Kenya Revenue Authority (KRA)</div>
    <div class="exp-desc"><ul>
      <li><i class="fas fa-caret-right"></i> Installed/configures KRA software applications, provided ICT support, preventive maintenance.</li>
      <li><i class="fas fa-caret-right"></i> Collaborated to develop ICT Asset Management & Inventory System and LAN IP Sniffing System.</li>
      <li><i class="fas fa-caret-right"></i> Monitored KRA Western Region Network using NagVis; configured routers/switches (CISCO & D‑LINK), LAN & structured cabling.</li>
    </ul></div>
  </div>

  <div class="exp-card">
    <div class="exp-header"><span class="exp-title">Computer Studies Instructor</span> <span class="exp-date">May 2022 – Aug 2022</span></div>
    <div class="exp-company">Royal Computer School</div>
    <div class="exp-desc"><ul>
      <li><i class="fas fa-caret-right"></i> Designed lesson plans, instructional materials, practical training; group training sessions and ICT troubleshooting for staff.</li>
    </ul></div>
  </div>

  <div class="exp-card">
    <div class="exp-header"><span class="exp-title">Business Development & Social Media Intern</span> <span class="exp-date">Dec 2021 – Jan 2022</span></div>
    <div class="exp-company">Funder Holdings</div>
    <div class="exp-desc"><ul>
      <li><i class="fas fa-caret-right"></i> Managed corporate social media, content calendar, market research, and growth strategies.</li>
    </ul></div>
  </div>

  <!-- EDUCATION & CERTIFICATIONS (two columns) -->
  <h2>📚 Education & certifications</h2>
  <div class="edu-cert-grid">
    <div>
      <div class="edu-item"><strong>🎓 B.Sc. Computer Science</strong> – University of Eldoret <br> Aug 2017 – Aug 2021 · Second Class Honours (Upper Division)</div>
      <div class="edu-item" style="margin-top:1rem;"><strong>🏫 K.C.S.E (B+)</strong> Kamashia Secondary School, 2013–2016</div>
      <div class="edu-item" style="margin-top:1rem;"><strong>📖 K.C.P.E (374 marks)</strong> Ebubole Primary, 2005–2012</div>
    </div>
    <div>
      <div class="cert-item"><strong>Cisco CCNA</strong> · Cisco Networking Academy <span class="date-badge">Jan–May 2023</span></div>
      <div class="cert-item"><strong>HCIA Cloud Computing & Data Storage</strong> · PDTP & HUAWEI <span class="date-badge">Mar–May 2023</span></div>
      <div class="cert-item"><strong>Google Coursera – Automation with Python</strong> <span class="date-badge">Apr–Jul 2023</span></div>
      <div class="cert-item"><strong>HARVARD EDX – CS50's Web Programming (Python/JS)</strong> <span class="date-badge">Jan–Aug 2023</span></div>
    </div>
  </div>

  <!-- PROJECTS -->
  <h2>🚀 Projects portfolio</h2>
  <div class="project-grid">
    <div class="project-card"><span class="project-name">ESS Portal – AKI</span> <span class="project-client">2025</span><div class="project-desc">Profile, leave, appraisal, payslip access. Full‑stack dev, deployment, training.</div></div>
    <div class="project-card"><span class="project-name">Pension System – QIJITO</span> <span class="project-client">2024</span><div class="project-desc">Contributions, statements, claims management. Architecture, reporting, client support.</div></div>
    <div class="project-card"><span class="project-name">Deft Technologies website</span> <span class="project-client">2024</span><div class="project-desc">Corporate site, SEO optimization, web design & deployment.</div></div>
    <div class="project-card"><span class="project-name">Online assignment help</span> <span class="project-client">2022</span><div class="project-desc">Student Saviors, Xpedia Assignment Help – full lifecycle.</div></div>
    <div class="project-card"><span class="project-name">ICT Asset Management</span> <span class="project-client">2023 (KRA)</span><div class="project-desc">Team development, asset tracking, inventory system.</div></div>
    <div class="project-card"><span class="project-name">LAN IP Sniffing System</span> <span class="project-client">2023</span><div class="project-desc">Collaborative tool for KRA network monitoring.</div></div>
  </div>

  <!-- REFEREES -->
  <h2>📞 Referees</h2>
  <div class="referee-list">
    <div class="referee-card">
      <div class="referee-name">Fredrick Wabala</div>
      <div class="referee-title">Pension Administration & Consulting, Zamara Group</div>
      <div class="referee-contact"><i class="fas fa-phone-alt"></i> +254713971765</div>
      <div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Fwabala123@Gmail.Com">Fwabala123@Gmail.Com</a></div>
    </div>
    <div class="referee-card">
      <div class="referee-name">Nelson Kinavuli</div>
      <div class="referee-title">ICT Supervisor, KRA – Kisumu</div>
      <div class="referee-contact"><i class="fas fa-phone-alt"></i> +254712887199</div>
      <div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Nelson.kinavuli@kra.go.ke">Nelson.kinavuli@kra.go.ke</a></div>
    </div>
    <div class="referee-card">
      <div class="referee-name">Kelvin Koome Mwiti</div>
      <div class="referee-title">Manager, Deft Technologies</div>
      <div class="referee-contact"><i class="fas fa-phone-alt"></i> +254701504693</div>
      <div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Kelvin.mwiti@defttech.co.ke">Kelvin.mwiti@defttech.co.ke</a></div>
    </div>
  </div>

  <hr>
  <div class="footer-note">
    <i class="fas fa-sync-alt"></i> Brian Muchere · Full‑stack developer · continuously building
  </div>
</div>
<!-- simple note: replace content in your github.io repo with this index.html -->
</body>
</html>
