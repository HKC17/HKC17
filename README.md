<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Harsh Chaudhari - Backend Developer</title>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: #0a0a0a;
            color: #e0e0e0;
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        /* Navigation */
        nav {
            position: fixed;
            top: 0;
            width: 100%;
            background: rgba(10, 10, 10, 0.9);
            backdrop-filter: blur(10px);
            z-index: 1000;
            padding: 1.5rem 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }

        nav .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: #fff;
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
            list-style: none;
        }

        .nav-links a {
            color: #e0e0e0;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            font-size: 0.95rem;
        }

        .nav-links a:hover {
            color: #6366f1;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            padding-top: 80px;
        }

        .hero h1 {
            font-size: 4rem;
            font-weight: 700;
            margin-bottom: 1rem;
            background: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero h2 {
            font-size: 1.5rem;
            font-weight: 400;
            color: #a0a0a0;
            margin-bottom: 2rem;
        }

        .hero p {
            font-size: 1.1rem;
            color: #c0c0c0;
            max-width: 600px;
            margin: 0 auto 3rem;
        }

        .social-links {
            display: flex;
            gap: 1.5rem;
            justify-content: center;
            margin-top: 2rem;
        }

        .social-links a {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 50%;
            background: rgba(255, 255, 255, 0.05);
            color: #e0e0e0;
            font-size: 1.2rem;
            transition: all 0.3s;
            text-decoration: none;
        }

        .social-links a:hover {
            background: #6366f1;
            color: #fff;
            transform: translateY(-5px);
        }

        /* Section Styling */
        section {
            padding: 5rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 3rem;
            text-align: center;
            color: #fff;
        }

        /* Skills */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
        }

        .skill-category {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 2rem;
            transition: all 0.3s;
        }

        .skill-category:hover {
            background: rgba(255, 255, 255, 0.05);
            border-color: #6366f1;
            transform: translateY(-5px);
        }

        .skill-category h3 {
            font-size: 1.3rem;
            margin-bottom: 1.5rem;
            color: #6366f1;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
        }

        .skill-tag {
            padding: 0.5rem 1rem;
            background: rgba(99, 102, 241, 0.1);
            border-radius: 20px;
            font-size: 0.9rem;
            color: #e0e0e0;
            border: 1px solid rgba(99, 102, 241, 0.3);
        }

        /* Experience */
        .experience-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 2.5rem;
            margin-bottom: 2rem;
        }

        .experience-card h3 {
            font-size: 1.5rem;
            color: #fff;
            margin-bottom: 0.5rem;
        }

        .experience-card .role {
            color: #6366f1;
            font-size: 1.1rem;
            margin-bottom: 1rem;
        }

        .experience-card ul {
            list-style: none;
            margin-top: 1.5rem;
        }

        .experience-card li {
            padding-left: 1.5rem;
            margin-bottom: 0.8rem;
            position: relative;
        }

        .experience-card li:before {
            content: "▹";
            position: absolute;
            left: 0;
            color: #6366f1;
        }

        /* Projects */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 2rem;
            transition: all 0.3s;
        }

        .project-card:hover {
            background: rgba(255, 255, 255, 0.05);
            border-color: #6366f1;
            transform: translateY(-5px);
        }

        .project-card h3 {
            font-size: 1.3rem;
            color: #fff;
            margin-bottom: 1rem;
        }

        .project-card p {
            color: #c0c0c0;
            margin-bottom: 1.5rem;
        }

        .tech-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin-top: 1rem;
        }

        .tech-badge {
            padding: 0.3rem 0.8rem;
            background: rgba(139, 92, 246, 0.1);
            border-radius: 15px;
            font-size: 0.85rem;
            color: #a78bfa;
        }

        /* Education */
        .education-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .education-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 12px;
            padding: 2rem;
        }

        .education-card h3 {
            color: #6366f1;
            margin-bottom: 0.5rem;
        }

        .education-card .institution {
            font-size: 1.1rem;
            color: #fff;
            margin-bottom: 0.5rem;
        }

        .education-card .year {
            color: #a0a0a0;
            font-size: 0.9rem;
        }

        /* Contact */
        .contact-info {
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-info p {
            font-size: 1.1rem;
            color: #c0c0c0;
            margin-bottom: 2rem;
        }

        .contact-links {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
        }

        .contact-btn {
            padding: 1rem 2rem;
            background: rgba(99, 102, 241, 0.1);
            border: 1px solid #6366f1;
            border-radius: 8px;
            color: #e0e0e0;
            text-decoration: none;
            transition: all 0.3s;
            display: flex;
            align-items: center;
            gap: 0.5rem;
        }

        .contact-btn:hover {
            background: #6366f1;
            color: #fff;
            transform: translateY(-3px);
        }

        /* Footer */
        footer {
            text-align: center;
            padding: 2rem 0;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            color: #a0a0a0;
        }

        @media (max-width: 768px) {
            .hero h1 {
                font-size: 2.5rem;
            }

            .nav-links {
                display: none;
            }
        }
    </style>
</head>
<body>
    <nav>
        <div class="container">
            <a href="#" class="logo">HKC</a>
            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </nav>

    <section class="hero">
        <div class="container">
            <h1>Harsh Kiran Chaudhari</h1>
            <h2>Backend Developer | Python Specialist</h2>
            <p>Backend Developer with 1+ years of experience specializing in building robust, scalable systems using Python, Django, and modern cloud technologies.</p>
            
            <div class="social-links">
                <a href="https://github.com/HKC17" target="_blank"><i class="fab fa-github"></i></a>
                <a href="https://linkedin.com/in/harsh-chaudhari-8704a817a" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="mailto:harshkiranchaudhari@gmail.com"><i class="fas fa-envelope"></i></a>
                <a href="tel:+917410779343"><i class="fas fa-phone"></i></a>
            </div>
        </div>
    </section>

    <section id="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Languages</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Python</span>
                        <span class="skill-tag">Java</span>
                        <span class="skill-tag">JavaScript</span>
                        <span class="skill-tag">SQL</span>
                        <span class="skill-tag">C#</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Frameworks</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Django</span>
                        <span class="skill-tag">Spring Boot</span>
                        <span class="skill-tag">React.js</span>
                        <span class="skill-tag">ASP.NET MVC</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Data Processing</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Pandas</span>
                        <span class="skill-tag">Polars</span>
                        <span class="skill-tag">NumPy</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Databases</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">MongoDB</span>
                        <span class="skill-tag">MySQL</span>
                        <span class="skill-tag">SQL Server</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>DevOps & Cloud</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">Docker</span>
                        <span class="skill-tag">Azure DevOps</span>
                        <span class="skill-tag">CI/CD</span>
                        <span class="skill-tag">Git</span>
                    </div>
                </div>

                <div class="skill-category">
                    <h3>Architecture</h3>
                    <div class="skill-tags">
                        <span class="skill-tag">REST APIs</span>
                        <span class="skill-tag">Microservices</span>
                        <span class="skill-tag">OOP</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="experience">
        <div class="container">
            <h2 class="section-title">Professional Experience</h2>
            <div class="experience-card">
                <h3>Associate Consultant (Backend Developer)</h3>
                <p class="role">Python | Django | MongoDB</p>
                <p style="color: #a0a0a0; margin-bottom: 1rem;">May 2024 – Present</p>
                <ul>
                    <li>Engineered and deployed RESTful APIs and core backend services using Django and MongoDB</li>
                    <li>Optimized performance-critical data processes handling millions of records using Pandas and Polars</li>
                    <li>Implemented advanced MongoDB aggregation pipelines for complex data transformations</li>
                    <li>Automated high-volume manual workflows, reducing operational effort by 100+ hours monthly</li>
                    <li>Led technical teams, conducted code reviews, and maintained 100% on-time delivery</li>
                    <li>Managed CI/CD workflows and production deployments using Docker and Azure DevOps</li>
                </ul>
            </div>
        </div>
    </section>

    <section id="projects">
        <div class="container">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3>🏔️ Trek Booking Web App</h3>
                    <p>Full-stack application for managing trekking packages with responsive UI and seamless REST API integration.</p>
                    <div class="tech-stack">
                        <span class="tech-badge">Java</span>
                        <span class="tech-badge">Spring Boot</span>
                        <span class="tech-badge">React.js</span>
                        <span class="tech-badge">MySQL</span>
                    </div>
                </div>

                <div class="project-card">
                    <h3>👥 Client Management System</h3>
                    <p>Enterprise CRUD solution with secure authentication and role-based access control for managing client records.</p>
                    <div class="tech-stack">
                        <span class="tech-badge">C#</span>
                        <span class="tech-badge">ASP.NET MVC</span>
                        <span class="tech-badge">SQL Server</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="education">
        <div class="container">
            <h2 class="section-title">Education & Certifications</h2>
            <div class="education-grid">
                <div class="education-card">
                    <h3>Post-Graduation Diploma</h3>
                    <p class="institution">Advanced Computing</p>
                    <p>C-DAC Thiruvananthapuram</p>
                    <p class="year">2023 | 76.13%</p>
                </div>

                <div class="education-card">
                    <h3>Bachelor of Engineering</h3>
                    <p class="institution">Mechanical Engineering</p>
                    <p>Terna Engineering College</p>
                    <p class="year">2022 | CGPA: 7.53</p>
                </div>

                <div class="education-card">
                    <h3>Certifications</h3>
                    <ul style="list-style: none; margin-top: 1rem;">
                        <li style="margin-bottom: 0.5rem;">✓ HackerRank SQL (Advanced)</li>
                        <li style="margin-bottom: 0.5rem;">✓ Microsoft Project Management</li>
                        <li style="margin-bottom: 0.5rem;">✓ HackerRank Java (Basic)</li>
                        <li style="margin-bottom: 0.5rem;">✓ Git and GitHub Workshop</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <section id="contact">
        <div class="container">
            <h2 class="section-title">Let's Connect</h2>
            <div class="contact-info">
                <p>I'm always open to interesting conversations and collaboration opportunities. Feel free to reach out!</p>
                <div class="contact-links">
                    <a href="mailto:harshkiranchaudhari@gmail.com" class="contact-btn">
                        <i class="fas fa-envelope"></i> Email Me
                    </a>
                    <a href="https://linkedin.com/in/harsh-chaudhari-8704a817a" target="_blank" class="contact-btn">
                        <i class="fab fa-linkedin"></i> LinkedIn
                    </a>
                    <a href="https://github.com/HKC17" target="_blank" class="contact-btn">
                        <i class="fab fa-github"></i> GitHub
                    </a>
                    <a href="tel:+917410779343" class="contact-btn">
                        <i class="fas fa-phone"></i> +91-7410779343
                    </a>
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>© 2024 Harsh Kiran Chaudhari. Built with passion.</p>
        </div>
    </footer>
</body>
</html>
