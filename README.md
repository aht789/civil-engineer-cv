<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <meta name="description"
          content="Personal portfolio of Amiel Henrich A. Tan, Licensed Civil Engineer and DPWH Accredited Materials Engineer.">

    <meta name="author" content="Amiel Henrich A. Tan">

    <title>Amiel Henrich A. Tan | Civil Engineer</title>

    <!-- Google Font -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link
        href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800&family=Montserrat:wght@600;700;800&display=swap"
        rel="stylesheet">

    <!-- Font Awesome Icons -->
    <link
        rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
    >

    <style>

        /* =========================================================
           GLOBAL
        ========================================================= */

        :root {
            --primary: #0b3d62;
            --primary-dark: #062b46;
            --secondary: #1e88c8;
            --accent: #f5a623;
            --light: #f4f7fa;
            --white: #ffffff;
            --dark: #16212b;
            --gray: #667784;
            --border: #dce4ea;
            --shadow: 0 10px 30px rgba(6, 43, 70, 0.10);
            --radius: 14px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: "Inter", sans-serif;
            color: var(--dark);
            background: var(--white);
            line-height: 1.7;
        }

        h1,
        h2,
        h3,
        h4 {
            font-family: "Montserrat", sans-serif;
        }

        a {
            text-decoration: none;
            color: inherit;
        }

        ul {
            list-style: none;
        }

        img {
            max-width: 100%;
            display: block;
        }

        .container {
            width: min(1120px, 92%);
            margin: auto;
        }

        section {
            padding: 100px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-header span {
            color: var(--secondary);
            font-size: 0.85rem;
            font-weight: 700;
            letter-spacing: 2px;
            text-transform: uppercase;
        }

        .section-header h2 {
            font-size: clamp(2rem, 4vw, 3rem);
            color: var(--primary);
            margin-top: 10px;
        }

        .section-header p {
            max-width: 650px;
            margin: 15px auto 0;
            color: var(--gray);
        }

        .btn {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            padding: 14px 24px;
            border-radius: 8px;
            font-weight: 700;
            transition: 0.3s ease;
            cursor: pointer;
            border: none;
        }

        .btn-primary {
            background: var(--secondary);
            color: white;
        }

        .btn-primary:hover {
            background: var(--primary);
            transform: translateY(-2px);
        }

        .btn-outline {
            border: 2px solid rgba(255,255,255,0.7);
            color: white;
            background: transparent;
        }

        .btn-outline:hover {
            background: white;
            color: var(--primary);
        }


        /* =========================================================
           NAVIGATION
        ========================================================= */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            transition: 0.3s ease;
        }

        header.scrolled {
            background: rgba(6, 43, 70, 0.97);
            box-shadow: 0 5px 20px rgba(0,0,0,0.15);
        }

        nav {
            height: 78px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-family: "Montserrat", sans-serif;
            font-weight: 800;
            font-size: 1.15rem;
            color: white;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            align-items: center;
            gap: 30px;
        }

        .nav-links a {
            color: white;
            font-size: 0.9rem;
            font-weight: 600;
            position: relative;
        }

        .nav-links a::after {
            content: "";
            position: absolute;
            width: 0;
            height: 2px;
            bottom: -7px;
            left: 0;
            background: var(--accent);
            transition: 0.3s;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .menu-btn {
            display: none;
            color: white;
            font-size: 1.5rem;
            cursor: pointer;
        }


        /* =========================================================
           HERO
        ========================================================= */

        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            position: relative;
            overflow: hidden;

            background:
                linear-gradient(
                    135deg,
                    rgba(6, 43, 70, 0.97),
                    rgba(11, 61, 98, 0.90)
                ),
                url("https://images.unsplash.com/photo-1503387762-592deb58ef4e?auto=format&fit=crop&w=1800&q=80");

            background-size: cover;
            background-position: center;
            color: white;
        }

        .hero::before {
            content: "";
            position: absolute;
            width: 500px;
            height: 500px;
            border: 1px solid rgba(255,255,255,0.08);
            border-radius: 50%;
            right: -150px;
            top: 10%;
        }

        .hero::after {
            content: "";
            position: absolute;
            width: 700px;
            height: 700px;
            border: 1px solid rgba(255,255,255,0.05);
            border-radius: 50%;
            right: -250px;
            top: -5%;
        }

        .hero-content {
            position: relative;
            z-index: 2;
            max-width: 850px;
        }

        .hero-label {
            display: inline-flex;
            align-items: center;
            gap: 10px;
            background: rgba(255,255,255,0.1);
            border: 1px solid rgba(255,255,255,0.2);
            padding: 8px 14px;
            border-radius: 30px;
            font-size: 0.85rem;
            margin-bottom: 25px;
        }

        .hero-label i {
            color: var(--accent);
        }

        .hero h1 {
            font-size: clamp(2.8rem, 7vw, 5.5rem);
            line-height: 1.05;
            margin-bottom: 20px;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero-description {
            font-size: 1.15rem;
            max-width: 720px;
            color: rgba(255,255,255,0.82);
            margin-bottom: 35px;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            flex-wrap: wrap;
        }

        .hero-info {
            margin-top: 40px;
            display: flex;
            flex-wrap: wrap;
            gap: 25px;
        }

        .hero-info-item {
            display: flex;
            align-items: center;
            gap: 10px;
            color: rgba(255,255,255,0.85);
            font-size: 0.9rem;
        }

        .hero-info-item i {
            color: var(--accent);
        }


        /* =========================================================
           ABOUT
        ========================================================= */

        .about {
            background: var(--light);
        }

        .about-grid {
            display: grid;
            grid-template-columns: 0.9fr 1.1fr;
            gap: 70px;
            align-items: center;
        }

        .profile-card {
            background: var(--primary);
            color: white;
            padding: 45px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            position: relative;
            overflow: hidden;
        }

        .profile-card::after {
            content: "";
            position: absolute;
            width: 200px;
            height: 200px;
            border: 30px solid rgba(255,255,255,0.04);
            border-radius: 50%;
            right: -70px;
            bottom: -70px;
        }

        .profile-icon {
            width: 85px;
            height: 85px;
            border-radius: 50%;
            display: grid;
            place-items: center;
            background: rgba(255,255,255,0.1);
            font-size: 2.2rem;
            margin-bottom: 25px;
        }

        .profile-card h3 {
            font-size: 1.7rem;
            margin-bottom: 8px;
        }

        .profile-card .position {
            color: var(--accent);
            font-weight: 700;
            margin-bottom: 25px;
        }

        .profile-details {
            display: grid;
            gap: 15px;
        }

        .profile-detail {
            display: flex;
            gap: 12px;
            align-items: flex-start;
        }

        .profile-detail i {
            color: var(--accent);
            width: 20px;
            margin-top: 5px;
        }

        .about-text h3 {
            font-size: 2rem;
            color: var(--primary);
            margin-bottom: 20px;
        }

        .about-text p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .highlight-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 15px;
            margin-top: 30px;
        }

        .highlight {
            padding: 20px;
            background: white;
            border-radius: 10px;
            border: 1px solid var(--border);
            text-align: center;
        }

        .highlight i {
            font-size: 1.5rem;
            color: var(--secondary);
            margin-bottom: 8px;
        }

        .highlight h4 {
            font-size: 0.9rem;
            color: var(--primary);
        }


        /* =========================================================
           EXPERIENCE
        ========================================================= */

        .timeline {
            position: relative;
            max-width: 900px;
            margin: auto;
        }

        .timeline::before {
            content: "";
            position: absolute;
            left: 20px;
            top: 0;
            bottom: 0;
            width: 2px;
            background: var(--border);
        }

        .timeline-item {
            position: relative;
            padding-left: 70px;
            margin-bottom: 50px;
        }

        .timeline-dot {
            position: absolute;
            left: 8px;
            top: 5px;
            width: 25px;
            height: 25px;
            border-radius: 50%;
            background: var(--secondary);
            border: 5px solid white;
            box-shadow: 0 0 0 2px var(--secondary);
        }

        .timeline-card {
            background: white;
            border: 1px solid var(--border);
            border-radius: var(--radius);
            padding: 30px;
            box-shadow: var(--shadow);
        }

        .timeline-date {
            color: var(--secondary);
            font-weight: 700;
            font-size: 0.85rem;
            margin-bottom: 8px;
        }

        .timeline-card h3 {
            color: var(--primary);
            font-size: 1.35rem;
            margin-bottom: 5px;
        }

        .company {
            color: var(--gray);
            font-weight: 600;
            margin-bottom: 20px;
        }

        .timeline-card ul {
            list-style: none;
        }

        .timeline-card li {
            position: relative;
            padding-left: 22px;
            margin-bottom: 10px;
            color: var(--gray);
        }

        .timeline-card li::before {
            content: "▹";
            position: absolute;
            left: 0;
            color: var(--secondary);
            font-weight: bold;
        }


        /* =========================================================
           LICENSES
        ========================================================= */

        .licenses {
            background: var(--light);
        }

        .license-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .license-card {
            background: white;
            padding: 35px 28px;
            border-radius: var(--radius);
            border-top: 4px solid var(--secondary);
            box-shadow: var(--shadow);
            transition: 0.3s ease;
        }

        .license-card:hover {
            transform: translateY(-8px);
        }

        .license-icon {
            width: 55px;
            height: 55px;
            border-radius: 10px;
            display: grid;
            place-items: center;
            background: rgba(30,136,200,0.1);
            color: var(--secondary);
            font-size: 1.4rem;
            margin-bottom: 20px;
        }

        .license-card h3 {
            color: var(--primary);
            font-size: 1.1rem;
            margin-bottom: 10px;
        }

        .license-card p {
            color: var(--gray);
            font-size: 0.9rem;
        }

        .license-date {
            display: inline-block;
            margin-top: 15px;
            background: var(--light);
            color: var(--secondary);
            padding: 5px 10px;
            border-radius: 5px;
            font-size: 0.78rem;
            font-weight: 700;
        }


        /* =========================================================
           SKILLS
        ========================================================= */

        .skills-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
        }

        .skills-column h3 {
            color: var(--primary);
            margin-bottom: 25px;
            font-size: 1.3rem;
        }

        .skill {
            margin-bottom: 22px;
        }

        .skill-top {
            display: flex;
            justify-content: space-between;
            margin-bottom: 8px;
        }

        .skill-top span:first-child {
            font-weight: 600;
        }

        .skill-top span:last-child {
            color: var(--secondary);
            font-size: 0.8rem;
        }

        .skill-bar {
            height: 8px;
            background: #e9eef2;
            border-radius: 10px;
            overflow: hidden;
        }

        .skill-progress {
            height: 100%;
            background: linear-gradient(90deg, var(--primary), var(--secondary));
            border-radius: 10px;
            width: 0;
            transition: width 1.5s ease;
        }

        .soft-skills {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .soft-skill {
            padding: 10px 15px;
            border-radius: 30px;
            background: var(--light);
            color: var(--primary);
            border: 1px solid var(--border);
            font-size: 0.9rem;
            font-weight: 600;
        }


        /* =========================================================
           EDUCATION & TRAINING
        ========================================================= */

        .education {
            background: var(--light);
        }

        .education-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 30px;
        }

        .education-card,
        .training-card {
            background: white;
            padding: 35px;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
        }

        .education-card h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        .education-card .school {
            color: var(--secondary);
            font-weight: 700;
            margin-bottom: 8px;
        }

        .education-card .date {
            color: var(--gray);
            font-size: 0.9rem;
        }

        .training-list {
            display: grid;
            gap: 20px;
        }

        .training-item {
            display: flex;
            gap: 15px;
        }

        .training-icon {
            min-width: 42px;
            height: 42px;
            display: grid;
            place-items: center;
            border-radius: 8px;
            background: rgba(30,136,200,0.1);
            color: var(--secondary);
        }

        .training-item h4 {
            color: var(--primary);
            font-size: 0.95rem;
            margin-bottom: 4px;
        }

        .training-item p {
            color: var(--gray);
            font-size: 0.82rem;
        }


        /* =========================================================
           REFERENCES
        ========================================================= */

        .references-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .reference-card {
            padding: 30px;
            border: 1px solid var(--border);
            border-radius: var(--radius);
            transition: 0.3s;
        }

        .reference-card:hover {
            box-shadow: var(--shadow);
            transform: translateY(-5px);
        }

        .reference-icon {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--primary);
            color: white;
            display: grid;
            place-items: center;
            margin-bottom: 20px;
        }

        .reference-card h3 {
            color: var(--primary);
            font-size: 1rem;
        }

        .reference-card p {
            color: var(--gray);
            font-size: 0.85rem;
            margin-top: 5px;
        }


        /* =========================================================
           CONTACT
        ========================================================= */

        .contact {
            background: var(--primary);
            color: white;
        }

        .contact .section-header h2 {
            color: white;
        }

        .contact .section-header p {
            color: rgba(255,255,255,0.7);
        }

        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 25px;
        }

        .contact-card {
            text-align: center;
            padding: 35px 20px;
            background: rgba(255,255,255,0.06);
            border: 1px solid rgba(255,255,255,0.1);
            border-radius: var(--radius);
        }

        .contact-card i {
            color: var(--accent);
            font-size: 1.8rem;
            margin-bottom: 15px;
        }

        .contact-card h3 {
            font-size: 1rem;
            margin-bottom: 8px;
        }

        .contact-card p {
            color: rgba(255,255,255,0.7);
            font-size: 0.85rem;
            word-break: break-word;
        }

        .contact-button {
            text-align: center;
            margin-top: 40px;
        }


        /* =========================================================
           FOOTER
        ========================================================= */

        footer {
            background: #041f32;
            color: rgba(255,255,255,0.65);
            padding: 25px 0;
            text-align: center;
            font-size: 0.85rem;
        }

        footer strong {
            color: white;
        }


        /* =========================================================
           BACK TO TOP
        ========================================================= */

        #backToTop {
            position: fixed;
            right: 25px;
            bottom: 25px;
            width: 45px;
            height: 45px;
            border: none;
            border-radius: 8px;
            background: var(--secondary);
            color: white;
            cursor: pointer;
            opacity: 0;
            visibility: hidden;
            transition: 0.3s;
            z-index: 999;
        }

        #backToTop.show {
            opacity: 1;
            visibility: visible;
        }


        /* =========================================================
           ANIMATIONS
        ========================================================= */

        .fade-up {
            opacity: 0;
            transform: translateY(30px);
            transition: 0.7s ease;
        }

        .fade-up.visible {
            opacity: 1;
            transform: translateY(0);
        }


        /* =========================================================
           RESPONSIVE
        ========================================================= */

        @media (max-width: 900px) {

            .nav-links {
                position: absolute;
                top: 78px;
                left: 0;
                width: 100%;
                background: var(--primary-dark);
                flex-direction: column;
                align-items: flex-start;
                padding: 25px;
                gap: 20px;
                transform: translateY(-150%);
                transition: 0.3s ease;
            }

            .nav-links.active {
                transform: translateY(0);
            }

            .menu-btn {
                display: block;
            }

            .about-grid,
            .skills-grid,
            .education-grid {
                grid-template-columns: 1fr;
            }

            .license-grid,
            .references-grid {
                grid-template-columns: repeat(2, 1fr);
            }

        }


        @media (max-width: 600px) {

            section {
                padding: 75px 0;
            }

            .hero h1 {
                font-size: 2.8rem;
            }

            .hero-description {
                font-size: 1rem;
            }

            .hero-info {
                flex-direction: column;
                gap: 12px;
            }

            .profile-card {
                padding: 30px;
            }

            .highlight-grid {
                grid-template-columns: 1fr;
            }

            .license-grid,
            .references-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .timeline-item {
                padding-left: 50px;
            }

            .timeline::before {
                left: 10px;
            }

            .timeline-dot {
                left: -2px;
            }

            .timeline-card {
                padding: 22px;
            }

            .hero-buttons {
                flex-direction: column;
                align-items: stretch;
            }

            .btn {
                justify-content: center;
            }

        }

    </style>
