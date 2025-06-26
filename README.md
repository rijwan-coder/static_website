<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rijwan Developer | Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles */
        :root {
            --primary-color: #3498db;
            --secondary-color: #2c3e50;
            --light-color: #ecf0f1;
            --dark-color: #333;
            --success-color: #2ecc71;
            --danger-color: #e74c3c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: var(--dark-color);
            background-color: #f9f9f9;
        }
        
        a {
            text-decoration: none;
            color: var(--primary-color);
        }
        
        ul {
            list-style: none;
        }
        
        .container {
            max-width: 1100px;
            margin: auto;
            padding: 0 2rem;
            overflow: hidden;
        }
        
        .text-center {
            text-align: center;
        }
        
        .section-title {
            font-size: 2rem;
            display: inline-block;
            padding: 0.5rem 0;
            border-bottom: 3px solid var(--primary-color);
            margin-bottom: 2rem;
        }
        
        .btn {
            display: inline-block;
            background: var(--primary-color);
            color: #fff;
            padding: 0.8rem 1.5rem;
            border: none;
            cursor: pointer;
            font-size: 1rem;
            border-radius: 5px;
            transition: all 0.3s ease;
        }
        
        .btn:hover {
            background: #2980b9;
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-dark {
            background: var(--secondary-color);
        }
        
        /* Header */
        header {
            background: var(--secondary-color);
            color: #fff;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            z-index: 100;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.5rem;
            font-weight: bold;
        }
        
        .logo span {
            color: var(--primary-color);
        }
        
        nav ul {
            display: flex;
        }
        
        nav ul li {
            margin-left: 2rem;
        }
        
        nav ul li a {
            color: #fff;
            font-weight: 500;
            transition: all 0.3s ease;
        }
        
        nav ul li a:hover {
            color: var(--primary-color);
        }
        
        .hamburger {
            display: none;
            cursor: pointer;
        }
        
        /* Hero Section */
        #hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(rgba(44, 62, 80, 0.9), rgba(44, 62, 80, 0.9)), 
                        url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1472&q=80') no-repeat center center/cover;
            color: #fff;
            text-align: center;
        }
        
        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }
        
        .hero-content h1 span {
            color: var(--primary-color);
        }
        
        .hero-content p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .social-icons {
            margin-top: 2rem;
        }
        
        .social-icons a {
            color: #fff;
            margin: 0 0.5rem;
            font-size: 1.5rem;
            transition: all 0.3s ease;
        }
        
        .social-icons a:hover {
            color: var(--primary-color);
            transform: translateY(-5px);
        }
        
        /* About Section */
        #about {
            padding: 6rem 0;
            background: #fff;
        }
        
        .about-content {
            display: grid;
            grid-template-columns: 1fr 2fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-img {
            border-radius: 50%;
            width: 250px;
            height: 250px;
            object-fit: cover;
            border: 5px solid var(--primary-color);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .about-text h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
        }
        
        .about-text p {
            margin-bottom: 1rem;
        }
        
        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }
        
        .skill {
            background: var(--light-color);
            padding: 0.5rem 1rem;
            border-radius: 5px;
            font-size: 0.9rem;
        }
        
        /* Projects Section */
        #projects {
            padding: 6rem 0;
            background: var(--light-color);
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .project-card {
            background: #fff;
            border-radius: 5px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.2);
        }
        
        .project-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }
        
        .project-info {
            padding: 1.5rem;
        }
        
        .project-info h3 {
            margin-bottom: 0.5rem;
        }
        
        .project-info p {
            margin-bottom: 1rem;
            color: #666;
        }
        
        .project-links {
            display: flex;
            gap: 1rem;
        }
        
        /* Contact Section */
        #contact {
            padding: 6rem 0;
            background: #fff;
        }
        
        .contact-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 3rem;
        }
        
        .contact-info h3 {
            margin-bottom: 1rem;
        }
        
        .contact-info p {
            margin-bottom: 2rem;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            margin-bottom: 1rem;
        }
        
        .contact-item i {
            margin-right: 1rem;
            color: var(--primary-color);
            font-size: 1.2rem;
        }
        
        .contact-form .form-group {
            margin-bottom: 1.5rem;
        }
        
        .contact-form label {
            display: block;
            margin-bottom: 0.5rem;
        }
        
        .contact-form input,
        .contact-form textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
        }
        
        .contact-form textarea {
            height: 150px;
        }
        
        /* Footer */
        footer {
            background: var(--secondary-color);
            color: #fff;
            text-align: center;
            padding: 2rem 0;
        }
        
        footer p {
            margin-bottom: 1rem;
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .header-container {
                flex-direction: column;
                text-align: center;
            }
            
            nav ul {
                margin-top: 1rem;
            }
            
            .about-content {
                grid-template-columns: 1fr;
                text-align: center;
            }
            
            .about-img {
                margin: 0 auto;
            }
            
            .skills {
                justify-content: center;
            }
            
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero-content h1 {
                font-size: 2.5rem;
            }
        }
        
        @media (max-width: 600px) {
            nav {
                display: none;
            }
            
            .hamburger {
                display: block;
            }
            
            nav.active {
                display: block;
                width: 100%;
            }
            
            nav.active ul {
                flex-direction: column;
                margin-top: 1rem;
            }
            
            nav.active ul li {
                margin: 0.5rem 0;
            }
            
            .hero-content h1 {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <div class="logo">Rijwan <span>Developer</span></div>
            <div class="hamburger" id="hamburger">
                <i class="fas fa-bars"></i>
            </div>
            <nav id="nav">
                <ul>
                    <li><a href="#hero">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="hero">
        <div class="container hero-content">
            <h1>Hi, I'm <span>Rijwan</span></h1>
            <p>A passionate front-end developer creating beautiful, responsive websites with clean code and modern design principles.</p>
            <a href="#projects" class="btn">View My Work</a>
            <div class="social-icons">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-codepen"></i></a>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <img src="riz.JPG" alt="Alex Developer" class="about-img">
                <div class="about-text">
                    <h3>Who am I?</h3>
                    <p>I'm a front-end developer with 1 years of experience building responsive websites and web applications. I specialize in HTML, CSS, JavaScript, and modern frameworks like React.</p>
                    <p>My approach combines technical expertise with an eye for design, ensuring that the websites I build are not only functional but also visually appealing and user-friendly.</p>
                    <p>When I'm not coding, you can find me hiking, reading sci-fi novels, or experimenting with new recipes in the kitchen.</p>
                    <div class="skills">
                        <span class="skill">HTML5</span>
                        <span class="skill">CSS3</span>
                        <span class="skill">JavaScript</span>
                        <span class="skill">React</span>
                        <span class="skill">SASS</span>
                        <span class="skill">Git</span>
                        <span class="skill">Responsive Design</span>
                        <span class="skill">UI/UX</span>
                    </div>
                    <a href="#" class="btn btn-dark">Download Resume</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-grid">
                <!-- Project 1 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400?text=E-Commerce+Website" alt="E-Commerce Website" class="project-img">
                    <div class="project-info">
                        <h3>E-Commerce Website</h3>
                        <p>A fully responsive online store built with React, Node.js, and MongoDB. Features product filtering, cart functionality, and secure checkout.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Live Demo</a>
                            <a href="#" class="btn btn-dark">Code</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 2 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400?text=Task+Management+App" alt="Task Management App" class="project-img">
                    <div class="project-info">
                        <h3>Task Management App</h3>
                        <p>A productivity application built with Vue.js that helps users organize their tasks with drag-and-drop functionality and deadline reminders.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Live Demo</a>
                            <a href="#" class="btn btn-dark">Code</a>
                        </div>
                    </div>
                </div>
                
                <!-- Project 3 -->
                <div class="project-card">
                    <img src="https://via.placeholder.com/600x400?text=Weather+Dashboard" alt="Weather Dashboard" class="project-img">
                    <div class="project-info">
                        <h3>Weather Dashboard</h3>
                        <p>A weather application that displays current conditions and 5-day forecasts using data from the OpenWeather API with location search functionality.</p>
                        <div class="project-links">
                            <a href="#" class="btn">Live Demo</a>
                            <a href="#" class="btn btn-dark">Code</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <h3>Let's talk about your project</h3>
                    <p>I'm currently available for freelance work or full-time positions. Feel free to reach out if you'd like to collaborate or just say hello!</p>
                    
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <span>shaikhrijvan325@gmail.com</span>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <span>9552638276</span>
                    </div>
                    
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <span>Pune</span>
                    </div>
                </div>
                
                <form class="contact-form">
                    <div class="form-group">
                        <label for="name">Name</label>
                        <input type="text" id="name" name="name" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" name="email" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" name="message" required></textarea>
                    </div>
                    
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-icons">
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-codepen"></i></a>
            </div>
            <p>&copy; 2023 Rijwan Developer. All rights reserved.</p>
            <p>Designed and built with ❤️ by Rijwan</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        const hamburger = document.getElementById('hamburger');
        const nav = document.getElementById('nav');
        
        hamburger.addEventListener('click', () => {
            nav.classList.toggle('active');
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if (targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if (targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 70,
                        behavior: 'smooth'
                    });
                    
                    // Close mobile menu if open
                    if (nav.classList.contains('active')) {
                        nav.classList.remove('active');
                    }
                }
            });
        });
    </script>
</body>
</html>
