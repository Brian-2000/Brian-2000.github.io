<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Brian Muchere · full‑stack developer</title>
    <!-- Fonts, icons, smooth scroll -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:ital,opsz,wght@0,14..32,100..900;1,14..32,100..900&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: "Inter", sans-serif;
            background: #0c0f15;
            color: #eaeef2;
            line-height: 1.6;
        }

        /* dark theme variables */
        :root {
            --bg: #0c0f15;
            --surface: #161b22;
            --surface-light: #1e2630;
            --primary: #4f9eff;
            --primary-glow: #2b6bcb;
            --text: #eaeef2;
            --text-muted: #a0b3c9;
            --border: #2d3748;
        }

        /* navbar */
        .navbar {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(12, 15, 21, 0.85);
            backdrop-filter: blur(12px);
            -webkit-backdrop-filter: blur(12px);
            border-bottom: 1px solid rgba(79, 158, 255, 0.15);
            padding: 0.8rem 2rem;
            display: flex;
            flex-wrap: wrap;
            align-items: center;
            justify-content: space-between;
        }

        .logo a {
            font-weight: 700;
            font-size: 1.8rem;
            letter-spacing: -0.02em;
            background: linear-gradient(135deg, #a6c9ff, #4f9eff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: var(--text);
            text-decoration: none;
            font-weight: 500;
            font-size: 1rem;
            transition: 0.2s;
            border-bottom: 2px solid transparent;
            padding-bottom: 4px;
        }

        .nav-links a:hover {
            border-bottom-color: var(--primary);
            color: white;
        }

        /* main container */
        .container {
            max-width: 1300px;
            margin: 0 auto;
            padding: 2rem 2rem 3rem;
        }

        /* hero */
        .hero {
            margin: 3rem 0 4rem;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 700;
            background: linear-gradient(to right, #ffffff, #b3d9ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            letter-spacing: -0.02em;
            line-height: 1.1;
        }

        .hero-tagline {
            font-size: 1.4rem;
            color: var(--primary);
            margin: 0.5rem 0 1.2rem;
            font-weight: 400;
        }

        .quick-info {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
            background: var(--surface);
            padding: 1.2rem 2rem;
            border-radius: 60px;
            width: fit-content;
            border: 1px solid var(--border);
            margin: 1.8rem 0;
        }

        .quick-info span {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: var(--text-muted);
        }

        .quick-info i {
            color: var(--primary);
            width: 1.2rem;
        }

        .quick-info a {
            color: var(--text-muted);
            text-decoration: none;
            transition: 0.2s;
        }

        .quick-info a:hover {
            color: white;
        }

        /* section styling */
        section {
            scroll-margin-top: 80px;
            margin-bottom: 5rem;
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 2.5rem;
        }

        .section-header h2 {
            font-size: 2.4rem;
            font-weight: 600;
            background: linear-gradient(135deg, #f0f5fa, #b0d0ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-header i {
            font-size: 2rem;
            color: var(--primary);
            opacity: 0.8;
        }

        .line {
            flex: 1;
            height: 2px;
            background: linear-gradient(90deg, var(--primary), transparent);
        }

        /* cards & grids */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 2rem;
            padding: 1.6rem 1.6rem 2rem;
            transition: 0.3s ease;
        }

        .skill-card:hover {
            border-color: var(--primary);
            transform: translateY(-6px);
            box-shadow: 0 20px 25px -10px #1e3a5f;
        }

        .skill-card h4 {
            font-size: 1.2rem;
            margin-bottom: 1.3rem;
            color: white;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.6rem;
        }

        .skill-tag {
            background: rgba(79, 158, 255, 0.1);
            border: 1px solid #2d4b70;
            border-radius: 40px;
            padding: 0.3rem 1.1rem;
            font-size: 0.85rem;
            color: #cdddec;
            transition: 0.2s;
        }

        .skill-tag:hover {
            background: var(--primary);
            color: black;
            border-color: var(--primary);
        }

        /* experience timeline style */
        .exp-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 2rem;
            padding: 2rem;
            margin-bottom: 1.8rem;
            transition: 0.2s;
        }

        .exp-card:hover {
            border-left: 6px solid var(--primary);
            background: #1a212a;
        }

        .exp-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
        }

        .exp-title {
            font-size: 1.5rem;
            font-weight: 650;
            color: white;
        }

        .exp-company {
            color: var(--primary);
            font-weight: 500;
            margin: 0.4rem 0 1rem;
        }

        .exp-date {
            background: #1f3245;
            padding: 0.3rem 1.2rem;
            border-radius: 30px;
            font-size: 0.9rem;
            color: #bfd7f0;
        }

        .exp-desc ul {
            list-style: none;
            margin-top: 1rem;
        }

        .exp-desc li {
            display: flex;
            gap: 0.8rem;
            margin-bottom: 0.8rem;
            color: #ced9e3;
        }

        .exp-desc i {
            color: var(--primary);
            margin-top: 0.2rem;
            font-size: 0.9rem;
        }

        /* education & certs side by side */
        .edu-cert-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .edu-item, .cert-item {
            background: var(--surface-light);
            border-radius: 2rem;
            padding: 1.8rem;
            border: 1px solid var(--border);
            transition: 0.2s;
        }

        .edu-item:hover, .cert-item:hover {
            background: #1f2b38;
        }

        .badge {
            background: #1e405e;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.8rem;
            margin-top: 0.8rem;
        }

        /* projects grid with images */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--surface);
            border-radius: 2rem;
            border: 1px solid var(--border);
            overflow: hidden;
            transition: 0.25s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: scale(1.02);
            border-color: var(--primary);
            box-shadow: 0 25px 30px -12px #0f2b44;
        }

        .project-img {
            height: 160px;
            background: linear-gradient(145deg, #132c40, #0b1b2b);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            color: #1d5278;
            border-bottom: 1px solid #253b50;
        }

        .project-img i {
            filter: drop-shadow(0 4px 6px #00000060);
        }

        .project-content {
            padding: 1.8rem 1.5rem 1.5rem;
        }

        .project-name {
            font-size: 1.4rem;
            font-weight: 700;
            color: white;
        }

        .project-client {
            color: var(--primary);
            margin-bottom: 0.7rem;
            font-size: 0.9rem;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        /* referees */
        .referee-list {
            display: flex;
            flex-wrap: wrap;
            gap: 2rem;
        }

        .referee-card {
            background: var(--surface);
            border: 1px solid var(--border);
            border-radius: 2rem;
            padding: 2rem;
            flex: 1 1 220px;
            transition: 0.2s;
        }

        .referee-card:hover {
            border-color: var(--primary);
            background: #1a232f;
        }

        .referee-name {
            font-size: 1.3rem;
            font-weight: 700;
            color: white;
        }

        .referee-title {
            color: var(--text-muted);
            margin: 0.3rem 0 1rem;
        }

        .referee-contact {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #b8c7dd;
        }

        .referee-contact a {
            color: #b8c7dd;
            text-decoration: none;
        }

        .referee-contact a:hover {
            color: white;
        }

        /* footer */
        .footer {
            margin-top: 5rem;
            padding: 2rem 0 1rem;
            border-top: 1px solid var(--border);
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            color: var(--text-muted);
        }

        .social-links {
            display: flex;
            gap: 1.8rem;
        }

        .social-links a {
            color: var(--text-muted);
            font-size: 1.6rem;
            transition: 0.2s;
        }

        .social-links a:hover {
            color: var(--primary);
            transform: translateY(-3px);
        }

        /* responsiveness */
        @media (max-width: 700px) {
            .navbar {
                flex-direction: column;
                gap: 0.8rem;
                padding: 1rem;
            }
            .nav-links {
                gap: 1.2rem;
                justify-content: center;
            }
            .hero h1 {
                font-size: 3rem;
            }
            .quick-info {
                flex-direction: column;
                gap: 0.8rem;
                width: 100%;
            }
            .edu-cert-row {
                grid-template-columns: 1fr;
            }
            .footer {
                flex-direction: column-reverse;
                gap: 1rem;
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <!-- Sticky Navbar -->
    <nav class="navbar">
        <div class="logo"><a href="#home">B.M.</a></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#summary">Profile</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#referees">Referees</a></li>
        </ul>
    </nav>

    <main class="container">
        <!-- HOME / HERO section (includes contact) -->
        <section id="home">
            <div class="hero">
                <h1>Brian Muchere</h1>
                <div class="hero-tagline">Full‑Stack Python & Web Developer · AI & BI</div>
                <div class="quick-info">
                    <span><i class="fas fa-map-pin"></i> Mumias, Kenya</span>
                    <span><i class="fas fa-phone-alt"></i> +254 799 737828</span>
                    <span><i class="fas fa-envelope"></i> <a href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a></span>
                    <span><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank">brian-muchere</a></span>
                    <span><i class="fab fa-github"></i> <a href="https://github.com/Brian-2000/" target="_blank">Brian-2000</a></span>
                </div>
            </div>
        </section>

        <!-- SUMMARY (profile) -->
        <section id="summary">
            <div class="section-header">
                <i class="fas fa-bullseye"></i>
                <h2>Career summary</h2>
                <div class="line"></div>
            </div>
            <div style="background: #1a222d; border-radius: 2.5rem; padding: 2rem 2.5rem; border-left: 6px solid #4f9eff;">
                <p style="font-size: 1.1rem; color: #d3e2f5;">Results-driven Full-Stack Python & Web Developer with over 5 years of proven expertise in architecting, developing, and deploying enterprise-grade business intelligence and data analytics solutions. Skilled in designing scalable RESTful APIs with Python (Django, Flask, FastAPI), implementing asynchronous workflows with Celery, and engineering AI-driven pipelines for predictive analytics, NLP, and anomaly detection. Strong front-end development experience with React, Redux, Ant Design, Vuejs, styled-components, and LESS, delivering responsive, user-centric interfaces. Proficient in SQL, SQLAlchemy, and advanced database engineering, including secure credential management and optimized connection pooling. Experienced in Docker-based deployments, DevOps practices, and troubleshooting complex production environments. Adept at building comprehensive test suites (pytest, Jest) to ensure reliability and scalability. Passionate about transforming business needs into robust, maintainable technical solutions through cross-functional collaboration in agile environments.</p>
            </div>
        </section>

        <!-- SKILLS -->
        <section id="skills">
            <div class="section-header">
                <i class="fas fa-cog"></i>
                <h2>Core skills</h2>
                <div class="line"></div>
            </div>
            <div class="skills-grid">
                <div class="skill-card"><h4><i class="fas fa-code"></i> Lang & frameworks</h4><div class="skill-tags"><span class="skill-tag">Python</span><span class="skill-tag">Django</span><span class="skill-tag">Flask</span><span class="skill-tag">FastAPI</span><span class="skill-tag">Laravel</span><span class="skill-tag">Vue.js</span><span class="skill-tag">JavaScript</span><span class="skill-tag">PHP</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-database"></i> SQL & ORM</h4><div class="skill-tags"><span class="skill-tag">Advanced SQL</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">PostgreSQL</span><span class="skill-tag">MySQL</span><span class="skill-tag">Enterprise DB</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-cloud"></i> DevOps & cloud</h4><div class="skill-tags"><span class="skill-tag">Docker</span><span class="skill-tag">CI/CD</span><span class="skill-tag">Git/GitHub</span><span class="skill-tag">HCIA Cloud</span><span class="skill-tag">Preventive maint.</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-robot"></i> AI / ML</h4><div class="skill-tags"><span class="skill-tag">Predictive analytics</span><span class="skill-tag">NLP (spaCy)</span><span class="skill-tag">Anomaly detection</span><span class="skill-tag">scikit-learn</span><span class="skill-tag">TensorFlow</span><span class="skill-tag">PyTorch</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-paint-brush"></i> Frontend & UI</h4><div class="skill-tags"><span class="skill-tag">React</span><span class="skill-tag">Redux</span><span class="skill-tag">Ant Design</span><span class="skill-tag">Vue.js</span><span class="skill-tag">styled-components</span><span class="skill-tag">LESS</span><span class="skill-tag">FluentUI</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-network-wired"></i> Networking & sys</h4><div class="skill-tags"><span class="skill-tag">CCNA</span><span class="skill-tag">CISCO/D-LINK</span><span class="skill-tag">LAN setup</span><span class="skill-tag">T24 Core Banking</span><span class="skill-tag">NagVis</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-shield-alt"></i> Specialised</h4><div class="skill-tags"><span class="skill-tag">AML/KYC/CFT</span><span class="skill-tag">API integration</span><span class="skill-tag">Asset mgmt</span><span class="skill-tag">Connection pooling</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-check-circle"></i> Testing & practices</h4><div class="skill-tags"><span class="skill-tag">pytest</span><span class="skill-tag">Jest</span><span class="skill-tag">performance opt.</span><span class="skill-tag">documentation</span><span class="skill-tag">agile</span></div></div>
                <div class="skill-card"><h4><i class="fas fa-users"></i> Soft skills</h4><div class="skill-tags"><span class="skill-tag">Analytical thinking</span><span class="skill-tag">teamwork</span><span class="skill-tag">adaptability</span><span class="skill-tag">reporting</span><span class="skill-tag">mentoring</span></div></div>
            </div>
        </section>

        <!-- EXPERIENCE -->
        <section id="experience">
            <div class="section-header">
                <i class="fas fa-briefcase"></i>
                <h2>Work experience</h2>
                <div class="line"></div>
            </div>

            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Full‑Stack Software Developer</span><span class="exp-date">Jan 2024 – present</span></div>
                <div class="exp-company">Deft Technologies Ltd · Nairobi</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Designed/delivered enterprise systems: ESS Portal (AKI), Pension Management (QIJITO), Deft website, EDMS.</li><li><i class="fas fa-chevron-right"></i> Full‑stack with Django, Laravel, Vue.js, UI/UX, DB architecture, testing, deployment.</li><li><i class="fas fa-chevron-right"></i> Integrated third‑party APIs, built enterprise data exchange (HR, procurement, finance).</li><li><i class="fas fa-chevron-right"></i> Innovation lead – automated internal processes, agile sprints & client analysis.</li></ul></div>
            </div>

            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Technical Support Intern (Presidential Digitalent)</span><span class="exp-date">Dec 2022 – Dec 2023</span></div>
                <div class="exp-company">Kenya Revenue Authority (KRA)</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Installed/configured KRA software, ICT support, preventive maintenance.</li><li><i class="fas fa-chevron-right"></i> Co‑developed ICT Asset Management & Inventory System and LAN IP Sniffing System.</li><li><i class="fas fa-chevron-right"></i> Monitored KRA Western Region Network (NagVis), configured routers/switches, LAN & cabling.</li></ul></div>
            </div>

            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Computer Studies Instructor</span><span class="exp-date">May 2022 – Aug 2022</span></div>
                <div class="exp-company">Royal Computer School</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Designed lesson plans, practical training, group sessions & ICT troubleshooting.</li></ul></div>
            </div>

            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Business Development & Social Media Intern</span><span class="exp-date">Dec 2021 – Jan 2022</span></div>
                <div class="exp-company">Funder Holdings</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Managed social media, content calendar, market research & growth strategies.</li></ul></div>
            </div>
        </section>

        <!-- EDUCATION & CERTIFICATIONS -->
        <section>
            <div class="section-header">
                <i class="fas fa-graduation-cap"></i>
                <h2>Education & certifications</h2>
                <div class="line"></div>
            </div>
            <div class="edu-cert-row">
                <div>
                    <div class="edu-item"><strong>🎓 B.Sc. Computer Science</strong> – University of Eldoret (2017–2021) <br> Second Class Honours (Upper Division)</div>
                    <div class="edu-item" style="margin-top:1.2rem;"><strong>🏫 K.C.S.E (B+)</strong> Kamashia Secondary School, 2013–2016</div>
                    <div class="edu-item" style="margin-top:1.2rem;"><strong>📖 K.C.P.E (374 marks)</strong> Ebubole Primary, 2005–2012</div>
                </div>
                <div>
                    <div class="cert-item"><strong>Cisco CCNA</strong> · Cisco Networking Academy <span class="badge">Jan–May 2023</span></div>
                    <div class="cert-item"><strong>HCIA Cloud Computing & Data Storage</strong> · PDTP & HUAWEI <span class="badge">Mar–May 2023</span></div>
                    <div class="cert-item"><strong>Google Coursera – Automation with Python</strong> <span class="badge">Apr–Jul 2023</span></div>
                    <div class="cert-item"><strong>HARVARD EDX – CS50's Web Programming (Python/JS)</strong> <span class="badge">Jan–Aug 2023</span></div>
                </div>
            </div>
        </section>

        <!-- PROJECTS with image icons -->
        <section id="projects">
            <div class="section-header">
                <i class="fas fa-rocket"></i>
                <h2>Projects</h2>
                <div class="line"></div>
            </div>
            <div class="projects-grid">
                <div class="project-card"><div class="project-img"><i class="fas fa-users-cog fa-3x"></i></div><div class="project-content"><div class="project-name">ESS Portal – AKI</div><div class="project-client">2025</div><div>Profile, leave, appraisal, payslip access. Full‑stack dev, deployment, training.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-hand-holding-usd fa-3x"></i></div><div class="project-content"><div class="project-name">Pension System – QIJITO</div><div class="project-client">2024</div><div>Contributions, statements, claims management. Architecture, reporting, client support.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-laptop-code fa-3x"></i></div><div class="project-content"><div class="project-name">Deft Technologies website</div><div class="project-client">2024</div><div>Corporate site, SEO optimization, design & deployment.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-pen-fancy fa-3x"></i></div><div class="project-content"><div class="project-name">Online assignment help</div><div class="project-client">2022</div><div>Student Saviors, Xpedia Assignment Help – full lifecycle.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-boxes fa-3x"></i></div><div class="project-content"><div class="project-name">ICT Asset Management</div><div class="project-client">2023 (KRA)</div><div>Team development, asset tracking, inventory system.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-network-wired fa-3x"></i></div><div class="project-content"><div class="project-name">LAN IP Sniffing System</div><div class="project-client">2023</div><div>Collaborative tool for KRA network monitoring.</div></div></div>
            </div>
        </section>

        <!-- REFEREES -->
        <section id="referees">
            <div class="section-header">
                <i class="fas fa-address-card"></i>
                <h2>Referees</h2>
                <div class="line"></div>
            </div>
            <div class="referee-list">
                <div class="referee-card"><div class="referee-name">Fredrick Wabala</div><div class="referee-title">Pension Admin, Zamara Group</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254713971765</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Fwabala123@Gmail.Com">Fwabala123@Gmail.Com</a></div></div>
                <div class="referee-card"><div class="referee-name">Nelson Kinavuli</div><div class="referee-title">ICT Supervisor, KRA – Kisumu</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254712887199</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Nelson.kinavuli@kra.go.ke">Nelson.kinavuli@kra.go.ke</a></div></div>
                <div class="referee-card"><div class="referee-name">Kelvin Koome Mwiti</div><div class="referee-title">Manager, Deft Technologies</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254701504693</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Kelvin.mwiti@defttech.co.ke">Kelvin.mwiti@defttech.co.ke</a></div></div>
            </div>
        </section>

        <!-- FOOTER -->
        <footer class="footer">
            <div>© 2026 Brian Muchere — full‑stack developer</div>
            <div class="social-links">
                <a href="https://github.com/Brian-2000/" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="mailto:mucherebrian@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
            </div>
        </footer>
    </main>
</body>
</html>
