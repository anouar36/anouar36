<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README Preview</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            padding: 20px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: #161b22;
            border-radius: 6px;
            border: 1px solid #30363d;
            padding: 40px;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        .header-image {
            width: 100%;
            height: 300px;
            background-image: url('https://i.imgur.com/your-uploaded-image.jpg');
            background-size: cover;
            background-position: center;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 30px;
            position: relative;
            overflow: hidden;
        }
        
        .header-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(0,0,0,0.6) 0%, rgba(220,20,60,0.3) 100%);
        }
        
        .header h1 {
            font-size: 2.5em;
            color: #dc143c;
            margin: 20px 0;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .header .subtitle {
            font-style: italic;
            color: #8b949e;
            font-size: 1.1em;
            margin-bottom: 20px;
        }
        
        .typing-effect {
            color: #dc143c;
            font-family: 'Courier New', monospace;
            font-size: 1em;
            padding: 10px;
            background: rgba(220, 20, 60, 0.1);
            border-radius: 4px;
            display: inline-block;
        }
        
        h2 {
            color: #58a6ff;
            font-size: 1.8em;
            margin: 40px 0 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid #21262d;
        }
        
        h3 {
            color: #dc143c;
            font-size: 1.3em;
            margin: 30px 0 15px;
        }
        
        .about-section {
            background: linear-gradient(135deg, rgba(220, 20, 60, 0.05) 0%, rgba(88, 166, 255, 0.05) 100%);
            padding: 25px;
            border-radius: 8px;
            border-left: 4px solid #dc143c;
            margin: 20px 0;
        }
        
        .tech-section {
            text-align: center;
            margin: 30px 0;
        }
        
        .tech-category {
            margin: 30px 0;
        }
        
        .tech-category h3 {
            margin-bottom: 15px;
        }
        
        .badges {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
            margin: 15px 0;
        }
        
        .badge {
            display: inline-block;
            padding: 8px 16px;
            background: #21262d;
            border-radius: 6px;
            font-size: 0.9em;
            font-weight: 600;
            color: #fff;
            border: 1px solid #30363d;
            transition: transform 0.2s;
        }
        
        .badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(220, 20, 60, 0.3);
        }
        
        .badge.java { background: linear-gradient(135deg, #ED8B00, #c97500); }
        .badge.spring { background: linear-gradient(135deg, #6DB33F, #5a9c32); }
        .badge.php { background: linear-gradient(135deg, #777BB4, #5f6396); }
        .badge.laravel { background: linear-gradient(135deg, #FF2D20, #cc2419); }
        .badge.docker { background: linear-gradient(135deg, #2496ED, #1a7bc7); }
        .badge.postgres { background: linear-gradient(135deg, #316192, #244a71); }
        .badge.mysql { background: linear-gradient(135deg, #005C84, #004666); }
        .badge.tailwind { background: linear-gradient(135deg, #38B2AC, #2d8e87); }
        
        .divider {
            text-align: center;
            margin: 60px 0;
            font-size: 80px;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0); }
            50% { transform: translateY(-20px); }
        }
        
        .project-card {
            background: linear-gradient(135deg, rgba(33, 38, 45, 0.8) 0%, rgba(22, 27, 34, 0.8) 100%);
            padding: 25px;
            border-radius: 8px;
            margin: 20px 0;
            border: 1px solid #30363d;
            border-left: 4px solid #dc143c;
            transition: all 0.3s;
        }
        
        .project-card:hover {
            transform: translateX(10px);
            box-shadow: -4px 4px 20px rgba(220, 20, 60, 0.2);
        }
        
        .project-card h3 {
            color: #dc143c;
            margin-top: 0;
        }
        
        .project-card .subtitle {
            color: #8b949e;
            font-style: italic;
            margin-bottom: 15px;
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-top: 15px;
        }
        
        .tech-tag {
            background: rgba(88, 166, 255, 0.1);
            color: #58a6ff;
            padding: 4px 12px;
            border-radius: 12px;
            font-size: 0.85em;
            border: 1px solid rgba(88, 166, 255, 0.3);
        }
        
        .path-section {
            background: #0d1117;
            padding: 25px;
            border-radius: 8px;
            border: 1px solid #dc143c;
            font-family: 'Courier New', monospace;
            margin: 20px 0;
        }
        
        .path-section pre {
            color: #58a6ff;
            overflow-x: auto;
        }
        
        .contact-section {
            text-align: center;
            margin: 40px 0;
        }
        
        .contact-badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin: 20px 0;
        }
        
        .contact-badge {
            padding: 12px 30px;
            background: linear-gradient(135deg, #dc143c, #a00f2d);
            color: white;
            text-decoration: none;
            border-radius: 6px;
            font-weight: 600;
            transition: all 0.3s;
            display: inline-block;
        }
        
        .contact-badge:hover {
            transform: scale(1.05);
            box-shadow: 0 6px 20px rgba(220, 20, 60, 0.4);
        }
        
        .footer {
            text-align: center;
            margin-top: 60px;
            padding: 40px 0;
            background: linear-gradient(135deg, rgba(220, 20, 60, 0.1) 0%, rgba(88, 166, 255, 0.1) 100%);
            border-radius: 8px;
        }
        
        .footer-quote {
            font-style: italic;
            color: #8b949e;
            font-size: 1.2em;
            margin-top: 20px;
        }
        
        hr {
            border: none;
            border-top: 1px solid #30363d;
            margin: 40px 0;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="header-image">
                <div style="color: #dc143c; font-size: 2em; z-index: 1;">SAMURAI CODE WARRIOR</div>
            </div>
            
            <h1>🐉 THE WAY OF THE CODE WARRIOR</h1>
            
            <p class="subtitle">"The blade is only as sharp as the hand that wields it."</p>
            
            <div class="typing-effect">
                Backend Engineer | Spring Boot & Laravel | Forging Secure Systems with Discipline
            </div>
        </div>

        <hr>

        <h2>⚔️ THE WAY OF THE SAMURAI</h2>
        
        <div class="about-section">
            <p>In the ancient land of code and architecture, where systems rise and fall like empires, I walk the path of the <strong>Backend Warrior</strong>. My blade is logic, my armor is security, and my honor is clean, maintainable code.</p>
            
            <p style="margin-top: 15px;">Trained in the art of <strong>Java Spring Boot</strong> and <strong>PHP Laravel</strong>, I craft scalable systems that stand the test of battle. From the depths of <strong>PostgreSQL</strong> to the heights of <strong>Keycloak</strong> authentication, I forge applications with the precision of a master swordsmith.</p>
            
            <p style="margin-top: 15px;">My journey began in the halls of learning, where I studied the ancient texts of <strong>Computer Science</strong> and <strong>Software Engineering</strong>. Now, I serve as a guardian of backend systems, defending against chaos with <strong>REST APIs</strong>, securing realms with <strong>Spring Security</strong>, and orchestrating containers with <strong>Docker</strong>.</p>
            
            <p style="margin-top: 15px; font-style: italic; color: #dc143c;"><em>I am not just a developer. I am a craftsman of digital destiny.</em></p>
        </div>

        <hr>

        <h2>🗡️ FORGED IN BATTLE</h2>
        
        <div class="tech-section">
            <div class="tech-category">
                <h3>⚔️ BACK-END ARSENAL</h3>
                <div class="badges">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="50" height="50" alt="Java" title="Java"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" width="50" height="50" alt="Spring Boot" title="Spring Boot"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/php/php-original.svg" width="50" height="50" alt="PHP" title="PHP"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/laravel/laravel-plain.svg" width="50" height="50" alt="Laravel" title="Laravel"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/hibernate/hibernate-original.svg" width="50" height="50" alt="Hibernate" title="Hibernate"/>
                </div>
            </div>

            <div class="tech-category">
                <h3>🎨 FRONT-END FORGE</h3>
                <div class="badges">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="50" height="50" alt="HTML5" title="HTML5"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="50" height="50" alt="CSS3" title="CSS3"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tailwindcss/tailwindcss-plain.svg" width="50" height="50" alt="TailwindCSS" title="TailwindCSS"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" width="50" height="50" alt="Bootstrap" title="Bootstrap"/>
                </div>
            </div>

            <div class="tech-category">
                <h3>🗄️ DATABASE STRONGHOLDS</h3>
                <div class="badges">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="50" height="50" alt="PostgreSQL" title="PostgreSQL"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" width="50" height="50" alt="MySQL" title="MySQL"/>
                </div>
            </div>

            <div class="tech-category">
                <h3>🛡️ SECURITY & IDENTITY</h3>
                <div class="badges">
                    <img src="https://www.svgrepo.com/show/331488/keycloak.svg" width="50" height="50" alt="Keycloak" title="Keycloak"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" width="50" height="50" alt="Spring Security" title="Spring Security"/>
                </div>
            </div>

            <div class="tech-category">
                <h3>🐳 DEVOPS BATTLEGROUND</h3>
                <div class="badges">
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="50" height="50" alt="Docker" title="Docker"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" width="50" height="50" alt="Linux" title="Linux"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/jenkins/jenkins-original.svg" width="50" height="50" alt="Jenkins" title="Jenkins"/>
                    <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/elasticsearch/elasticsearch-original.svg" width="50" height="50" alt="Elasticsearch" title="Elasticsearch"/>
                </div>
            </div>
        </div>

        <div class="divider">⚔️</div>

        <h2>🐉 BATTLES & CREATIONS</h2>

        <div class="project-card">
            <h3>🏯 LogiTrack</h3>
            <div class="subtitle">The Fortress of Order</div>
            <p>A legendary <strong>Logistics & Warehouse Management System</strong> designed to bring order to chaos. Built with the precision of a master strategist, this fortress manages inventory, tracks shipments, and orchestrates supply chains with military efficiency.</p>
            <div class="project-tech">
                <span class="tech-tag">Spring Boot</span>
                <span class="tech-tag">PostgreSQL</span>
                <span class="tech-tag">Docker</span>
                <span class="tech-tag">Keycloak</span>
                <span class="tech-tag">REST APIs</span>
            </div>
        </div>

        <div class="project-card">
            <h3>🏪 ShopZone</h3>
            <div class="subtitle">The Merchant's Domain</div>
            <p>An <strong>E-commerce Platform</strong> where commerce flows like rivers and transactions are sealed with honor. A complete marketplace with secure authentication, product management, and seamless checkout experiences.</p>
            <div class="project-tech">
                <span class="tech-tag">Laravel</span>
                <span class="tech-tag">MySQL</span>
                <span class="tech-tag">TailwindCSS</span>
                <span class="tech-tag">Eloquent ORM</span>
            </div>
        </div>

        <div class="project-card">
            <h3>💼 CareerLink</h3>
            <div class="subtitle">The Path of Destiny</div>
            <p>A <strong>Career Management Application</strong> that connects warriors to their calling. This system handles job postings, applications, and career tracking with the wisdom of an ancient sage.</p>
            <div class="project-tech">
                <span class="tech-tag">Spring Boot</span>
                <span class="tech-tag">Hibernate</span>
                <span class="tech-tag">PostgreSQL</span>
                <span class="tech-tag">Spring Security</span>
            </div>
        </div>

        <div class="project-card">
            <h3>🎬 Cinema Management System</h3>
            <div class="subtitle">The Theater of Dreams</div>
            <p>A comprehensive <strong>Cinema Management Platform</strong> where stories come alive. Manages screenings, bookings, seat reservations, and customer experiences with cinematic excellence.</p>
            <div class="project-tech">
                <span class="tech-tag">PHP Laravel</span>
                <span class="tech-tag">MySQL</span>
                <span class="tech-tag">Bootstrap</span>
                <span class="tech-tag">REST APIs</span>
            </div>
        </div>

        <div class="divider">🐉</div>

        <h2>🈶 PATH OF THE WARRIOR</h2>

        <div class="path-section">
            <pre>
Primary Path:
  ⚔️ Backend Engineer
  ☕ Java / Spring Boot Developer
  🐘 PHP / Laravel Developer
  
Secondary Mastery:
  🛡️ Security-Oriented Applications
  🔐 Identity & Access Management (Keycloak)
  📦 Microservices Architecture
  
Philosophy:
  "Code with honor. Build with purpose. Deploy with confidence."
            </pre>
        </div>

        <hr>

        <h2>📜 SUMMON THE WARRIOR</h2>

        <div class="contact-section">
            <div class="contact-badges">
                <a href="#" class="contact-badge">GitHub</a>
                <a href="#" class="contact-badge">LinkedIn</a>
                <a href="#" class="contact-badge">Email</a>
            </div>
        </div>

        <div class="footer">
            <div style="font-size: 3em; margin-bottom: 20px;">道を歩む者</div>
            <div class="footer-quote">"The code is written. The path is set. The warrior moves forward."</div>
        </div>
    </div>
</body>
</html>