</head>


<body>


<!-- =============================================================
     NAVIGATION
============================================================== -->

<header id="header">

    <div class="container">

        <nav>

            <a href="#home" class="logo">
                AMIEL <span>TAN</span>
            </a>

            <div class="nav-links" id="navLinks">

                <a href="#home">Home</a>
                <a href="#about">About</a>
                <a href="#experience">Experience</a>
                <a href="#licenses">Licenses</a>
                <a href="#skills">Skills</a>
                <a href="#education">Education</a>
                <a href="#contact">Contact</a>

            </div>

            <div class="menu-btn" id="menuBtn">
                <i class="fas fa-bars"></i>
            </div>

        </nav>

    </div>

</header>


<!-- =============================================================
     HERO
============================================================== -->

<section class="hero" id="home">

    <div class="container">

        <div class="hero-content fade-up">

            <div class="hero-label">
                <i class="fas fa-hard-hat"></i>
                Licensed Civil Engineer
            </div>

            <h1>
                Amiel Henrich<br>
                <span>A. Tan</span>
            </h1>

            <p class="hero-description">
                Civil Engineer specializing in materials testing,
                quality control, laboratory operations, and
                construction project documentation.
            </p>

            <div class="hero-buttons">

                <a href="#experience" class="btn btn-primary">
                    <i class="fas fa-briefcase"></i>
                    View Experience
                </a>

                <a href="#contact" class="btn btn-outline">
                    <i class="fas fa-envelope"></i>
                    Contact Me
                </a>

            </div>

            <div class="hero-info">

                <div class="hero-info-item">
                    <i class="fas fa-location-dot"></i>
                    Davao City, Philippines
                </div>

                <div class="hero-info-item">
                    <i class="fas fa-certificate"></i>
                    Licensed Since April 2024
                </div>

                <div class="hero-info-item">
                    <i class="fas fa-building"></i>
                    DPWH Accredited
                </div>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     ABOUT
