<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jasa Pembuatan Website Profesional</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            line-height: 1.6;
            color: #333;
            background: #f4f4f4;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Navigation */
        nav {
            background: white;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            position: sticky;
            top: 0;
            z-index: 1000;
        }

        .nav-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            height: 70px;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: bold;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 30px;
            align-items: center;
        }

        .nav-menu a {
            text-decoration: none;
            color: #333;
            font-weight: 500;
            transition: color 0.3s;
            position: relative;
        }

        .nav-menu a:hover {
            color: #667eea;
        }

        .nav-menu a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background: #667eea;
            transition: width 0.3s;
        }

        .nav-menu a:hover::after {
            width: 100%;
        }

        .language-switcher {
            display: flex;
            gap: 10px;
            align-items: center;
        }

        .lang-btn {
            padding: 5px 12px;
            border: 2px solid #667eea;
            background: white;
            color: #667eea;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 600;
            transition: all 0.3s;
        }

        .lang-btn.active {
            background: #667eea;
            color: white;
        }

        .lang-btn:hover {
            background: #667eea;
            color: white;
        }

        .mobile-menu-btn {
            display: none;
            flex-direction: column;
            gap: 5px;
            background: none;
            border: none;
            cursor: pointer;
        }

        .mobile-menu-btn span {
            width: 25px;
            height: 3px;
            background: #333;
            transition: 0.3s;
        }

        /* Header */
        header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 100px 0;
            text-align: center;
        }

        header h1 {
            font-size: 3rem;
            margin-bottom: 20px;
            animation: fadeInDown 1s;
        }

        header p {
            font-size: 1.3rem;
            opacity: 0.95;
            animation: fadeInUp 1s;
            max-width: 700px;
            margin: 0 auto;
        }

        /* Education Section */
        .education {
            padding: 80px 0;
            background: white;
        }

        .education-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .education-text h2 {
            font-size: 2.5rem;
            color: #333;
            margin-bottom: 20px;
        }

        .education-text p {
            color: #555;
            font-size: 1.1rem;
            margin-bottom: 15px;
            line-height: 1.8;
        }

        .benefits-list {
            list-style: none;
            margin-top: 30px;
        }

        .benefits-list li {
            padding: 15px 0;
            padding-left: 40px;
            position: relative;
            color: #555;
            font-size: 1.05rem;
        }

        .benefits-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
            font-size: 1.5rem;
        }

        .education-image {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            color: white;
        }

        .education-image h3 {
            font-size: 2rem;
            margin-bottom: 20px;
        }

        .stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }

        .stat-item {
            background: rgba(255,255,255,0.2);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin-bottom: 10px;
        }

        .stat-label {
            font-size: 1rem;
            opacity: 0.9;
        }

        /* Packages Section */
        .packages {
            padding: 80px 0;
            background: #f8f9fa;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 2.8rem;
            color: #333;
            margin-bottom: 15px;
        }

        .section-title p {
            font-size: 1.2rem;
            color: #666;
        }

        .package-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(380px, 1fr));
            gap: 40px;
            margin-top: 50px;
        }

        .package-card {
            background: white;
            border-radius: 20px;
            padding: 45px 35px;
            box-shadow: 0 15px 40px rgba(0,0,0,0.08);
            transition: transform 0.3s, box-shadow 0.3s;
            position: relative;
            overflow: hidden;
        }

        .package-card:hover {
            transform: translateY(-15px);
            box-shadow: 0 20px 50px rgba(0,0,0,0.15);
        }

        .package-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 6px;
            background: linear-gradient(90deg, #667eea 0%, #764ba2 100%);
        }

        .package-header {
            text-align: center;
            margin-bottom: 35px;
        }

        .package-number {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 10px 25px;
            border-radius: 30px;
            font-size: 0.95rem;
            font-weight: 600;
            margin-bottom: 20px;
        }

        .package-title {
            font-size: 2rem;
            color: #333;
            margin-bottom: 12px;
        }

        .package-subtitle {
            font-size: 1rem;
            color: #666;
            font-style: italic;
        }

        .package-description {
            background: #f8f9fa;
            padding: 25px;
            border-radius: 12px;
            margin-bottom: 30px;
        }

        .package-description h3 {
            font-size: 1.05rem;
            color: #667eea;
            margin-bottom: 12px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .package-description p {
            color: #555;
            line-height: 1.8;
        }

        .package-features {
            margin-bottom: 30px;
        }

        .package-features h3 {
            font-size: 1.05rem;
            color: #667eea;
            margin-bottom: 18px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .feature-list {
            list-style: none;
        }

        .feature-list li {
            padding: 12px 0;
            padding-left: 35px;
            position: relative;
            color: #555;
            line-height: 1.7;
        }

        .feature-list li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: #667eea;
            font-weight: bold;
            font-size: 1.3rem;
        }

        .package-price {
            text-align: center;
            padding: 30px;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            border-radius: 12px;
            margin-bottom: 25px;
        }

        .price-label {
            color: rgba(255,255,255,0.95);
            font-size: 0.95rem;
            margin-bottom: 8px;
        }

        .price-amount {
            color: white;
            font-size: 2.2rem;
            font-weight: bold;
        }

        .price-range {
            color: white;
            font-size: 2rem;
            font-weight: bold;
        }

        .cta-button {
            display: block;
            width: 100%;
            padding: 18px;
            background: #333;
            color: white;
            text-align: center;
            text-decoration: none;
            border-radius: 10px;
            font-weight: 600;
            font-size: 1.05rem;
            transition: background 0.3s, transform 0.3s;
        }

        .cta-button:hover {
            background: #555;
            transform: scale(1.02);
        }

        /* Explore Section */
        .explore {
            padding: 80px 0;
            background: white;
        }

        .explore-content {
            text-align: center;
            max-width: 800px;
            margin: 0 auto;
        }

        .explore-content h2 {
            font-size: 2.8rem;
            color: #333;
            margin-bottom: 20px;
        }

        .explore-content p {
            font-size: 1.2rem;
            color: #666;
            margin-bottom: 40px;
        }

        .social-links {
            display: flex;
            gap: 30px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .social-card {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px 50px;
            border-radius: 15px;
            text-decoration: none;
            transition: transform 0.3s, box-shadow 0.3s;
            display: flex;
            align-items: center;
            gap: 15px;
            font-size: 1.1rem;
            font-weight: 600;
        }

        .social-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(102, 126, 234, 0.4);
        }

        .social-icon {
            font-size: 2rem;
        }

        /* Contact Section */
        .contact {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 80px 0;
            text-align: center;
        }

        .contact h2 {
            font-size: 2.8rem;
            margin-bottom: 25px;
        }

        .contact p {
            font-size: 1.3rem;
            margin-bottom: 40px;
            opacity: 0.95;
        }

        .contact-buttons {
            display: flex;
            gap: 25px;
            justify-content: center;
            flex-wrap: wrap;
        }

        .contact-btn {
            padding: 18px 50px;
            background: white;
            color: #667eea;
            text-decoration: none;
            border-radius: 10px;
            font-weight: 600;
            font-size: 1.1rem;
            transition: transform 0.3s, box-shadow 0.3s;
        }

        .contact-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 10px 30px rgba(255,255,255,0.3);
        }

        /* Footer */
        footer {
            background: #222;
            color: white;
            padding: 40px 0;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 40px;
            margin-bottom: 30px;
        }

        .footer-section h3 {
            margin-bottom: 20px;
            font-size: 1.3rem;
        }

        .footer-section p, .footer-section a {
            color: rgba(255,255,255,0.8);
            text-decoration: none;
            display: block;
            margin-bottom: 10px;
            transition: color 0.3s;
        }

        .footer-section a:hover {
            color: #667eea;
        }

        .footer-bottom {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255,255,255,0.1);
            color: rgba(255,255,255,0.7);
        }

        /* Animations */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
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

        /* Responsive */
        @media (max-width: 968px) {
            .nav-menu {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background: white;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                box-shadow: 0 10px 27px rgba(0,0,0,0.05);
                padding: 20px 0;
            }

            .nav-menu.active {
                left: 0;
            }

            .mobile-menu-btn {
                display: flex;
            }

            .education-content {
                grid-template-columns: 1fr;
            }

            .stats {
                grid-template-columns: 1fr;
            }

            header h1 {
                font-size: 2.2rem;
            }

            .package-grid {
                grid-template-columns: 1fr;
            }

            .section-title h2 {
                font-size: 2rem;
            }

            .contact h2 {
                font-size: 2rem;
            }
        }

        /* Hidden class for language switching */
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav>
        <div class="nav-container">
            <div class="logo">WebPro</div>
            <ul class="nav-menu" id="navMenu">
                <li><a href="#home" class="lang-id">Beranda</a><a href="#home" class="lang-en hidden">Home</a></li>
                <li><a href="#education" class="lang-id">Edukasi</a><a href="#education" class="lang-en hidden">Education</a></li>
                <li><a href="#packages" class="lang-id">Paket Layanan</a><a href="#packages" class="lang-en hidden">Packages</a></li>
                <li><a href="#explore" class="lang-id">Jelajahi</a><a href="#explore" class="lang-en hidden">Explore</a></li>
                <li><a href="#contact" class="lang-id">Kontak</a><a href="#contact" class="lang-en hidden">Contact</a></li>
                <li class="language-switcher">
                    <button class="lang-btn active" onclick="switchLanguage('id')">ID</button>
                    <button class="lang-btn" onclick="switchLanguage('en')">EN</button>
                </li>
            </ul>
            <button class="mobile-menu-btn" id="mobileMenuBtn">
                <span></span>
                <span></span>
                <span></span>
            </button>
        </div>
    </nav>

    <!-- Header -->
    <header id="home">
        <div class="container">
            <h1 class="lang-id">Jasa Pembuatan Website Profesional</h1>
            <h1 class="lang-en hidden">Professional Website Development Services</h1>
            <p class="lang-id">Wujudkan Website Impian Anda Bersama Kami. Tingkatkan Brand dan Raih Pelanggan Lebih Banyak dengan Website Berkualitas</p>
            <p class="lang-en hidden">Realize Your Dream Website With Us. Boost Your Brand and Reach More Customers with Quality Websites</p>
        </div>
    </header>

    <!-- Education Section -->
    <section class="education" id="education">
        <div class="container">
            <div class="education-content">
                <div class="education-text">
                    <h2 class="lang-id">Mengapa UMKM Harus Memiliki Website?</h2>
                    <h2 class="lang-en hidden">Why Should SMEs Have a Website?</h2>
                    <p class="lang-id">Di era digital ini, memiliki website bukan lagi pilihan, tapi <strong>kebutuhan</strong>. Website adalah wajah bisnis Anda di dunia maya yang dapat diakses 24/7 oleh calon pelanggan.</p>
                    <p class="lang-en hidden">In this digital era, having a website is no longer an option, but a <strong>necessity</strong>. A website is your business face in the digital world that can be accessed 24/7 by potential customers.</p>
                    
                    <ul class="benefits-list">
                        <li class="lang-id"><strong>Dikenal Masyarakat Luas</strong> - Jangkau pelanggan di seluruh Indonesia bahkan dunia</li>
                        <li class="lang-en hidden"><strong>Widely Recognized</strong> - Reach customers across Indonesia and even the world</li>
                        
                        <li class="lang-id"><strong>Kredibilitas Meningkat</strong> - Bisnis terlihat lebih profesional dan terpercaya</li>
                        <li class="lang-en hidden"><strong>Increased Credibility</strong> - Business looks more professional and trustworthy</li>
                        
                        <li class="lang-id"><strong>E-Commerce Sendiri</strong> - Jual produk online tanpa tergantung marketplace</li>
                        <li class="lang-en hidden"><strong>Own E-Commerce</strong> - Sell products online without relying on marketplaces</li>
                        
                        <li class="lang-id"><strong>Marketing 24/7</strong> - Website bekerja untuk Anda setiap saat</li>
                        <li class="lang-en hidden"><strong>24/7 Marketing</strong> - Website works for you all the time</li>
                        
                        <li class="lang-id"><strong>Hemat Biaya</strong> - Lebih murah dari iklan konvensional jangka panjang</li>
                        <li class="lang-en hidden"><strong>Cost Effective</strong> - Cheaper than conventional long-term advertising</li>
                    </ul>
                </div>
                <div class="education-image">
                    <h3 class="lang-id">Fakta Menarik</h3>
                    <h3 class="lang-en hidden">Interesting Facts</h3>
                    <div class="stats">
                        <div class="stat-item">
                            <div class="stat-number">75%</div>
                            <div class="stat-label lang-id">Konsumen cek website sebelum membeli</div>
                            <div class="stat-label lang-en hidden">Consumers check website before buying</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">24/7</div>
                            <div class="stat-label lang-id">Bisnis tetap buka walau Anda tidur</div>
                            <div class="stat-label lang-en hidden">Business stays open while you sleep</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">3x</div>
                            <div class="stat-label lang-id">Lebih banyak pelanggan potensial</div>
                            <div class="stat-label lang-en hidden">More potential customers</div>
                        </div>
                        <div class="stat-item">
                            <div class="stat-number">88%</div>
                            <div class="stat-label lang-id">UMKM sukses dengan website</div>
                            <div class="stat-label lang-en hidden">SMEs succeed with website</div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Packages Section -->
    <section class="packages" id="packages">
        <div class="container">
            <div class="section-title">
                <h2 class="lang-id">Paket Layanan Kami</h2>
                <h2 class="lang-en hidden">Our Service Packages</h2>
                <p class="lang-id">Pilih paket yang sesuai dengan kebutuhan bisnis Anda</p>
                <p class="lang-en hidden">Choose the package that suits your business needs</p>
            </div>

            <div class="package-grid">
                <!-- Package 1: STARTER -->
                <div class="package-card">
                    <div class="package-header">
                        <span class="package-number lang-id">Paket 1</span>
                        <span class="package-number lang-en hidden">Package 1</span>
                        <h2 class="package-title">STARTER</h2>
                        <p class="package-subtitle lang-id">Website Sederhana / Landing Page</p>
                        <p class="package-subtitle lang-en hidden">Simple Website / Landing Page</p>
                    </div>

                    <div class="package-description">
                        <h3 class="lang-id">Deskripsi</h3>
                        <h3 class="lang-en hidden">Description</h3>
                        <p class="lang-id"><strong>Cocok Untuk:</strong> Peluncuran cepat, profil bisnis sederhana, individu, atau landing page promosi.</p>
                        <p class="lang-en hidden"><strong>Perfect For:</strong> Quick launch, simple business profile, individuals, or promotional landing pages.</p>
                    </div>

                    <div class="package-features">
                        <h3 class="lang-id">Fitur dan Layanan</h3>
                        <h3 class="lang-en hidden">Features & Services</h3>
                        <ul class="feature-list">
                            <li class="lang-id">Desain Kustom 1-2 Halaman Utama (Landing Page & Kontak)</li>
                            <li class="lang-en hidden">Custom Design 1-2 Main Pages (Landing Page & Contact)</li>
                            
                            <li class="lang-id">Desain Responsif (Optimal di HP & Tablet)</li>
                            <li class="lang-en hidden">Responsive Design (Optimized for Mobile & Tablet)</li>
                            
                            <li class="lang-id">Integrasi Formulir Kontak</li>
                            <li class="lang-en hidden">Contact Form Integration</li>
                            
                            <li class="lang-id">Integrasi Google Analytics Dasar</li>
                            <li class="lang-en hidden">Basic Google Analytics Integration</li>
                            
                            <li class="lang-id"><strong>Revisi:</strong> 1x Minor</li>
                            <li class="lang-en hidden"><strong>Revision:</strong> 1x Minor</li>
                        </ul>
                    </div>

                    <div class="package-price">
                        <p class="price-label lang-id">Harga Estimasi (Mulai Dari)</p>
                        <p class="price-label lang-en hidden">Estimated Price (Starting From)</p>
                        <p class="price-amount">Rp 2.500.000 - Rp 4.500.000</p>
                    </div>

                    <a href="#contact" class="cta-button lang-id">Pesan Sekarang</a>
                    <a href="#contact" class="cta-button lang-en hidden">Order Now</a>
                </div>

                <!-- Package 2: BUSINESS -->
                <div class="package-card">
                    <div class="package-header">
                        <span class="package-number lang-id">Paket 2</span>
                        <span class="package-number lang-en hidden">Package 2</span>
                        <h2 class="package-title">BUSINESS</h2>
                        <p class="package-subtitle lang-id">Website Perusahaan / Blog Profesional</p>
                        <p class="package-subtitle lang-en hidden">Company Website / Professional Blog</p>
                    </div>

                    <div class="package-description">
                        <h3 class="lang-id">Deskripsi</h3>
                        <h3 class="lang-en hidden">Description</h3>
                        <p class="lang-id"><strong>Cocok Untuk:</strong> UKM, perusahaan jasa, konsultan, dan entitas yang membutuhkan fitur dinamis dan konten yang bisa diperbarui secara berkala.</p>
                        <p class="lang-en hidden"><strong>Perfect For:</strong> SMEs, service companies, consultants, and entities requiring dynamic features and regularly updated content.</p>
                    </div>

                    <div class="package-features">
                        <h3 class="lang-id">Fitur dan Layanan</h3>
                        <h3 class="lang-en hidden">Features & Services</h3>
                        <ul class="feature-list">
                            <li class="lang-id">Desain Kustom 7-10 Halaman (Termasuk Blog/Berita & Portfolio)</li>
                            <li class="lang-en hidden">Custom Design 7-10 Pages (Including Blog/News & Portfolio)</li>
                            
                            <li class="lang-id">Menggunakan <strong>CMS WordPress</strong> (Dinamis)</li>
                            <li class="lang-en hidden">Using <strong>WordPress CMS</strong> (Dynamic)</li>
                            
                            <li class="lang-id">Optimasi Kecepatan dan Keamanan Dasar</li>
                            <li class="lang-en hidden">Speed and Basic Security Optimization</li>
                            
                            <li class="lang-id">Integrasi SEO On-Page Dasar (Meta Tags, Site Map)</li>
                            <li class="lang-en hidden">Basic SEO On-Page Integration (Meta Tags, Site Map)</li>
                            
                            <li class="lang-id">Integrasi Media Sosial & WhatsApp Chat</li>
                            <li class="lang-en hidden">Social Media & WhatsApp Chat Integration</li>
                            
                            <li class="lang-id"><strong>Revisi:</strong> 2x Mayor</li>
                            <li class="lang-en hidden"><strong>Revision:</strong> 2x Major</li>
                            
                            <li class="lang-id"><strong>Bonus:</strong> Pelatihan Penggunaan CMS (1 Jam)</li>
                            <li class="lang-en hidden"><strong>Bonus:</strong> CMS Usage Training (1 Hour)</li>
                        </ul>
                    </div>

                    <div class="package-price">
                        <p class="price-label lang-id">Harga Estimasi (Mulai Dari)</p>
                        <p class="price-label lang-en hidden">Estimated Price (Starting From)</p>
                        <p class="price-range">Rp 5.500.000 - Rp 9.500.000</p>
                    </div>

                    <a href="#contact" class="cta-button lang-id">Pesan Sekarang</a>
                    <a href="#contact" class="cta-button lang-en hidden">Order Now</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Explore Section -->
    <section class="explore" id="explore">
        <div class="container">
            <div class="explore-content">
                <h2 class="lang-id">Jelajahi & Hubungi Kami</h2>
                <div class="social-links">
                <a href="https://instagram.com/fahreza_aw" target="_blank" class="social-card">
                    <span class="social-icon">📷</span>
                    <div>
                        <div>Instagram</div>
                        <div style="font-size: 0.9rem; opacity: 0.9;">@fahreza_aw</div>
                    </div>
                </a>
                <a href="https://wa.me/6289676943668" target="_blank" class="social-card">
                    <span class="social-icon">💬</span>
                    <div>
                        <div>WhatsApp</div>
                        <div style="font-size: 0.9rem; opacity: 0.9;">+62 896-7694-3668</div>
                    </div>
                </a>
            </div>
        </div>
    </div>
