<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>RedRelic Software | Financial, Energy & EV Charging Solutions</title>
    <style>
        :root {
            --primary: #dc2626; /* RedRelic red */
            --primary-dark: #b91c1c;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #94a3b8;
            --energy: #f59e0b; /* Energy sector color */
            --finance: #10b981; /* Finance sector color */
            --ev: #3b82f6; /* EV sector color */
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            color: var(--dark);
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        /* Header */
        header {
            background-color: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: fixed;
            width: 100%;
            z-index: 100;
        }
        
        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }
        
        .logo {
            font-size: 24px;
            font-weight: 700;
            color: var(--primary);
        }
        
        .logo span {
            color: var(--dark);
        }
        
        .nav-links {
            display: flex;
            gap: 30px;
        }
        
        .nav-links a {
            text-decoration: none;
            color: var(--dark);
            font-weight: 500;
            transition: color 0.3s;
        }
        
        .nav-links a:hover {
            color: var(--primary);
        }
        
        .btn {
            display: inline-block;
            background-color: var(--primary);
            color: white;
            padding: 10px 20px;
            border-radius: 5px;
            text-decoration: none;
            font-weight: 500;
            transition: all 0.3s;
        }
        
        .btn:hover {
            background-color: var(--primary-dark);
            transform: translateY(-2px);
        }
        
        /* Hero Section */
        .hero {
            padding: 150px 0 100px;
            background: linear-gradient(135deg, #fef2f2 0%, #fee2e2 100%);
            text-align: center;
        }
        
        .hero h1 {
            font-size: 48px;
            margin-bottom: 20px;
            line-height: 1.2;
        }
        
        .hero p {
            font-size: 20px;
            color: var(--gray);
            max-width: 700px;
            margin: 0 auto 40px;
        }
        
        .sector-tags {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 30px;
            flex-wrap: wrap;
        }
        
        .sector-tag {
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: 600;
            font-size: 14px;
        }
        
        .sector-tag.finance {
            background-color: rgba(16, 185, 129, 0.1);
            color: var(--finance);
        }
        
        .sector-tag.energy {
            background-color: rgba(245, 158, 11, 0.1);
            color: var(--energy);
        }
        
        .sector-tag.ev {
            background-color: rgba(59, 130, 246, 0.1);
            color: var(--ev);
        }
        
        /* Services */
        .services {
            padding: 100px 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }
        
        .section-title h2 {
            font-size: 36px;
            margin-bottom: 15px;
        }
        
        .section-title p {
            color: var(--gray);
            max-width: 600px;
            margin: 0 auto;
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .service-card {
            background: white;
            border-radius: 10px;
            padding: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: all 0.3s;
            border-top: 4px solid transparent;
        }
        
        .service-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
        }
        
        .service-card.finance {
            border-top-color: var(--finance);
        }
        
        .service-card.energy {
            border-top-color: var(--energy);
        }
        
        .service-card.ev {
            border-top-color: var(--ev);
        }
        
        .service-icon {
            font-size: 40px;
            margin-bottom: 20px;
        }
        
        .service-card.finance .service-icon {
            color: var(--finance);
        }
        
        .service-card.energy .service-icon {
            color: var(--energy);
        }
        
        .service-card.ev .service-icon {
            color: var(--ev);
        }
        
        .service-card h3 {
            font-size: 22px;
            margin-bottom: 15px;
        }
        
        .sector-indicator {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 4px;
            font-size: 12px;
            font-weight: 600;
            margin-bottom: 15px;
        }
        
        .finance-bg {
            background-color: rgba(16, 185, 129, 0.1);
            color: var(--finance);
        }
        
        .energy-bg {
            background-color: rgba(245, 158, 11, 0.1);
            color: var(--energy);
        }
        
        .ev-bg {
            background-color: rgba(59, 130, 246, 0.1);
            color: var(--ev);
        }
        
        /* Sector Focus */
        .sector-focus {
            padding: 100px 0;
            background-color: #f8fafc;
        }
        
        .sectors {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
        }
        
        .sector-card {
            background: white;
            border-radius: 10px;
            padding: 40px 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            text-align: center;
        }
        
        .sector-card h3 {
            font-size: 24px;
            margin: 20px 0 15px;
        }
        
        .sector-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto;
            font-size: 32px;
        }
        
        .sector-icon.finance {
            background-color: rgba(16, 185, 129, 0.1);
            color: var(--finance);
        }
        
        .sector-icon.energy {
            background-color: rgba(245, 158, 11, 0.1);
            color: var(--energy);
        }
        
        .sector-icon.ev {
            background-color: rgba(59, 130, 246, 0.1);
            color: var(--ev);
        }
        
        /* Clients */
        .clients {
            padding: 80px 0;
            text-align: center;
        }
        
        .client-logos {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 40px;
            margin-top: 50px;
        }
        
        .client-logo {
            opacity: 0.7;
            transition: opacity 0.3s;
            height: 40px;
        }
        
        .client-logo:hover {
            opacity: 1;
        }
        
        .client-sector {
            font-size: 12px;
            margin-top: 5px;
            font-weight: 600;
        }
        
        .finance-text {
            color: var(--finance);
        }
        
        .energy-text {
            color: var(--energy);
        }
        
        .ev-text {
            color: var(--ev);
        }
        
        /* CTA */
        .cta {
            padding: 100px 0;
            background: linear-gradient(135deg, var(--primary) 0%, var(--primary-dark) 100%);
            color: white;
            text-align: center;
        }
        
        .cta h2 {
            font-size: 36px;
            margin-bottom: 20px;
        }
        
        .cta p {
            max-width: 600px;
            margin: 0 auto 40px;
            opacity: 0.9;
        }
        
        .btn-light {
            background-color: white;
            color: var(--primary);
        }
        
        .btn-light:hover {
            background-color: rgba(255,255,255,0.9);
        }
        
        /* Footer */
        footer {
            background-color: var(--dark);
            color: white;
            padding: 60px 0 30px;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 40px;
            margin-bottom: 50px;
        }
        
        .footer-column h3 {
            font-size: 18px;
            margin-bottom: 20px;
            color: var(--light);
        }
        
        .footer-column ul {
            list-style: none;
        }
        
        .footer-column ul li {
            margin-bottom: 10px;
        }
        
        .footer-column ul li a {
            color: var(--gray);
            text-decoration: none;
            transition: color 0.3s;
        }
        
        .footer-column ul li a:hover {
            color: white;
        }
        
        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: var(--gray);
            font-size: 14px;
        }
        
        @media (max-width: 768px) {
            .hero h1 {
                font-size: 36px;
            }
            
            .hero p {
                font-size: 18px;
            }
            
            .nav-links {
                gap: 15px;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container">
            <nav>
                <div class="logo">Red<span>Relic</span></div>
                <div class="nav-links">
                    <a href="#services">Services</a>
                    <a href="#sectors">Sectors</a>
                    <a href="#clients">Clients</a>
                    <a href="#contact" class="btn">Contact Us</a>
                </div>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="container">
            <h1>Specialized Software Solutions for Finance, Energy & EV Charging</h1>
            <p>RedRelic delivers cutting-edge technology solutions tailored to the unique challenges of your industry.</p>
            <a href="#contact" class="btn">Get Your Free Consultation</a>
            
            <div class="sector-tags">
                <span class="sector-tag finance">Financial Technology</span>
                <span class="sector-tag energy">Energy Sector</span>
                <span class="sector-tag ev">EV Charging Infrastructure</span>
            </div>
        </div>
    </section>

    <!-- Services -->
    <section class="services" id="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Specialized Services</h2>
                <p>Industry-specific solutions designed to address your sector's unique challenges</p>
            </div>
            <div class="services-grid">
                <!-- Finance Services -->
                <div class="service-card finance">
                    <span class="sector-indicator finance-bg">Finance</span>
                    <div class="service-icon">💰</div>
                    <h3>Regulatory Compliance Systems</h3>
                    <p>Automated compliance solutions that adapt to changing financial regulations across jurisdictions.</p>
                </div>
                <div class="service-card finance">
                    <span class="sector-indicator finance-bg">Finance</span>
                    <div class="service-icon">📈</div>
                    <h3>Risk Analysis Platforms</h3>
                    <p>Advanced analytics for real-time risk assessment and mitigation strategies.</p>
                </div>
                
                <!-- Energy Services -->
                <div class="service-card energy">
                    <span class="sector-indicator energy-bg">Energy</span>
                    <div class="service-icon">⚡</div>
                    <h3>Grid Management Solutions</h3>
                    <p>Smart systems for energy distribution, load balancing, and outage prediction.</p>
                </div>
                <div class="service-card energy">
                    <span class="sector-indicator energy-bg">Energy</span>
                    <div class="service-icon">🌱</div>
                    <h3>Renewable Energy Integration</h3>
                    <p>Software to optimize the incorporation of renewable sources into existing infrastructure.</p>
                </div>
                
                <!-- EV Services -->
                <div class="service-card ev">
                    <span class="sector-indicator ev-bg">EV Charging</span>
                    <div class="service-icon">🔌</div>
                    <h3>Charging Network Management</h3>
                    <p>Comprehensive platforms for managing EV charging station networks and user experiences.</p>
                </div>
                <div class="service-card ev">
                    <span class="sector-indicator ev-bg">EV Charging</span>
                    <div class="service-icon">🔋</div>
                    <h3>Battery Optimization Systems</h3>
                    <p>AI-driven solutions to extend battery life and optimize charging cycles.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Sector Focus -->
    <section class="sector-focus" id="sectors">
        <div class="container">
            <div class="section-title">
                <h2>Our Sector Expertise</h2>
                <p>Deep industry knowledge combined with technical excellence</p>
            </div>
            <div class="sectors">
                <div class="sector-card">
                    <div class="sector-icon finance">💳</div>
                    <h3>Financial Services</h3>
                    <p>From banking to insurance and fintech, we build secure, compliant systems that handle sensitive financial data with precision.</p>
                </div>
                <div class="sector-card">
                    <div class="sector-icon energy">⚡</div>
                    <h3>Energy Sector</h3>
                    <p>Solutions for utilities, renewable energy providers, and grid operators to optimize energy production and distribution.</p>
                </div>
                <div class="sector-card">
                    <div class="sector-icon ev">🚗</div>
                    <h3>EV Charging Business</h3>
                    <p>Software infrastructure for charging networks, payment systems, and fleet management in the growing EV market.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Clients -->
    <section class="clients" id="clients">
        <div class="container">
            <div class="section-title">
                <h2>Trusted By Industry Leaders</h2>
                <p>We've helped companies across our focus sectors achieve their technology goals</p>
            </div>
            <div class="client-logos">
                <div>
                    <img src="https://via.placeholder.com/120x40?text=Finance+Corp" alt="Finance Corp" class="client-logo">
                    <div class="client-sector finance-text">Financial Services</div>
                </div>
                <div>
                    <img src="https://via.placeholder.com/120x40?text=Green+Energy" alt="Green Energy" class="client-logo">
                    <div class="client-sector energy-text">Energy Sector</div>
                </div>
                <div>
                    <img src="https://via.placeholder.com/120x40?text=EV+Networks" alt="EV Networks" class="client-logo">
                    <div class="client-sector ev-text">EV Charging</div>
                </div>
                <div>
                    <img src="https://via.placeholder.com/120x40?text=Bank+Global" alt="Bank Global" class="client-logo">
                    <div class="client-sector finance-text">Financial Services</div>
                </div>
                <div>
                    <img src="https://via.placeholder.com/120x40?text=Power+Grid" alt="Power Grid" class="client-logo">
                    <div class="client-sector energy-text">Energy Sector</div>
                </div>
            </div>
        </div>
    </section>

    <!-- CTA -->
    <section class="cta" id="contact">
        <div class="container">
            <h2>Ready to Power Your Business With Specialized Software?</h2>
            <p>Our sector-specific expertise means faster implementation and better results for your unique challenges.</p>
            <a href="#" class="btn btn-light">Contact Our Experts</a>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div class="footer-column">
                    <h3>RedRelic Software</h3>
                    <p>Specialized software solutions for finance, energy, and EV charging businesses.</p>
                </div>
                <div class="footer-column">
                    <h3>Sectors</h3>
                    <ul>
                        <li><a href="#">Financial Services</a></li>
                        <li><a href="#">Energy Sector</a></li>
                        <li><a href="#">EV Charging</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Services</h3>
                    <ul>
                        <li><a href="#">Custom Development</a></li>
                        <li><a href="#">System Integration</a></li>
                        <li><a href="#">Digital Transformation</a></li>
                        <li><a href="#">Technical Consultancy</a></li>
                    </ul>
                </div>
                <div class="footer-column">
                    <h3>Contact</h3>
                    <ul>
                        <li><a href="#">contact@redrelic.com</a></li>
                        <li><a href="#">+44 (0)20 1234 5678</a></li>
                        <li><a href="#">London, UK</a></li>
                    </ul>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2023 RedRelic Software Limited. All rights reserved.</p>
            </div>
        </div>
    </footer>
</body>
</html>