============================================================== -->

<section class="about" id="about">

    <div class="container">

        <div class="section-header fade-up">

            <span>About Me</span>

            <h2>Engineering With Precision</h2>

            <p>
                A dedicated Civil Engineer committed to quality,
                accuracy, and continuous professional development.
            </p>

        </div>


        <div class="about-grid">

            <div class="profile-card fade-up">

                <div class="profile-icon">
                    <i class="fas fa-user-tie"></i>
                </div>

                <h3>Amiel Henrich A. Tan</h3>

                <div class="position">
                    Licensed Civil Engineer
                </div>

                <div class="profile-details">

                    <div class="profile-detail">
                        <i class="fas fa-location-dot"></i>
                        <span>Calinan, Davao City, Davao del Sur</span>
                    </div>

                    <div class="profile-detail">
                        <i class="fas fa-phone"></i>
                        <span>0925 771 0899</span>
                    </div>

                    <div class="profile-detail">
                        <i class="fas fa-envelope"></i>
                        <span>amieltan24@gmail.com</span>
                    </div>

                </div>

            </div>


            <div class="about-text fade-up">

                <h3>Building Quality Through Engineering</h3>

                <p>
                    I am a Licensed Civil Engineer with professional
                    experience in construction quality control,
                    materials testing, laboratory management, and
                    project documentation.
                </p>

                <p>
                    My experience includes working with construction
                    teams on road and bridge projects, performing and
                    documenting laboratory tests, monitoring materials,
                    maintaining laboratory records, and preparing
                    reports for contractors, consultants, and DPWH
                    personnel.
                </p>

                <p>
                    I value accuracy, teamwork, quality workmanship,
                    and continuous improvement in every project I
                    contribute to.
                </p>


                <div class="highlight-grid">

                    <div class="highlight">
                        <i class="fas fa-hard-hat"></i>
                        <h4>Construction</h4>
                    </div>

                    <div class="highlight">
                        <i class="fas fa-flask"></i>
                        <h4>Materials Testing</h4>
                    </div>

                    <div class="highlight">
                        <i class="fas fa-clipboard-check"></i>
                        <h4>Quality Control</h4>
                    </div>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     EXPERIENCE