</section>

<!-- Contact Section -->
<section class="contact" id="contact">
    <div class="container">
        <h2 class="lang-id">Siap Memulai Proyek Anda?</h2>
        <h2 class="lang-en hidden">Ready to Start Your Project?</h2>
        <p class="lang-id">Hubungi kami sekarang untuk konsultasi gratis dan penawaran terbaik!</p>
        <p class="lang-en hidden">Contact us now for free consultation and best offers!</p>
        <div class="contact-buttons">
            <a href="https://wa.me/6289676943668" class="contact-btn">WhatsApp</a>
            <a href="mailto:info@webpro.com" class="contact-btn">Email</a>
            <a href="tel:+6289676943668" class="contact-btn lang-id">Telepon</a>
            <a href="tel:+6289676943668" class="contact-btn lang-en hidden">Phone</a>
        </div>
    </div>
</section>

<!-- Footer -->
<footer>
    <div class="container">
        <div class="footer-content">
            <div class="footer-section">
                <h3>WebPro</h3>
                <p class="lang-id">Solusi profesional untuk kebutuhan website bisnis Anda. Kami siap membantu mewujudkan website impian Anda.</p>
                <p class="lang-en hidden">Professional solutions for your business website needs. We are ready to help realize your dream website.</p>
            </div>
            <div class="footer-section">
                <h3 class="lang-id">Layanan</h3>
                <h3 class="lang-en hidden">Services</h3>
                <a href="#packages" class="lang-id">Paket Website</a>
                <a href="#packages" class="lang-en hidden">Website Packages</a>
                <a href="#education" class="lang-id">Konsultasi Gratis</a>
                <a href="#education" class="lang-en hidden">Free Consultation</a>
                <a href="#contact" class="lang-id">Hubungi Kami</a>
                <a href="#contact" class="lang-en hidden">Contact Us</a>
            </div>
            <div class="footer-section">
                <h3 class="lang-id">Kontak</h3>
                <h3 class="lang-en hidden">Contact</h3>
                <p>WhatsApp: +62 896-7694-3668</p>
                <p>Email: info@webpro.com</p>
                <p>Instagram: @fahreza_aw</p>
            </div>
        </div>
        <div class="footer-bottom">
            <p>&copy; 2024 WebPro. All Rights Reserved.</p>
        </div>
    </div>
