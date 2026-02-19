<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Shulochana Chemicals | Premium Cleaning Solutions</title>
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&family=Roboto:wght@300;400;500&display=swap" rel="stylesheet">
    
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- CSS VARIABLES --- */
        :root {
            --bg-dark: #121212;
            --bg-light: #1a1a1a;
            --primary: #00d4ff;
            --primary-dark: #00a8cc;
            --secondary: #ff6b35;
            --text-light: #ffffff;
            --text-gray: #b0b0b0;
            --gradient: linear-gradient(135deg, #00d4ff 0%, #00a8cc 100%);
        }

        /* --- RESET & BASE STYLES --- */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background-color: var(--bg-dark);
            color: var(--text-light);
            line-height: 1.6;
            overflow-x: hidden;
        }

        h1, h2, h3, h4, h5, h6 {
            font-family: 'Poppins', sans-serif;
            font-weight: 600;
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
            height: auto;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* --- HEADER --- */
        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            z-index: 1000;
            background: rgba(18, 18, 18, 0.95);
            backdrop-filter: blur(10px);
            padding: 15px 0;
            transition: all 0.3s ease;
        }

        header.scrolled {
            padding: 10px 0;
            box-shadow: 0 2px 20px rgba(0, 212, 255, 0.1);
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-family: 'Poppins', sans-serif;
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary);
        }

        .logo span {
            color: var(--text-light);
        }

        .nav-links {
            display: flex;
            gap: 30px;
        }

        .nav-links a {
            font-weight: 500;
            transition: color 0.3s ease;
            position: relative;
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--primary);
            transition: width 0.3s ease;
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .mobile-menu-btn {
            display: none;
            font-size: 1.5rem;
            cursor: pointer;
            color: var(--text-light);
        }

        /* --- HERO SECTION --- */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding-top: 80px;
            background: 
                radial-gradient(ellipse at 20% 50%, rgba(0, 212, 255, 0.1) 0%, transparent 50%),
                radial-gradient(ellipse at 80% 20%, rgba(255, 107, 53, 0.05) 0%, transparent 40%),
                var(--bg-dark);
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: url("data:image/svg+xml,%3Csvg width='60' height='60' viewBox='0 0 60 60' xmlns='http://www.w3.org/2000/svg'%3E%3Cg fill='none' fill-rule='evenodd'%3E%3Cg fill='%2300d4ff' fill-opacity='0.03'%3E%3Cpath d='M36 34v-4h-2v4h-4v2h4v4h2v-4h4v-2h-4zm0-30V0h-2v4h-4v2h4v4h2V6h4V4h-4zM6 34v-4H4v4H0v2h4v4h2v-4h4v-2H6zM6 4V0H4v4H0v2h4v4h2V6h4V4H6z'/%3E%3C/g%3E%3C/g%3E%3C/svg%3E");
            opacity: 0.5;
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 700px;
        }

        .hero-badge {
            display: inline-block;
            background: rgba(0, 212, 255, 0.1);
            border: 1px solid rgba(0, 212, 255, 0.3);
            padding: 8px 20px;
            border-radius: 50px;
            font-size: 0.9rem;
            color: var(--primary);
            margin-bottom: 20px;
            animation: fadeInUp 0.6s ease forwards;
        }

        .hero h1 {
            font-size: 3.5rem;
            line-height: 1.2;
            margin-bottom: 20px;
            animation: fadeInUp 0.6s ease 0.1s forwards;
            opacity: 0;
        }

        .hero h1 span {
            background: var(--gradient);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .hero p {
            font-size: 1.1rem;
            color: var(--text-gray);
            margin-bottom: 30px;
            animation: fadeInUp 0.6s ease 0.2s forwards;
            opacity: 0;
        }

        .hero-buttons {
            display: flex;
            gap: 15px;
            animation: fadeInUp 0.6s ease 0.3s forwards;
            opacity: 0;
        }

        .btn {
            padding: 12px 30px;
            border-radius: 8px;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            display: inline-flex;
            align-items: center;
            gap: 8px;
        }

        .btn-primary {
            background: var(--gradient);
            color: var(--bg-dark);
        }

        .btn-primary:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.3);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid var(--primary);
            color: var(--primary);
        }

        .btn-secondary:hover {
            background: var(--primary);
            color: var(--bg-dark);
        }

        .hero-image {
            position: absolute;
            right: -100px;
            top: 50%;
            transform: translateY(-50%);
            width: 500px;
            opacity: 0.2;
            animation: float 6s ease-in-out infinite;
        }

        @keyframes float {
            0%, 100% { transform: translateY(-50%) translateX(0); }
            50% { transform: translateY(-55%) translateX(-20px); }
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

        /* --- SECTION STYLES --- */
        section {
            padding: 80px 0;
        }

        .section-header {
            text-align: center;
            margin-bottom: 50px;
        }

        .section-header h2 {
            font-size: 2.5rem;
            margin-bottom: 15px;
        }

        .section-header p {
            color: var(--text-gray);
            max-width: 600px;
            margin: 0 auto;
        }

        .section-header .line {
            width: 60px;
            height: 4px;
            background: var(--gradient);
            margin: 15px auto 0;
            border-radius: 2px;
        }

        /* --- PRODUCTS SECTION --- */
        .products {
            background: var(--bg-light);
        }

        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .product-card {
            background: var(--bg-dark);
            border-radius: 15px;
            overflow: hidden;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .product-card:hover {
            transform: translateY(-10px);
            border-color: rgba(0, 212, 255, 0.3);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
        }

        .product-image {
            height: 200px;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.1) 0%, rgba(255, 107, 53, 0.1) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 4rem;
            color: var(--primary);
        }

        .product-info {
            padding: 25px;
        }

        .product-info h3 {
            font-size: 1.3rem;
            margin-bottom: 10px;
        }

        .product-info p {
            color: var(--text-gray);
            font-size: 0.95rem;
            margin-bottom: 15px;
        }

        .product-price {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--secondary);
        }

        .product-btn {
            margin-top: 15px;
            width: 100%;
            padding: 10px;
            background: transparent;
            border: 1px solid var(--primary);
            color: var(--primary);
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .product-btn:hover {
            background: var(--primary);
            color: var(--bg-dark);
        }

        /* --- SERVICES SECTION --- */
        .services {
            background: var(--bg-dark);
        }

        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }

        .service-card {
            background: var(--bg-light);
            padding: 40px 30px;
            border-radius: 15px;
            text-align: center;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.05);
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: rgba(0, 212, 255, 0.3);
        }

        .service-icon {
            width: 80px;
            height: 80px;
            background: var(--gradient);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 25px;
            font-size: 2rem;
            color: var(--bg-dark);
        }

        .service-card h3 {
            font-size: 1.4rem;
            margin-bottom: 15px;
        }

        .service-card p {
            color: var(--text-gray);
            line-height: 1.7;
        }

        /* --- ABOUT SECTION --- */
        .about {
            background: var(--bg-light);
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
            align-items: center;
        }

        .about-text h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .about-text p {
            color: var(--text-gray);
            margin-bottom: 20px;
            line-height: 1.8;
        }

        .about-features {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 20px;
            margin-top: 30px;
        }

        .about-feature {
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .about-feature i {
            color: var(--primary);
            font-size: 1.2rem;
        }

        .about-image {
            position: relative;
        }

        .about-image-main {
            border-radius: 20px;
            overflow: hidden;
            background: linear-gradient(135deg, rgba(0, 212, 255, 0.2) 0%, rgba(255, 107, 53, 0.2) 100%);
            height: 400px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 8rem;
            color: var(--primary);
        }

        .about-image::after {
            content: '';
            position: absolute;
            top: 20px;
            left: 20px;
            right: -20px;
            bottom: -20px;
            border: 2px solid var(--primary);
            border-radius: 20px;
            z-index: -1;
        }

        /* --- CONTACT SECTION --- */
        .contact {
            background: var(--bg-dark);
        }

        .contact-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 60px;
        }

        .contact-info h2 {
            font-size: 2.5rem;
            margin-bottom: 20px;
        }

        .contact-info > p {
            color: var(--text-gray);
            margin-bottom: 30px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            margin-bottom: 25px;
        }

        .contact-icon {
            width: 50px;
            height: 50px;
            background: rgba(0, 212, 255, 0.1);
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--primary);
            font-size: 1.2rem;
            flex-shrink: 0;
        }

        .contact-details h4 {
            font-size: 1.1rem;
            margin-bottom: 5px;
        }

        .contact-details p {
            color: var(--text-gray);
        }

        .contact-form {
            background: var(--bg-light);
            padding: 40px;
            border-radius: 20px;
        }

        .form-group {
            margin-bottom: 20px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            font-weight: 500;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 12px 15px;
            background: var(--bg-dark);
            border: 1px solid rgba(255, 255, 255, 0.1);
            border-radius: 8px;
            color: var(--text-light);
            font-size: 1rem;
            transition: border-color 0.3s ease;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--primary);
        }

        .form-group textarea {
            min-height: 120px;
            resize: vertical;
        }

        .submit-btn {
            width: 100%;
            padding: 15px;
            background: var(--gradient);
            border: none;
            border-radius: 8px;
            color: var(--bg-dark);
            font-size: 1rem;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
        }

        .submit-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 10px 30px rgba(0, 212, 255, 0.3);
        }

        /* --- FOOTER --- */
        footer {
            background: var(--bg-light);
            padding: 50px 0 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
        }

        .footer-content {
            display: grid;
            grid-template-columns: 2fr 1fr 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .footer-brand .logo {
            margin-bottom: 20px;
            display: inline-block;
        }

        .footer-brand p {
            color: var(--text-gray);
            line-height: 1.7;
        }

        .footer-links h4 {
            font-size: 1.1rem;
            margin-bottom: 20px;
            color: var(--text-light);
        }

        .footer-links ul li {
            margin-bottom: 10px;
        }

        .footer-links a {
            color: var(--text-gray);
            transition: color 0.3s ease;
        }

        .footer-links a:hover {
            color: var(--primary);
        }

        .footer-social {
            display: flex;
            gap: 15px;
            margin-top: 20px;
        }

        .footer-social a {
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.05);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: var(--text-gray);
            transition: all 0.3s ease;
        }

        .footer-social a:hover {
            background: var(--primary);
            color: var(--bg-dark);
        }

        .footer-bottom {
            text-align: center;
            padding-top: 20px;
            border-top: 1px solid rgba(255, 255, 255, 0.05);
            color: var(--text-gray);
            font-size: 0.9rem;
        }

        /* --- RESPONSIVE --- */
        @media (max-width: 992px) {
            .hero h1 {
                font-size: 2.5rem;
            }
            
            .about-content,
            .contact-content {
                grid-template-columns: 1fr;
                gap: 40px;
            }
            
            .footer-content {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                display: none;
                position: absolute;
                top: 100%;
                left: 0;
                right: 0;
                background: var(--bg-dark);
                flex-direction: column;
                padding: 20px;
                gap: 15px;
                text-align: center;
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .mobile-menu-btn {
                display: block;
            }
            
            .hero h1 {
                font-size: 2rem;
            }
            
            .hero-buttons {
                flex-direction: column;
            }
            
            .section-header h2 {
                font-size: 2rem;
            }
            
            .about-features {
                grid-template-columns: 1fr;
            }
            
            .footer-content {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <a href="#" class="logo">Shulochana <span>Chemicals</span></a>
                <ul class="nav-links">
                    <li><a href="#home">Home</a></li>
                    <li><a href="#products">Products</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
                <div class="mobile-menu-btn">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="hero-content">
                <span class="hero-badge">Premium Cleaning Solutions</span>
                <h1>Your Trusted Partner for <span>Industrial & Household Cleaning Chemicals</span></h1>
                <p>Shulochana Chemicals delivers high-quality cleaning solutions for homes and industries. Experience the difference with our premium products and expert services.</p>
                <div class="hero-buttons">
                    <a href="#products" class="btn btn-primary">
                        <i class="fas fa-shopping-cart"></i> Our Products
                    </a>
                    <a href="#contact" class="btn btn-secondary">
                        <i class="fas fa-phone-alt"></i> Contact Us
                    </a>
                </div>
            </div>
        </div>
        <div class="hero-image">
            <i class="fas fa-flask"></i>
        </div>
    </section>

    <!-- Products Section -->
    <section class="products" id="products">
        <div class="container">
            <div class="section-header">
                <h2>Our Products</h2>
                <p>Explore our range of premium cleaning chemicals designed for every need</p>
                <div class="line"></div>
            </div>
            <div class="products-grid">
                <!-- Product 1 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-soap"></i>
                    </div>
                    <div class="product-info">
                        <h3>Multi-Surface Cleaner</h3>
                        <p>Powerful all-purpose cleaner for homes and offices. Safe on all surfaces.</p>
                        <span class="product-price">₹299</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
                <!-- Product 2 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-sparkles"></i>
                    </div>
                    <div class="product-info">
                        <h3>Industrial Degreaser</h3>
                        <p>Heavy-duty degreaser for machinery and industrial equipment.</p>
                        <span class="product-price">₹599</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
                <!-- Product 3 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-pump-soap"></i>
                    </div>
                    <div class="product-info">
                        <h3>Liquid Dishwash</h3>
                        <p>Grease-cutting dishwash liquid that leaves your dishes sparkling clean.</p>
                        <span class="product-price">₹149</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
                <!-- Product 4 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-spray-can"></i>
                    </div>
                    <div class="product-info">
                        <h3>Floor Cleaner Concentrate</h3>
                        <p>Professional floor cleaning solution for tiles, marble, and wood.</p>
                        <span class="product-price">₹349</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
                <!-- Product 5 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-hands-wash"></i>
                    </div>
                    <div class="product-info">
                        <h3>Hand Sanitizer</h3>
                        <p>Alcohol-based hand sanitizer for effective germ protection.</p>
                        <span class="product-price">₹99</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
                <!-- Product 6 -->
                <div class="product-card">
                    <div class="product-image">
                        <i class="fas fa-broom"></i>
                    </div>
                    <div class="product-info">
                        <h3>Toilet Cleaner Gel</h3>
                        <p>Powerful toilet cleaner that removes stains and kills germs.</p>
                        <span class="product-price">₹179</span>
                        <button class="product-btn">View Details</button>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-header">
                <h2>Our Services</h2>
                <p>Comprehensive cleaning solutions tailored to your needs</p>
                <div class="line"></div>
            </div>
            <div class="services-grid">
                <!-- Service 1 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-industry"></i>
                    </div>
                    <h3>Industrial Cleaning</h3>
                    <p>Professional industrial cleaning services for factories, warehouses, and manufacturing units using advanced chemical solutions.</p>
                </div>
                <!-- Service 2 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-building"></i>
                    </div>
                    <h3>Commercial Cleaning</h3>
                    <p>Complete office and commercial space cleaning solutions including sanitization and maintenance services.</p>
                </div>
                <!-- Service 3 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-home"></i>
                    </div>
                    <h3>Residential Cleaning</h3>
                    <p>Full home cleaning services including deep cleaning, sanitization, and post-construction cleaning.</p>
                </div>
                <!-- Service 4 -->
                <div class="service-card">
                    <div class="service-icon">
                        <i class="fas fa-prescription-bottle"></i>
                    </div>
                    <h3>Chemical Supply</h3>
                    <p>Bulk supply of industrial and household cleaning chemicals to businesses and organizations.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About Section -->
    <section class="about" id="about">
        <div class="container">
            <div class="about-content">
                <div class="about-text">
                    <h2>About Shulochana Chemicals</h2>
                    <p>Shulochana Chemicals is a premier provider of high-quality cleaning solutions, committed to delivering excellence in both products and services. With years of industry experience, we understand the unique cleaning challenges faced by households and businesses alike.</p>
                    <p>Our mission is to provide effective, safe, and environmentally friendly cleaning solutions that exceed customer expectations. We continuously innovate and improve our products to meet the evolving needs of our clients.</p>
                    <div class="about-features">
                        <div class="about-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Quality Assured</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Eco-Friendly</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>Expert Team</span>
                        </div>
                        <div class="about-feature">
                            <i class="fas fa-check-circle"></i>
                            <span>24/7 Support</span>
                        </div>
                    </div>
                </div>
                <div class="about-image">
                    <div class="about-image-main">
                        <i class="fas fa-flask"></i>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section class="contact" id="contact">
        <div class="container">
            <div class="contact-content">
                <div class="contact-info">
                    <h2>Get In Touch</h2>
                    <p>Have questions about our products or services? Contact us today and our team will be happy to assist you.</p>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-map-marker-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Our Location</h4>
                            <p>123 Chemical Industrial Area<br>City, State - 123456</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-phone-alt"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Phone Number</h4>
                            <p>+91 98765 43210<br>+91 12345 67890</p>
                        </div>
                    </div>
                    
                    <div class="contact-item">
                        <div class="contact-icon">
                            <i class="fas fa-envelope"></i>
                        </div>
                        <div class="contact-details">
                            <h4>Email Address</h4>
                            <p>info@shulochana.com<br>sales@shulochana.com</p>
                        </div>
                    </div>
                </div>
                
                <div class="contact-form">
                    <form>
                        <div class="form-group">
                            <label for="name">Your Name</label>
                            <input type="text" id="name" name="name" placeholder="Enter your name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" name="email" placeholder="Enter your email" required>
                        </div>
                        <div class="form-group">
                            <label for="phone">Phone Number</label>
                            <input type="tel" id="phone" name="phone" placeholder="Enter your phone number">
                        </div>
                        <div class="form-group">
                            <label for="message">Your Message</label>
                            <textarea id="message" name="message" placeholder="How can we help you?" required></textarea>
                        </div>
                        <button type="submit" class="submit-btn">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                    <a href="#" class="logo">Shulochana <span>Chemicals</span></a>
                    <p>Your trusted partner for premium cleaning solutions. We deliver quality products and services for homes and industries.</p>
                    <div class="footer-social">
                        <a href="#"><i class="fab fa-facebook-f"></i></a>
                        <a href="#"><i class="fab fa-instagram"></i></a>
                        <a href="#"><i class="fab fa-twitter"></i></a>
                        <a href="#"><i class="fab fa-linkedin-in"></i></a>
                    </div>
                </div>
                <div class="footer-links">
                    <h4>Quick Links</h4>
                    <ul>
                        <li><a href="#home">Home</a></li>
                        <li><a href="#products">Products</a></li>
                        <li><a href="#services">Services</a></li>
                        <li><a href="#about">About Us</a></li>
                        <li><a href="#contact">Contact</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Products</h4>
                    <ul>
                        <li><a href="#">Multi-Surface Cleaner</a></li>
                        <li><a href="#">Industrial Degreaser</a></li>
                        <li><a href="#">Liquid Dishwash</a></li>
                        <li><a href="#">Floor Cleaner</a></li>
                        <li><a href="#">Hand Sanitizer</a></li>
                    </ul>
                </div>
                <div class="footer-links">
                    <h4>Services</h4>
                    <ul>
                        <li><a href="#">Industrial Cleaning</a></li>
                        <li><a href="#">Commercial Cleaning</a></li>
                        <li><a href="#">Residential Cleaning</a></li>
                        <li><a href="#">Chemical Supply</a></li>
                    </ul>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2024 Shulochana Chemicals. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Mobile Menu Toggle
        const mobileMenuBtn = document.querySelector('.mobile-menu-btn');
        const navLinks = document.querySelector('.nav-links');

        mobileMenuBtn.addEventListener('click', () => {
            navLinks.classList.toggle('active');
        });

        // Header Scroll Effect
        window.addEventListener('scroll', () => {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
        });

        // Smooth Scrolling for Anchor Links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth'
                    });
                    // Close mobile menu if open
                    navLinks.classList.remove('active');
                }
            });
        });

        // Form Submission (prevent default for demo)
        document.querySelector('.contact-form form').addEventListener('submit', function(e) {
            e.preventDefault();
            alert('Thank you for your message! We will get back to you soon.');
            this.reset();
        });
    </script>
</body>
</html>
# shulochanachemicals
made in india