============================================================== -->

<section id="experience">

    <div class="container">

        <div class="section-header fade-up">

            <span>Career</span>

            <h2>Professional Experience</h2>

            <p>
                Experience gained through construction,
                materials testing, laboratory management,
                and quality control.
            </p>

        </div>


        <div class="timeline">


            <!-- CURRENT POSITION -->

            <div class="timeline-item fade-up">

                <div class="timeline-dot"></div>

                <div class="timeline-card">

                    <div class="timeline-date">
                        September 24, 2024 – Present
                    </div>

                    <h3>JV Lab Technician / Lab Manager</h3>

                    <div class="company">
                        CAVDEAL / WECI / Coastland Construction
                        and Development Corporation – Joint Venture
                    </div>

                    <p>
                        Molave Homes, Phase 3, Indangan, Davao City
                    </p>

                    <br>

                    <ul>

                        <li>
                            Coordinate laboratory activities related
                            to quality control for the Davao Bypass
                            Construction Project, Package II,
                            North Section.
                        </li>

                        <li>
                            Conduct and document materials testing
                            including compression and flexural testing.
                        </li>

                        <li>
                            Provide results for concrete structures
                            including compression and flexural tests.
                        </li>

                        <li>
                            Provide thickness results for coring
                            specimens of Portland Cement Concrete
                            Pavement (PCCP).
                        </li>

                        <li>
                            Evaluate Cocolog samples based on required
                            diameter and weight.
                        </li>

                        <li>
                            Prepare and submit monthly materials
                            reports for contractors, consultants,
                            and DPWH personnel.
                        </li>

                        <li>
                            Monitor and update calibrated equipment
                            summary reports and plans.
                        </li>

                        <li>
                            Prepare Engineer's Certificates based on
                            monthly Statements of Work Accomplishment.
                        </li>

                        <li>
                            Prepare reports related to concrete works.
                        </li>

                        <li>
                            Monitor sample cards submitted by
                            contractors for report preparation.
                        </li>

                        <li>
                            Inspect and maintain Monthly Materials
                            Logbooks.
                        </li>

                        <li>
                            Monitor field and laboratory test status.
                        </li>

                        <li>
                            Prepare and submit test status reports.
                        </li>

                    </ul>

                </div>

            </div>


            <!-- INTERNSHIP -->

            <div class="timeline-item fade-up">

                <div class="timeline-dot"></div>

                <div class="timeline-card">

                    <div class="timeline-date">
                        March 14, 2022 – May 02, 2022
                    </div>

                    <h3>Civil Engineer Intern</h3>

                    <div class="company">
                        Ulticon Builders, Inc.
                    </div>

                    <p>
                        Don Julian Rodriguez Avenue, Ma-a,
                        Davao City
                    </p>

                    <br>

                    <ul>

                        <li>
                            Quantified contract plans for 2022
                            projects through materials estimation.
                        </li>

                        <li>
                            Learned fundamental quality control
                            procedures for road and bridge projects.
                        </li>

                        <li>
                            Conducted sieve analysis on aggregates.
                        </li>

                        <li>
                            Assisted in compression and flexural
                            testing of concrete samples.
                        </li>

                        <li>
                            Visited ongoing bridge construction
                            activities including board pile works.
                        </li>

                        <li>
                            Encoded road plan data for the
                            Engineering Department.
                        </li>

                        <li>
                            Encoded equipment time requirements
                            for the Fleet Department.
                        </li>

                        <li>
                            Observed material testing and roadwork
                            procedures under the MQC Department.
                        </li>

                    </ul>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     LICENSES
