<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Matheus Leidow - QA Engineer & Developer</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            background: #0d1117;
            color: #c9d1d9;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        /* Animated Background */
        .bg-container {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            background: linear-gradient(135deg, #0d1117 0%, #161b22 100%);
        }
        
        .bg-container::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background-image: 
                linear-gradient(rgba(88, 166, 255, 0.03) 1px, transparent 1px),
                linear-gradient(90deg, rgba(88, 166, 255, 0.03) 1px, transparent 1px);
            background-size: 50px 50px;
            animation: moveGrid 20s linear infinite;
        }
        
        @keyframes moveGrid {
            0% { transform: translate(0, 0); }
            100% { transform: translate(50px, 50px); }
        }
        
        /* Container */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header/Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding: 60px 20px;
        }
        
        .hero-content {
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
        
        .hero h1 {
            font-size: 4em;
            font-weight: 700;
            margin-bottom: 20px;
            background: linear-gradient(135deg, #58a6ff 0%, #a371f7 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        .hero .subtitle {
            font-size: 1.8em;
            color: #8b949e;
            margin-bottom: 15px;
        }
        
        .typing-text {
            font-size: 1.3em;
            color: #58a6ff;
            min-height: 40px;
            margin: 20px 0;
        }
        
        .hero-badges {
            display: flex;
            gap: 15px;
            justify-content: center;
            flex-wrap: wrap;
            margin: 30px 0;
        }
        
        .badge {
            background: rgba(88, 166, 255, 0.1);
            border: 1px solid rgba(88, 166, 255, 0.3);
            padding: 10px 20px;
            border-radius: 20px;
            font-size: 0.95em;
            transition: all 0.3s;
        }
        
        .badge:hover {
            background: rgba(88, 166, 255, 0.2);
            transform: translateY(-3px);
        }
        
        .cta-buttons {
            display: flex;
            gap: 20px;
            justify-content: center;
            margin-top: 40px;
        }
        
        .btn {
            padding: 14px 32px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
            font-size: 1.05em;
            transition: all 0.3s;
            display: inline-block;
        }
        
        .btn-primary {
            background: #58a6ff;
            color: #0d1117;
        }
        
        .btn-primary:hover {
            background: #79c0ff;
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(88, 166, 255, 0.3);
        }
        
        .btn-secondary {
            background: transparent;
            color: #58a6ff;
            border: 2px solid #58a6ff;
        }
        
        .btn-secondary:hover {
            background: rgba(88, 166, 255, 0.1);
            transform: translateY(-2px);
        }
        
        /* Section Styles */
        .section {
            padding: 100px 0;
            animation: fadeInUp 1s ease;
        }
        
        .section-title {
            font-size: 2.8em;
            text-align: center;
            margin-bottom: 20px;
            color: #f0f6fc;
        }
        
        .section-subtitle {
            text-align: center;
            color: #8b949e;
            font-size: 1.2em;
            margin-bottom: 60px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }
        
        /* Timeline */
        .timeline {
            position: relative;
            max-width: 900px;
            margin: 0 auto;
            padding: 40px 0;
        }
        
        .timeline::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            bottom: 0;
            width: 2px;
            background: linear-gradient(180deg, #58a6ff, #a371f7);
            transform: translateX(-50%);
        }
        
        .timeline-item {
            margin: 50px 0;
            position: relative;
        }
        
        .timeline-item::before {
            content: '';
            position: absolute;
            left: 50%;
            top: 0;
            width: 20px;
            height: 20px;
            background: #58a6ff;
            border: 4px solid #0d1117;
            border-radius: 50%;
            transform: translateX(-50%);
            z-index: 1;
        }
        
        .timeline-content {
            background: rgba(22, 27, 34, 0.6);
            border: 1px solid rgba(48, 54, 61, 0.8);
            padding: 30px;
            border-radius: 12px;
            width: 45%;
            transition: all 0.3s;
            backdrop-filter: blur(10px);
        }
        
        .timeline-content:hover {
            background: rgba(22, 27, 34, 0.8);
            border-color: #58a6ff;
            transform: scale(1.03);
            box-shadow: 0 8px 30px rgba(88, 166, 255, 0.2);
        }
        
        .timeline-item:nth-child(odd) .timeline-content {
            margin-left: auto;
        }
        
        .timeline-date {
            color: #58a6ff;
            font-weight: 600;
            font-size: 1.1em;
            margin-bottom: 10px;
        }
        
        .timeline-content h3 {
            font-size: 1.6em;
            color: #f0f6fc;
            margin-bottom: 10px;
        }
        
        .timeline-content h4 {
            color: #a371f7;
            margin-bottom: 15px;
            font-size: 1.1em;
        }
        
        .timeline-content p {
            color: #8b949e;
            line-height: 1.7;
        }
        
        /* Tech Stack */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
            gap: 20px;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .tech-item {
            background: rgba(22, 27, 34, 0.6);
            border: 1px solid rgba(48, 54, 61, 0.8);
            padding: 30px 20px;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s;
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
            background: linear-gradient(90deg, transparent, rgba(88, 166, 255, 0.1), transparent);
            transition: left 0.5s;
        }
        
        .tech-item:hover::before {
            left: 100%;
        }
        
        .tech-item:hover {
            background: rgba(22, 27, 34, 0.8);
            border-color: #58a6ff;
            transform: translateY(-8px);
        }
        
        .tech-icon {
            font-size: 2.5em;
            margin-bottom: 10px;
        }
        
        .tech-name {
            font-weight: 600;
            color: #f0f6fc;
        }
        
        .tech-category {
            font-size: 0.85em;
            color: #8b949e;
            margin-top: 5px;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            max-width: 1000px;
            margin: 0 auto;
        }
        
        .skill-category {
            background: rgba(22, 27, 34, 0.6);
            border: 1px solid rgba(48, 54, 61, 0.8);
            padding: 30px;
            border-radius: 12px;
            transition: all 0.3s;
        }
        
        .skill-category:hover {
            border-color: #58a6ff;
            transform: translateY(-5px);
        }
        
        .skill-category h3 {
            color: #58a6ff;
            margin-bottom: 20px;
            font-size: 1.4em;
        }
        
        .skill-item {
            margin: 15px 0;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
            color: #f0f6fc;
        }
        
        .skill-bar {
            background: rgba(48, 54, 61, 0.5);
            height: 8px;
            border-radius: 4px;
            overflow: hidden;
        }
        
        .skill-progress {
            background: linear-gradient(90deg, #58a6ff, #a371f7);
            height: 100%;
            border-radius: 4px;
            transition: width 1s ease;
        }
        
        /* Contact Section */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            max-width: 900px;
            margin: 0 auto;
        }
        
        .contact-card {
            background: rgba(22, 27, 34, 0.6);
            border: 1px solid rgba(48, 54, 61, 0.8);
            padding: 40px 30px;
            border-radius: 12px;
            text-align: center;
            transition: all 0.3s;
        }
        
        .contact-card:hover {
            background: rgba(22, 27, 34, 0.8);
            border-color: #58a6ff;
            transform: translateY(-8px);
            box-shadow: 0 12px 40px rgba(88, 166, 255, 0.2);
        }
        
        .contact-icon {
            font-size: 3em;
            margin-bottom: 15px;
        }
        
        .contact-card h3 {
            color: #f0f6fc;
            margin-bottom: 15px;
            font-size: 1.3em;
        }
        
        .contact-card a {
            color: #58a6ff;
            text-decoration: none;
            font-weight: 500;
        }
        
        .contact-card a:hover {
            color: #79c0ff;
        }
        
        /* Footer */
        footer {
            text-align: center;
            padding: 40px 20px;
            color: #8b949e;
            border-top: 1px solid rgba(48, 54, 61, 0.5);
        }
        
        /* Responsive */
        @media (max-width: 768px) {
            .hero h1 { font-size: 2.5em; }
            .hero .subtitle { font-size: 1.3em; }
            .typing-text { font-size: 1.1em; }
            .cta-buttons { flex-direction: column; }
            .timeline::before { left: 20px; }
            .timeline-content { width: calc(100% - 60px); margin-left: 60px !important; }
            .timeline-item::before { left: 20px; }
            .section { padding: 60px 0; }
            .section-title { font-size: 2em; }
        }
    </style>
</head>
<body>
    <div class="bg-container"></div>
    
    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>Matheus Leidow</h1>
            <p class="subtitle">QA Engineer & Software Developer</p>
            <div class="typing-text">Transformando Qualidade em Código</div>
            
            <div class="hero-badges">
                <span class="badge">🔍 Test Automation</span>
                <span class="badge">💻 Full-Stack Developer</span>
                <span class="badge">☕ Java Engineer</span>
                <span class="badge">📍 Concórdia, SC</span>
            </div>
            
            <div class="cta-buttons">
                <a href="#contato" class="btn btn-primary">Entre em Contato</a>
                <a href="#experiencia" class="btn btn-secondary">Ver Trajetória</a>
            </div>
        </div>
    </section>
    
    <!-- Experience Timeline -->
    <section id="experiencia" class="section">
        <div class="container">
            <h2 class="section-title">📚 Minha Jornada</h2>
            <p class="section-subtitle">Da qualidade manual ao código: uma evolução contínua</p>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Jan/2026 - Dez/2026</div>
                        <h3>Pós-Graduação em Engenharia de Software com Java</h3>
                        <h4>Instituto Infnet</h4>
                        <p>Especialização focada em Java e arquitetura de software moderna. Aprofundamento em padrões de projeto, microsserviços, cloud computing e boas práticas de desenvolvimento.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">Jan/2024 - Atualmente</div>
                        <h3>QA Automation Engineer</h3>
                        <h4>Automação com TestComplete</h4>
                        <p>Desenvolvimento e manutenção de testes automatizados utilizando TestComplete com Pascal e DelphiScript. Implementação de frameworks de teste e otimização de processos.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2023 - Jun/2025</div>
                        <h3>Análise e Desenvolvimento de Sistemas</h3>
                        <h4>UNOPAR</h4>
                        <p>Formação completa em desenvolvimento de software, cobrindo fundamentos de programação, banco de dados, engenharia de software e metodologias ágeis.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <div class="timeline-date">2023 - 2024</div>
                        <h3>QA Manual Tester</h3>
                        <h4>Início da Carreira em QA</h4>
                        <p>Primeiro contato profissional com testes de software. Experiência em testes funcionais, exploratórios, regressão e documentação de bugs. Desenvolvimento de casos de teste e participação ativa em sprints ágeis.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Tech Stack -->
    <section class="section" style="background: rgba(22, 27, 34, 0.3);">
        <div class="container">
            <h2 class="section-title">🛠️ Tecnologias & Ferramentas</h2>
            <p class="section-subtitle">Stack principal que utilizo no dia a dia</p>
            
            <div class="tech-grid">
                <div class="tech-item">
                    <div class="tech-icon">☕</div>
                    <div class="tech-name">Java</div>
                    <div class="tech-category">Backend</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🔧</div>
                    <div class="tech-name">TestComplete</div>
                    <div class="tech-category">Automation</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">📜</div>
                    <div class="tech-name">Pascal Script</div>
                    <div class="tech-category">Scripting</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🔷</div>
                    <div class="tech-name">DelphiScript</div>
                    <div class="tech-category">Automation</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">⚛️</div>
                    <div class="tech-name">React</div>
                    <div class="tech-category">Frontend</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">📘</div>
                    <div class="tech-name">TypeScript</div>
                    <div class="tech-category">Language</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🐘</div>
                    <div class="tech-name">PostgreSQL</div>
                    <div class="tech-category">Database</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🐙</div>
                    <div class="tech-name">Git</div>
                    <div class="tech-category">Version Control</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🐳</div>
                    <div class="tech-name">Docker</div>
                    <div class="tech-category">DevOps</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🚀</div>
                    <div class="tech-name">CI/CD</div>
                    <div class="tech-category">Automation</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">▲</div>
                    <div class="tech-name">Next.js</div>
                    <div class="tech-category">Framework</div>
                </div>
                
                <div class="tech-item">
                    <div class="tech-icon">🎯</div>
                    <div class="tech-name">Agile</div>
                    <div class="tech-category">Methodology</div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Skills -->
    <section class="section">
        <div class="container">
            <h2 class="section-title">💪 Competências</h2>
            <p class="section-subtitle">Principais áreas de atuação e expertise</p>
            
            <div class="skills-container">
                <div class="skill-category">
                    <h3>🔍 Quality Assurance</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Test Automation</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Manual Testing</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 95%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>TestComplete</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>💻 Desenvolvimento</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Java</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 80%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>JavaScript/TypeScript</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>React/Next.js</span>
                            <span>80%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 80%"></div>
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>🔧 Ferramentas & DevOps</h3>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Git & GitHub</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 90%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>SQL & PostgreSQL</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 85%"></div>
                        </div>
                    </div>
                    <div class="skill-item">
                        <div class="skill-name">
                            <span>Docker & CI/CD</span>
                            <span>75%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-progress" style="width: 75%"></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Contact -->
    <section id="contato" class="section" style="background: rgba(22, 27, 34, 0.3);">
        <div class="container">
            <h2 class="section-title">📫 Vamos Conversar?</h2>
            <p class="section-subtitle">Estou sempre aberto a novas oportunidades e conexões</p>
            
            <div class="contact-grid">
                <div class="contact-card">
                    <div class="contact-icon">💼</div>
                    <h3>LinkedIn</h3>
                    <p><a href="https://linkedin.com/in/matheus-gabriel-leidow/" target="_blank">Conectar no LinkedIn</a></p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">💻</div>
                    <h3>GitHub</h3>
                    <p><a href="https://github.com/math3ux" target="_blank">Ver meus projetos</a></p>
                </div>
                
                <div class="contact-card">
                    <div class="contact-icon">📧</div>
                    <h3>Email</h3>
                    <p><a href="mailto:matheusleidow@gmail.com">matheusleidow@gmail.com</a></p>
                </div>
            </div>
        </div>
    </section>
    
    <!-- Footer -->
    <footer>
        <div class="container">
            <p>© 2025 Matheus Leidow. Desenvolvido com ☕ e 💙</p>
            <p style="margin-top: 10px; font-size: 0.9em;">QA Engineer | Full-Stack Developer | Em constante evolução</p>
        </div>
    </footer>
    
    <script>
        // Typing effect
        const typingTexts = [
            'Transformando Qualidade em Código',
            'QA Automation Specialist',
            'Full-Stack Developer',
            'Java Engineer',
            'Problem Solver'
        ];
        let textIndex = 0;
        let charIndex = 0;
        let isDeleting = false;
        const typingElement = document.querySelector('.typing-text');
        
        function type() {
            const currentText = typingTexts[textIndex];
            
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
                textIndex = (textIndex + 1) % typingTexts.length;
            }
            
            setTimeout(type, isDeleting ? 50 : 100);
        }
        
        // Start typing effect
        setTimeout(type, 1000);
        
        // Smooth scroll
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });
        
        // Scroll animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };
        
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.transform = 'translateY(0)';
                }
            });
        }, observerOptions);
        
        // Observe all sections
        document.querySelectorAll('.section').forEach(section => {
            section.style.opacity = '0';
            section.style.transform = 'translateY(30px)';
            section.style.transition = 'opacity 0.6s ease, transform 0.6s ease';
            observer.observe(section);
        });
        
        // Animate skill bars on scroll
        const skillObserver = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    const progressBars = entry.target.querySelectorAll('.skill-progress');
                    progressBars.forEach(bar => {
                        const width = bar.style.width;
                        bar.style.width = '0';
                        setTimeout(() => {
                            bar.style.width = width;
                        }, 100);
                    });
                    skillObserver.unobserve(entry.target);
                }
            });
        }, observerOptions);
        
        document.querySelectorAll('.skills-container').forEach(container => {
            skillObserver.observe(container);
        });
    </script>
</body>
</html>
