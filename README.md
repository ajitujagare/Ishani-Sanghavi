<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ishani Sanghavi | Growing Between Reps and Healing</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">
    <style>
        :root {
            --primary: #ff0066;
            --secondary: #222;
            --dark: #121212;
            --light: #f5f5f5;
            --accent: #00ff88;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--dark);
            color: var(--light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background-color: rgba(18, 18, 18, 0.9);
            backdrop-filter: blur(10px);
            padding: 1rem 2rem;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--accent);
            text-decoration: none;
        }

        .nav-links {
            display: flex;
            gap: 2rem;
        }

        .nav-links a {
            color: var(--light);
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .social-icons {
            display: flex;
            gap: 1rem;
        }

        .social-icons a {
            color: var(--light);
            font-size: 1.2rem;
            transition: color 0.3s;
        }

        .social-icons a:hover {
            color: var(--accent);
        }

        .hamburger {
            display: none;
            cursor: pointer;
        }

        .hero {
            height: 100vh;
            background: linear-gradient(rgba(0, 0, 0, 0.7), rgba(0, 0, 0, 0.7)), url(' /home/ajit/Downloads/hero1.png') no-repeat center center/cover;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 2rem;
        }

        .hero-content {
            max-width: 800px;
            animation: fadeIn 1.5s ease-in-out;
        }

        .hero h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
            color: var(--light);
        }

        .hero p {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            color: var(--light);
        }

        .hero-links {
            display: flex;
            gap: 1rem;
            margin-bottom: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .hero-links a {
            color: var(--light);
            font-size: 1.5rem;
            transition: color 0.3s;
        }

        .hero-links a:hover {
            color: var(--accent);
        }

        .cta-buttons {
            display: flex;
            gap: 1rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .btn {
            padding: 0.8rem 1.8rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            text-decoration: none;
            display: inline-block;
            text-align: center;
        }

        .btn-primary {
            background-color: var(--primary);
            color: white;
        }

        .btn-primary:hover {
            background-color: var(--accent);
            transform: translateY(-3px);
        }

        .btn-secondary {
            background-color: transparent;
            color: var(--light);
            border: 1px solid var(--light);
        }

        .btn-secondary:hover {
            background-color: var(--light);
            color: var(--dark);
        }

        .about {
            padding: 5rem 2rem;
            background-color: var(--dark);
            background-image: linear-gradient(rgba(18, 18, 18, 0.9), rgba(18, 18, 18, 0.9)), url('https://mistralaichatupprodswe.blob.core.windows.net/chat-images/3f/0f/0a/3f0f0a7a-d392-4c22-9aea-8917285412e0/50be6004-1d05-4728-80a3-721f662bea44/b38f7e94-7721-4b32-bc3a-b7c41f7e8839?sv=2025-01-05&st=2026-03-22T13%3A37%3A52Z&se=2026-03-22T14%3A37%3A52Z&sr=b&sp=r&sig=xf3DVX%2BfZ4j0KsFXxol%2Bc3781iBDwJEbPXX1x8PJqbo%3D');
            background-size: cover;
            background-position: center;
            background-attachment: fixed;
        }

        .about-container {
            max-width: 1200px;
            margin: 0 auto;
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 2rem;
        }

        .about-content {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            gap: 2rem;
        }

        .profile-img {
            width: 200px;
            height: 200px;
            border-radius: 50%;
            object-fit: cover;
            border: 3px solid var(--accent);
        }

        .stats {
            display: flex;
            gap: 2rem;
            flex-wrap: wrap;
            justify-content: center;
        }

        .stat {
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: 700;
            color: var(--accent);
            margin-bottom: 0.5rem;
        }

        .stat-text {
            font-size: 1rem;
            color: var(--light);
        }

        .section {
            padding: 5rem 2rem;
        }

        .section-title {
            text-align: center;
            margin-bottom: 3rem;
            font-size: 2.5rem;
            color: var(--light);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .card {
            background-color: var(--secondary);
            border-radius: 10px;
            overflow: hidden;
            transition: transform 0.3s;
        }

        .card:hover {
            transform: translateY(-10px);
        }

        .card-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .card-content {
            padding: 1.5rem;
        }

        .card-content h3 {
            margin-bottom: 1rem;
            color: var(--light);
        }

        .card-content p {
            margin-bottom: 1.5rem;
            color: var(--light);
        }

        .reels-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 1.5rem;
        }

        .reel-card {
            position: relative;
            aspect-ratio: 9/16;
            border-radius: 10px;
            overflow: hidden;
        }

        .reel-card img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .reel-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: rgba(0, 0, 0, 0.5);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .reel-card:hover .reel-overlay {
            opacity: 1;
        }

        .reel-overlay i {
            color: white;
            font-size: 3rem;
            margin: 0 1rem;
        }

        .posts-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .post-card {
            background-color: var(--secondary);
            border-radius: 10px;
            overflow: hidden;
        }

        .post-img {
            width: 100%;
            height: 200px;
            object-fit: cover;
        }

        .post-content {
            padding: 1.5rem;
        }

        .post-content h3 {
            margin-bottom: 1rem;
            color: var(--light);
        }

        .post-content p {
            color: var(--light);
            margin-bottom: 1rem;
        }

        .instagram-follow {
            text-align: center;
            margin: 3rem 0;
        }

        .instagram-follow-btn {
            background: linear-gradient(45deg, #f09433 0%,#e6683c 25%,#dc2743 50%,#cc2366 75%,#bc1888 100%);
            color: white;
            padding: 0.8rem 2rem;
            border: none;
            border-radius: 50px;
            font-weight: 600;
            cursor: pointer;
            text-decoration: none;
            display: inline-block;
        }

        .instagram-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 1rem;
        }

        .instagram-post {
            position: relative;
            aspect-ratio: 1;
            overflow: hidden;
            border-radius: 10px;
        }

        .instagram-post img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.3s;
        }

        .instagram-post:hover img {
            transform: scale(1.1);
        }

        .instagram-overlay {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background-color: rgba(0, 0, 0, 0.5);
            display: flex;
            justify-content: center;
            align-items: center;
            opacity: 0;
            transition: opacity 0.3s;
        }

        .instagram-post:hover .instagram-overlay {
            opacity: 1;
        }

        .instagram-overlay i {
            color: white;
            font-size: 2rem;
            margin: 0 0.5rem;
        }

        .contact-form {
            width: 100%;
            max-width: 500px;
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin: 0 auto;
        }

        .form-group {
            display: flex;
            flex-direction: column;
            gap: 0.5rem;
        }

        .form-group input,
        .form-group textarea {
            padding: 0.8rem;
            border: none;
            border-radius: 5px;
            background-color: var(--secondary);
            color: var(--light);
        }

        .form-group textarea {
            min-height: 150px;
            resize: vertical;
        }

        footer {
            background-color: var(--secondary);
            padding: 2rem;
            text-align: center;
        }

        .footer-links {
            display: flex;
            justify-content: center;
            gap: 2rem;
            margin-bottom: 1rem;
            flex-wrap: wrap;
        }

        .footer-links a {
            color: var(--light);
            text-decoration: none;
        }

        .footer-links a:hover {
            color: var(--accent);
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                flex-direction: column;
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background-color: rgba(18, 18, 18, 0.9);
                padding: 1rem;
                gap: 1rem;
            }

            .nav-links.active {
                display: flex;
            }

            .hamburger {
                display: block;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .stats {
                flex-direction: column;
                gap: 1rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <a href="#" class="logo">Ishani Sanghavi</a>
        <nav class="nav-links">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#programs">Programs</a>
            <a href="#reels">Reels</a>
            <a href="#posts">Posts</a>
            <a href="#contact">Contact</a>
        </nav>
        <div class="social-icons">
            <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://www.youtube.com/@_ishani_sanghavi" target="_blank"><i class="fab fa-youtube"></i></a>
            <a href="https://www.tiktok.com/@ishanisanghavi" target="_blank"><i class="fab fa-tiktok"></i></a>
        </div>
        <div class="hamburger">
            <i class="fas fa-bars"></i>
        </div>
    </header>

    <section class="hero" id="home">
        <div class="hero-content">
            <h1>Growing Between Reps and Healing</h1>
            <p>Break stereotypes, embrace strength, and transform your life with my fitness and dance programs.</p>
            <div class="hero-links">
                <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank"><i class="fab fa-instagram"></i></a>
                <a href="https://www.youtube.com/@_ishani_sanghavi" target="_blank"><i class="fab fa-youtube"></i></a>
                <a href="https://www.tiktok.com/@ishanisanghavi" target="_blank"><i class="fab fa-tiktok"></i></a>
            </div>
            <div class="cta-buttons">
                <a href="https://www.instagram.com/_ishani_sanghavi/" class="btn btn-primary" target="_blank">Follow Me on Instagram</a>
                <a href="#programs" class="btn btn-secondary">Join My Programs</a>
            </div>
        </div>
    </section>

    <section class="about" id="about">
        <div class="about-container">
            <h2 class="section-title" style="color: var(--light);">About Me</h2>
            <div class="about-content">
                <img src="https://qoruz.com/_next/image?url=https%3A%2F%2Flive-qoruz.sgp1.digitaloceanspaces.com%2Fprofile_images%2Fishani_sanghavi_original_1773727596.645015.JPEG&w=256&q=75" alt="Ishani Sanghavi" class="profile-img">
                <p style="max-width: 600px; margin: 0 auto; font-size: 1.1rem;">Hi, I'm Ishani Sanghavi—a fitness influencer, belly dancer, and co-founder of @thearmourstrength and @muscleblaze. My mission is to motivate you to hit the gym, break barriers, and live your best life. With over 1M followers, I'm here to inspire and guide your fitness journey.</p>
                <div class="stats">
                    <div class="stat">
                        <div class="stat-number" data-aos="flip-up">1M+</div>
                        <div class="stat-text">Followers</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number" data-aos="flip-up">500+</div>
                        <div class="stat-text">Transformations</div>
                    </div>
                    <div class="stat">
                        <div class="stat-number" data-aos="flip-up">2</div>
                        <div class="stat-text">Brands Co-founded</div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="programs">
        <div class="container">
            <h2 class="section-title">My Programs</h2>
            <div class="grid">
                <div class="card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/7e/8a/83/7e8a830745da9c08f112f696e289db19.jpg" alt="Fitness Program" class="card-img">
                    <div class="card-content">
                        <h3>8-Week Shred</h3>
                        <p>Get shredded and strong with my signature workout plan.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
                <div class="card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/6b/c1/d3/6bc1d3816376438f9c4a65db5b88bc0a.jpg" alt="Belly Dance" class="card-img">
                    <div class="card-content">
                        <h3>Belly Dance Masterclass</h3>
                        <p>Learn the art of belly dancing and connect with your body.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
                <div class="card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/43/e0/3f/43e03fd75c2aded784c32d7637294e36.jpg" alt="Nutrition Guide" class="card-img">
                    <div class="card-content">
                        <h3>Nutrition Guide</h3>
                        <p>Fuel your body right with my custom meal plans.</p>
                        <a href="#" class="btn btn-primary">Learn More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="reels">
        <div class="container">
            <h2 class="section-title">Viral Reels</h2>
            <div class="reels-grid">
                <div class="reel-card" data-aos="zoom-in">
                    <img src="https://i.pinimg.com/originals/7e/8a/83/7e8a830745da9c08f112f696e289db19.jpg" alt="Viral Reel">
                    <div class="reel-overlay">
                        <a href="https://www.instagram.com/reel/..." target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.tiktok.com/..." target="_blank" style="color: white;"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
                <div class="reel-card" data-aos="zoom-in">
                    <img src="https://i.pinimg.com/originals/6b/c1/d3/6bc1d3816376438f9c4a65db5b88bc0a.jpg" alt="Viral Reel">
                    <div class="reel-overlay">
                        <a href="https://www.instagram.com/reel/..." target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.tiktok.com/..." target="_blank" style="color: white;"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
                <div class="reel-card" data-aos="zoom-in">
                    <img src="https://i.pinimg.com/originals/43/e0/3f/43e03fd75c2aded784c32d7637294e36.jpg" alt="Viral Reel">
                    <div class="reel-overlay">
                        <a href="https://www.instagram.com/reel/..." target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.tiktok.com/..." target="_blank" style="color: white;"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
                <div class="reel-card" data-aos="zoom-in">
                    <img src="https://i.pinimg.com/originals/6f/94/83/6f9483bab053e11d415b7670a6a7675f.jpg" alt="Viral Reel">
                    <div class="reel-overlay">
                        <a href="https://www.instagram.com/reel/..." target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                        <a href="https://www.tiktok.com/..." target="_blank" style="color: white;"><i class="fab fa-tiktok"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="posts">
        <div class="container">
            <h2 class="section-title">Latest Posts</h2>
            <div class="posts-grid">
                <div class="post-card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/7e/8a/83/7e8a830745da9c08f112f696e289db19.jpg" alt="Post" class="post-img">
                    <div class="post-content">
                        <h3>How I Stay Motivated</h3>
                        <p>Read my latest blog post on staying motivated and consistent with your fitness goals.</p>
                        <a href="#" class="btn btn-primary">Read More</a>
                    </div>
                </div>
                <div class="post-card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/6b/c1/d3/6bc1d3816376438f9c4a65db5b88bc0a.jpg" alt="Post" class="post-img">
                    <div class="post-content">
                        <h3>My Fitness Journey</h3>
                        <p>Learn about my fitness journey and how I overcame challenges to become who I am today.</p>
                        <a href="#" class="btn btn-primary">Read More</a>
                    </div>
                </div>
                <div class="post-card" data-aos="fade-up">
                    <img src="https://i.pinimg.com/originals/43/e0/3f/43e03fd75c2aded784c32d7637294e36.jpg" alt="Post" class="post-img">
                    <div class="post-content">
                        <h3>Nutrition Tips</h3>
                        <p>Discover my top nutrition tips for a healthier lifestyle.</p>
                        <a href="#" class="btn btn-primary">Read More</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section">
        <div class="container">
            <div class="instagram-follow">
                <a href="https://www.instagram.com/_ishani_sanghavi/" class="instagram-follow-btn" target="_blank">Follow Me on Instagram</a>
            </div>
            <h2 class="section-title">Instagram Feed</h2>
            <div class="instagram-grid">
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/7e/8a/83/7e8a830745da9c08f112f696e289db19.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/6b/c1/d3/6bc1d3816376438f9c4a65db5b88bc0a.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/43/e0/3f/43e03fd75c2aded784c32d7637294e36.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/6f/94/83/6f9483bab053e11d415b7670a6a7675f.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/9d/47/01/9d4701841956a9c6523ce73cbf2e254d.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
                <div class="instagram-post" data-aos="flip-left">
                    <img src="https://i.pinimg.com/originals/59/bf/b2/59bfb289a26d03938f9fdd16277b9b22.jpg" alt="Instagram Post">
                    <div class="instagram-overlay">
                        <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank" style="color: white;"><i class="fab fa-instagram"></i></a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="section" id="contact">
        <div class="container">
            <h2 class="section-title">Get in Touch</h2>
            <form class="contact-form">
                <div class="form-group">
                    <label for="name">Name</label>
                    <input type="text" id="name" placeholder="Your Name" required>
                </div>
                <div class="form-group">
                    <label for="email">Email</label>
                    <input type="email" id="email" placeholder="Your Email" required>
                </div>
                <div class="form-group">
                    <label for="message">Message</label>
                    <textarea id="message" placeholder="Your Message" required></textarea>
                </div>
                <button type="submit" class="btn btn-primary">Send Message</button>
            </form>
        </div>
    </section>

    <footer>
        <div class="footer-links">
            <a href="#home">Home</a>
            <a href="#about">About</a>
            <a href="#programs">Programs</a>
            <a href="#reels">Reels</a>
            <a href="#posts">Posts</a>
            <a href="#contact">Contact</a>
        </div>
        <div class="social-icons">
            <a href="https://www.instagram.com/_ishani_sanghavi/" target="_blank"><i class="fab fa-instagram"></i></a>
            <a href="https://www.youtube.com/@_ishani_sanghavi" target="_blank"><i class="fab fa-youtube"></i></a>
            <a href="https://www.tiktok.com/@ishanisanghavi" target="_blank"><i class="fab fa-tiktok"></i></a>
        </div>
        <p>&copy; 2026 Ishani Sanghavi. All rights reserved.</p>
    </footer>

    <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
    <script>
        AOS.init({
            duration: 1000,
            once: true,
        });

        const hamburger = document.querySelector('.hamburger');
        const navLinks = document.querySelector('.nav-links');

        hamburger.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
                navLinks.classList.remove('active');
            });
        });

        const counters = document.querySelectorAll('.stat-number');
        const speed = 200;

        counters.forEach(counter => {
            const updateCount = () => {
                const target = +counter.getAttribute('data-target') || +counter.innerText.replace('+', '');
                const count = +counter.innerText.replace('+', '');
                const increment = target / speed;

                if (count < target) {
                    counter.innerText = Math.ceil(count + increment) + (counter.innerText.includes('+') ? '+' : '');
                    setTimeout(updateCount, 1);
                } else {
                    counter.innerText = target + (counter.innerText.includes('+') ? '+' : '');
                }
            };

            updateCount();
        });

        const contactForm = document.querySelector('.contact-form');
        contactForm.addEventListener('submit', (e) => {
            e.preventDefault();
            alert('Thank you for your message! I will get back to you soon.');
            contactForm.reset();
        });
    </script>
</body>
</html>
