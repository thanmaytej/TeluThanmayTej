<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Telu Thanmay Tej - Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Global Styles - Red Theme */
        :root {
            --primary-color: #d32f2f;
            --secondary-color: #b71c1c;
            --accent-color: #ff5252;
            --text-color: #212121;
            --light-color: #f5f5f5;
            --dark-color: #1a1a1a;
            --gradient-start: #d32f2f;
            --gradient-end: #b71c1c;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            color: var(--text-color);
            background-color: var(--light-color);
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        section {
            padding: 80px 0;
        }
        
        h1, h2, h3, h4 {
            margin-bottom: 20px;
            color: var(--dark-color);
        }
        
        p {
            margin-bottom: 15px;
        }
        
        a {
            text-decoration: none;
            color: var(--primary-color);
            transition: color 0.3s;
        }
        
        a:hover {
            color: var(--secondary-color);
        }
        
        .btn {
            display: inline-block;
            padding: 12px 30px;
            background-color: var(--primary-color);
            color: white;
            border-radius: 5px;
            font-weight: 600;
            transition: all 0.3s;
            border: none;
            cursor: pointer;
            text-align: center;
        }
        
        .btn:hover {
            background-color: var(--secondary-color);
            transform: translateY(-3px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
        }
        
        .btn-outline {
            background-color: transparent;
            color: var(--primary-color);
            border: 2px solid var(--primary-color);
        }
        
        .btn-outline:hover {
            background-color: var(--primary-color);
            color: white;
        }
        
        .btn-download {
            background-color: #4CAF50;
            display: flex;
            align-items: center;
            justify-content: center;
        }
        
        .btn-download:hover {
            background-color: #388E3C;
        }
        
        .btn i {
            margin-right: 8px;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
            position: relative;
        }
        
        .section-title::after {
            content: '';
            position: absolute;
            bottom: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 80px;
            height: 4px;
            background: linear-gradient(to right, var(--gradient-start), var(--gradient-end));
            border-radius: 2px;
        }
        
        /* Header & Navigation */
        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(255, 255, 255, 0.95);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            padding: 15px 0;
            transition: all 0.3s;
        }
        
        header.scrolled {
            padding: 10px 0;
            background-color: rgba(255, 255, 255, 0.98);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }
        
        .logo::before {
            content: "";
            display: inline-block;
            width: 10px;
            height: 10px;
            background-color: var(--primary-color);
            border-radius: 50%;
            margin-right: 8px;
            animation: pulse 2s infinite;
        }
        
        @keyframes pulse {
            0% { transform: scale(1); opacity: 1; }
            50% { transform: scale(1.5); opacity: 0.7; }
            100% { transform: scale(1); opacity: 1; }
        }
        
        .nav-links {
            display: flex;
            list-style: none;
        }
        
        .nav-links li {
            margin-left: 30px;
        }
        
        .nav-links a {
            color: var(--text-color);
            font-weight: 500;
            position: relative;
        }
        
        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary-color);
            transition: width 0.3s;
        }
        
        .nav-links a:hover::after {
            width: 100%;
        }
        
        .menu-toggle {
            display: none;
            font-size: 24px;
            cursor: pointer;
        }
        
        /* Hero Section */
        .hero {
            height: 100vh;
            display: flex;
            align-items: center;
            background: linear-gradient(135deg, rgba(211, 47, 47, 0.1) 0%, rgba(183, 28, 28, 0.2) 100%);
            position: relative;
            overflow: hidden;
        }
        
        .hero-content {
            max-width: 600px;
            z-index: 1;
        }
        
        .hero-title {
            font-size: 3.5rem;
            margin-bottom: 20px;
            color: var(--dark-color);
        }
        
        .hero-subtitle {
            font-size: 1.5rem;
            margin-bottom: 30px;
            color: var(--text-color);
        }
        
        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }
        
        /* Floating Elements */
        .floating-elements {
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            overflow: hidden;
        }
        
        .floating-element {
            position: absolute;
            background: white;
            border-radius: 10px;
            padding: 15px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: 600;
            color: var(--primary-color);
            opacity: 0.9;
            transition: transform 0.3s, opacity 0.3s;
            animation: float 20s infinite ease-in-out;
            z-index: 0;
        }
        
        .floating-element:nth-child(2n) {
            animation-duration: 25s;
        }
        
        .floating-element:nth-child(3n) {
            animation-duration: 30s;
        }
        
        .floating-element:nth-child(4n) {
            animation-duration: 35s;
        }
        
        .floating-element:hover {
            transform: scale(1.2) !important;
            opacity: 1;
            z-index: 2;
            box-shadow: 0 8px 25px rgba(0, 0, 0, 0.15);
        }
        
        @keyframes float {
            0%, 100% {
                transform: translate(0, 0) rotate(0deg);
            }
            25% {
                transform: translate(5vw, 10vh) rotate(5deg);
            }
            50% {
                transform: translate(10vw, 5vh) rotate(-5deg);
            }
            75% {
                transform: translate(5vw, -5vh) rotate(3deg);
            }
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            align-items: center;
        }
        
        .about-text {
            padding-right: 20px;
        }
        
        .about-image {
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            position: relative;
        }
        
        .about-image::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(45deg, rgba(211, 47, 47, 0.2), rgba(183, 28, 28, 0.2));
            z-index: 1;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .about-image:hover::before {
            opacity: 1;
            cursor: pointer;
        }
        
        .about-image img {
            width: 100%;
            height: auto;
            display: block;
            transition: transform 0.5s;
        }
        
        .about-image:hover img {
            transform: scale(1.05);
        }
        
        /* Education Section */
        .education-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .education-item {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .education-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 0;
            background: linear-gradient(to bottom, var(--gradient-start), var(--gradient-end));
            transition: height 0.5s;
            z-index: 1;
        }
        
        .education-item:hover::before {
            height: 100%;
        }
        
        .education-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .education-year {
            color: var(--primary-color);
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .education-degree {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .education-institute {
            color: var(--text-color);
            margin-bottom: 15px;
        }
        
        .education-marks {
            font-weight: 600;
        }
        
        /* Experience Section */
        .experience-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .experience-item {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            overflow: hidden;
        }
        
        .experience-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 0;
            background: linear-gradient(to bottom, var(--gradient-start), var(--gradient-end));
            transition: height 0.5s;
        }
        
        .experience-item:hover::before {
            height: 100%;
        }
        
        .experience-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .experience-company {
            color: var(--primary-color);
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .experience-role {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        /* Projects Section */
        .projects-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .project-item {
            background: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
        }
        
        .project-item::before {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: linear-gradient(to right, var(--gradient-start), var(--gradient-end));
            transition: height 0.3s;
            z-index: 1;
        }
        
        .project-item:hover::before {
            height: 5px;
        }
        
        .project-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
        }
        
        .project-image {
            height: 200px;
            overflow: hidden;
            position: relative;
        }
        
        .project-image::after {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: linear-gradient(to bottom, rgba(211, 47, 47, 0.1), rgba(183, 28, 28, 0.3));
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .project-item:hover .project-image::after {
            opacity: 1;
        }
        
        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }
        
        .project-item:hover .project-image img {
            transform: scale(1.1);
        }
        
        .project-content {
            padding: 20px;
        }
        
        .project-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .project-date {
            color: var(--primary-color);
            font-size: 0.9rem;
            margin-bottom: 15px;
        }
        
        /* Skills Section */
        .skills-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }
        
        .skill-category {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .skill-category:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1);
        }
        
        .skill-title {
            font-size: 1.2rem;
            font-weight: 600;
            margin-bottom: 20px;
            color: var(--primary-color);
            display: flex;
            align-items: center;
        }
        
        .skill-title::before {
            content: '';
            display: inline-block;
            width: 12px;
            height: 12px;
            background-color: var(--primary-color);
            border-radius: 50%;
            margin-right: 10px;
        }
        
        .skill-list {
            list-style: none;
        }
        
        .skill-item {
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            transition: transform 0.3s;
        }
        
        .skill-item:hover {
            transform: translateX(5px);
        }
        
        .skill-item i {
            color: var(--primary-color);
            margin-right: 10px;
            width: 20px;
            text-align: center;
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 20px;
        }
        
        .contact-item {
            display: flex;
            align-items: center;
            padding: 15px;
            background: white;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
        }
        
        .contact-item:hover {
            transform: translateX(10px);
        }
        
        .contact-item i {
            font-size: 1.5rem;
            color: var(--primary-color);
            margin-right: 15px;
        }
        
        .contact-form {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 5px;
            font-weight: 500;
        }
        
        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-size: 1rem;
            transition: border-color 0.3s, box-shadow 0.3s;
        }
        
        .form-group input:focus,
        .form-group textarea:focus {
            border-color: var(--primary-color);
            box-shadow: 0 0 0 2px rgba(211, 47, 47, 0.2);
            outline: none;
        }
        
        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }
        
        /* Footer */
        footer {
            background-color: var(--dark-color);
            color: white;
            padding: 40px 0;
            text-align: center;
            position: relative;
            overflow: hidden;
        }
        
        .footer-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            position: relative;
            z-index: 1;
        }
        
        .social-links {
            display: flex;
            gap: 20px;
            margin: 20px 0;
        }
        
        .social-links a {
            color: white;
            font-size: 1.5rem;
            transition: all 0.3s;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
        }
        
        .social-links a:hover {
            color: var(--accent-color);
            transform: translateY(-5px);
            background: rgba(255, 255, 255, 0.2);
        }
        
        .copyright {
            margin-top: 20px;
            font-size: 0.9rem;
            opacity: 0.8;
        }
        
        /* Responsive Styles */
        @media (max-width: 992px) {
            .about-content,
            .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero-title {
                font-size: 2.5rem;
            }
            
            .hero-subtitle {
                font-size: 1.2rem;
            }
        }
        
        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: fixed;
                top: 70px;
                left: -100%;
                width: 100%;
                height: calc(100vh - 70px);
                background-color: white;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                transition: left 0.3s;
                box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                left: 0;
            }
            
            .nav-links li {
                margin: 15px 0;
            }
            
            .hero-buttons {
                flex-direction: column;
                gap: 10px;
            }
            
            .btn {
                width: 100%;
                text-align: center;
            }
            
            .floating-element {
                display: none;
            }
            
            .floating-element:nth-child(-n+6) {
                display: flex;
            }
        }
        
        /* Particle background for hero */
        .particles {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0;
        }
        
        .particle {
            position: absolute;
            background-color: var(--primary-color);
            border-radius: 50%;
            opacity: 0.3;
            animation: float-particle 15s infinite linear;
        }
        
        @keyframes float-particle {
            0% {
                transform: translateY(0) rotate(0deg);
                opacity: 0.3;
            }
            100% {
                transform: translateY(-100vh) rotate(720deg);
                opacity: 0;
            }
        }
        
        /* Scroll to top button */
        .scroll-to-top {
            position: fixed;
            bottom: 30px;
            right: 30px;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background-color: var(--primary-color);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 20px;
            cursor: pointer;
            transition: all 0.3s;
            opacity: 0;
            visibility: hidden;
            z-index: 999;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .scroll-to-top.visible {
            opacity: 1;
            visibility: visible;
        }
        
        .scroll-to-top:hover {
            background-color: var(--secondary-color);
            transform: translateY(-5px);
        }
        
        /* Toast notification */
        .toast {
            position: fixed;
            bottom: 20px;
            left: 50%;
            transform: translateX(-50%);
            background-color: #333;
            color: white;
            padding: 16px;
            border-radius: 4px;
            z-index: 1000;
            opacity: 0;
            transition: opacity 0.3s;
        }
        
        .toast.show {
            opacity: 1;
        }
    </style>
</head>
<body>
    <!-- Scroll to top button -->
    <div class="scroll-to-top">
        <i class="fas fa-arrow-up"></i>
    </div>

    <!-- Toast notification -->
    <div class="toast" id="downloadToast"></div>

    <!-- Header & Navigation -->
    <header>
        <div class="container header-container">
            <div class="logo">T.T.T</div>
            <div class="menu-toggle">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#education">Education</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container hero-content">
            <h1 class="hero-title">Telu Thanmay Tej</h1>
            <p class="hero-subtitle">Electronics and Computer Science Engineer <br> |  Full Stack Developer </p>
            <div class="hero-buttons">
                <a href="#contact" class="btn"><i class="fas fa-paper-plane"></i>Get In Touch</a>
                <a href="#projects" class="btn btn-outline"><i class="fas fa-briefcase"></i>View Projects</a>
                <a href="#" class="btn btn-download" id="downloadResume"><i class="fas fa-download"></i>Download Resume</a>
            </div>
        </div>
        
        <!-- Floating Elements -->
        <div class="floating-elements">
            <!-- These will be generated by JavaScript -->
        </div>
        
        <!-- Particle Background -->
        <div class="particles"></div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-text">
                    <p>I am a passionate Electronics and Computer Science Engineer with expertise in Full Stack Web Development. I enjoy creating innovative solutions to complex problems and continuously expanding my skill set.</p>
                    <p>With experience in both front-end and back-end development, as well as data analysis and machine learning, I bring a unique perspective to technology projects.</p>
                    <p>When I'm not coding, you can find me playing football, organizing events, or exploring new technologies.</p>
                </div>
                <div class="about-image">
                    <img src="THREETimg1.jpg" alt="Telu Thanmay Tej">
                </div>
            </div>
        </div>
    </section>

    <!-- Education Section -->
    <section id="education" class="education">
        <div class="container">
            <h2 class="section-title">Education</h2>
            <div class="education-container">
                <div class="education-item">
                    <div class="education-year">2025</div>
                    <h3 class="education-degree">B.Tech in Electronics and Computer Science</h3>
                    <div class="education-institute">K.L University</div>
                    <div class="education-marks">CGPA: 8.47</div>
                </div>
                <div class="education-item">
                    <div class="education-year">2021</div>
                    <h3 class="education-degree">Board of Intermediate Education</h3>
                    <div class="education-institute">FIITJEE International</div>
                    <div class="education-marks">Percentage: 91.7%</div>
                </div>
                <div class="education-item">
                    <div class="education-year">2019</div>
                    <h3 class="education-degree">Board of Secondary Education</h3>
                    <div class="education-institute">Sri Chaitanya Techno School</div>
                    <div class="education-marks">CGPA: 9.3</div>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience" class="experience">
        <div class="container">
            <h2 class="section-title">Work Experience</h2>
            <div class="experience-container">
                <div class="experience-item">
                    <div class="experience-company">SEGURA INVENDORS</div>
                    <h3 class="experience-role">Full Stack Web Developer Intern</h3>
                    <div class="project-date">May-August 2023</div>
                    <p>Worked on  Data retrieval API’s and and their properties such as retrieving weather data ,weather conditions in a particular place. Created a website 
"WEATHER REPORT" using the Weather API’s. Where we can give the cities names as inputs which will give the weather condition in that particular place.</p>
                </div>
                <div class="experience-item">
                    <div class="experience-company">TECHNOHOOK</div>
                    <h3 class="experience-role">Data Scientist Intern</h3>
                    <div class="project-date">May-June 2024</div>
                    <p>Various aspects of data analysis and modelling. This includes tasks like data collection, cleaning, and exploration to uncover patterns and insights. Application of  
statistical techniques and machine learning algorithms to build predictive models, while also learning about feature engineering and model evaluation. Additionally, 
gained exposure to big data technologies for handling large datasets and deploying models into production. Effective data visualization and communication skills are 
emphasized, along with collaboration within inter-disciplinary teams. Throughout, the focus was on practical experience and skill development in the diverse 
landscape of data science. </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Projects Section -->
    <section id="projects" class="projects">
        <div class="container">
            <h2 class="section-title">Projects</h2>
            <div class="projects-container">
                <div class="project-item">
                    <div class="project-image">
                        <img src="https://placehold.co/600x400/d32f2f/white?text=Admin+System" alt="Administration System">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Administration System Django Full Stack Project</h3>
                        <div class="project-date">March-April 2023</div>
                        <ul>
                        <p>• Developed Django-based college administration website mirroring university's platform.</p>
                        <p>• Student-focused features: Enrolment, course browsing, and fee details.</p>
                        <p>• Faculty functionalities: Access to pertinent student and course info.</p>
                        <p>• Ensured data security and privacy.</p>
                        <p>• Conducted thorough testing and debugging.</p>
                        </ul>
                    </div>
                </div>
                <div class="project-item">
                    <div class="project-image">
                        <img src="https://placehold.co/600x400/d32f2f/white?text=Weather+App" alt="Weather API Project">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Weather Conditions Display using API</h3>
                        <div class="project-date">June-August 2023</div>
                        <ul>
                        <p>• Developed a project aimed at displaying current weather conditions to users based on their location by utilizing a reliable weather API. </p>
                        <p>• Provides up-to-date information about atmospheric conditions for any given location.  </p>
                        <p>• Utilized a weather API to provide accurate and up-to-date information about temperature, humidity, wind speed, and other relevant data. </p>
                        <p>• Leverages geolocation technology to detect the user's current location automatically, and then fetch real-time data from the selected API.</p>
                        </ul>
                    </div>
                </div>
                <div class="project-item">
                    <div class="project-image">
                        <img src="https://placehold.co/600x400/d32f2f/white?text=Weed+Detection" alt="Weed Detection">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Automated Weed Detection using TensorFlow</h3>
                        <div class="project-date">March-May 2024</div>
                        <ul>
                            <p>• The Weed Detection project using an LSTM RNN (Long Short-Term Memory Recurrent Neural Network) with TensorFlow. </p>
                            <p>• Through the implementation of convolutional neural networks (CNNs) and deep learning techniques, developed a robust system capable of accurately 
identifying and classifying weeds in agricultural fields. </p>
<p>• The main moto of this project is to show the integration of automation into weed detection offers numerous benefits to farmers in various ways.</p>
                        </ul>
                    </div>
                </div>
                <div class="project-item">
                    <div class="project-image">
                        <img src="https://placehold.co/800x600/d32f2f/white?text=Android+Malware+Detection" alt="Bone X-RAY Analysis">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Android Malware Detection using ML with Feature Selection based on Genetic Algorithm</h3>
                        <div class="project-date">Feb - April 2025 </div>
                        <ul>
                            <p>• Built a machine learning system to detect Android malware by analyzing app characteristics like permissions and network activity, enhancing mobile security.</p>
                            <p>• Trained and compared multiple machine learning models (including Random Forest and Neural Networks) on this refined dataset to determine the best performer.</p>
                            <p>• Significantly boosted detection accuracy and performance scores by using this smart feature selection method, outperforming the standard approach.</p>
                            <p>• The final outcome was deployed through a webpage through with the app can be installed.</p>
                            <p>• Developed a robust and efficient solution suitable for resource-constrained environments, contributing to advanced threat detection in mobile ecosystems</p>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills" class="skills">
        <div class="container">
            <h2 class="section-title">Technical Skills</h2>
            <div class="skills-container">
                <div class="skill-category">
                    <h3 class="skill-title">Programming</h3>
                    <ul class="skill-list">
                        <li class="skill-item"><i class="fas fa-code"></i> Java</li>
                        <li class="skill-item"><i class="fas fa-code"></i> Python</li>
                        <li class="skill-item"><i class="fas fa-code"></i> HTML/CSS</li>
                        <li class="skill-item"><i class="fas fa-code"></i> C</li>
                        <li class="skill-item"><i class="fas fa-code"></i> JavaScript</li>
                        <li class="skill-item"><i class="fas fa-code"></i> SQL</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3 class="skill-title">Libraries & Frameworks</h3>
                    <ul class="skill-list">
                        <li class="skill-item"><i class="fas fa-cogs"></i> Django</li>
                        <li class="skill-item"><i class="fas fa-cogs"></i> Pandas</li>
                        <li class="skill-item"><i class="fas fa-cogs"></i> Numpy</li>
                        <li class="skill-item"><i class="fas fa-cogs"></i> sklearn</li>
                        <li class="skill-item"><i class="fas fa-cogs"></i> Node.js</li>
                        <li class="skill-item"><i class="fas fa-cogs"></i> TensorFlow</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3 class="skill-title">Tools & Software</h3>
                    <ul class="skill-list">
                        <li class="skill-item"><i class="fas fa-wrench"></i> PyCharm</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> VS Code</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> Eclipse</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> PostgreSQL</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> MongoDB</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> LaTeX</li>
                        <li class="skill-item"><i class="fas fa-wrench"></i> Photoshop</li>
                    </ul>
                </div>
                <div class="skill-category">
                    <h3 class="skill-title">Certifications & Languages</h3>
                    <ul class="skill-list">
                        <li class="skill-item"><i class="fas fa-certificate"></i> Embedded and IoT Training (IBM Global Certification)</li>
                        <li class="skill-item"><i class="fas fa-certificate"></i> AI & ML using Python (Tessolve Global certification) </li>
                        <li class="skill-item"><i class="fas fa-certificate"></i> Embedded and IoT Systems (Tessolve Global certification) </li>
                        <li class="skill-item"><i class="fas fa-language"></i> English</li>
                        <li class="skill-item"><i class="fas fa-language"></i> Telugu</li>
                        <li class="skill-item"><i class="fas fa-language"></i> Hindi</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <h2 class="section-title">Contact Me</h2>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-item">
                        <i class="fas fa-envelope"></i>
                        <div class="contact-detail" onclick="sendEmail()">thanmaytejtelu@gmail.com</div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-phone"></i>
                        <div class="contact-detail" onclick="openWhatsApp()">+91 7207507250</div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-map-marker-alt"></i>
                        <div>24-1-71/1, Sambamurthy Road, Durgapuram, Vijayawada, A.P, India</div>
                    </div>
                    <div class="contact-item">
                        <i class="fas fa-globe"></i>
                        <div>Available for freelance work and full-time opportunities</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container footer-content">
            <div class="logo" style="color: white;">Telu Thanmay Tej</div>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/thanmaytej/" target="_blank"><i class="fab fa-linkedin"></i></a>
                <a href="#"><i class="fab fa-github"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="https://www.instagram.com/__threet__/" target="_blank"><i class="fab fa-instagram"></i></a>
            </div>
            <div class="copyright">
                &copy; 2025 Telu Thanmay Tej. All Rights Reserved.
            </div>
        </div>
    </footer>

    <!-- JavaScript -->
    <script>
        // Mobile Menu Toggle
        const menuToggle = document.querySelector('.menu-toggle');
        const navLinks = document.querySelector('.nav-links');
        
        menuToggle.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });
        
        // Close mobile menu when clicking on a link
        document.querySelectorAll('.nav-links a').forEach(link => {
            link.addEventListener('click', () => {
                navLinks.classList.remove('active');
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
            
            // Scroll to top button visibility
            const scrollToTop = document.querySelector('.scroll-to-top');
            if (window.scrollY > 500) {
                scrollToTop.classList.add('visible');
            } else {
                scrollToTop.classList.remove('visible');
            }
        });
        
        // Scroll to top functionality
        document.querySelector('.scroll-to-top').addEventListener('click', () => {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        });
        
        // Floating Elements
        const floatingElements = document.querySelector('.floating-elements');
        const professionalTerms = [
            'Full Stack', 'Web Development', 'Python', 'Django', 
            'Java', 'JavaScript', 'Pandas' , 'Numpy', 'API Integration',
            'TensorFlow', 'C', 'Database Management', 'HTML' , 'CSS' , 'SKLearn', 'PyCharm' , 
            'VS Code', 'Eclipse', 'PostgreSQL', 'Photoshop', 'Data Science', 'Machine Learning',
            'AI', 'IoT', 'Embedded Systems', 'React', 'Node.js', 'SQL', 'NoSQL', 'Git', 'GitHub',
            'Responsive Design', 'UI/UX', 'REST API', 'GraphQL', 'Cloud Computing', 'AWS'
        ];
        
        // Create floating elements
        for (let i = 0; i < 20; i++) {
            const element = document.createElement('div');
            element.className = 'floating-element';
            element.textContent = professionalTerms[i];
            element.style.left = `${Math.random() * 100}%`;
            element.style.top = `${Math.random() * 100}%`;
            element.style.fontSize = `${14 + Math.random() * 8}px`;
            element.style.width = `${element.textContent.length * 10}px`;
            element.style.animationDelay = `${Math.random() * 5}s`;
            floatingElements.appendChild(element);
        }
        
        // Particle background
        const particlesContainer = document.querySelector('.particles');
        for (let i = 0; i < 50; i++) {
            const particle = document.createElement('div');
            particle.className = 'particle';
            particle.style.left = `${Math.random() * 100}%`;
            particle.style.top = `${Math.random() * 100}%`;
            particle.style.width = `${2 + Math.random() * 5}px`;
            particle.style.height = particle.style.width;
            particle.style.animationDelay = `${Math.random() * 15}s`;
            particle.style.animationDuration = `${10 + Math.random() * 20}s`;
            particlesContainer.appendChild(particle);
        }
        
        // Animate floating elements on scroll
        function animateFloatingElements() {
            const elements = document.querySelectorAll('.floating-element');
            const scrollY = window.scrollY;
            const windowHeight = window.innerHeight;
            
            elements.forEach(element => {
                const elementY = element.getBoundingClientRect().top + scrollY;
                const elementPercent = (elementY - scrollY) / windowHeight;
                
                // Adjust speed based on scroll position
                const speed = 0.5 + elementPercent * 2;
                element.style.transform = `translateY(${scrollY * speed * 0.1}px)`;
            });
            
            requestAnimationFrame(animateFloatingElements);
        }
        
        // Start animation
        animateFloatingElements();
        
        // Download Resume functionality
        document.getElementById('downloadResume').addEventListener('click', function(e) {
            e.preventDefault();
            
            // Show toast notification
            const toast = document.getElementById('downloadToast');
            toast.textContent = 'Downloading your resume...';
            toast.classList.add('show');
            
            // Simulate download after a short delay
            setTimeout(() => {
                // Create a temporary link element
                const link = document.createElement('a');
                link.href = 'TeluThanmayTej-Resume.pdf'; // Replace with your actual resume file path
                link.download = 'TeluThanmayTej-Resume.pdf';
                
                // Trigger the download
                document.body.appendChild(link);
                link.click();
                document.body.removeChild(link);
                
                // Update toast message
                toast.textContent = 'Resume downloaded successfully!';
                
                // Hide toast after 3 seconds
                setTimeout(() => {
                    toast.classList.remove('show');
                }, 3000);
            }, 1000);
        });
        
        // Form submission
        const contactForm = document.querySelector('.contact-form');
        if (contactForm) {
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                alert('Thank you for your message! I will get back to you soon.');
                contactForm.reset();
            });
        }
        
        // Open WhatsApp function
        function openWhatsApp() {
            const phoneNumber = "+917207507250";
            const message = "Hello, I went through your portfolio. I would like to connect with you.";
            const url = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(message)}`;
            window.open(url, '_blank');
        }
        
        // Send Email function
        function sendEmail() {
            const email = "thanmaytejtelu@gmail.com";
            const subject = "Inquiry about Job";
            const body = "Hello, I went through your portfolio. I would like to connect with you.";
            const url = `mailto:${email}?subject=${encodeURIComponent(subject)}&body=${encodeURIComponent(body)}`;
            window.location.href = url;
        }
        
        // Add click events to contact details
        document.querySelectorAll('.contact-detail').forEach(element => {
            element.style.cursor = 'pointer';
        });
    </script>
</body>
</html>