============================================================== -->

<section class="licenses" id="licenses">

    <div class="container">

        <div class="section-header fade-up">

            <span>Credentials</span>

            <h2>Licenses & Accreditation</h2>

            <p>
                Professional credentials supporting my work in
                civil engineering and construction quality control.
            </p>

        </div>


        <div class="license-grid">


            <div class="license-card fade-up">

                <div class="license-icon">
                    <i class="fas fa-certificate"></i>
                </div>

                <h3>Licensed Civil Engineer</h3>

                <p>
                    Civil Engineering Board Exam Passer
                </p>

                <span class="license-date">
                    April 2024
                </span>

            </div>


            <div class="license-card fade-up">

                <div class="license-icon">
                    <i class="fas fa-flask"></i>
                </div>

                <h3>DPWH Accredited Materials Engineer 1</h3>

                <p>
                    Department of Public Works and Highways
                    accreditation.
                </p>

                <span class="license-date">
                    March 2025
                </span>

            </div>


            <div class="license-card fade-up">

                <div class="license-icon">
                    <i class="fas fa-helmet-safety"></i>
                </div>

                <h3>DPWH Provisional Project Engineer</h3>

                <p>
                    Department of Public Works and Highways
                    provisional accreditation.
                </p>

                <span class="license-date">
                    June 2025
                </span>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     SKILLS
