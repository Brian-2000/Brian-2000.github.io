<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=5.0">
    <title>Brian Muchere · Full‑Stack Engineer (Python, PHP, C#, Dart, ML)</title>
    <!-- Google Fonts & Font Awesome (reliable CDNs) -->
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
            scroll-padding-top: 80px; /* offset for fixed navbar */
        }

        body {
            font-family: "Inter", sans-serif;
            background: #0b0e14;
            color: #ecf1f7;
            line-height: 1.6;
        }

        /* modern dark theme variables */
        :root {
            --bg-deep: #0b0e14;
            --bg-surface: #151b24;
            --bg-card: #1e2632;
            --border-dim: #2b3648;
            --primary: #3b82f6;
            --primary-glow: #2563eb;
            --text-bright: #f0f6ff;
            --text-soft: #c9d9f0;
        }

        /* sticky navbar */
        .navbar {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(11, 14, 20, 0.85);
            backdrop-filter: blur(14px);
            -webkit-backdrop-filter: blur(14px);
            border-bottom: 1px solid rgba(59, 130, 246, 0.25);
            padding: 0.8rem 2rem;
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
        }

        .logo a {
            font-weight: 800;
            font-size: 1.9rem;
            letter-spacing: -0.02em;
            background: linear-gradient(145deg, #b3d9ff, #3b82f6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2.2rem;
            list-style: none;
            flex-wrap: wrap;
        }

        .nav-links a {
            color: var(--text-soft);
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
            padding: 2rem 1.5rem 3rem;
        }

        /* hero */
        .hero {
            margin: 2.5rem 0 3.5rem;
        }

        .hero h1 {
            font-size: clamp(2.2rem, 8vw, 4.2rem);
            font-weight: 700;
            background: linear-gradient(to right, #ffffff, #b3d9ff, #7cb2ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.1;
        }

        .hero-tagline {
            font-size: 1.5rem;
            color: var(--primary);
            margin: 0.5rem 0 1.2rem;
            font-weight: 400;
        }

        .quick-info {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem 2.2rem;
            background: var(--bg-surface);
            padding: 1.2rem 2rem;
            border-radius: 60px;
            width: fit-content;
            border: 1px solid var(--border-dim);
            margin: 1.8rem 0;
        }

        .quick-info span {
            display: flex;
            align-items: center;
            gap: 0.6rem;
            color: var(--text-soft);
            font-size: 0.95rem;
        }

        .quick-info i {
            color: var(--primary);
            width: 1.2rem;
        }

        .quick-info a {
            color: var(--text-soft);
            text-decoration: none;
            transition: 0.2s;
        }

        .quick-info a:hover {
            color: white;
        }

        /* section headers */
        section {
            scroll-margin-top: 90px;
            margin-bottom: 5rem;
        }

        .section-header {
            display: flex;
            align-items: center;
            gap: 1rem;
            margin-bottom: 2.5rem;
        }

        .section-header h2 {
            font-size: clamp(1.8rem, 5vw, 2.5rem);
            font-weight: 600;
            background: linear-gradient(135deg, #f0f5fa, #b0d0ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .section-header i {
            font-size: 2rem;
            color: var(--primary);
            opacity: 0.9;
        }

        .line {
            flex: 1;
            height: 2px;
            background: linear-gradient(90deg, var(--primary), transparent);
        }

        /* summary card */
        .summary-card {
            background: var(--bg-card);
            border-radius: 2.5rem;
            padding: 2rem 2.5rem;
            border-left: 6px solid var(--primary);
            border: 1px solid var(--border-dim);
            box-shadow: 0 20px 30px -15px #00000080;
        }

        /* skills grid – fully responsive */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 1.5rem;
        }

        .skill-card {
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 2rem;
            padding: 1.5rem 1.5rem 2rem;
            transition: transform 0.2s, border-color 0.2s, box-shadow 0.2s;
        }

        .skill-card:hover {
            border-color: var(--primary);
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -12px #1e3f6e;
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
            background: rgba(59, 130, 246, 0.12);
            border: 1px solid #2d4b70;
            border-radius: 40px;
            padding: 0.3rem 1.2rem;
            font-size: 0.85rem;
            color: #d2e3ff;
            transition: 0.15s;
        }

        .skill-tag:hover {
            background: var(--primary);
            color: #0b0e14;
            border-color: var(--primary);
        }

        /* experience cards */
        .exp-card {
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 2rem;
            padding: 2rem;
            margin-bottom: 1.8rem;
            transition: 0.2s;
        }

        .exp-card:hover {
            border-left: 6px solid var(--primary);
            background: #1f2a36;
        }

        .exp-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.8rem;
        }

        .exp-title {
            font-size: 1.4rem;
            font-weight: 700;
            color: white;
        }

        .exp-company {
            color: var(--primary);
            font-weight: 500;
            margin: 0.3rem 0 0.8rem;
        }

        .exp-date {
            background: #1a2b3e;
            padding: 0.3rem 1.2rem;
            border-radius: 30px;
            font-size: 0.85rem;
            color: #bdd3f0;
        }

        .exp-desc ul {
            list-style: none;
            margin-top: 1rem;
        }

        .exp-desc li {
            display: flex;
            gap: 0.8rem;
            margin-bottom: 0.7rem;
            color: #ccddf5;
        }

        .exp-desc i {
            color: var(--primary);
            font-size: 0.9rem;
            margin-top: 0.2rem;
        }

        /* education & certs row */
        .edu-cert-row {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 2rem;
        }

        .edu-item, .cert-item {
            background: var(--bg-card);
            border-radius: 2rem;
            padding: 1.8rem;
            border: 1px solid var(--border-dim);
            transition: 0.2s;
        }

        .edu-item:hover, .cert-item:hover {
            background: #1f2b3a;
            border-color: var(--primary);
        }

        .badge {
            background: #1e3a5a;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.8rem;
            margin-top: 0.8rem;
        }

        /* projects grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: var(--bg-card);
            border-radius: 2rem;
            border: 1px solid var(--border-dim);
            overflow: hidden;
            transition: 0.25s ease;
            display: flex;
            flex-direction: column;
        }

        .project-card:hover {
            transform: scale(1.02);
            border-color: var(--primary);
            box-shadow: 0 25px 30px -12px #0f2b4b;
        }

        .project-img {
            height: 160px;
            background: linear-gradient(145deg, #1a2a38, #0d1a28);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            color: #2f577b;
            border-bottom: 1px solid #2d4055;
        }

        .project-img i {
            filter: drop-shadow(0 6px 8px #00000060);
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
            margin-bottom: 0.6rem;
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
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 2rem;
            padding: 2rem;
            flex: 1 1 220px;
            transition: 0.2s;
        }

        .referee-card:hover {
            border-color: var(--primary);
            background: #1e2a37;
        }

        .referee-name {
            font-size: 1.3rem;
            font-weight: 700;
            color: white;
        }

        .referee-title {
            color: var(--text-soft);
            margin: 0.3rem 0 1rem;
        }

        .referee-contact {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            color: #c1d2e8;
        }

        .referee-contact a {
            color: #c1d2e8;
            text-decoration: none;
        }

        .referee-contact a:hover {
            color: white;
        }

        /* footer */
        .footer {
            margin-top: 5rem;
            padding: 2rem 0 1rem;
            border-top: 1px solid var(--border-dim);
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            color: var(--text-soft);
        }

        .social-links {
            display: flex;
            gap: 1.8rem;
        }

        .social-links a {
            color: var(--text-soft);
            font-size: 1.6rem;
            transition: 0.2s;
        }

        .social-links a:hover {
            color: var(--primary);
            transform: translateY(-4px);
        }

        /* responsive tweaks for very small devices */
        @media (max-width: 480px) {
            .navbar {
                padding: 0.8rem 1rem;
            }
            .nav-links {
                gap: 1rem;
                justify-content: center;
                margin-top: 0.5rem;
            }
            .quick-info {
                flex-direction: column;
                width: 100%;
                border-radius: 40px;
                padding: 1rem 1.5rem;
            }
            .hero h1 {
                font-size: 2.2rem;
            }
            .hero-tagline {
                font-size: 1.2rem;
            }
            .section-header h2 {
                font-size: 1.8rem;
            }
            .summary-card {
                padding: 1.5rem;
            }
            .edu-cert-row {
                grid-template-columns: 1fr;
                gap: 1rem;
            }
            .referee-list {
                flex-direction: column;
            }
        }

        /* medium tablets */
        @media (min-width: 481px) and (max-width: 768px) {
            .quick-info {
                width: 100%;
                justify-content: space-around;
            }
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <div class="logo"><a href="#home">B.M.</a></div>
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#summary">Profile</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#experience">Experience</a></li>
            <li><a href="#education">Edu & Certs</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#referees">Referees</a></li>
        </ul>
    </nav>

    <main class="container">
        <!-- HERO section with title updated -->
        <section id="home">
            <div class="hero">
                <h1>Brian Muchere</h1>
                <div class="hero-tagline">Full‑stack Software Engineer (Python, PHP, C#, Dart, Machine Learning)</div>
                <div class="quick-info">
                    <span><i class="fas fa-map-marker-alt"></i> Mumias, Kenya</span>
                    <span><i class="fas fa-phone-alt"></i> +254 799 737828</span>
                    <span><i class="fas fa-envelope"></i> <a href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a></span>
                    <span><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank">brian-muchere</a></span>
                    <span><i class="fab fa-github"></i> <a href="https://github.com/Brian-2000/" target="_blank">Brian-2000</a></span>
                </div>
            </div>
        </section>

        <!-- SUMMARY (Profile) -->
        <section id="summary">
            <div class="section-header">
                <i class="fas fa-user-astronaut"></i>
                <h2>Profile</h2>
                <div class="line"></div>
            </div>
            <div class="summary-card">
                <p style="font-size: 1.1rem;">Results-driven Full-Stack Software Engineer with 5+ years of experience architecting enterprise-grade business intelligence and data analytics solutions. Expert in Python (Django, Flask, FastAPI), PHP (Laravel), C# (.NET), Dart (Flutter), and Machine Learning pipelines (scikit-learn, TensorFlow, PyTorch). Skilled in building scalable RESTful APIs, real‑time systems, and AI-driven features. Frontend expertise in React, Vue.js, and cross-platform UI. Proficient in SQL, Docker, DevOps, and agile delivery. Passionate about transforming complex business needs into robust, maintainable systems.</p>
            </div>
        </section>

        <!-- SKILLS – expanded with all frameworks & languages -->
        <section id="skills">
            <div class="section-header">
                <i class="fas fa-cogs"></i>
                <h2>Technical skills</h2>
                <div class="line"></div>
            </div>
            <div class="skills-grid">
                <!-- Python & frameworks -->
                <div class="skill-card"><h4><i class="fab fa-python"></i> Python</h4><div class="skill-tags"><span class="skill-tag">Django</span><span class="skill-tag">Flask</span><span class="skill-tag">FastAPI</span><span class="skill-tag">Celery</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">Pandas</span></div></div>
                <!-- PHP & frameworks -->
                <div class="skill-card"><h4><i class="fab fa-php"></i> PHP</h4><div class="skill-tags"><span class="skill-tag">Laravel</span><span class="skill-tag">Symfony</span><span class="skill-tag">Composer</span><span class="skill-tag">PHPUnit</span></div></div>
                <!-- C# / .NET -->
                <div class="skill-card"><h4><i class="fab fa-microsoft"></i> C# / .NET</h4><div class="skill-tags"><span class="skill-tag">ASP.NET Core</span><span class="skill-tag">Entity Framework</span><span class="skill-tag">LINQ</span><span class="skill-tag">Blazor</span></div></div>
                <!-- Dart / Flutter -->
                <div class="skill-card"><h4><i class="fab fa-dart"></i> Dart / Flutter</h4><div class="skill-tags"><span class="skill-tag">Flutter</span><span class="skill-tag">Dart</span><span class="skill-tag">Riverpod</span><span class="skill-tag">Firebase</span></div></div>
                <!-- Machine Learning & AI -->
                <div class="skill-card"><h4><i class="fas fa-brain"></i> Machine Learning</h4><div class="skill-tags"><span class="skill-tag">scikit-learn</span><span class="skill-tag">TensorFlow</span><span class="skill-tag">PyTorch</span><span class="skill-tag">spaCy</span><span class="skill-tag">HuggingFace</span><span class="skill-tag">OpenCV</span></div></div>
                <!-- Frontend & frameworks -->
                <div class="skill-card"><h4><i class="fas fa-code"></i> Frontend</h4><div class="skill-tags"><span class="skill-tag">React</span><span class="skill-tag">Vue.js</span><span class="skill-tag">Redux</span><span class="skill-tag">Ant Design</span><span class="skill-tag">Tailwind</span><span class="skill-tag">styled‑comp</span></div></div>
                <!-- Databases & ORM -->
                <div class="skill-card"><h4><i class="fas fa-database"></i> Databases</h4><div class="skill-tags"><span class="skill-tag">PostgreSQL</span><span class="skill-tag">MySQL</span><span class="skill-tag">SQL Server</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">MongoDB</span></div></div>
                <!-- DevOps & cloud -->
                <div class="skill-card"><h4><i class="fas fa-cloud"></i> DevOps</h4><div class="skill-tags"><span class="skill-tag">Docker</span><span class="skill-tag">Kubernetes</span><span class="skill-tag">GitHub Actions</span><span class="skill-tag">Azure</span><span class="skill-tag">HCIA Cloud</span></div></div>
                <!-- Networking & special -->
                <div class="skill-card"><h4><i class="fas fa-network-wired"></i> Networking</h4><div class="skill-tags"><span class="skill-tag">CCNA</span><span class="skill-tag">CISCO</span><span class="skill-tag">LAN</span><span class="skill-tag">NagVis</span><span class="skill-tag">T24</span></div></div>
                <!-- Testing & tools -->
                <div class="skill-card"><h4><i class="fas fa-vial"></i> Testing</h4><div class="skill-tags"><span class="skill-tag">pytest</span><span class="skill-tag">Jest</span><span class="skill-tag">NUnit</span><span class="skill-tag">PHPUnit</span></div></div>
            </div>
        </section>

        <!-- EXPERIENCE -->
        <section id="experience">
            <div class="section-header">
                <i class="fas fa-briefcase"></i>
                <h2>Experience</h2>
                <div class="line"></div>
            </div>

            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Full‑Stack Software Developer</span><span class="exp-date">Jan 2024 – present</span></div>
                <div class="exp-company">Deft Technologies Ltd · Nairobi</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Delivered enterprise systems: ESS Portal (AKI), Pension Management (QIJITO), Deft website, EDMS (Python/Django, Laravel, Vue).</li><li><i class="fas fa-chevron-right"></i> Integrated third‑party APIs, built data exchange across HR, procurement, finance.</li><li><i class="fas fa-chevron-right"></i> Led innovation, automated internal processes, active in agile sprints.</li></ul></div>
            </div>
            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Technical Support Intern (Digitalent)</span><span class="exp-date">Dec 2022 – Dec 2023</span></div>
                <div class="exp-company">Kenya Revenue Authority (KRA)</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> ICT support, software installation, preventive maintenance.</li><li><i class="fas fa-chevron-right"></i> Co‑developed ICT Asset Management & LAN IP Sniffing System.</li><li><i class="fas fa-chevron-right"></i> Network monitoring (NagVis), router/switch config, LAN setup.</li></ul></div>
            </div>
            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Computer Studies Instructor</span><span class="exp-date">May 2022 – Aug 2022</span></div>
                <div class="exp-company">Royal Computer School</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Designed curriculum, practical training, ICT troubleshooting.</li></ul></div>
            </div>
            <div class="exp-card">
                <div class="exp-header"><span class="exp-title">Business Development Intern</span><span class="exp-date">Dec 2021 – Jan 2022</span></div>
                <div class="exp-company">Funder Holdings</div>
                <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Social media management, content calendar, market research.</li></ul></div>
            </div>
        </section>

        <!-- EDUCATION & CERTIFICATIONS -->
        <section id="education">
            <div class="section-header">
                <i class="fas fa-graduation-cap"></i>
                <h2>Education & certifications</h2>
                <div class="line"></div>
            </div>
            <div class="edu-cert-row">
                <div>
                    <div class="edu-item"><strong>🎓 B.Sc. Computer Science</strong> – University of Eldoret (2017–2021) <br> Second Class Honours (Upper Division)</div>
                    <div class="edu-item" style="margin-top:1.2rem;"><strong>🏫 K.C.S.E (B+)</strong> Kamashia Secondary School, 2013–2016</div>
                    <div class="edu-item" style="margin-top:1.2rem;"><strong>📖 K.C.P.E (374)</strong> Ebubole Primary, 2005–2012</div>
                </div>
                <div>
                    <div class="cert-item"><strong>Cisco CCNA</strong> · Cisco Networking Academy <span class="badge">Jan–May 2023</span></div>
                    <div class="cert-item"><strong>HCIA Cloud Computing & Data Storage</strong> · PDTP & HUAWEI <span class="badge">Mar–May 2023</span></div>
                    <div class="cert-item"><strong>Google Coursera – Automation with Python</strong> <span class="badge">Apr–Jul 2023</span></div>
                    <div class="cert-item"><strong>HARVARD EDX – CS50's Web Programming (Python/JS)</strong> <span class="badge">Jan–Aug 2023</span></div>
                </div>
            </div>
        </section>

        <!-- PROJECTS with images (icons) -->
        <section id="projects">
            <div class="section-header">
                <i class="fas fa-rocket"></i>
                <h2>Projects</h2>
                <div class="line"></div>
            </div>
            <div class="projects-grid">
                <div class="project-card"><div class="project-img"><i class="fas fa-users-cog fa-3x"></i></div><div class="project-content"><div class="project-name">ESS Portal – AKI</div><div class="project-client">2025</div><div>Profile, leave, appraisal, payslip. Full‑stack (Django/React).</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-hand-holding-usd fa-3x"></i></div><div class="project-content"><div class="project-name">Pension System – QIJITO</div><div class="project-client">2024</div><div>Contributions, statements, claims. Laravel/Vue.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-laptop-code fa-3x"></i></div><div class="project-content"><div class="project-name">Deft Technologies website</div><div class="project-client">2024</div><div>Corporate site, SEO, full‑stack (Django, Tailwind).</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-pen-fancy fa-3x"></i></div><div class="project-content"><div class="project-name">Online assignment help</div><div class="project-client">2022</div><div>Student Saviors, Xpedia – PHP/Laravel, Vue.</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-boxes fa-3x"></i></div><div class="project-content"><div class="project-name">ICT Asset Management</div><div class="project-client">2023 (KRA)</div><div>Inventory system (C# .NET, SQL Server).</div></div></div>
                <div class="project-card"><div class="project-img"><i class="fas fa-network-wired fa-3x"></i></div><div class="project-content"><div class="project-name">LAN IP Sniffing System</div><div class="project-client">2023</div><div>Python, Flask, network monitoring.</div></div></div>
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
            <div>© 2026 Brian Muchere — full‑stack software engineer</div>
            <div class="social-links">
                <a href="https://github.com/Brian-2000/" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
                <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
                <a href="mailto:mucherebrian@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
            </div>
        </footer>
    </main>
    <!-- smooth scroll is native with css, no extra js needed -->
</body>
</html>
