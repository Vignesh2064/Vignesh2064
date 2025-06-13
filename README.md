<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Vignesh CloudCampa - DevOps Engineer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, sans-serif;
            background: linear-gradient(135deg, #0f0f23 0%, #1a1a2e 50%, #16213e 100%);
            color: #ffffff;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 2rem;
        }

        .header {
            text-align: center;
            margin-bottom: 4rem;
            position: relative;
        }

        .wave-emoji {
            font-size: 3rem;
            animation: wave 2s ease-in-out infinite;
            display: inline-block;
            margin-bottom: 1rem;
        }

        @keyframes wave {
            0%, 100% { transform: rotate(0deg); }
            25% { transform: rotate(20deg); }
            75% { transform: rotate(-20deg); }
        }

        .name {
            font-size: 4rem;
            font-weight: 800;
            background: linear-gradient(135deg, #00d4ff, #4f46e5, #7c3aed);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 1rem;
            text-shadow: 0 0 30px rgba(79, 70, 229, 0.5);
        }

        .title {
            font-size: 1.5rem;
            font-weight: 600;
            color: #94a3b8;
            margin-bottom: 1rem;
            position: relative;
        }

        .title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 100px;
            height: 3px;
            background: linear-gradient(135deg, #00d4ff, #4f46e5);
            border-radius: 2px;
        }

        .subtitle {
            font-size: 1.2rem;
            color: #64748b;
            font-style: italic;
            margin-bottom: 2rem;
        }

        .section {
            background: rgba(255, 255, 255, 0.05);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 20px;
            padding: 2.5rem;
            margin-bottom: 2rem;
            position: relative;
            transition: all 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(79, 70, 229, 0.2);
            border-color: rgba(79, 70, 229, 0.3);
        }

        .section-title {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .section-icon {
            font-size: 2rem;
            background: linear-gradient(135deg, #00d4ff, #4f46e5);
            background-clip: text;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        .about-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
        }

        .about-item {
            display: flex;
            align-items: flex-start;
            gap: 1rem;
            padding: 1rem;
            background: rgba(255, 255, 255, 0.03);
            border-radius: 15px;
            transition: all 0.3s ease;
        }

        .about-item:hover {
            background: rgba(79, 70, 229, 0.1);
            transform: translateX(10px);
        }

        .about-emoji {
            font-size: 1.5rem;
            background: linear-gradient(135deg, #00d4ff, #4f46e5);
            padding: 0.8rem;
            border-radius: 12px;
            backdrop-filter: blur(10px);
        }

        .about-text {
            flex: 1;
        }

        .about-text strong {
            color: #00d4ff;
        }

        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 1.5rem;
            margin-top: 1.5rem;
        }

        .tech-item {
            background: linear-gradient(135deg, rgba(79, 70, 229, 0.1), rgba(124, 58, 237, 0.1));
            border: 1px solid rgba(79, 70, 229, 0.2);
            border-radius: 15px;
            padding: 1.5rem 1rem;
            text-align: center;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .tech-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.1), transparent);
            transition: left 0.5s ease;
        }

        .tech-item:hover::before {
            left: 100%;
        }

        .tech-item:hover {
            transform: translateY(-10px) scale(1.05);
            box-shadow: 0 15px 30px rgba(79, 70, 229, 0.3);
            border-color: #00d4ff;
        }

        .tech-icon {
            font-size: 2.5rem;
            margin-bottom: 0.5rem;
            display: block;
        }

        .tech-name {
            font-weight: 600;
            font-size: 0.9rem;
            color: #e2e8f0;
        }

        .connect-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1.5rem;
        }

        .connect-item {
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(79, 70, 229, 0.1));
            border: 1px solid rgba(0, 212, 255, 0.2);
            border-radius: 15px;
            padding: 1.5rem;
            text-align: center;
            text-decoration: none;
            color: #ffffff;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .connect-item::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: radial-gradient(circle, rgba(0, 212, 255, 0.2) 0%, transparent 70%);
            transition: all 0.3s ease;
            transform: translate(-50%, -50%);
        }

        .connect-item:hover::before {
            width: 300px;
            height: 300px;
        }

        .connect-item:hover {
            transform: translateY(-5px);
            border-color: #00d4ff;
            box-shadow: 0 10px 25px rgba(0, 212, 255, 0.3);
        }

        .connect-icon {
            font-size: 2rem;
            margin-bottom: 0.5rem;
            display: block;
            position: relative;
            z-index: 1;
        }

        .connect-text {
            font-weight: 600;
            position: relative;
            z-index: 1;
        }

        .quote-section {
            text-align: center;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1), rgba(124, 58, 237, 0.1));
            border: 2px solid rgba(0, 212, 255, 0.3);
            border-radius: 25px;
            padding: 3rem;
            position: relative;
            overflow: hidden;
        }

        .quote-section::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: conic-gradient(from 0deg, transparent, rgba(0, 212, 255, 0.1), transparent);
            animation: rotate 10s linear infinite;
        }

        @keyframes rotate {
            to { transform: rotate(360deg); }
        }

        .quote-content {
            position: relative;
            z-index: 1;
        }

        .quote-text {
            font-size: 2rem;
            font-weight: 700;
            color: #00d4ff;
            margin-bottom: 1rem;
            text-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
        }

        .quote-attribution {
            font-size: 1.2rem;
            color: #94a3b8;
            font-style: italic;
        }

        .floating-particles {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .particle {
            position: absolute;
            width: 4px;
            height: 4px;
            background: rgba(0, 212, 255, 0.5);
            border-radius: 50%;
            animation: float 15s infinite linear;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh) rotate(0deg);
                opacity: 0;
            }
            10% {
                opacity: 1;
            }
            90% {
                opacity: 1;
            }
            100% {
                transform: translateY(-100vh) rotate(360deg);
                opacity: 0;
            }
        }

        @media (max-width: 768px) {
            .name {
                font-size: 2.5rem;
            }
            
            .container {
                padding: 1rem;
            }
            
            .section {
                padding: 1.5rem;
            }
            
            .tech-grid {
                grid-template-columns: repeat(auto-fit, minmax(100px, 1fr));
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <div class="floating-particles" id="particles"></div>
    
    <div class="container">
        <header class="header">
            <div class="wave-emoji">👋</div>
            <h1 class="name">Hi, I'm Vignesh — CloudCampa</h1>
            <div class="title">DevOps Engineer | Cloud Architect | Kubernetes Specialist | AI+DevOps Innovator</div>
            <p class="subtitle">Helping the next generation master real-world Cloud & DevOps engineering.</p>
        </header>

        <section class="section">
            <h2 class="section-title">
                <span class="section-icon">🔥</span>
                About Me
            </h2>
            <div class="about-grid">
                <div class="about-item">
                    <div class="about-emoji">🧠</div>
                    <div class="about-text">Proficient in <strong>AWS, Azure, GCP, Kubernetes, Docker, Terraform</strong></div>
                </div>
                <div class="about-item">
                    <div class="about-emoji">⚙️</div>
                    <div class="about-text">Building automation-first solutions with <strong>Ansible</strong>, <strong>CI/CD</strong>, and <strong>Helm</strong></div>
                </div>
                <div class="about-item">
                    <div class="about-emoji">🤖</div>
                    <div class="about-text">Exploring AI-driven DevOps with tools like <strong>Hugging Face</strong></div>
                </div>
                <div class="about-item">
                    <div class="about-emoji">🎯</div>
                    <div class="about-text">Mission: To create <strong>hands-on, real-world learning</strong> for everyone</div>
                </div>
                <div class="about-item">
                    <div class="about-emoji">🧑‍🏫</div>
                    <div class="about-text">Educator | Open-source Contributor | Mentor at heart</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">
                <span class="section-icon">🧰</span>
                Tech Stack
            </h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <span class="tech-icon">☁️</span>
                    <div class="tech-name">AWS</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">⚡</span>
                    <div class="tech-name">Azure</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🌐</span>
                    <div class="tech-name">GCP</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🚢</span>
                    <div class="tech-name">Kubernetes</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🐳</span>
                    <div class="tech-name">Docker</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🏗️</span>
                    <div class="tech-name">Terraform</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔧</span>
                    <div class="tech-name">Ansible</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">⚓</span>
                    <div class="tech-name">Helm</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔄</span>
                    <div class="tech-name">GitHub</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🏗️</span>
                    <div class="tech-name">Jenkins</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">💬</span>
                    <div class="tech-name">Helm Chat</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">📈</span>
                    <div class="tech-name">Keda</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🌐</span>
                    <div class="tech-name">Istio</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🚀</span>
                    <div class="tech-name">Karpenter</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🛡️</span>
                    <div class="tech-name">Valero</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🔷</span>
                    <div class="tech-name">Azure DevOps</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">📊</span>
                    <div class="tech-name">ELK Stack</div>
                </div>
                <div class="tech-item">
                    <span class="tech-icon">🤖</span>
                    <div class="tech-name">AI Tools</div>
                </div>
            </div>
        </section>

        <section class="section">
            <h2 class="section-title">
                <span class="section-icon">🌐</span>
                Connect With Me
            </h2>
            <div class="connect-grid">
                <a href="#" class="connect-item">
                    <span class="connect-icon">💼</span>
                    <div class="connect-text">LinkedIn</div>
                </a>
                <a href="#" class="connect-item">
                    <span class="connect-icon">🐙</span>
                    <div class="connect-text">GitHub</div>
                </a>
                <a href="#" class="connect-item">
                    <span class="connect-icon">🌍</span>
                    <div class="connect-text">Website</div>
                </a>
                <a href="#" class="connect-item">
                    <span class="connect-icon">📧</span>
                    <div class="connect-text">Email</div>
                </a>
            </div>
        </section>

        <section class="section quote-section">
            <div class="quote-content">
                <h2 class="section-title">
                    <span class="section-icon">✨</span>
                    Quote I Live By
                </h2>
                <div class="quote-text">"Empowering and Growing Through Learning"</div>
            </div>
        </section>
    </div>

    <script>
        // Create floating particles
        function createParticles() {
            const particlesContainer = document.getElementById('particles');
            const particleCount = 20;
            
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                particle.style