============================================================== -->

<section id="skills">

    <div class="container">

        <div class="section-header fade-up">

            <span>Capabilities</span>

            <h2>Skills & Expertise</h2>

            <p>
                A combination of technical knowledge,
                construction experience, and professional
                working skills.
            </p>

        </div>


        <div class="skills-grid">


            <div class="skills-column fade-up">

                <h3>
                    <i class="fas fa-laptop-code"></i>
                    Technical Skills
                </h3>


                <div class="skill">

                    <div class="skill-top">
                        <span>Microsoft Office Suite</span>
                        <span>Advanced</span>
                    </div>

                    <div class="skill-bar">
                        <div
                            class="skill-progress"
                            data-width="90%">
                        </div>
                    </div>

                </div>


                <div class="skill">

                    <div class="skill-top">
                        <span>Materials Testing</span>
                        <span>Advanced</span>
                    </div>

                    <div class="skill-bar">
                        <div
                            class="skill-progress"
                            data-width="88%">
                        </div>
                    </div>

                </div>


                <div class="skill">

                    <div class="skill-top">
                        <span>Quality Control</span>
                        <span>Advanced</span>
                    </div>

                    <div class="skill-bar">
                        <div
                            class="skill-progress"
                            data-width="88%">
                        </div>
                    </div>

                </div>


                <div class="skill">

                    <div class="skill-top">
                        <span>Construction Documentation</span>
                        <span>Advanced</span>
                    </div>

                    <div class="skill-bar">
                        <div
                            class="skill-progress"
                            data-width="85%">
                        </div>
                    </div>

                </div>


                <div class="skill">

                    <div class="skill-top">
                        <span>SketchUp</span>
                        <span>Intermediate</span>
                    </div>

                    <div class="skill-bar">
                        <div
                            class="skill-progress"
                            data-width="70%">
                        </div>
                    </div>

                </div>

            </div>


            <div class="skills-column fade-up">

                <h3>
                    <i class="fas fa-user-check"></i>
                    Professional Strengths
                </h3>

                <div class="soft-skills">

                    <span class="soft-skill">
                        Results-driven
                    </span>

                    <span class="soft-skill">
                        Quality-oriented
                    </span>

                    <span class="soft-skill">
                        Collaborative
                    </span>

                    <span class="soft-skill">
                        Industrious
                    </span>

                    <span class="soft-skill">
                        Detail-oriented
                    </span>

                    <span class="soft-skill">
                        Problem Solving
                    </span>

                    <span class="soft-skill">
                        Documentation
                    </span>

                    <span class="soft-skill">
                        Teamwork
                    </span>

                </div>

                <br><br>

                <h3>
                    <i class="fas fa-list-check"></i>
                    Areas of Expertise
                </h3>

                <div class="soft-skills">

                    <span class="soft-skill">
                        Materials Testing
                    </span>

                    <span class="soft-skill">
                        Concrete Testing
                    </span>

                    <span class="soft-skill">
                        Aggregate Testing
                    </span>

                    <span class="soft-skill">
                        Laboratory Management
                    </span>

                    <span class="soft-skill">
                        Quality Control
                    </span>

                    <span class="soft-skill">
                        Construction
                    </span>

                    <span class="soft-skill">
                        Technical Reporting
                    </span>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     EDUCATION & TRAINING
