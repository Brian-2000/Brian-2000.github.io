<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brian Muchere – Full‑Stack Python Developer</title>
    <style>
        /* embedded styles – work safely inside README.md */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
            background: #f0f5fa;
            color: #1c2e3f;
            line-height: 1.5;
            padding: 2rem 1rem;
        }
        .readme-container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 2rem;
            box-shadow: 0 20px 30px -10px rgba(0, 40, 60, 0.2);
            padding: 2.5rem 2rem;
        }
        h1 {
            font-size: 2.8rem;
            font-weight: 700;
            color: #0b3043;
            letter-spacing: -0.02em;
        }
        .subhead {
            font-size: 1.3rem;
            color: #2b5a7a;
            margin: 0.2rem 0 1.5rem;
            font-weight: 400;
        }
        .contact-bar {
            background: #e9f0f7;
            border-radius: 3rem;
            padding: 1rem 2rem;
            display: flex;
            flex-wrap: wrap;
            gap: 1.8rem 2.2rem;
            margin: 1.5rem 0 2rem;
            font-size: 1rem;
        }
        .contact-item {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #173e56;
        }
        .contact-item a {
            color: #1a4b6b;
            text-decoration: none;
            border-bottom: 1px dotted #8ab3cf;
        }
        .contact-item a:hover { border-bottom-color: #0a3142; }
        .summary-card {
            background: #eef4fc;
            border-left: 6px solid #1f6a94;
            border-radius: 2rem;
            padding: 1.8rem 2.2rem;
            margin: 2rem 0;
            font-size: 1.05rem;
            box-shadow: inset 0 2px 5px rgba(0,0,0,0.02);
        }
        h2 {
            font-size: 2rem;
            font-weight: 600;
            border-bottom: 4px solid #cde1ef;
            padding-bottom: 0.4rem;
            margin: 2.5rem 0 1.5rem;
            color: #0b3e57;
        }
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }
        .skill-card {
            background: #f7fafd;
            border-radius: 1.8rem;
            padding: 1.4rem 1.5rem;
            border: 1px solid #d5e4f0;
        }
        .skill-card h4 {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            color: #124b6b;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }
        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
        }
        .skill-tag {
            background: white;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            font-size: 0.9rem;
            border: 1px solid #b9d3e9;
            color: #103e57;
        }
        .exp-card {
            background: white;
            border: 1px solid #d0e0ec;
            border-radius: 2rem;
            padding: 1.8rem 2rem;
            margin-bottom: 1.8rem;
            box-shadow: 0 6px 14px rgba(0, 35, 50, 0.05);
        }
        .exp-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
        }
        .exp-title {
            font-size: 1.4rem;
            font-weight: 650;
            color: #0c3b52;
        }
        .exp-company {
            color: #2b6c95;
            font-weight: 500;
            margin: 0.2rem 0 0.8rem;
        }
        .exp-date {
            background: #dcebf7;
            padding: 0.3rem 1rem;
            border-radius: 30px;
            font-size: 0.9rem;
        }
        .exp-desc ul {
            list-style: none;
            margin-top: 0.8rem;
        }
        .exp-desc li {
            display: flex;
            gap: 0.8rem;
            margin-bottom: 0.6rem;
        }
        .edu-cert-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
            margin: 1.5rem 0;
        }
        .edu-item, .cert-item {
            background: #f3f9ff;
            border-radius: 1.5rem;
            padding: 1.5rem;
            border-left: 4px solid #2e7baf;
        }
        .badge {
            background: #d1e3f5;
            display: inline-block;
            padding: 0.2rem 0.9rem;
            border-radius: 30px;
            font-size: 0.85rem;
            margin-top: 0.6rem;
        }
        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
            gap: 1.5rem;
            margin: 1.5rem 0;
        }
        .project-card {
            background: #f5faff;
            border-radius: 1.8rem;
            padding: 1.5rem;
            border: 1px solid #c9ddec;
        }
        .project-name {
            font-size: 1.3rem;
            font-weight: 650;
            color: #0d4260;
        }
        .project-client {
            color: #3a6d8f;
            margin-bottom: 0.4rem;
        }
        .referee-list {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            margin: 2rem 0;
        }
        .referee-card {
            background: #f0f7fe;
            flex: 1 1 220px;
            border-radius: 2rem;
            padding: 1.5rem;
            border: 1px solid #c1d9ed;
        }
        .referee-name {
            font-weight: 700;
            font-size: 1.2rem;
            color: #0b3c57;
        }
        .referee-title {
            color: #2a6182;
            margin: 0.3rem 0 0.8rem;
        }
        hr {
            border: none;
            height: 2px;
            background: linear-gradient(to right, #c9ddec, transparent);
            margin: 2rem 0 0.5rem;
        }
        .footer-note {
            text-align: center;
            color: #5e7e99;
            font-size: 0.95rem;
            margin-top: 2rem;
        }
        @media (max-width: 600px) {
            h1 { font-size: 2.2rem; }
            .contact-bar { flex-direction: column; gap: 0.8rem; }
            .edu-cert-row { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
<div class="readme-container">

    <!-- header -->
    <h1>BRIAN MUCHERE</h1>
    <div class="subhead">Full‑Stack Python & Web Developer · Business Intelligence & AI</div>

    <div class="contact-bar">
        <span class="contact-item">📍 P.O Box 783-50102, Mumias</span>
        <span class="contact-item">📞 +254 799 737828</span>
        <span class="contact-item">✉️ <a href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a></span>
        <span class="contact-item">🔗 <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank">linkedin.com/in/brian-muchere</a></span>
        <span class="contact-item">🐙 <a href="https://github.com/Brian-2000/" target="_blank">github.com/Brian-2000</a></span>
    </div>

    <!-- summary -->
    <div class="summary-card">
        <strong>🎯 Career Profile Summary</strong><br>
        Results-driven Full-Stack Python & Web Developer with over 5 years of proven expertise in architecting, developing, and deploying enterprise-grade business intelligence and data analytics solutions. Skilled in designing scalable RESTful APIs with Python (Django, Flask, FastAPI), implementing asynchronous workflows with Celery, and engineering AI-driven pipelines for predictive analytics, NLP, and anomaly detection. Strong front-end development experience with React, Redux, Ant Design, Vuejs, styled-components, and LESS, delivering responsive, user-centric interfaces. Proficient in SQL, SQLAlchemy, and advanced database engineering, including secure credential management and optimized connection pooling. Experienced in Docker-based deployments, DevOps practices, and troubleshooting complex production environments. Adept at building comprehensive test suites (pytest, Jest) to ensure reliability and scalability. Passionate about transforming business needs into robust, maintainable technical solutions through cross-functional collaboration in agile environments.
    </div>

    <!-- skills (grouped) -->
    <h2>⚙️ Core technical skills</h2>
    <div class="skills-grid">
        <div class="skill-card"><h4>💻 Languages & frameworks</h4><div class="skill-tags"><span class="skill-tag">Python</span><span class="skill-tag">Django</span><span class="skill-tag">Flask</span><span class="skill-tag">FastAPI</span><span class="skill-tag">Laravel</span><span class="skill-tag">Vue.js</span><span class="skill-tag">JavaScript</span><span class="skill-tag">PHP</span></div></div>
        <div class="skill-card"><h4>🗄️ SQL & ORM</h4><div class="skill-tags"><span class="skill-tag">Advanced SQL</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">PostgreSQL</span><span class="skill-tag">MySQL</span><span class="skill-tag">Enterprise DB</span></div></div>
        <div class="skill-card"><h4>☁️ DevOps & cloud</h4><div class="skill-tags"><span class="skill-tag">Docker</span><span class="skill-tag">CI/CD</span><span class="skill-tag">Git/GitHub</span><span class="skill-tag">HCIA Cloud</span><span class="skill-tag">Preventive maint.</span></div></div>
        <div class="skill-card"><h4>🤖 AI / ML</h4><div class="skill-tags"><span class="skill-tag">Predictive analytics</span><span class="skill-tag">NLP (spaCy)</span><span class="skill-tag">Anomaly detection</span><span class="skill-tag">scikit-learn</span><span class="skill-tag">TensorFlow</span><span class="skill-tag">PyTorch</span></div></div>
        <div class="skill-card"><h4>🎨 Frontend & UI</h4><div class="skill-tags"><span class="skill-tag">React</span><span class="skill-tag">Redux</span><span class="skill-tag">Ant Design</span><span class="skill-tag">Vue.js</span><span class="skill-tag">styled-components</span><span class="skill-tag">LESS</span><span class="skill-tag">FluentUI</span></div></div>
        <div class="skill-card"><h4>🌐 Networking & systems</h4><div class="skill-tags"><span class="skill-tag">CCNA</span><span class="skill-tag">CISCO/D-LINK</span><span class="skill-tag">LAN setup</span><span class="skill-tag">T24 Core Banking</span><span class="skill-tag">NagVis</span></div></div>
        <div class="skill-card"><h4>🔐 Specialised & compliance</h4><div class="skill-tags"><span class="skill-tag">AML/KYC/CFT</span><span class="skill-tag">API integration</span><span class="skill-tag">Asset management</span><span class="skill-tag">Connection pooling</span></div></div>
        <div class="skill-card"><h4>🧪 Testing & practices</h4><div class="skill-tags"><span class="skill-tag">pytest</span><span class="skill-tag">Jest</span><span class="skill-tag">performance opt.</span><span class="skill-tag">documentation</span><span class="skill-tag">agile</span></div></div>
        <div class="skill-card"><h4>🤝 Soft skills</h4><div class="skill-tags"><span class="skill-tag">Analytical thinking</span><span class="skill-tag">teamwork</span><span class="skill-tag">adaptability</span><span class="skill-tag">reporting</span><span class="skill-tag">mentoring</span></div></div>
    </div>

    <!-- experience -->
    <h2>💼 Work experience</h2>
    <div class="exp-card">
        <div class="exp-header"><span class="exp-title">Full‑Stack Software Developer</span><span class="exp-date">Jan 2024 – Present</span></div>
        <div class="exp-company">Deft Technologies Ltd · Nairobi</div>
        <div class="exp-desc"><ul><li>🔹 Designed/delivered enterprise insurance systems: ESS Portal (AKI), Pension Management (QIJITO), Deft website, EDMS.</li><li>🔹 Full‑stack with Django, Laravel, Vue.js, UI/UX, DB architecture, testing, deployment.</li><li>🔹 Integrated third‑party APIs, built enterprise data exchange across HR, procurement, finance.</li><li>🔹 Innovation lead – automated internal processes, active in agile sprints & client analysis.</li></ul></div>
    </div>
    <div class="exp-card">
        <div class="exp-header"><span class="exp-title">Technical Support Intern (Presidential Digitalent)</span><span class="exp-date">Dec 2022 – Dec 2023</span></div>
        <div class="exp-company">Kenya Revenue Authority (KRA)</div>
        <div class="exp-desc"><ul><li>🔹 Installed/configures KRA software, provided ICT support, preventive maintenance.</li><li>🔹 Co‑developed ICT Asset Management & Inventory System and LAN IP Sniffing System.</li><li>🔹 Monitored KRA Western Region Network (NagVis), configured routers/switches, LAN & cabling.</li></ul></div>
    </div>
    <div class="exp-card">
        <div class="exp-header"><span class="exp-title">Computer Studies Instructor</span><span class="exp-date">May 2022 – Aug 2022</span></div>
        <div class="exp-company">Royal Computer School</div>
        <div class="exp-desc"><ul><li>🔹 Designed lesson plans, practical training, group sessions & ICT troubleshooting.</li></ul></div>
    </div>
    <div class="exp-card">
        <div class="exp-header"><span class="exp-title">Business Development & Social Media Intern</span><span class="exp-date">Dec 2021 – Jan 2022</span></div>
        <div class="exp-company">Funder Holdings</div>
        <div class="exp-desc"><ul><li>🔹 Managed social media, content calendar, market research & growth strategies.</li></ul></div>
    </div>

    <!-- education & certifications -->
    <h2>📚 Education & certifications</h2>
    <div class="edu-cert-row">
        <div>
            <div class="edu-item"><strong>🎓 B.Sc. Computer Science</strong> – University of Eldoret (Aug 2017 – Aug 2021) <br> Second Class Honours (Upper Division)</div>
            <div class="edu-item" style="margin-top:1rem;"><strong>🏫 K.C.S.E (B+)</strong> Kamashia Secondary School, 2013–2016</div>
            <div class="edu-item" style="margin-top:1rem;"><strong>📖 K.C.P.E (374 marks)</strong> Ebubole Primary, 2005–2012</div>
        </div>
        <div>
            <div class="cert-item"><strong>Cisco CCNA</strong> · Cisco Networking Academy <span class="badge">Jan–May 2023</span></div>
            <div class="cert-item"><strong>HCIA Cloud Computing & Data Storage</strong> · PDTP & HUAWEI <span class="badge">Mar–May 2023</span></div>
            <div class="cert-item"><strong>Google Coursera – Automation with Python</strong> <span class="badge">Apr–Jul 2023</span></div>
            <div class="cert-item"><strong>HARVARD EDX – CS50's Web Programming (Python/JS)</strong> <span class="badge">Jan–Aug 2023</span></div>
        </div>
    </div>

    <!-- projects -->
    <h2>🚀 Projects portfolio</h2>
    <div class="project-grid">
        <div class="project-card"><span class="project-name">ESS Portal – AKI</span> <span class="project-client">2025</span><div>Profile, leave, appraisal, payslip access. Full‑stack dev, deployment, training.</div></div>
        <div class="project-card"><span class="project-name">Pension System – QIJITO</span> <span class="project-client">2024</span><div>Contributions, statements, claims. Architecture, reporting, client support.</div></div>
        <div class="project-card"><span class="project-name">Deft Technologies website</span> <span class="project-client">2024</span><div>Corporate site, SEO optimization, design & deployment.</div></div>
        <div class="project-card"><span class="project-name">Online assignment help</span> <span class="project-client">2022</span><div>Student Saviors, Xpedia Assignment Help – full lifecycle.</div></div>
        <div class="project-card"><span class="project-name">ICT Asset Management</span> <span class="project-client">2023 (KRA)</span><div>Team development, asset tracking, inventory system.</div></div>
        <div class="project-card"><span class="project-name">LAN IP Sniffing System</span> <span class="project-client">2023</span><div>Collaborative tool for KRA network monitoring.</div></div>
    </div>

    <!-- referees -->
    <h2>📞 Referees</h2>
    <div class="referee-list">
        <div class="referee-card"><div class="referee-name">Fredrick Wabala</div><div class="referee-title">Pension Admin, Zamara Group</div><div>📞 +254713971765</div><div>✉️ <a href="mailto:Fwabala123@Gmail.Com">Fwabala123@Gmail.Com</a></div></div>
        <div class="referee-card"><div class="referee-name">Nelson Kinavuli</div><div class="referee-title">ICT Supervisor, KRA – Kisumu</div><div>📞 +254712887199</div><div>✉️ <a href="mailto:Nelson.kinavuli@kra.go.ke">Nelson.kinavuli@kra.go.ke</a></div></div>
        <div class="referee-card"><div class="referee-name">Kelvin Koome Mwiti</div><div class="referee-title">Manager, Deft Technologies</div><div>📞 +254701504693</div><div>✉️ <a href="mailto:Kelvin.mwiti@defttech.co.ke">Kelvin.mwiti@defttech.co.ke</a></div></div>
    </div>

    <hr>
    <div class="footer-note">✨ Brian Muchere · full‑stack developer · continuously building ✨</div>
</div>
<!-- 
  Place this entire HTML block into your README.md.
  For the best portfolio website, also create an index.html file with the same content.
-->
</body>
</html>
