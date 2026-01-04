<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matheus Leidow - QA → Full-Stack Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, sans-serif;
            background: #0a0e27;
            color: #e0e0e0;
            min-height: 100vh;
            overflow-x: hidden;
        }
        
        /* Animated background */
        .bg-animation {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #0a0e27 0%, #1a1f3a 100%);
        }
        
        .bg-animation::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(102, 126, 234, 0.1) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveBackground 20s linear infinite;
        }
        
        @keyframes moveBackground {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 40px 20px;
        }
        
        /* Header Section */
        .header {
            text-align: center;
            padding: 100px 20px;
            animation: fadeInUp 1s ease;
        }
        
        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            border: 4px solid #667eea;
            margin-bottom: 20px;
            animation: float 3s ease-in-out infinite;
        }
        
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-10px); }
        }
        
        h1 {
            font-size: 3.5em;
            margin-bottom: 10px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .typing-effect {
            font-size: 1.5em;
            color: #a0a0a0;
            margin: 20px 0;
            min-height: 40px;
        }
        
        .badges {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
            justify-content: center;
            margin: 30px 0;
        }
        
        .badge {
            background: rgba(102, 126, 234, 0.2);
            padding: 10px 20px;
            border-radius: 25px;
            font-size: 0.9em;
            font-weight: 500;
            border: 1px solid rgba(102, 126, 234, 0.3);
            transition: all 0.3s;
        }
        
        .badge:hover {
            background: rgba(102, 126, 234, 0.3);
            transform: translateY(-3px);
        }
        
        /* Section Styles */
        .section {
            margin: 80px 0;
            animation: fadeInUp 1s ease;
        }
        
        h2 {
            font-size: 2.5em;
            margin-bottom: 40px;
            text-align: center;
            position: relative;
        }
        
        h2::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            margin: 15px auto;
            border-radius: 2px;
        }
        
        /* Tech Stack Grid */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .tech-item {
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
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
            background: linear-gradient(90deg, transparent, rgba(102, 126, 234, 0.2), transparent);
            transition: left 0.5s;
        }
        
        .tech-item:hover::before {
            left: 100%;
        }
        
        .tech-item:hover {
            transform: translateY(-10px);
            background: rgba(102, 126, 234, 0.1);
            border-color: #667eea;
        }
        
        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 30px;
            margin: 40px 0;
        }
        
        .project-card {
            background: rgba(255, 255, 255, 0.05);
            border-radius: 20px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: all 0.4s;
            position: relative;
            overflow: hidden;
        }
        
        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transform: scaleX(0);
            transition: transform 0.4s;
        }
        
        .project-card:hover::before {
            transform: scaleX(1);
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            background: rgba(255, 255, 255, 0.08);
            border-color: #667eea;
            box-shadow: 0 20px 40px rgba(102, 126, 234, 0.2);
        }
        
        .project-card h3 {
            font-size: 1.8em;
            margin-bottom: 15px;
            color: #667eea;
        }
        
        .project-card p {
            color: #b0b0b0;
            line-height: 1.6;
            margin-bottom: 20px;
        }
        
        .project-tech {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        
        .tech-tag {
            background: rgba(102, 126, 234, 0.2);
            padding: 5px 12px;
            border-radius: 15px;
            font-size: 0.85em;
            color: #a0c4ff;
        }
        
        .project-links {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }
        
        .project-links a {
            padding: 8px 16px;
            font-size: 0.9em;
        }
        
        /* Timeline */
        .timeline {
            position: relative;
            padding: 20px 0;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(180deg, #667eea, #764ba2);
        }
        
        .timeline-item {
            margin: 40px 0;
            position: relative;
        }
        
        .timeline-content {
            background: rgba(255, 255, 255, 0.05);
            padding: 25px;
            border-radius: 15px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            width: 45%;
            transition: all 0.3s;
        }
        
        .timeline-content:hover {
            background: rgba(255, 255, 255, 0.08);
            transform: scale(1.05);
        }
        
        .timeline-item:nth-child(odd) .timeline-content {
            margin-left: auto;
        }
        
        .timeline-date {
            color: #667eea;
            font-weight: bold;
            margin-bottom: 10px;
        }
        
        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin: 40px 0;
        }
        
        .contact-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .contact-card:hover {
            background: rgba(102, 126, 234, 0.1);
            transform: translateY(-5px);
            border-color: #667eea;
        }
        
        .contact-icon {
            font-size: 2.5em;
            margin-bottom: 15px;
        }
        
        a {
            color: #667eea;
            text-decoration: none;
            transition: all 0.3s;
        }
        
        a:hover {
            color: #764ba2;
        }
        
        .btn {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: #fff;
            padding: 12px 30px;
            border-radius: 25px;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            font-size: 1em;
        }
        
        .btn:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(102, 126, 234, 0.4);
            color: #fff;
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            h1 { font-size: 2.5em; }
            h2 { font-size: 2em; }
            .header { padding: 60px 20px; }
            .timeline::before { left: 20px; }
            .timeline-content { width: calc(100% - 60px); margin-left: 60px !important; }
            .projects-grid { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="bg-animation"></div>
    
    <div class="container">
        <!-- Header -->
        <div class="header">
            <h1>👋 Matheus Leidow</h1>
            <div class="typing-effect">QA Software Tester → Full-Stack Developer</div>
            
            <div class="badges">
                <span class="badge">🔍 Test Automation</span>
                <span class="badge">💻 Full-Stack</span>
                <span class="badge">🤖 Future ML Engineer</span>
                <span class="badge">📍 Concórdia, SC, BR</span>
            </div>
        </div>
        
        <!-- About Section -->
        <div class="section">
            <h2>🚀 Sobre Mim</h2>
            <p style="text-align: center; max-width: 800px; margin: 0 auto; line-height: 1.8; font-size: 1.1em;">
                Profissional de QA em transição para desenvolvimento full-stack. Experiência em automação de testes com TestComplete, 
                otimização de databases PostgreSQL e desenvolvimento web moderno. Apaixonado por tecnologia e sempre em busca de novos desafios.
            </p>
            <p style="text-align: center; margin-top: 20px; color: #667eea;">
                🎓 Pós-Graduação em Engenharia de Software (Java) - INFNET | Início: Fev/2026
            </p>
        </div>
        
        <!-- Tech Stack -->
        <div class="section">
            <h2>🛠️ Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-item">☕ Java</div>
                <div class="tech-item">📜 JavaScript</div>
                <div class="tech-item">🔷 TypeScript</div>
                <div class="tech-item">🐍 Python</div>
                <div class="tech-item">⚛️ React</div>
                <div class="tech-item">▲ Next.js</div>
                <div class="tech-item">🦋 Flutter</div>
                <div class="tech-item">🐘 PostgreSQL</div>
                <div class="tech-item">🔧 TestComplete</div>
                <div class="tech-item">🐙 Git</div>
                <div class="tech-item">🐳 Docker</div>
                <div class="tech-item">☁️ Cloud</div>
            </div>
        </div>
        
        <!-- Projects Section -->
        <div class="section">
            <h2>💼 Projetos em Destaque</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🤖 Automação de Testes</h3>
                    <p>Framework de automação de testes desenvolvido com TestComplete para garantir qualidade e eficiência no ciclo de desenvolvimento.</p>
                    <div class="project-tech">
                        <span class="tech-tag">TestComplete</span>
                        <span class="tech-tag">Python</span>
                        <span class="tech-tag">CI/CD</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <h3>🌐 Web Application</h3>
                    <p>Aplicação web moderna desenvolvida com React e Next.js, focada em performance e experiência do usuário.</p>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">TypeScript</span>
                    </div>
                </div>
                
                <div class="project-card">
                    <h3>📱 Mobile App</h3>
                    <p>Aplicativo mobile cross-platform desenvolvido com Flutter, oferecendo experiência nativa em iOS e Android.</p>
                    <div class="project-tech">
                        <span class="tech-tag">Flutter</span>
                        <span class="tech-tag">Dart</span>
                        <span class="tech-tag">Firebase</span>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Experience Timeline -->
        <div class="section">
            <h2>📚 Experiência & Educação</h2>
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2026 - Presente</div>
                        <h3>Pós-Graduação em Engenharia de Software</h3>
                        <p>INFNET - Especialização em Java e arquitetura de software</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2024 - Presente</div>
                        <h3>QA Software Tester</h3>
                        <p>Automação de testes, otimização de processos e garantia de qualidade</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2023 - 2024</div>
                        <h3>Transição para Full-Stack</h3>
                        <p>Desenvolvimento de habilidades em React, Next.js e tecnologias modernas</p>
                    </div>
                </div>
            </div>
        </div>
        
        <!-- Contact Section -->
        <div class="section">
            <h2>📫 Vamos Conectar?</h2>
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon">💼</div>
                    <h3>LinkedIn</h3>
                    <a href="https://linkedin.com/in/matheus-gabriel-leidow/" target="_blank" class="btn">Conectar</a>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">💻</div>
                    <h3>GitHub</h3>
                    <a href="https://github.com/math3ux" target="_blank" class="btn">Ver Projetos</a>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">📧</div>
                    <h3>Email</h3>
                    <a href="mailto:matheusleidow@gmail.com" class="btn">Enviar Email</a>
                </div>
            </div>
        </div>
    </div>
    
    <script>
        // Typing effect
        const texts = [
            'QA Software Tester → Full-Stack Developer',
            'Automation Specialist',
            'Problem Solver',
            'Continuous Learner'
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.querySelector('.typing-effect');
        
        function type() {
            const currentText = texts[textIndex];
            
            if (isDeleting) {
                typingElement.textContent = currentText.substring(0, charIndex - 1);
                charIndex--;
            } else {
                typingElement.textContent = currentText.substring(0, charIndex + 1);
                charIndex++;
            }
            
            if (!isDeleting && charIndex === currentText.length) {
                setTimeout(() => isDeleting = true, 2000);
            } else if (isDeleting && charIndex === 0) {
                isDeleting = false;
                textIndex = (textIndex + 1) % texts.length;
            }
            
            setTimeout(type, isDeleting ? 50 : 100);
        }
        
        type();
        
        // Scroll animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.animation = 'fadeInUp 1s ease forwards';
                }
            });
        });
        
        document.querySelectorAll('.section').forEach(section => {
            observer.observe(section);
        });
    </script>
</body>
</html>