============================================================== -->

<section class="education" id="education">

    <div class="container">

        <div class="section-header fade-up">

            <span>Academic Background</span>

            <h2>Education & Training</h2>

        </div>


        <div class="education-grid">


            <!-- EDUCATION -->

            <div class="education-card fade-up">

                <h3>
                    <i class="fas fa-graduation-cap"></i>
                    Bachelor of Science in Civil Engineering
                </h3>

                <div class="school">
                    Mapúa Malayan Colleges Mindanao
                </div>

                <div class="date">
                    McArthur Highway, Matina, Davao City
                </div>

                <br>

                <p>
                    Graduation Date:
                    <strong>July 31, 2023</strong>
                </p>

                <br>

                <p>
                    <strong>Organization:</strong>
                    JPICE – MMCM Member
                </p>

            </div>


            <!-- TRAINING -->

            <div class="training-card fade-up">

                <div class="training-list">


                    <div class="training-item">

                        <div class="training-icon">
                            <i class="fas fa-building"></i>
                        </div>

                        <div>

                            <h4>
                                Construction Project Management 101:
                                Latest Trends & Best Practices
                            </h4>

                            <p>
                                MST Connect – Educational Consultancy
                                | July 02, 2023
                            </p>

                        </div>

                    </div>


                    <div class="training-item">

                        <div class="training-icon">
                            <i class="fas fa-calculator"></i>
                        </div>

                        <div>

                            <h4>
                                Manual Construction Building Estimates
                                with Microsoft Excel and AutoCAD
                            </h4>

                            <p>
                                MST Connect – Educational Consultancy
                                | June 14, 2024
                            </p>

                            <p>
                                Approved 5 CPD Points
                            </p>

                        </div>

                    </div>


                    <div class="training-item">

                        <div class="training-icon">
                            <i class="fas fa-solar-panel"></i>
                        </div>

                        <div>

                            <h4>
                                Photovoltaic System Installer (PVSI)
                            </h4>

                            <p>
                                TESDA – Technical Education and
                                Skills Development Authority
                            </p>

                            <p>
                                National Certificate II | May 31, 2023
                            </p>

                        </div>

                    </div>


                </div>

            </div>

        </div>

    </div>

</section>


<!-- =============================================================
     REFERENCES
============================================================== -->

<section id="references">

    <div class="container">

        <div class="section-header fade-up">

            <span>Professional Network</span>

            <h2>References</h2>

            <p>
                Professional references available upon request.
            </p>

        </div>


        <div class="references-grid">


            <div class="reference-card fade-up">

                <div class="reference-icon">
                    <i class="fas fa-user-tie"></i>
                </div>

                <h3>
                    Engr. Daryl Papevera
                </h3>

                <p>
                    Project Engineer
                </p>

                <p>
                    Ulticon Builders, Inc.
                </p>

            </div>


            <div class="reference-card fade-up">

                <div class="reference-icon">
                    <i class="fas fa-user-tie"></i>
                </div>

                <h3>
                    Atty. Kristine C. Javier
                </h3>

                <p>
                    AVP-HR & Admin
                </p>

                <p>
                    Ulticon Builders, Inc.
                </p>

            </div>


            <div class="reference-card fade-up">

                <div class="reference-icon">
                    <i class="fas fa-user-tie"></i>
                </div>

                <h3>
                    Engr. Kevin Kimpooi Babate
                </h3>

                <p>
                    Kwiver Construction OPC
                </p>

            </div>


        </div>

    </div>

</section>


<!-- =============================================================
     CONTACT
============================================================== -->

