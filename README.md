<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=yes">
    <title>Brian Muchere · Full‑Stack Engineer (Python, PHP, C#, Dart, ML)</title>
    <!-- Google Fonts & Font Awesome -->
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
            background: #0b0e14;
            color: #ecf1f7;
            line-height: 1.5;
        }

        /* dark theme */
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

        /* header / hero (always visible) */
        .hero {
            background: var(--bg-surface);
            padding: 1.5rem 1rem 1.2rem;
            border-bottom: 1px solid var(--border-dim);
            position: sticky;
            top: 0;
            z-index: 50;
            backdrop-filter: blur(10px);
            background: rgba(21, 27, 36, 0.95);
        }

        .hero h1 {
            font-size: 2rem;
            font-weight: 700;
            background: linear-gradient(to right, #ffffff, #b3d9ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            line-height: 1.2;
        }

        .hero-tagline {
            font-size: 1rem;
            color: var(--primary);
            margin: 0.2rem 0 0.8rem;
            font-weight: 400;
        }

        .quick-info {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem 1.5rem;
            background: var(--bg-card);
            padding: 0.8rem 1rem;
            border-radius: 40px;
            border: 1px solid var(--border-dim);
            font-size: 0.85rem;
        }

        .quick-info span {
            display: flex;
            align-items: center;
            gap: 0.4rem;
            color: var(--text-soft);
        }

        .quick-info i {
            color: var(--primary);
            width: 1rem;
            font-size: 0.9rem;
        }

        .quick-info a {
            color: var(--text-soft);
            text-decoration: none;
        }

        /* tab bar – sticky below header */
        .tab-bar {
            position: sticky;
            top: 115px; /* adjust based on hero height */
            z-index: 45;
            background: var(--bg-deep);
            display: flex;
            flex-wrap: nowrap;
            overflow-x: auto;
            gap: 0.5rem;
            padding: 0.8rem 1rem;
            border-bottom: 1px solid var(--border-dim);
            scrollbar-width: thin;
            scrollbar-color: var(--primary) var(--border-dim);
            -webkit-overflow-scrolling: touch;
        }

        .tab-bar::-webkit-scrollbar {
            height: 4px;
        }

        .tab-bar::-webkit-scrollbar-thumb {
            background: var(--primary);
            border-radius: 8px;
        }

        .tab-btn {
            background: transparent;
            border: 1px solid var(--border-dim);
            color: var(--text-soft);
            padding: 0.5rem 1.2rem;
            border-radius: 40px;
            font-size: 0.9rem;
            font-weight: 500;
            white-space: nowrap;
            cursor: pointer;
            transition: 0.2s;
            flex-shrink: 0;
        }

        .tab-btn.active {
            background: var(--primary);
            color: #0b0e14;
            border-color: var(--primary);
            font-weight: 600;
        }

        .tab-btn:hover {
            background: var(--primary-glow);
            color: white;
            border-color: var(--primary-glow);
        }

        /* tab panes */
        .tab-pane {
            display: none;
            padding: 2rem 1rem;
            animation: fade 0.25s ease;
        }

        .tab-pane.active-pane {
            display: block;
        }

        @keyframes fade {
            from { opacity: 0.3; }
            to { opacity: 1; }
        }

        /* container for content inside panes */
        .pane-content {
            max-width: 1300px;
            margin: 0 auto;
        }

        /* section headers inside panes (optional) */
        .pane-title {
            font-size: 1.8rem;
            font-weight: 600;
            margin-bottom: 1.8rem;
            background: linear-gradient(135deg, #f0f5fa, #b0d0ff);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            display: flex;
            align-items: center;
            gap: 0.6rem;
        }

        /* skills grid (same as before, fully responsive) */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.2rem;
        }

        .skill-card {
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 1.5rem;
            padding: 1.3rem;
            transition: 0.2s;
        }

        .skill-card:hover {
            border-color: var(--primary);
            transform: translateY(-3px);
        }

        .skill-card h4 {
            font-size: 1.1rem;
            margin-bottom: 1rem;
            color: white;
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
            background: rgba(59, 130, 246, 0.12);
            border: 1px solid #2d4b70;
            border-radius: 40px;
            padding: 0.25rem 1rem;
            font-size: 0.8rem;
            color: #d2e3ff;
        }

        /* experience cards */
        .exp-card {
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 1.5rem;
            padding: 1.5rem;
            margin-bottom: 1.5rem;
        }

        .exp-header {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: baseline;
            gap: 0.5rem;
        }

        .exp-title {
            font-size: 1.2rem;
            font-weight: 700;
            color: white;
        }

        .exp-company {
            color: var(--primary);
            margin: 0.2rem 0 0.8rem;
        }

        .exp-date {
            background: #1a2b3e;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.75rem;
        }

        .exp-desc ul {
            list-style: none;
            margin-top: 0.8rem;
        }

        .exp-desc li {
            display: flex;
            gap: 0.6rem;
            margin-bottom: 0.5rem;
            font-size: 0.9rem;
            color: #ccddf5;
        }

        .exp-desc i {
            color: var(--primary);
            font-size: 0.8rem;
            margin-top: 0.2rem;
        }

        /* education & certs row */
        .edu-cert-row {
            display: grid;
            grid-template-columns: 1fr;
            gap: 1.2rem;
        }

        @media (min-width: 600px) {
            .edu-cert-row {
                grid-template-columns: 1fr 1fr;
            }
        }

        .edu-item, .cert-item {
            background: var(--bg-card);
            border-radius: 1.5rem;
            padding: 1.5rem;
            border: 1px solid var(--border-dim);
        }

        .badge {
            background: #1e3a5a;
            display: inline-block;
            padding: 0.2rem 1rem;
            border-radius: 30px;
            font-size: 0.75rem;
            margin-top: 0.8rem;
        }

        /* projects grid */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
            gap: 1.2rem;
        }

        .project-card {
            background: var(--bg-card);
            border-radius: 1.5rem;
            border: 1px solid var(--border-dim);
            overflow: hidden;
        }

        .project-img {
            height: 130px;
            background: linear-gradient(145deg, #1a2a38, #0d1a28);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.8rem;
            color: #2f577b;
            border-bottom: 1px solid #2d4055;
        }

        .project-content {
            padding: 1.2rem;
        }

        .project-name {
            font-size: 1.2rem;
            font-weight: 700;
            color: white;
        }

        .project-client {
            color: var(--primary);
            font-size: 0.8rem;
            text-transform: uppercase;
        }

        /* referees */
        .referee-list {
            display: flex;
            flex-direction: column;
            gap: 1rem;
        }

        @media (min-width: 600px) {
            .referee-list {
                flex-direction: row;
                flex-wrap: wrap;
            }
        }

        .referee-card {
            background: var(--bg-card);
            border: 1px solid var(--border-dim);
            border-radius: 1.5rem;
            padding: 1.5rem;
            flex: 1 1 200px;
        }

        .referee-name {
            font-size: 1.2rem;
            font-weight: 700;
            color: white;
        }

        .referee-title {
            color: var(--text-soft);
            margin: 0.3rem 0 0.8rem;
            font-size: 0.9rem;
        }

        .referee-contact {
            display: flex;
            align-items: center;
            gap: 0.5rem;
            font-size: 0.85rem;
            color: #c1d2e8;
        }

        .referee-contact a {
            color: #c1d2e8;
            text-decoration: none;
        }

        /* footer – always visible after tabs */
        .footer {
            margin-top: 2rem;
            padding: 1.5rem 1rem 1rem;
            border-top: 1px solid var(--border-dim);
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            color: var(--text-soft);
            font-size: 0.9rem;
        }

        .social-links {
            display: flex;
            gap: 1.2rem;
        }

        .social-links a {
            color: var(--text-soft);
            font-size: 1.4rem;
            transition: 0.2s;
        }

        .social-links a:hover {
            color: var(--primary);
        }

        /* extra small screens */
        @media (max-width: 380px) {
            .hero h1 {
                font-size: 1.8rem;
            }
            .quick-info {
                flex-direction: column;
                gap: 0.3rem;
            }
            .tab-btn {
                padding: 0.4rem 1rem;
                font-size: 0.8rem;
            }
        }
    </style>
</head>
<body>

    <!-- fixed header with name & contact (always visible) -->
    <div class="hero">
        <h1>Brian Muchere</h1>
        <div class="hero-tagline">Full‑stack Software Engineer (Python, PHP, C#, Dart, ML)</div>
        <div class="quick-info">
            <span><i class="fas fa-map-marker-alt"></i> Mumias, Kenya</span>
            <span><i class="fas fa-phone-alt"></i> +254 799 737828</span>
            <span><i class="fas fa-envelope"></i> <a href="mailto:mucherebrian@gmail.com">mucherebrian@gmail.com</a></span>
            <span><i class="fab fa-linkedin"></i> <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank">brian-muchere</a></span>
            <span><i class="fab fa-github"></i> <a href="https://github.com/Brian-2000/" target="_blank">Brian-2000</a></span>
        </div>
    </div>

    <!-- Tab navigation (sticky) -->
    <div class="tab-bar" id="tabBar">
        <button class="tab-btn active" data-tab="profile">Profile</button>
        <button class="tab-btn" data-tab="skills">Skills</button>
        <button class="tab-btn" data-tab="experience">Experience</button>
        <button class="tab-btn" data-tab="education">Edu & Certs</button>
        <button class="tab-btn" data-tab="projects">Projects</button>
        <button class="tab-btn" data-tab="referees">Referees</button>
    </div>

    <!-- Tab panes (only one visible at a time) -->
    <div class="tab-panes">
        <!-- PROFILE pane -->
        <div class="tab-pane active-pane" id="profile">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-user-astronaut"></i> Career Profile</div>
                <div style="background: var(--bg-card); border-radius: 2rem; padding: 1.8rem; border-left: 6px solid var(--primary);">
                    <p style="font-size: 1rem;">Results-driven Full-Stack Software Engineer with 5+ years of experience architecting enterprise-grade business intelligence and data analytics solutions. Expert in Python (Django, Flask, FastAPI), PHP (Laravel), C# (.NET), Dart (Flutter), and Machine Learning pipelines (scikit-learn, TensorFlow, PyTorch). Skilled in building scalable RESTful APIs, real‑time systems, and AI-driven features. Frontend expertise in React, Vue.js, and cross-platform UI. Proficient in SQL, Docker, DevOps, and agile delivery. Passionate about transforming complex business needs into robust, maintainable systems.</p>
                </div>
            </div>
        </div>

        <!-- SKILLS pane -->
        <div class="tab-pane" id="skills">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-cogs"></i> Technical skills</div>
                <div class="skills-grid">
                    <div class="skill-card"><h4><i class="fab fa-python"></i> Python</h4><div class="skill-tags"><span class="skill-tag">Django</span><span class="skill-tag">Flask</span><span class="skill-tag">FastAPI</span><span class="skill-tag">Celery</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">Pandas</span></div></div>
                    <div class="skill-card"><h4><i class="fab fa-php"></i> PHP</h4><div class="skill-tags"><span class="skill-tag">Laravel</span><span class="skill-tag">Symfony</span><span class="skill-tag">Composer</span><span class="skill-tag">PHPUnit</span></div></div>
                    <div class="skill-card"><h4><i class="fab fa-microsoft"></i> C# / .NET</h4><div class="skill-tags"><span class="skill-tag">ASP.NET Core</span><span class="skill-tag">Entity Framework</span><span class="skill-tag">LINQ</span><span class="skill-tag">Blazor</span></div></div>
                    <div class="skill-card"><h4><i class="fab fa-dart"></i> Dart / Flutter</h4><div class="skill-tags"><span class="skill-tag">Flutter</span><span class="skill-tag">Dart</span><span class="skill-tag">Riverpod</span><span class="skill-tag">Firebase</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-brain"></i> Machine Learning</h4><div class="skill-tags"><span class="skill-tag">scikit-learn</span><span class="skill-tag">TensorFlow</span><span class="skill-tag">PyTorch</span><span class="skill-tag">spaCy</span><span class="skill-tag">HuggingFace</span><span class="skill-tag">OpenCV</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-code"></i> Frontend</h4><div class="skill-tags"><span class="skill-tag">React</span><span class="skill-tag">Vue.js</span><span class="skill-tag">Redux</span><span class="skill-tag">Ant Design</span><span class="skill-tag">Tailwind</span><span class="skill-tag">styled‑comp</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-database"></i> Databases</h4><div class="skill-tags"><span class="skill-tag">PostgreSQL</span><span class="skill-tag">MySQL</span><span class="skill-tag">SQL Server</span><span class="skill-tag">SQLAlchemy</span><span class="skill-tag">MongoDB</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-cloud"></i> DevOps</h4><div class="skill-tags"><span class="skill-tag">Docker</span><span class="skill-tag">Kubernetes</span><span class="skill-tag">GitHub Actions</span><span class="skill-tag">Azure</span><span class="skill-tag">HCIA Cloud</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-network-wired"></i> Networking</h4><div class="skill-tags"><span class="skill-tag">CCNA</span><span class="skill-tag">CISCO</span><span class="skill-tag">LAN</span><span class="skill-tag">NagVis</span><span class="skill-tag">T24</span></div></div>
                    <div class="skill-card"><h4><i class="fas fa-vial"></i> Testing</h4><div class="skill-tags"><span class="skill-tag">pytest</span><span class="skill-tag">Jest</span><span class="skill-tag">NUnit</span><span class="skill-tag">PHPUnit</span></div></div>
                </div>
            </div>
        </div>

        <!-- EXPERIENCE pane -->
        <div class="tab-pane" id="experience">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-briefcase"></i> Work experience</div>
                <div class="exp-card">
                    <div class="exp-header"><span class="exp-title">Full‑Stack Developer</span><span class="exp-date">Jan 2024 – present</span></div>
                    <div class="exp-company">Deft Technologies Ltd · Nairobi</div>
                    <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> ESS Portal (AKI), Pension Management (QIJITO), Deft website, EDMS (Python/Django, Laravel, Vue).</li><li><i class="fas fa-chevron-right"></i> Integrated third‑party APIs, built data exchange across HR, procurement, finance.</li><li><i class="fas fa-chevron-right"></i> Led innovation, automated processes, active in agile sprints.</li></ul></div>
                </div>
                <div class="exp-card">
                    <div class="exp-header"><span class="exp-title">Technical Support (Digitalent)</span><span class="exp-date">Dec 2022 – Dec 2023</span></div>
                    <div class="exp-company">Kenya Revenue Authority (KRA)</div>
                    <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> ICT support, software installation, preventive maintenance.</li><li><i class="fas fa-chevron-right"></i> Co‑developed ICT Asset Management & LAN IP Sniffing System.</li><li><i class="fas fa-chevron-right"></i> Network monitoring (NagVis), router/switch config, LAN setup.</li></ul></div>
                </div>
                <div class="exp-card">
                    <div class="exp-header"><span class="exp-title">Computer Instructor</span><span class="exp-date">May 2022 – Aug 2022</span></div>
                    <div class="exp-company">Royal Computer School</div>
                    <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Designed curriculum, practical training, ICT troubleshooting.</li></ul></div>
                </div>
                <div class="exp-card">
                    <div class="exp-header"><span class="exp-title">Business Development Intern</span><span class="exp-date">Dec 2021 – Jan 2022</span></div>
                    <div class="exp-company">Funder Holdings</div>
                    <div class="exp-desc"><ul><li><i class="fas fa-chevron-right"></i> Social media management, content calendar, market research.</li></ul></div>
                </div>
            </div>
        </div>

        <!-- EDUCATION & CERTS pane -->
        <div class="tab-pane" id="education">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-graduation-cap"></i> Education & certifications</div>
                <div class="edu-cert-row">
                    <div>
                        <div class="edu-item"><strong>🎓 B.Sc. Computer Science</strong> – University of Eldoret (2017–2021) <br> Second Class Honours (Upper Division)</div>
                        <div class="edu-item" style="margin-top:1rem;"><strong>🏫 K.C.S.E (B+)</strong> Kamashia Secondary School, 2013–2016</div>
                        <div class="edu-item" style="margin-top:1rem;"><strong>📖 K.C.P.E (374)</strong> Ebubole Primary, 2005–2012</div>
                    </div>
                    <div>
                        <div class="cert-item"><strong>Cisco CCNA</strong> · Cisco Networking Academy <span class="badge">Jan–May 2023</span></div>
                        <div class="cert-item"><strong>HCIA Cloud Computing & Data Storage</strong> · PDTP & HUAWEI <span class="badge">Mar–May 2023</span></div>
                        <div class="cert-item"><strong>Google Coursera – Automation with Python</strong> <span class="badge">Apr–Jul 2023</span></div>
                        <div class="cert-item"><strong>HARVARD EDX – CS50's Web Programming (Python/JS)</strong> <span class="badge">Jan–Aug 2023</span></div>
                    </div>
                </div>
            </div>
        </div>

        <!-- PROJECTS pane -->
        <div class="tab-pane" id="projects">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-rocket"></i> Projects</div>
                <div class="projects-grid">
                    <div class="project-card"><div class="project-img"><i class="fas fa-users-cog"></i></div><div class="project-content"><div class="project-name">ESS Portal – AKI</div><div class="project-client">2025</div><div>Django/React, profile, leave, payslip.</div></div></div>
                    <div class="project-card"><div class="project-img"><i class="fas fa-hand-holding-usd"></i></div><div class="project-content"><div class="project-name">Pension System – QIJITO</div><div class="project-client">2024</div><div>Laravel/Vue, contributions, claims.</div></div></div>
                    <div class="project-card"><div class="project-img"><i class="fas fa-laptop-code"></i></div><div class="project-content"><div class="project-name">Deft website</div><div class="project-client">2024</div><div>Django, Tailwind, SEO.</div></div></div>
                    <div class="project-card"><div class="project-img"><i class="fas fa-pen-fancy"></i></div><div class="project-content"><div class="project-name">Online assignment help</div><div class="project-client">2022</div><div>PHP/Laravel, Vue.</div></div></div>
                    <div class="project-card"><div class="project-img"><i class="fas fa-boxes"></i></div><div class="project-content"><div class="project-name">ICT Asset Management</div><div class="project-client">2023 (KRA)</div><div>C# .NET, SQL Server.</div></div></div>
                    <div class="project-card"><div class="project-img"><i class="fas fa-network-wired"></i></div><div class="project-content"><div class="project-name">LAN IP Sniffing</div><div class="project-client">2023</div><div>Python, Flask.</div></div></div>
                </div>
            </div>
        </div>

        <!-- REFEREES pane -->
        <div class="tab-pane" id="referees">
            <div class="pane-content">
                <div class="pane-title"><i class="fas fa-address-card"></i> Referees</div>
                <div class="referee-list">
                    <div class="referee-card"><div class="referee-name">Fredrick Wabala</div><div class="referee-title">Pension Admin, Zamara Group</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254713971765</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Fwabala123@Gmail.Com">Fwabala123@Gmail.Com</a></div></div>
                    <div class="referee-card"><div class="referee-name">Nelson Kinavuli</div><div class="referee-title">ICT Supervisor, KRA – Kisumu</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254712887199</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Nelson.kinavuli@kra.go.ke">Nelson.kinavuli@kra.go.ke</a></div></div>
                    <div class="referee-card"><div class="referee-name">Kelvin Koome Mwiti</div><div class="referee-title">Manager, Deft Technologies</div><div class="referee-contact"><i class="fas fa-phone-alt"></i> +254701504693</div><div class="referee-contact"><i class="fas fa-envelope"></i> <a href="mailto:Kelvin.mwiti@defttech.co.ke">Kelvin.mwiti@defttech.co.ke</a></div></div>
                </div>
            </div>
        </div>
    </div>

    <!-- footer (always visible) -->
    <footer class="footer">
        <div>© 2026 Brian Muchere — full‑stack engineer</div>
        <div class="social-links">
            <a href="https://github.com/Brian-2000/" target="_blank" aria-label="GitHub"><i class="fab fa-github"></i></a>
            <a href="https://www.linkedin.com/in/brian-muchere/" target="_blank" aria-label="LinkedIn"><i class="fab fa-linkedin"></i></a>
            <a href="mailto:mucherebrian@gmail.com" aria-label="Email"><i class="fas fa-envelope"></i></a>
        </div>
    </footer>

    <!-- simple tab switching script -->
    <script>
        (function() {
            const tabButtons = document.querySelectorAll('.tab-btn');
            const panes = document.querySelectorAll('.tab-pane');

            function activateTab(tabId) {
                // remove active class from all buttons and panes
                tabButtons.forEach(btn => btn.classList.remove('active'));
                panes.forEach(pane => pane.classList.remove('active-pane'));

                // add active class to selected button and pane
                const activeBtn = document.querySelector(`.tab-btn[data-tab="${tabId}"]`);
                if (activeBtn) activeBtn.classList.add('active');
                const activePane = document.getElementById(tabId);
                if (activePane) activePane.classList.add('active-pane');
            }

            tabButtons.forEach(btn => {
                btn.addEventListener('click', (e) => {
                    const tabId = btn.getAttribute('data-tab');
                    activateTab(tabId);
                });
            });

            // optionally set default (already set in html)
        })();
    </script>
</body>
</html>
