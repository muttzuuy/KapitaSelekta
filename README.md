<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mutiara Khairunnisa Zulkifli | Portfolio & Materi Kuliah</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>

        /* ====================================
           1. Variabel dan Reset Dasar
        ==================================== */
        :root {
            --primary: #6C63FF;
            --secondary: #FF6584;
            --accent: #36D1DC;
            --light: #F8F9FC;
            --dark: #2D3748;
            --success: #4ADE80;
            --warning: #FBBF24;
            --info: #60A5FA;
            --gradient-primary: linear-gradient(135deg, var(--primary), var(--accent));
            --gradient-secondary: linear-gradient(135deg, var(--secondary), #FF9A8B);
            --shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
            --shadow-hover: 0 15px 40px rgba(0, 0, 0, 0.15);
            --radius: 16px;
            --transition: all 0.3s ease;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Poppins', sans-serif;
            line-height: 1.6;
            color: var(--dark);
            background-color: var(--light);
            overflow-x: hidden;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* ====================================
           2. Layout Dasar dan Typography
        ==================================== */

        .section {
            padding: 80px 0;
        }

        .section-title {
            font-size: 2.5rem;
            font-weight: 700;
            text-align: center;
            margin-bottom: 1rem;
            background: var(--gradient-primary);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .section-subtitle {
            text-align: center;
            color: var(--dark);
            opacity: 0.8;
            margin-bottom: 3rem;
            font-size: 1.1rem;
        }

        /* ====================================
           3. Header dan Navigasi
        ==================================== */

        header {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
            transition: var(--transition);
        }

        header.scrolled {
            padding: 10px 0;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: var(--primary);
            display: flex;
            align-items: center;
        }

        .logo-icon {
            margin-right: 8px;
            font-size: 1.5rem;
        }

        .nav-links {
            display: flex;
            list-style: none;
            gap: 2.5rem;
        }

        .nav-links a {
            color: var(--dark);
            text-decoration: none;
            font-weight: 500;
            font-size: 1.1rem;
            transition: var(--transition);
            position: relative;
        }

        .nav-links a:after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--gradient-primary);
            border-radius: 10px;
            transition: var(--transition);
        }

        .nav-links a:hover {
            color: var(--primary);
        }

        .nav-links a:hover:after {
            width: 100%;
        }

        .hamburger {
            display: none;
            cursor: pointer;
            background: var(--gradient-primary);
            color: white;
            width: 45px;
            height: 45px;
            border-radius: 50%;
            justify-content: center;
            align-items: center;
            font-size: 1.5rem;
            box-shadow: var(--shadow);
        }

        /* ====================================
           4. Hero Section & Photo Zoom
        ==================================== */

        .hero {
            padding: 160px 0 100px;
            background: var(--gradient-primary);
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,255,255,0.05)"/></svg>');
            background-size: cover;
        }

        .hero-content {
            max-width: 800px;
            margin: 0 auto;
            text-align: center;
            position: relative;
            z-index: 1;
        }

        .hero-avatar {
            width: 180px;
            height: 180px;
            border-radius: 50%;
            margin: 0 auto 30px;
            border: 5px solid rgba(255, 255, 255, 0.2);
            box-shadow: var(--shadow);
            background: #ccc;
            display: flex;
            justify-content: center;
            align-items: center;
            color: white;
            font-size: 4rem;
            /* Penting untuk menahan overflow gambar saat zoom */
            overflow: hidden; 
        }

        /* Styling untuk gambar di dalam hero-avatar */
        .hero-avatar img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            /* Transisi untuk efek zoom halus */
            transition: transform 0.4s ease-in-out, filter 0.4s ease; 
        }

        /* Efek Zoom saat dihover */
        .hero-avatar:hover img {
            transform: scale(1.1); /* Zoom 10% */
            filter: brightness(1.05); 
        }

        .hero h1 {
            font-size: 3.5rem;
            font-weight: 800;
            margin-bottom: 1rem;
        }

        .hero p {
            font-size: 1.3rem;
            opacity: 0.9;
            margin-bottom: 2.5rem;
        }

        .hero-nim {
            background: rgba(255, 255, 255, 0.15);
            padding: 8px 20px;
            border-radius: 50px;
            display: inline-block;
            backdrop-filter: blur(10px);
            margin-top: 1rem;
        }


        /* ====================================
           5. Analisis Section (SWOT & Porter)
        ==================================== */
        .analysis-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(500px, 1fr));
            gap: 2.5rem;
            margin-top: 2rem;
        }

        .analysis-card {
            background: white;
            border-radius: var(--radius);
            padding: 2.5rem;
            box-shadow: var(--shadow);
            transition: var(--transition);
            position: relative;
            overflow: hidden;
        }
        
        .analysis-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 5px;
            height: 100%;
            background: var(--gradient-primary);
        }

        .analysis-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
        }

        .card-header {
            margin-bottom: 2rem;
            display: flex;
            align-items: center;
        }

        .card-icon {
            width: 60px;
            height: 60px;
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin-right: 1rem;
            font-size: 1.8rem;
            color: white;
        }

        .swot-icon {
            background: var(--gradient-primary);
        }

        .porter-icon {
            background: var(--gradient-secondary);
        }

        .card-header h3 {
            font-size: 1.8rem;
            color: var(--dark);
        }

        /* SWOT Details */
        .swot-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 1.5rem;
        }

        .swot-item {
            padding: 1.5rem;
            border-radius: 12px;
            transition: var(--transition);
        }

        .swot-item:hover {
            transform: translateY(-5px);
        }

        .strength {
            background: linear-gradient(135deg, rgba(74, 222, 128, 0.1), rgba(74, 222, 128, 0.2));
            border-left: 4px solid var(--success);
        }

        .weakness {
            background: linear-gradient(135deg, rgba(251, 191, 36, 0.1), rgba(251, 191, 36, 0.2));
            border-left: 4px solid var(--warning);
        }

        .opportunity {
            background: linear-gradient(135deg, rgba(96, 165, 250, 0.1), rgba(96, 165, 250, 0.2));
            border-left: 4px solid var(--info);
        }

        .threat {
            background: linear-gradient(135deg, rgba(255, 101, 132, 0.1), rgba(255, 101, 132, 0.2));
            border-left: 4px solid var(--secondary);
        }

        .swot-item h4 {
            font-size: 1.2rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
        }

        .swot-item h4 i {
            margin-right: 10px;
        }

        .swot-item ul {
            list-style: none;
        }

        .swot-item li {
            margin-bottom: 0.8rem;
            padding-left: 1.5rem;
            position: relative;
        }

        .swot-item li::before {
            content: '•';
            position: absolute;
            left: 0;
            color: currentColor;
            font-weight: bold;
        }


        /* Porter's Five Forces Details */
        .forces-grid {
            display: grid;
            gap: 1.5rem;
        }
        
        .force-item {
            background: #F8FAFF;
            padding: 1.5rem;
            border-radius: 12px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            transition: var(--transition);
        }

        .force-item:hover {
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }

        .force-header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 0.5rem;
        }

        .force-name {
            font-weight: 600;
            font-size: 1.1rem;
        }

        .force-value {
            font-weight: 700;
            background: var(--gradient-primary);
            padding: 4px 12px;
            border-radius: 20px;
            color: white;
            font-size: 0.9rem;
        }

        .force-item p {
            font-size: 0.95rem;
            opacity: 0.8;
            margin-bottom: 0.5rem;
        }

        .force-level-container {
            background: #E2E8F0;
            height: 10px;
            border-radius: 10px;
            overflow: hidden;
            margin-top: 0.5rem;
        }

        .force-level {
            height: 100%;
            border-radius: 10px;
            /* Inisialisasi width 0 untuk animasi JS */
            width: 0; 
            transition: width 1.5s ease;
        }

        .high { background: var(--secondary); }
        .medium { background: var(--primary); }
        .low { background: var(--accent); }


        /* ====================================
           6. Rencana Akademik (NEW)
        ==================================== */
        
        .academic-plan-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
            gap: 2.5rem;
            margin-top: 3rem;
        }

        .academic-card {
            background: white;
            padding: 2.5rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            border-top: 5px solid var(--secondary); /* Warna berbeda untuk estetika */
            transition: var(--transition);
        }
        
        .academic-card:nth-child(2) {
            border-top: 5px solid var(--info); 
        }

        .academic-card h3 {
            font-size: 1.6rem;
            color: var(--dark);
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .academic-card h4 {
            font-size: 1.1rem;
            font-weight: 700;
            margin-top: 1rem;
            color: var(--primary);
        }

        .academic-card p {
            font-size: 0.95rem;
            opacity: 0.8;
            margin-top: 0.5rem;
            line-height: 1.5;
        }

        /* ====================================
           7. Open Source Philosophy
        ==================================== */
        
        .philosophy {
            background: linear-gradient(to bottom, #F8FAFF, #FFFFFF);
        }

        .philosophy-content {
            max-width: 900px;
            margin: 0 auto;
            text-align: center;
        }

        .philosophy-text {
            font-size: 1.1rem;
            line-height: 1.8;
            margin-bottom: 3rem;
            color: var(--dark);
            opacity: 0.9;
        }

        .philosophy-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 2rem;
            margin-top: 3rem;
        }

        .philosophy-card {
            background: white;
            padding: 2.5rem 2rem;
            border-radius: var(--radius);
            box-shadow: var(--shadow);
            transition: var(--transition);
            text-align: center;
        }

        .philosophy-card:hover {
            transform: translateY(-10px);
            box-shadow: var(--shadow-hover);
        }

        .philosophy-icon {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto 1.5rem;
            font-size: 2rem;
            color: white;
            background: var(--gradient-primary);
        }

        .philosophy-card h3 {
            font-size: 1.4rem;
            margin-bottom: 1rem;
            color: var(--dark);
        }

        .philosophy-card p {
            color: var(--dark);
            opacity: 0.8;
            line-height: 1.6;
        }
        
        /* ====================================
           8. Footer dan Kontak
        ==================================== */
        
        footer {
            background: var(--dark);
            color: white;
            padding: 80px 0 30px;
        }

        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 3rem;
            margin-bottom: 3rem;
        }

        .footer-col h3 {
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            position: relative;
            padding-bottom: 10px;
        }

        .footer-col h3::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 50px;
            height: 3px;
            background: var(--gradient-primary);
            border-radius: 3px;
        }

        .footer-col p {
            margin-bottom: 1rem;
            opacity: 0.8;
        }

        .social-links {
            display: flex;
            gap: 1rem;
            margin-top: 1.5rem;
        }

        .social-link {
            width: 45px;
            height: 45px;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            background: rgba(255, 255, 255, 0.1);
            color: white;
            font-size: 1.2rem;
            transition: var(--transition);
        }

        .social-link:hover {
            background: var(--primary);
            transform: translateY(-5px);
        }

        .copyright {
            text-align: center;
            padding-top: 30px;
            border-top: 1px solid rgba(255, 255, 255, 0.1);
            opacity: 0.7;
        }

        /* ====================================
           9. Responsive Design
        ==================================== */
        @media (max-width: 1024px) {
            .analysis-grid {
                grid-template-columns: 1fr;
            }
        }

        @media (max-width: 768px) {
            .nav-links {
                position: fixed;
                top: 0;
                right: -300px;
                width: 300px;
                height: 100vh;
                background: white;
                flex-direction: column;
                align-items: center;
                justify-content: center;
                gap: 2rem;
                box-shadow: -5px 0 30px rgba(0, 0, 0, 0.1);
                transition: var(--transition);
            }

            .nav-links.active {
                right: 0;
            }

            .hamburger {
                display: flex;
            }

            .hero h1 {
                font-size: 2.5rem;
            }

            .hero p {
                font-size: 1.1rem;
            }

            .swot-grid {
                grid-template-columns: 1fr;
            }
            
            .academic-plan-grid {
                grid-template-columns: 1fr;
            }

            .section-title {
                font-size: 2rem;
            }
        }

        @media (max-width: 480px) {
            .container {
                padding: 0 15px;
            }

            .hero {
                padding: 130px 0 80px;
            }

            .hero-avatar {
                width: 150px;
                height: 150px;
            }

            .hero h1 {
                font-size: 2rem;
            }

            .analysis-card {
                padding: 2rem 1.5rem;
            }

            .section {
                padding: 60px 0;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">
                    <span class="logo-icon"><i class="fas fa-code"></i></span>
                    MutiaraKZ
                </div>
                <ul class="nav-links">
                    <li><a href="#home"><i class="fas fa-home"></i> Beranda</a></li>
                    <li><a href="#analysis"><i class="fas fa-chart-pie"></i> Analisis</a></li>
                    <li><a href="#academic-plan"><i class="fas fa-book"></i> Akademik</a></li> 
                    <li><a href="#philosophy"><i class="fas fa-lightbulb"></i> Open Source</a></li>
                    <li><a href="#contact"><i class="fas fa-envelope"></i> Kontak</a></li>
                </ul>
                <div class="hamburger">
                    <i class="fas fa-bars"></i>
                </div>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container hero-content">
            <div class="hero-avatar">
                <img src="muti.jpeg" alt="Foto Profil Mutiara Khairunnisa Zulkifli">
            </div>
            <h1>Mutiara Khairunnisa Zulkifli</h1>
            <p>Mahasiswa Teknik Informatika | Frontend Developer</p>
            <p>Selamat datang di laman pribadi saya yang berisi portofolio dan materi kuliah Kapita Selekta.</p>
            <div class="hero-nim">
                <i class="fas fa-id-card"></i> NPM: 2315061060
            </div>
        </div>
    </section>

    <section id="analysis" class="section">
        <div class="container">
            <h2 class="section-title">Analisis Kapita Selekta</h2>
            <p class="section-subtitle">Analisis SWOT dan Porter's Five Forces untuk Frontend Web Development</p>
            
            <div class="analysis-grid">
                <div class="analysis-card">
                    <div class="card-header">
                        <div class="card-icon swot-icon">
                            <i class="fas fa-swot-analysis"></i>
                        </div>
                        <h3>Analisis SWOT</h3>
                    </div>
                    <div class="swot-grid">
                        <div class="swot-item strength">
                            <h4><i class="fas fa-plus-circle"></i> Strength</h4>
                            <ul>
                                <li>Menguasai dasar HTML & CSS</li>
                                <li>Bisa menggunakan Bootstrap untuk desain responsif</li>
                                <li>Teliti dalam layout dan visual</li>
                                <li>Termotivasi untuk terus belajar</li>
                            </ul>
                        </div>
                        <div class="swot-item weakness">
                            <h4><i class="fas fa-minus-circle"></i> Weakness</h4>
                            <ul>
                                <li>Belum familiar dengan JavaScript & framework modern</li>
                                <li>Masih bergantung pada template</li>
                                <li>Minim pengalaman optimasi performa & testing</li>
                            </ul>
                        </div>
                        <div class="swot-item opportunity">
                            <h4><i class="fas fa-arrow-up-right-from-square"></i> Opportunity</h4>
                            <ul>
                                <li>Banyak sumber belajar online untuk tingkatkan skill</li>
                                <li>Permintaan besar untuk frontend developer</li>
                                <li>Digitalisasi membuka peluang skripsi & KP</li>
                                <li>Bisa mulai bangun portofolio kecil</li>
                            </ul>
                        </div>
                        <div class="swot-item threat">
                            <h4><i class="fas fa-exclamation-triangle"></i> Threat</h4>
                            <ul>
                                <li>Persaingan ketat dengan developer lebih mahir</li>
                                <li>Website builder bisa gantikan web sederhana</li>
                                <li>Teknologi frontend cepat berubah</li>
                                <li>Ekspektasi industri cukup tinggi</li>
                            </ul>
                        </div>
                    </div>
                </div>

                <div class="analysis-card">
                    <div class="card-header">
                        <div class="card-icon porter-icon">
                            <i class="fas fa-chess-board"></i>
                        </div>
                        <h3>Porter's Five Forces</h3>
                    </div>
                    <div class="forces-grid">
                        <div class="force-item">
                            <div class="force-header">
                                <span class="force-name">01. Threat of New Entrants</span>
                                <span class="force-value" style="background: var(--gradient-secondary);">Sangat Tinggi</span>
                            </div>
                            <p>Banyak kursus online dan bootcamp yang menawarkan pembelajaran intensif, sehingga jumlah pendatang baru semakin besar.</p>
                            <div class="force-level-container"><div class="force-level high" style="width: 90%"></div></div>
                        </div>
                        <div class="force-item">
                            <div class="force-header">
                                <span class="force-name">02. Bargaining Power of Supplier</span>
                                <span class="force-value" style="background: var(--gradient-primary);">Rendah - Sedang</span>
                            </div>
                            <p>Framework, library, dan browser bersifat open-source dan memiliki banyak alternatif, sehingga kekuatan tawar mereka tidak terlalu dominan.</p>
                            <div class="force-level-container"><div class="force-level medium" style="width: 45%"></div></div>
                        </div>
                        <div class="force-item">
                            <div class="force-header">
                                <span class="force-name">03. Bargaining Power of Buyers</span>
                                <span class="force-value" style="background: var(--gradient-secondary);">Tinggi</span>
                            </div>
                            <p>Perusahaan dan klien memiliki banyak opsi pengembang, sehingga dapat menekan harga dan waktu pengerjaan.</p>
                            <div class="force-level-container"><div class="force-level high" style="width: 80%"></div></div>
                        </div>
                        <div class="force-item">
                            <div class="force-header">
                                <span class="force-name">04. Threat of Substitutes</span>
                                <span class="force-value" style="background: var(--gradient-secondary);">Tinggi</span>
                            </div>
                            <p>Website builder, CMS, dan platform SaaS mampu menggantikan sebagian besar kebutuhan web standar.</p>
                            <div class="force-level-container"><div class="force-level high" style="width: 85%"></div></div>
                        </div>
                        <div class="force-item">
                            <div class="force-header">
                                <span class="force-name">05. Industry Rivalry</span>
                                <span class="force-value" style="background: var(--gradient-secondary);">Sangat Ketat</span>
                            </div>
                            <p>Frontend menjadi bidang populer sehingga banyak developer bersaing di tingkat lokal maupun global.</p>
                            <div class="force-level-container"><div class="force-level high" style="width: 95%"></div></div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="academic-plan" class="section">
        <div class="container">
            <h2 class="section-title">Rencana Akademik</h2>
            <p class="section-subtitle">Rencana Kerja Praktik (KP) dan Skripsi di Bidang Rekayasa Perangkat Lunak</p>
            
            <div class="academic-plan-grid">
                
                <div class="academic-card">
                    <h3><i class="fas fa-clipboard-list"></i> Kerja Praktik (KP)</h3>
                    <h4>Implementasi Sistem Penjadwalan Kuliah Otomatis Berbasis Web dengan Constraint-Based Scheduling dan Fitur Validasi Bentrok Jadwal.</h4>
                    <p>Rencana KP ini berfokus pada penerapan dasar-dasar frontend web development dalam membangun antarmuka pengguna yang intuitif untuk sistem penjadwalan. Tujuannya adalah mengimplementasikan tampilan jadwal, formulir input constraint, dan menampilkan hasil validasi bentrok jadwal secara visual dan user-friendly.</p>
                    <p>KP ini menjadi batu loncatan praktik untuk memahami alur kerja dan kebutuhan fungsional sebelum pengembangan proyek akhir skripsi yang lebih kompleks.</p>
                </div>

                <div class="academic-card">
                    <h3><i class="fas fa-graduation-cap"></i> Skripsi</h3>
                    <h4>Perancangan dan Implementasi Aplikasi Penjadwalan Kuliah Otomatis Berbasis Web dan Mobile dengan Pendekatan Constraint-Based Scheduling serta Evaluasi Usability.</h4>
                    <p>Proyek skripsi ini merupakan pengembangan holistik dari KP, mencakup perancangan sistem dari hulu ke hilir, pengembangan aplikasi multi-platform (Web dan Mobile), serta penerapan algoritma Constraint-Based Scheduling yang solid.</p>
                    <p>Fokus akhirnya adalah melakukan evaluasi usability menggunakan metodologi terstruktur untuk memastikan sistem tidak hanya berfungsi secara teknis tetapi juga mudah dan efektif digunakan oleh pengguna, baik admin maupun mahasiswa.</p>
                </div>
                
            </div>
        </div>
    </section>

    <section id="philosophy" class="section philosophy">
        <div class="container">
            <h2 class="section-title">Filosofi Open Source</h2>
            <p class="section-subtitle">Konsep dan pentingnya Open Source dalam pengembangan perangkat lunak</p>
            
            <div class="philosophy-content">
                <p class="philosophy-text">
                    Open Source Philosophy adalah pendekatan pengembangan perangkat lunak yang menekankan pada transparansi, kolaborasi, dan kebebasan dalam mengakses, memodifikasi, dan mendistribusikan kode sumber. 
                    Filosofi ini telah mengubah landscape teknologi modern dan menjadi fondasi bagi inovasi di dunia pengembangan web dan software.
                </p>
                
                <div class="philosophy-grid">
                    <div class="philosophy-card">
                        <div class="philosophy-icon"> <i class="fas fa-lock-open"></i> </div>
                        <h3>Transparansi</h3>
                        <p>Kode sumber terbuka untuk dilihat dan diaudit oleh siapa saja, menciptakan kepercayaan dan akuntabilitas dalam pengembangan software.</p>
                    </div>
                    <div class="philosophy-card">
                        <div class="philosophy-icon"> <i class="fas fa-users"></i> </div>
                        <h3>Kolaborasi</h3>
                        <p>Developer dari seluruh dunia dapat berkontribusi, memperbaiki bug, dan menambahkan fitur baru, mempercepat inovasi dan perbaikan.</p>
                    </div>
                    <div class="philosophy-card">
                        <div class="philosophy-icon"> <i class="fas fa-rocket"></i> </div>
                        <h3>Inovasi</h3>
                        <p>Open Source mendorong inovasi cepat melalui berbagi pengetahuan dan kode yang dapat digunakan kembali untuk membangun solusi yang lebih baik.</p>
                    </div>
                    <div class="philosophy-card">
                        <div class="philosophy-icon"> <i class="fas fa-graduation-cap"></i> </div>
                        <h3>Pembelajaran</h3>
                        <p>Memberikan kesempatan belajar yang luar biasa bagi developer pemula dan profesional dengan mempelajari kode dari proyek-proyek real-world.</p>
                    </div>
                </div>

                <p class="philosophy-text" style="margin-top: 3rem;">
                    Dalam konteks Frontend Development, filosofi open source memungkinkan developer untuk memanfaatkan library dan framework yang sudah terbukti, 
                    berkontribusi pada komunitas, dan terus mengembangkan skill melalui kolaborasi dengan developer lainnya di seluruh dunia.
                </p>
            </div>
        </div>
    </section>

    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-col">
                    <h3>Tentang Saya</h3>
                    <p>Mahasiswa Teknik Informatika yang bersemangat dalam pengembangan web frontend dan tertarik dengan teknologi terkini.</p>
                    <div class="social-links">
                        <a href="https://www.linkedin.com/in/mutiara-khairunnisa-zulkifli-15692b293 " class="social-link" target="_blank"><i class="fab fa-linkedin"></i></a>
                        <a href="https://github.com/muttzuuy/KapitaSelekta" class="social-link" target="_blank"><i class="fab fa-github"></i></a>
                        <a href="https://www.instagram.com/muttzuu" class="social-link" target="_blank"><i class="fab fa-instagram"></i></a>
                        <a href="#" class="social-link"><i class="fab fa-twitter"></i></a>
                    </div>
                </div>
                <div class="footer-col">
                    <h3>Kontak Saya (Contact Me)</h3>
                    <p><i class="fas fa-envelope"></i> mutiarakhzz88@gmail.com</p>
                    <p><i class="fab fa-whatsapp"></i> WhatsApp: <a href="https://wa.me/6281367865908" style="color:white; text-decoration:none;">081367865908</a></p>
                    <p><i class="fas fa-map-marker-alt"></i> Bandar Lampung, Indonesia</p>
                </div>
                <div class="footer-col">
                    <h3>Pendidikan</h3>
                    <p><i class="fas fa-university"></i> Universitas Lampung</p>
                    <p><i class="fas fa-code"></i> Teknik Informatika</p>
                    <p><i class="fas fa-id-card"></i> NPM: 2315061060</p>
                </div>
            </div>
            <div class="copyright">
                <p>&copy; 2025 Mutiara Khairunnisa Zulkifli. Dibuat dengan <i class="fas fa-heart" style="color: var(--secondary);"></i> </p>
            </div>
        </div>
    </footer>

    <script>
    
        document.addEventListener('DOMContentLoaded', function() {
            const hamburger = document.querySelector('.hamburger');
            const navLinks = document.querySelector('.nav-links');
            const header = document.querySelector('header');
            
            // Toggle Nav untuk Mobile
            hamburger.addEventListener('click', function() {
                navLinks.classList.toggle('active');
                hamburger.innerHTML = navLinks.classList.contains('active') ? 
                    '<i class="fas fa-times"></i>' : '<i class="fas fa-bars"></i>';
            });

            // Efek Scroll pada Header
            window.addEventListener('scroll', function() {
                if (window.scrollY > 50) {
                    header.classList.add('scrolled');
                } else {
                    header.classList.remove('scrolled');
                }
            });

            // Smooth Scrolling dan Menutup Nav Mobile setelah klik
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                        navLinks.classList.remove('active');
                        hamburger.innerHTML = '<i class="fas fa-bars"></i>';
                    }
                });
            });

            
            // Observer untuk Animasi Porter's Five Forces (Progress Bar)
            const observerOptions = {
                threshold: 0.3 // Mulai animasi ketika 30% elemen terlihat
            };

            const observer = new IntersectionObserver((entries, observer) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        const forceLevels = entry.target.querySelectorAll('.force-level');
                        forceLevels.forEach(level => {
                            const width = level.style.width;
                            // Set ulang width ke 0
                            level.style.width = '0';
                            // Terapkan width asli setelah timeout singkat untuk animasi
                            setTimeout(() => {
                                level.style.width = width;
                            }, 100); 
                        });
                        // Hentikan observasi setelah animasi berjalan
                        observer.unobserve(entry.target); 
                    }
                });
            }, observerOptions);

            // Mulai mengamati setiap item Porter's Five Forces
            document.querySelectorAll('#analysis .analysis-card:nth-child(2)').forEach(card => {
                observer.observe(card);
            });
        });
    </script>
</body>
</html>