<section class="contact" id="contact">

    <div class="container">

        <div class="section-header fade-up">

            <span>Get In Touch</span>

            <h2>Let's Work Together</h2>

            <p>
                Interested in discussing a construction project,
                engineering opportunity, or professional
                collaboration? Feel free to reach out.
            </p>

        </div>


        <div class="contact-grid">


            <div class="contact-card fade-up">

                <i class="fas fa-envelope"></i>

                <h3>Email</h3>

                <p>
                    amieltan24@gmail.com
                </p>

            </div>


            <div class="contact-card fade-up">

                <i class="fas fa-phone"></i>

                <h3>Phone</h3>

                <p>
                    0925 771 0899
                </p>

            </div>


            <div class="contact-card fade-up">

                <i class="fas fa-location-dot"></i>

                <h3>Location</h3>

                <p>
                    Calinan, Davao City,
                    Davao del Sur, Philippines
                </p>

            </div>


        </div>


        <div class="contact-button">

            <a
                href="mailto:amieltan24@gmail.com"
                class="btn btn-primary"
            >
                <i class="fas fa-paper-plane"></i>
                Send Me an Email
            </a>

        </div>

    </div>

</section>


<!-- =============================================================
     FOOTER
============================================================== -->

<footer>

    <div class="container">

        <p>
            © <span id="year"></span>
            <strong>Amiel Henrich A. Tan</strong>.
            All Rights Reserved.
        </p>

        <p>
            Licensed Civil Engineer | DPWH Accredited Materials Engineer
        </p>

    </div>

</footer>


<!-- BACK TO TOP -->

<button id="backToTop" aria-label="Back to top">
    <i class="fas fa-arrow-up"></i>
</button>


<!-- =============================================================
     JAVASCRIPT
============================================================== -->

<script>

    /* =========================================================
       MOBILE MENU
    ========================================================= */

    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", () => {

        navLinks.classList.toggle("active");

        const icon = menuBtn.querySelector("i");

        if (navLinks.classList.contains("active")) {
            icon.classList.remove("fa-bars");
            icon.classList.add("fa-xmark");
        } else {
            icon.classList.remove("fa-xmark");
            icon.classList.add("fa-bars");
        }

    });


    /* Close mobile menu after clicking a link */

    document.querySelectorAll(".nav-links a").forEach(link => {

        link.addEventListener("click", () => {

            navLinks.classList.remove("active");

            const icon = menuBtn.querySelector("i");

            icon.classList.remove("fa-xmark");
            icon.classList.add("fa-bars");

        });

    });


    /* =========================================================
       HEADER ON SCROLL
    ========================================================= */

    const header = document.getElementById("header");

    window.addEventListener("scroll", () => {

        if (window.scrollY > 50) {
            header.classList.add("scrolled");
        } else {
            header.classList.remove("scrolled");
        }

    });


    /* =========================================================
       BACK TO TOP
    ========================================================= */

    const backToTop = document.getElementById("backToTop");

    window.addEventListener("scroll", () => {

        if (window.scrollY > 500) {
            backToTop.classList.add("show");
        } else {
            backToTop.classList.remove("show");
        }

    });

    backToTop.addEventListener("click", () => {

        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });

    });


    /* =========================================================
       CURRENT YEAR
    ========================================================= */

    document.getElementById("year").textContent =
        new Date().getFullYear();


    /* =========================================================
       SCROLL ANIMATION
    ========================================================= */

    const animatedElements =
        document.querySelectorAll(".fade-up");

    const observer = new IntersectionObserver(
        (entries) => {

            entries.forEach(entry => {

                if (entry.isIntersecting) {

                    entry.target.classList.add("visible");

                    observer.unobserve(entry.target);

                }

            });

        },
        {
            threshold: 0.12
        }
    );


    animatedElements.forEach(element => {
        observer.observe(element);
    });


    /* =========================================================
       SKILL BAR ANIMATION
    ========================================================= */

    const skillBars =
        document.querySelectorAll(".skill-progress");

    const skillObserver = new IntersectionObserver(
        (entries) => {

            entries.forEach(entry => {

                if (entry.isIntersecting) {

                    const width =
                        entry.target.getAttribute("data-width");

                    entry.target.style.width = width;

                    skillObserver.unobserve(entry.target);

                }

            });

        },
        {
            threshold: 0.5
        }
    );


    skillBars.forEach(bar => {
        skillObserver.observe(bar);
    });


    /* =========================================================
       ACTIVE NAVIGATION
    ========================================================= */

    const sections =
        document.querySelectorAll("section[id]");

    const navItems =
        document.querySelectorAll(".nav-links a");

    window.addEventListener("scroll", () => {

        let current = "";

        sections.forEach(section => {

            const sectionTop =
                section.offsetTop - 150;

            if (window.scrollY >= sectionTop) {
                current = section.getAttribute("id");
            }

        });

        navItems.forEach(link => {

            link.style.color = "white";

            if (
                link.getAttribute("href") ===
                "#" + current
            ) {
                link.style.color = "#f5a623";
            }

        });

    });

</script>

</body>
</html>