</footer>

<script>
    // Mobile Menu Toggle
    const mobileMenuBtn = document.getElementById('mobileMenuBtn');
    const navMenu = document.getElementById('navMenu');

    mobileMenuBtn.addEventListener('click', () => {
        navMenu.classList.toggle('active');
    });

    // Close mobile menu when clicking on a link
    document.querySelectorAll('.nav-menu a').forEach(link => {
        link.addEventListener('click', () => {
            navMenu.classList.remove('active');
        });
    });

    // Language Switcher
    function switchLanguage(lang) {
        const langBtns = document.querySelectorAll('.lang-btn');
        const idElements = document.querySelectorAll('.lang-id');
        const enElements = document.querySelectorAll('.lang-en');

        if (lang === 'id') {
            idElements.forEach(el => el.classList.remove('hidden'));
            enElements.forEach(el => el.classList.add('hidden'));
            langBtns[0].classList.add('active');
            langBtns[1].classList.remove('active');
        } else {
            idElements.forEach(el => el.classList.add('hidden'));
            enElements.forEach(el => el.classList.remove('hidden'));
            langBtns[0].classList.remove('active');
            langBtns[1].classList.add('active');
        }
    }

    // Smooth Scrolling
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
        anchor.addEventListener('click', function (e) {
            e.preventDefault();
            const target = document.querySelector(this.getAttribute('href'));
            if (target) {
                target.scrollIntoView({
                    behavior: 'smooth',
                    block: 'start'
                });
            }
        });
    });

    // Add scroll effect to navigation
    window.addEventListener('scroll', () => {
        const nav = document.querySelector('nav');
        if (window.scrollY > 100) {
            nav.style.boxShadow = '0 5px 20px rgba(0,0,0,0.15)';
        } else {
            nav.style.boxShadow = '0 2px 10px rgba(0,0,0,0.1)';
        }
    });
</script>
