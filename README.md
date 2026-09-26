<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Pelayanan Kefarmasian</title>

    <meta name="description" content="Website pelayanan kefarmasian yang memberikan informasi pelayanan serta memudahkan pasien melakukan pendaftaran secara online.">

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: #ffffff;
            color: #35443A;
            line-height: 1.7;
        }

        /* =========================
           COLOR
        ========================= */
        :root {
            --sage: #A8BFAE;
            --sage-dark: #789781;
            --sage-light: #EFF5F0;
            --pink: #E8B7C3;
            --pink-dark: #D38FA0;
            --white: #FFFFFF;
            --text: #35443A;
            --gray: #68766d;
            --light: #f8faf8;
        }

        /* =========================
           NAVBAR
        ========================= */
        .navbar {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            z-index: 1000;
            background: rgba(255,255,255,0.96);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 15px rgba(53,68,58,0.08);
        }

        .nav-container {
            max-width: 1200px;
            margin: auto;
            padding: 15px 25px;
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            text-decoration: none;
            color: var(--sage-dark);
            font-weight: 800;
            font-size: 21px;
            letter-spacing: 0.5px;
        }

        .logo span {
            color: var(--pink-dark);
        }

        .nav-menu {
            display: flex;
            align-items: center;
            gap: 22px;
            list-style: none;
        }

        .nav-menu a {
            text-decoration: none;
            color: var(--text);
            font-size: 14px;
            font-weight: 600;
            transition: 0.3s;
        }

        .nav-menu a:hover {
            color: var(--pink-dark);
        }

        .nav-button {
            background: var(--sage-dark) !important;
            color: white !important;
            padding: 10px 17px;
            border-radius: 10px;
        }

        .nav-button:hover {
            background: var(--pink-dark) !important;
        }

        .menu-toggle {
            display: none;
            font-size: 27px;
            cursor: pointer;
            color: var(--sage-dark);
        }

        /* =========================
           HERO
        ========================= */
        .hero {
            min-height: 100vh;
            padding: 150px 25px 80px;
            background: linear-gradient(
                135deg,
                #EFF5F0 0%,
                #FFFFFF 60%,
                #f9e9ed 100%
            );
            display: flex;
            align-items: center;
        }

        .hero-container {
            max-width: 1200px;
            margin: auto;
            width: 100%;
            display: grid;
            grid-template-columns: 1.1fr 0.9fr;
            gap: 60px;
            align-items: center;
        }

        .hero-small {
            color: var(--pink-dark);
            font-weight: 700;
            margin-bottom: 10px;
            font-size: 16px;
        }

        .hero h1 {
            font-size: clamp(38px, 6vw, 65px);
            line-height: 1.1;
            margin-bottom: 20px;
            color: var(--sage-dark);
        }

        .hero h2 {
            font-size: 25px;
            color: var(--text);
            margin-bottom: 18px;
            font-weight: 600;
        }

        .hero p {
            color: var(--gray);
            max-width: 650px;
            margin-bottom: 30px;
        }

        .hero-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 14px;
        }

        .btn {
            display: inline-block;
            padding: 13px 22px;
            border-radius: 11px;
            text-decoration: none;
            font-weight: 700;
            transition: 0.3s ease;
            border: none;
            cursor: pointer;
        }

        .btn-primary {
            background: var(--sage-dark);
            color: white;
        }

        .btn-primary:hover {
            background: var(--pink-dark);
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: white;
            color: var(--sage-dark);
            border: 1px solid var(--sage);
        }

        .btn-secondary:hover {
            background: var(--sage-light);
        }

        .hero-illustration {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .medical-card {
            width: 330px;
            height: 330px;
            border-radius: 50%;
            background: var(--sage);
            position: relative;
            display: flex;
            align-items: center;
            justify-content: center;
            box-shadow: 0 20px 50px rgba(120,151,129,0.22);
        }

        .medical-card::before {
            content: "";
            width: 130px;
            height: 130px;
            background: white;
            border-radius: 25px;
            position: absolute;
        }

        .medical-cross {
            position: relative;
            width: 80px;
            height: 80px;
            z-index: 2;
        }

        .medical-cross::before,
        .medical-cross::after {
            content: "";
            position: absolute;
            background: var(--pink-dark);
            border-radius: 10px;
        }

        .medical-cross::before {
            width: 80px;
            height: 25px;
            top: 27px;
            left: 0;
        }

        .medical-cross::after {
            width: 25px;
            height: 80px;
            top: 0;
            left: 27px;
        }

        /* =========================
           GENERAL SECTION
        ========================= */
        .section {
            padding: 90px 25px;
        }

        .section:nth-child(even) {
            background: var(--light);
        }

        .container {
            max-width: 1200px;
            margin: auto;
        }

        .section-header {
            text-align: center;
            max-width: 750px;
            margin: 0 auto 45px;
        }

        .section-label {
            color: var(--pink-dark);
            font-weight: 800;
            text-transform: uppercase;
            font-size: 13px;
            letter-spacing: 1px;
        }

        .section-header h2 {
            font-size: 35px;
            margin: 8px 0 15px;
            color: var(--sage-dark);
        }

        .section-header p {
            color: var(--gray);
        }

        /* =========================
           PENGERTIAN
        ========================= */
        .definition-box {
            background: white;
            border-left: 6px solid var(--pink);
            padding: 28px;
            border-radius: 15px;
            box-shadow: 0 8px 25px rgba(53,68,58,0.07);
            max-width: 950px;
            margin: auto;
        }

        .definition-box p {
            color: var(--gray);
        }

        .info-grid {
            display: grid;
            grid-template-columns: repeat(3,1fr);
            gap: 22px;
            margin-top: 30px;
        }

        .info-card {
            background: white;
            border-radius: 18px;
            padding: 27px;
            box-shadow: 0 8px 25px rgba(53,68,58,0.07);
            border: 1px solid #e7eee9;
        }

        .info-icon {
            font-size: 32px;
            margin-bottom: 12px;
        }

        .info-card h3 {
            color: var(--sage-dark);
            margin-bottom: 8px;
        }

        .info-card p {
            color: var(--gray);
            font-size: 14px;
        }

        /* =========================
           SERVICE
        ========================= */
        .service-grid {
            display: grid;
            grid-template-columns: repeat(3,1fr);
            gap: 22px;
        }

        .service-card {
            background: white;
            padding: 28px;
            border-radius: 18px;
            border: 1px solid #e5ece7;
            box-shadow: 0 7px 22px rgba(53,68,58,0.06);
            transition: 0.3s;
        }

        .service-card:hover {
            transform: translateY(-5px);
            border-color: var(--pink);
        }

        .service-card .icon {
            font-size: 35px;
            margin-bottom: 12px;
        }

        .service-card h3 {
            color: var(--sage-dark);
            margin-bottom: 8px;
        }

        .service-card p {
            color: var(--gray);
            font-size: 14px;
        }

        /* =========================
           PENDAFTARAN
        ========================= */
        .registration-box {
            background: linear-gradient(135deg, var(--sage-light), #fff5f7);
            padding: 45px;
            border-radius: 25px;
            text-align: center;
            border: 1px solid #e3ebe5;
        }

        .registration-box h3 {
            font-size: 27px;
            color: var(--sage-dark);
            margin-bottom: 12px;
        }

        .registration-box p {
            max-width: 750px;
            margin: 0 auto 25px;
            color: var(--gray);
        }

        .registration-list {
            max-width: 600px;
            margin: 20px auto 30px;
            text-align: left;
        }

        .registration-list div {
            background: white;
            padding: 12px 18px;
            border-radius: 10px;
            margin-bottom: 9px;
            border-left: 4px solid var(--pink);
        }

        /* =========================
           ANTREAN
        ========================= */
        .queue-grid {
            display: grid;
            grid-template-columns: repeat(5,1fr);
            gap: 15px;
        }

        .queue-step {
            text-align: center;
            background: white;
            border-radius: 17px;
            padding: 22px 15px;
            box-shadow: 0 7px 20px rgba(53,68,58,0.06);
        }

        .queue-number {
            width: 45px;
            height: 45px;
            margin: 0 auto 12px;
            border-radius: 50%;
            background: var(--pink);
            color: white;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
        }

        .queue-step h4 {
            font-size: 15px;
            color: var(--sage-dark);
            margin-bottom: 6px;
        }

        .queue-step p {
            color: var(--gray);
            font-size: 13px;
        }

        /* =========================
           ALUR PENDAFTARAN
        ========================= */
        .timeline {
            max-width: 850px;
            margin: auto;
            position: relative;
        }

        .timeline::before {
            content: "";
            position: absolute;
            left: 24px;
            top: 10px;
            bottom: 10px;
            width: 2px;
            background: var(--sage);
        }

        .timeline-item {
            position: relative;
            display: flex;
            gap: 25px;
            margin-bottom: 25px;
        }

        .timeline-number {
            flex-shrink: 0;
            width: 50px;
            height: 50px;
            border-radius: 50%;
            background: var(--sage-dark);
            color: white;
            display: flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            z-index: 2;
        }

        .timeline-content {
            background: white;
            padding: 20px 25px;
            border-radius: 15px;
            box-shadow: 0 7px 20px rgba(53,68,58,0.06);
            flex: 1;
        }

        .timeline-content h3 {
            color: var(--sage-dark);
            margin-bottom: 5px;
        }

        .timeline-content p {
            color: var(--gray);
            font-size: 14px;
        }

        /* =========================
           RESEP
        ========================= */
        .prescription-flow {
            display: grid;
            grid-template-columns: repeat(4,1fr);
            gap: 18px;
        }

        .prescription-step {
            background: white;
            padding: 25px 18px;
            border-radius: 17px;
            text-align: center;
            box-shadow: 0 7px 20px rgba(53,68,58,0.06);
            border-top: 4px solid var(--sage);
        }

        .prescription-step:nth-child(even) {
            border-top-color: var(--pink);
        }

        .prescription-step span {
            font-size: 30px;
        }

        .prescription-step h4 {
            margin: 10px 0 5px;
            color: var(--sage-dark);
        }

        .prescription-step p {
            color: var(--gray);
            font-size: 13px;
        }

        /* =========================
           KONSULTASI
        ========================= */
        .consultation-intro {
            max-width: 850px;
            margin: 0 auto 35px;
            text-align: center;
            color: var(--gray);
        }

        .consultation-topics {
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            margin-bottom: 40px;
        }

        .topic {
            background: var(--sage-light);
            color: var(--sage-dark);
            border-radius: 30px;
            padding: 9px 16px;
            font-size: 13px;
            font-weight: 600;
        }

        .pharmacist-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 24px;
        }

        .pharmacist-card {
            background: #ffffff;
            border: 1px solid #dfe9e1;
            border-radius: 20px;
            padding: 28px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(120,151,129,0.10);
            transition: 0.3s ease;
        }

        .pharmacist-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 12px 30px rgba(120,151,129,0.18);
        }

        .pharmacist-icon {
            width: 65px;
            height: 65px;
            margin: 0 auto 15px;
            background: #f8e5ea;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 30px;
        }

        .pharmacist-card h3 {
            color: var(--text);
            font-size: 18px;
            margin-bottom: 10px;
        }

        .pharmacist-card p {
            color: var(--gray);
            margin-bottom: 20px;
        }

        .btn-whatsapp {
            display: inline-block;
            background: var(--sage-dark);
            color: white;
            padding: 11px 18px;
            border-radius: 10px;
            text-decoration: none;
            font-weight: 600;
            transition: 0.3s ease;
        }

        .btn-whatsapp:hover {
            background: var(--pink-dark);
        }

        /* =========================
           SWAMEDIKASI
        ========================= */
        .self-medication-box {
            max-width: 900px;
            margin: auto;
            background: white;
            border-radius: 22px;
            padding: 35px;
            box-shadow: 0 8px 25px rgba(53,68,58,0.07);
        }

        .self-medication-box h3 {
            color: var(--sage-dark);
            margin-bottom: 12px;
        }

        .self-medication-box p {
            color: var(--gray);
            margin-bottom: 15px;
        }

        .warning {
            background: #fff1f4;
            border-left: 5px solid var(--pink-dark);
            padding: 15px 18px;
            border-radius: 10px;
            color: #72505a;
        }

        /* =========================
           FAQ
        ========================= */
        .faq-container {
            max-width: 850px;
            margin: auto;
        }

        .faq-item {
            background: white;
            margin-bottom: 12px;
            border-radius: 14px;
            padding: 20px 22px;
            box-shadow: 0 5px 17px rgba(53,68,58,0.06);
        }

        .faq-item h3 {
            color: var(--sage-dark);
            font-size: 16px;
            margin-bottom: 7px;
        }

        .faq-item p {
            color: var(--gray);
            font-size: 14px;
        }

        /* =========================
           KONTAK
        ========================= */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(3,1fr);
            gap: 22px;
        }

        .contact-card {
            text-align: center;
            background: white;
            padding: 30px 20px;
            border-radius: 18px;
            box-shadow: 0 7px 22px rgba(53,68,58,0.06);
        }

        .contact-icon {
            font-size: 32px;
            margin-bottom: 10px;
        }

        .contact-card h3 {
            color: var(--sage-dark);
            margin-bottom: 8px;
        }

        .contact-card p,
        .contact-card a {
            color: var(--gray);
            text-decoration: none;
            font-size: 14px;
        }

        .contact-card a:hover {
            color: var(--pink-dark);
        }

        /* =========================
           FOOTER
        ========================= */
        footer {
            background: #35443A;
            color: white;
            padding: 50px 25px 25px;
        }

        .footer-grid {
            max-width: 1200px;
            margin: auto;
            display: grid;
            grid-template-columns: 1.2fr 1fr 1fr;
            gap: 40px;
        }

        .footer-title {
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 12px;
        }

        .footer-grid p {
            color: #d8e0da;
            font-size: 14px;
        }

        .footer-grid a {
            color: #d8e0da;
            text-decoration: none;
            display: block;
            margin-bottom: 7px;
            font-size: 14px;
        }

        .footer-grid a:hover {
            color: var(--pink);
        }

        .copyright {
            max-width: 1200px;
            margin: 35px auto 0;
            padding-top: 20px;
            border-top: 1px solid rgba(255,255,255,0.15);
            text-align: center;
            color: #c9d2cb;
            font-size: 13px;
        }

        /* =========================
           BACK TO TOP
        ========================= */
        #backToTop {
            position: fixed;
            right: 20px;
            bottom: 20px;
            width: 45px;
            height: 45px;
            border: none;
            border-radius: 50%;
            background: var(--pink-dark);
            color: white;
            font-size: 20px;
            cursor: pointer;
            display: none;
            z-index: 999;
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
        }

        /* =========================
           RESPONSIVE
        ========================= */
        @media (max-width: 1000px) {

            .nav-menu {
                gap: 12px;
            }

            .nav-menu a {
                font-size: 12px;
            }

            .hero-container {
                grid-template-columns: 1fr;
                text-align: center;
            }

            .hero p {
                margin-left: auto;
                margin-right: auto;
            }

            .hero-buttons {
                justify-content: center;
            }

            .info-grid,
            .service-grid {
                grid-template-columns: repeat(2,1fr);
            }

            .queue-grid {
                grid-template-columns: repeat(3,1fr);
            }

            .prescription-flow {
                grid-template-columns: repeat(2,1fr);
            }

            .contact-grid {
                grid-template-columns: repeat(2,1fr);
            }
        }

        @media (max-width: 768px) {

            .nav-menu {
                position: absolute;
                top: 70px;
                left: 0;
                width: 100%;
                background: white;
                display: none;
                flex-direction: column;
                align-items: stretch;
                padding: 20px;
                box-shadow: 0 8px 20px rgba(53,68,58,0.08);
            }

            .nav-menu.active {
                display: flex;
            }

            .nav-menu li {
                text-align: center;
            }

            .nav-menu a {
                display: block;
                padding: 10px;
                font-size: 14px;
            }

            .menu-toggle {
                display: block;
            }

            .hero {
                padding-top: 130px;
            }

            .medical-card {
                width: 250px;
                height: 250px;
            }

            .section {
                padding: 70px 18px;
            }

            .section-header h2 {
                font-size: 29px;
            }

            .info-grid,
            .service-grid,
            .pharmacist-grid,
            .contact-grid {
                grid-template-columns: 1fr;
            }

            .queue-grid {
                grid-template-columns: 1fr 1fr;
            }

            .prescription-flow {
                grid-template-columns: 1fr;
            }

            .registration-box {
                padding: 28px 20px;
            }

            .footer-grid {
                grid-template-columns: 1fr;
                gap: 25px;
            }
        }

        @media (max-width: 450px) {

            .hero h1 {
                font-size: 38px;
            }

            .hero h2 {
                font-size: 20px;
            }

            .queue-grid {
                grid-template-columns: 1fr;
            }

            .timeline-item {
                gap: 15px;
            }

            .timeline-content {
                padding: 17px;
            }

            .pharmacist-card {
                padding: 23px 17px;
            }

            .pharmacist-card h3 {
                font-size: 16px;
            }
        }
    </style>
</head>

<body>

<!-- =========================
     NAVBAR
========================= -->
<header class="navbar">
    <div class="nav-container">

        <a href="#beranda" class="logo">
            PELAYANAN <span>KEFARMASIAN</span>
        </a>

        <div class="menu-toggle" onclick="toggleMenu()">☰</div>

        <ul class="nav-menu" id="navMenu">
            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#pengertian">Pengertian</a></li>
            <li><a href="#pendaftaran">Pendaftaran</a></li>
            <li><a href="#alur">Alur Pendaftaran</a></li>
            <li><a href="#resep">Pelayanan Resep</a></li>
            <li><a href="#konsultasi">Konsultasi</a></li>
            <li><a href="#swamedikasi">Swamedikasi</a></li>
            <li><a href="#kontak">Kontak</a></li>

            <!-- GANTI DENGAN LINK GFORM YANG SAMA -->
            <li>
                <a href="LINK_GOOGLE_FORM_ANDA"
                   target="_blank"
                   class="nav-button">
                    Daftar Sekarang
                </a>
            </li>
        </ul>

    </div>
</header>


<!-- =========================
     HERO / BERANDA
========================= -->
<section class="hero" id="beranda">

    <div class="hero-container">

        <div class="hero-content">

            <div class="hero-small">
                ✦ Pelayanan Kesehatan Berbasis Informasi
            </div>

            <h1>PELAYANAN<br>KEFARMASIAN</h1>

            <h2>
                Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
            </h2>

            <p>
                Website pelayanan kefarmasian yang memberikan informasi
                pelayanan serta memudahkan pasien melakukan pendaftaran
                secara online.
            </p>

            <div class="hero-buttons">

                <!-- GANTI DENGAN LINK GFORM YANG SAMA -->
                <a href="LINK_GOOGLE_FORM_ANDA"
                   target="_blank"
                   class="btn btn-primary">
                    📋 Daftar Sekarang
                </a>

                <a href="#pelayanan"
                   class="btn btn-secondary">
                    💊 Lihat Pelayanan
                </a>

            </div>

        </div>

        <div class="hero-illustration">

            <div class="medical-card">
                <div class="medical-cross"></div>
            </div>

        </div>

    </div>

</section>


<!-- =========================
     PENGERTIAN
========================= -->
<section class="section" id="pengertian">

    <div class="container">

        <div class="section-header">
            <span class="section-label">Tentang Pelayanan</span>

            <h2>Pengertian Pelayanan Kefarmasian</h2>

            <p>
                Mengenal pelayanan kefarmasian dan manfaatnya bagi pasien.
            </p>
        </div>


        <div class="definition-box">

            <p>
                Pelayanan kefarmasian merupakan pelayanan yang diberikan
                oleh tenaga kefarmasian kepada pasien yang berkaitan dengan
                penggunaan obat dan pelayanan kesehatan untuk membantu
                memastikan obat digunakan secara tepat, aman, dan efektif.
            </p>

            <br>

            <p>
                Pelayanan kefarmasian berorientasi pada kebutuhan pasien,
                sehingga pasien dapat memperoleh informasi yang benar
                mengenai obat, cara penggunaan, aturan pakai, efek samping,
                penyimpanan, serta hal-hal lain yang berkaitan dengan
                penggunaan obat.
            </p>

        </div>


        <div class="info-grid">

            <div class="info-card">
                <div class="info-icon">💊</div>
                <h3>Pengelolaan Obat</h3>
                <p>
                    Meliputi kegiatan pengadaan, penyimpanan, pengelolaan
                    stok, hingga penyiapan obat agar mutu dan keamanan obat
                    tetap terjaga.
                </p>
            </div>


            <div class="info-card">
                <div class="info-icon">👩‍⚕️</div>
                <h3>Pelayanan kepada Pasien</h3>
                <p>
                    Pelayanan diberikan dengan memperhatikan kebutuhan
                    pasien dan memastikan obat digunakan secara tepat,
                    aman, dan efektif.
                </p>
            </div>


            <div class="info-card">
                <div class="info-icon">💬</div>
                <h3>Informasi dan Konsultasi</h3>
                <p>
                    Pasien dapat memperoleh informasi dan berkonsultasi
                    mengenai penggunaan obat bersama tenaga kefarmasian.
                </p>
            </div>

        </div>

    </div>

</section>


<!-- =========================
     PELAYANAN
========================= -->
<section class="section" id="pelayanan">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Layanan Kami
            </span>

            <h2>Jenis Pelayanan Kefarmasian</h2>

            <p>
                Berbagai pelayanan yang dapat membantu pasien dalam
                memperoleh informasi dan menggunakan obat dengan tepat.
            </p>

        </div>


        <div class="service-grid">

            <div class="service-card">
                <div class="icon">💊</div>
                <h3>Pelayanan Resep</h3>
                <p>
                    Pelayanan resep mulai dari penerimaan resep,
                    pemeriksaan, penyiapan obat hingga penyerahan obat
                    kepada pasien disertai informasi penggunaan.
                </p>
            </div>


            <div class="service-card">
                <div class="icon">🌿</div>
                <h3>Swamedikasi</h3>
                <p>
                    Membantu pasien memilih obat yang sesuai untuk keluhan
                    ringan dengan memperhatikan keamanan dan ketepatan
                    penggunaannya.
                </p>
            </div>


            <div class="service-card">
                <div class="icon">🩺</div>
                <h3>Konsultasi Kefarmasian</h3>
                <p>
                    Konsultasi mengenai penggunaan obat, aturan pakai,
                    efek samping, interaksi obat dan masalah terkait obat.
                </p>
            </div>


            <div class="service-card">
                <div class="icon">💬</div>
                <h3>Konseling Obat</h3>
                <p>
                    Pemberian penjelasan kepada pasien agar memahami cara
                    penggunaan obat dan dapat menggunakannya dengan benar.
                </p>
            </div>


            <div class="service-card">
                <div class="icon">📚</div>
                <h3>Informasi Obat</h3>
                <p>
                    Informasi mengenai nama obat, indikasi, aturan pakai,
                    efek samping, penyimpanan dan hal penting lainnya.
                </p>
            </div>


            <div class="service-card">
                <div class="icon">❤️</div>
                <h3>Pemeriksaan Kesehatan Sederhana</h3>
                <p>
                    Informasi dan pemeriksaan kesehatan sederhana sesuai
                    dengan fasilitas pelayanan yang tersedia.
                </p>
            </div>

        </div>

    </div>

</section>


<!-- =========================
     PENDAFTARAN
========================= -->
<section class="section" id="pendaftaran">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Pendaftaran Online
            </span>

            <h2>Pendaftaran Pelayanan</h2>

            <p>
                Silakan melakukan pendaftaran terlebih dahulu sebelum
                mendapatkan pelayanan. Isi formulir dengan data yang benar
                agar proses pelayanan dapat berjalan dengan baik.
            </p>

        </div>


        <div class="registration-box">

            <h3>📋 Daftar Pelayanan Secara Online</h3>

            <p>
                Pendaftaran dilakukan melalui Google Form.
                Pastikan data yang dimasukkan benar dan nomor WhatsApp
                yang dicantumkan masih aktif.
            </p>


            <div class="registration-list">

                <div>
                    👤 <strong>Nama pasien</strong>
                </div>

                <div>
                    🪪 <strong>Nomor BPJS</strong> (jika ada)
                </div>

                <div>
                    🩺 <strong>Keluhan pasien</strong>
                </div>

                <div>
                    📱 <strong>Nomor WhatsApp yang dapat dihubungi</strong>
                </div>

            </div>


            <!-- GANTI DENGAN LINK GFORM YANG SAMA -->
            <a href="https://forms.gle/jG8p9wozy5nmoMrS8"
               target="_blank"
               class="btn btn-primary">
                📋 Buka Formulir Pendaftaran
            </a>


            <p style="margin-top:20px;font-size:13px;">
                Setelah mengirim formulir, nomor antrean akan diproses
                berdasarkan urutan pengiriman formulir dan dikirimkan
                melalui WhatsApp.
            </p>

        </div>

    </div>

</section>


<!-- =========================
     INFORMASI ANTREAN
========================= -->
<section class="section" id="antrean">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Informasi Antrean
            </span>

            <h2>Bagaimana Nomor Antrean Diperoleh?</h2>

            <p>
                Nomor antrean diberikan berdasarkan urutan pasien
                mengirimkan formulir pendaftaran.
            </p>

        </div>


        <div class="queue-grid">

            <div class="queue-step">
                <div class="queue-number">1</div>
                <h4>Isi Google Form</h4>
                <p>
                    Pasien mengisi data pendaftaran dengan lengkap.
                </p>
            </div>


            <div class="queue-step">
                <div class="queue-number">2</div>
                <h4>Data Diterima</h4>
                <p>
                    Data pendaftaran diterima oleh petugas.
                </p>
            </div>


            <div class="queue-step">
                <div class="queue-number">3</div>
                <h4>Antrean Diproses</h4>
                <p>
                    Urutan antrean mengikuti waktu pengiriman formulir.
                </p>
            </div>


            <div class="queue-step">
                <div class="queue-number">4</div>
                <h4>Nomor Dikirim</h4>
                <p>
                    Nomor antrean dikirim melalui WhatsApp.
                </p>
            </div>


            <div class="queue-step">
                <div class="queue-number">5</div>
                <h4>Datang ke Pelayanan</h4>
                <p>
                    Pasien datang sesuai nomor antrean.
                </p>
            </div>

        </div>

    </div>

</section>


<!-- =========================
     ALUR PENDAFTARAN
========================= -->
<section class="section" id="alur">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Langkah Pendaftaran
            </span>

            <h2>Alur Pendaftaran</h2>

            <p>
                Ikuti langkah berikut untuk melakukan pendaftaran
                pelayanan kefarmasian.
            </p>

        </div>


        <div class="timeline">

            <div class="timeline-item">

                <div class="timeline-number">1</div>

                <div class="timeline-content">

                    <h3>Buka Website</h3>

                    <p>
                        Pasien membuka website pelayanan kefarmasian.
                    </p>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-number">2</div>

                <div class="timeline-content">

                    <h3>Pilih Pendaftaran</h3>

                    <p>
                        Pilih menu pendaftaran untuk melakukan
                        pendaftaran pelayanan secara online.
                    </p>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-number">3</div>

                <div class="timeline-content">

                    <h3>Isi Google Form</h3>

                    <p>
                        Isi nama pasien, nomor BPJS jika ada, keluhan,
                        dan nomor WhatsApp yang aktif.
                    </p>

                    <!-- GANTI DENGAN LINK GFORM YANG SAMA -->
                    <a href="https://forms.gle/jG8p9wozy5nmoMrS8"
                       target="_blank"
                       class="btn btn-primary"
                       style="margin-top:15px;">
                        📋 Daftar Sekarang
                    </a>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-number">4</div>

                <div class="timeline-content">

                    <h3>Kirim Formulir</h3>

                    <p>
                        Periksa kembali data yang telah diisi kemudian
                        kirim formulir pendaftaran.
                    </p>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-number">5</div>

                <div class="timeline-content">

                    <h3>Mendapatkan Nomor Antrean</h3>

                    <p>
                        Nomor antrean diproses berdasarkan urutan
                        pengiriman formulir dan dikirimkan melalui WhatsApp.
                    </p>

                </div>

            </div>


            <div class="timeline-item">

                <div class="timeline-number">6</div>

                <div class="timeline-content">

                    <h3>Datang ke Pelayanan</h3>

                    <p>
                        Pasien datang dan mendapatkan pelayanan sesuai
                        dengan nomor antrean yang telah diterima.
                    </p>

                </div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     PELAYANAN RESEP
========================= -->
<section class="section" id="resep">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Pelayanan Resep
            </span>

            <h2>Alur Pelayanan Resep</h2>

            <p>
                Pelayanan resep dilakukan melalui beberapa tahapan untuk
                membantu memastikan obat yang diberikan sesuai dengan resep.
            </p>

        </div>


        <div class="prescription-flow">

            <div class="prescription-step">
                <span>📄</span>
                <h4>1. Penerimaan Resep</h4>
                <p>
                    Resep diterima dari pasien untuk diproses.
                </p>
            </div>


            <div class="prescription-step">
                <span>🔎</span>
                <h4>2. Pemeriksaan Resep</h4>
                <p>
                    Resep diperiksa untuk memastikan kelengkapan dan
                    kesesuaian informasi.
                </p>
            </div>


            <div class="prescription-step">
                <span>💊</span>
                <h4>3. Penyiapan Obat</h4>
                <p>
                    Obat disiapkan sesuai dengan resep.
                </p>
            </div>


            <div class="prescription-step">
                <span>✅</span>
                <h4>4. Pemeriksaan Kembali</h4>
                <p>
                    Obat diperiksa kembali sebelum diserahkan.
                </p>
            </div>


            <div class="prescription-step">
                <span>🤲</span>
                <h4>5. Penyerahan Obat</h4>
                <p>
                    Obat diserahkan kepada pasien.
                </p>
            </div>


            <div class="prescription-step">
                <span>💬</span>
                <h4>6. Pemberian KIE</h4>
                <p>
                    Pasien mendapatkan informasi mengenai penggunaan obat.
                </p>
            </div>


            <div class="prescription-step">
                <span>❤️</span>
                <h4>7. Pelayanan Selesai</h4>
                <p>
                    Pasien dapat menggunakan obat sesuai informasi yang diberikan.
                </p>
            </div>

        </div>

    </div>

</section>


<!-- =========================
     KONSULTASI
========================= -->
<section class="section" id="konsultasi">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Konsultasi
            </span>

            <h2>Konsultasi Kefarmasian</h2>

            <p>
                Konsultasikan pertanyaan mengenai obat dan penggunaannya
                bersama apoteker.
            </p>

        </div>


        <div class="consultation-intro">

            <p>
                Konsultasi dapat dilakukan untuk memperoleh informasi
                mengenai cara penggunaan obat, aturan pakai, waktu
                penggunaan, efek samping, interaksi obat, penyimpanan obat,
                penggunaan beberapa obat sekaligus, serta masalah terkait
                penggunaan obat.
            </p>

        </div>


        <div class="consultation-topics">

            <span class="topic">Cara penggunaan obat</span>
            <span class="topic">Aturan pakai</span>
            <span class="topic">Waktu penggunaan</span>
            <span class="topic">Efek samping</span>
            <span class="topic">Interaksi obat</span>
            <span class="topic">Penyimpanan obat</span>
            <span class="topic">Penggunaan beberapa obat</span>
            <span class="topic">Masalah terkait obat</span>

        </div>


        <div class="pharmacist-grid">


            <!-- APOTEKER 1 -->
            <div class="pharmacist-card">

                <div class="pharmacist-icon">
                    👩‍⚕️
                </div>

                <h3>
                    apt. Aisyah Ramadhani Wijaya Putri, S.Farm
                </h3>

                <p>
                    CP: +62 852-3205-8261
                </p>

                <a href="https://wa.me/6285232058261?text=Halo%20apt.%20Aisyah,%20saya%20ingin%20berkonsultasi%20mengenai%20obat."
                   target="_blank"
                   class="btn-whatsapp">
                    💬 Konsultasi via WhatsApp
                </a>

            </div>


            <!-- APOTEKER 2 -->
            <div class="pharmacist-card">

                <div class="pharmacist-icon">
                    👩‍⚕️
                </div>

                <h3>
                    apt. Sasi Putri Mauritania, S.Farm
                </h3>

                <p>
                    CP: +62 853-3425-5376
                </p>

                <a href="https://wa.me/6285334255376?text=Halo%20apt.%20Sasi,%20saya%20ingin%20berkonsultasi%20mengenai%20obat."
                   target="_blank"
                   class="btn-whatsapp">
                    💬 Konsultasi via WhatsApp
                </a>

            </div>


            <!-- APOTEKER 3 -->
            <div class="pharmacist-card">

                <div class="pharmacist-icon">
                    👩‍⚕️
                </div>

                <h3>
                    apt. Sri Wahyuni, S.Farm
                </h3>

                <p>
                    CP: +62 877-5737-6296
                </p>

                <a href="https://wa.me/6287757376296?text=Halo%20apt.%20Sri,%20saya%20ingin%20berkonsultasi%20mengenai%20obat."
                   target="_blank"
                   class="btn-whatsapp">
                    💬 Konsultasi via WhatsApp
                </a>

            </div>


            <!-- APOTEKER 4 -->
            <div class="pharmacist-card">

                <div class="pharmacist-icon">
                    👩‍⚕️
                </div>

                <h3>
                    apt. Tyara Novelia Putri, S.Farm
                </h3>

                <p>
                    CP: +62 857-1742-0989
                </p>

                <a href="https://wa.me/6285717420989?text=Halo%20apt.%20Tyara,%20saya%20ingin%20berkonsultasi%20mengenai%20obat."
                   target="_blank"
                   class="btn-whatsapp">
                    💬 Konsultasi via WhatsApp
                </a>

            </div>

        </div>


        <!-- CONTOH CHAT -->
        <div class="definition-box" style="margin-top:40px;">

            <h3 style="color:#789781;margin-bottom:12px;">
                💬 Contoh Konsultasi
            </h3>

            <p>
                <strong>Pasien:</strong><br>
                “Saya ingin berkonsultasi mengenai obat yang sedang saya gunakan.”
            </p>

            <br>

            <p>
                <strong>Apoteker:</strong><br>
                “Silakan sampaikan nama obat, aturan penggunaan,
                serta keluhan atau pertanyaan yang ingin dikonsultasikan.”
            </p>

        </div>

    </div>

</section>


<!-- =========================
     SWAMEDIKASI
========================= -->
<section class="section" id="swamedikasi">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Penggunaan Obat
            </span>

            <h2>Swamedikasi</h2>

            <p>
                Mengenal penggunaan obat secara mandiri dengan tetap
                memperhatikan keamanan dan ketepatan penggunaannya.
            </p>

        </div>


        <div class="self-medication-box">

            <h3>🌿 Apa itu Swamedikasi?</h3>

            <p>
                Swamedikasi adalah upaya seseorang untuk mengatasi keluhan
                atau gangguan kesehatan ringan dengan menggunakan obat
                yang dapat diperoleh tanpa resep sesuai ketentuan.
            </p>

            <p>
                Dalam melakukan swamedikasi, pasien perlu memperhatikan
                keluhan yang dialami, obat yang digunakan, aturan pakai,
                dosis, lama penggunaan, serta kemungkinan adanya kondisi
                tertentu yang memerlukan pemeriksaan lebih lanjut.
            </p>

            <div class="warning">
                ⚠️ <strong>Perhatian:</strong>
                Jika keluhan semakin berat, tidak membaik setelah
                penggunaan obat, atau muncul gejala yang mengkhawatirkan,
                segera konsultasikan kepada tenaga kesehatan.
            </div>

        </div>

    </div>

</section>


<!-- =========================
     FAQ
========================= -->
<section class="section" id="faq">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Pertanyaan Umum
            </span>

            <h2>FAQ</h2>

        </div>


        <div class="faq-container">


            <div class="faq-item">

                <h3>
                    Bagaimana cara melakukan pendaftaran?
                </h3>

                <p>
                    Klik tombol “Daftar Sekarang” atau “Buka Formulir
                    Pendaftaran”, kemudian isi Google Form dengan data
                    yang diperlukan dan kirimkan formulir.
                </p>

            </div>


            <div class="faq-item">

                <h3>
                    Apakah semua pasien dapat melakukan pendaftaran?
                </h3>

                <p>
                    Pendaftaran dilakukan secara online melalui formulir
                    yang tersedia. Pasien perlu mengisi data sesuai dengan
                    informasi yang diminta.
                </p>

            </div>


            <div class="faq-item">

                <h3>
                    Apakah nomor BPJS wajib diisi?
                </h3>

                <p>
                    Nomor BPJS diisi jika pasien memilikinya. Jika tidak
                    memiliki BPJS, bagian tersebut dapat dikosongkan.
                </p>

            </div>


            <div class="faq-item">

                <h3>
                    Bagaimana cara mendapatkan nomor antrean?
                </h3>

                <p>
                    Setelah formulir dikirim, data akan diproses dan
                    nomor antrean dikirimkan melalui WhatsApp yang
                    dicantumkan pada formulir.
                </p>

            </div>


            <div class="faq-item">

                <h3>
                    Bagaimana urutan antrean ditentukan?
                </h3>

                <p>
                    Urutan antrean mengikuti urutan pasien dalam
                    mengirimkan formulir pendaftaran.
                </p>

            </div>


            <div class="faq-item">

                <h3>
                    Apa yang dilakukan setelah mendapatkan nomor antrean?
                </h3>

                <p>
                    Pasien datang ke tempat pelayanan sesuai nomor antrean
                    yang telah diterima melalui WhatsApp.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     KONTAK
========================= -->
<section class="section" id="kontak">

    <div class="container">

        <div class="section-header">

            <span class="section-label">
                Hubungi Kami
            </span>

            <h2>Kontak</h2>

            <p>
                Silakan hubungi kontak berikut untuk mendapatkan informasi
                lebih lanjut mengenai pelayanan.
            </p>

        </div>


        <div class="contact-grid">


            <div class="contact-card">

                <div class="contact-icon">
                    📍
                </div>

                <h3>Alamat</h3>

                <p>
                    Jl. Pangandaran No. 77,
                    Kelurahan Antirogo,
                    Kecamatan Sumbersari,
                    Kabupaten Jember
                </p>

            </div>


            <div class="contact-card">

                <div class="contact-icon">
                    📱
                </div>

                <h3>WhatsApp</h3>

                <a href="https://wa.me/6285717420989"
                   target="_blank">
                    0857-1742-0989
                </a>

            </div>


            <div class="contact-card">

                <div class="contact-icon">
                    ✉️
                </div>

                <h3>Email</h3>

                <a href="mailto:tyaranovelia118@gmail.com">
                    tyaranovelia118@gmail.com
                </a>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     FOOTER
========================= -->
<footer>

    <div class="footer-grid">


        <div>

            <div class="footer-title">
                PELAYANAN KEFARMASIAN
            </div>

            <p>
                Mudah Mendaftar, Nyaman Mendapatkan Pelayanan.
            </p>

            <p style="margin-top:10px;">
                Website informasi pelayanan kefarmasian yang membantu
                pasien memperoleh informasi dan melakukan pendaftaran
                pelayanan secara online.
            </p>

        </div>


        <div>

            <div class="footer-title">
                Navigasi
            </div>

            <a href="#beranda">Beranda</a>
            <a href="#pengertian">Pengertian</a>
            <a href="#pendaftaran">Pendaftaran</a>
            <a href="#alur">Alur Pendaftaran</a>
            <a href="#resep">Pelayanan Resep</a>
            <a href="#konsultasi">Konsultasi</a>
            <a href="#swamedikasi">Swamedikasi</a>
            <a href="#kontak">Kontak</a>

        </div>


        <div>

            <div class="footer-title">
                Kontak
            </div>

            <p>
                📍 Jl. Pangandaran No. 77,
                Kelurahan Antirogo,
                Kecamatan Sumbersari,
                Kabupaten Jember
            </p>

            <br>

            <p>
                📱 0857-1742-0989
            </p>

            <p>
                ✉️ tyaranovelia118@gmail.com
            </p>

        </div>

    </div>


    <div class="copyright">

        © 2026 PELAYANAN KEFARMASIAN.
        All Rights Reserved.

    </div>

</footer>


<!-- =========================
     BACK TO TOP
========================= -->
<button id="backToTop" onclick="topFunction()">
    ↑
</button>


<!-- =========================
     JAVASCRIPT
========================= -->
<script>

    /* MOBILE MENU */
    function toggleMenu() {

        const menu = document.getElementById("navMenu");

        menu.classList.toggle("active");

    }


    /* CLOSE MOBILE MENU AFTER CLICK */
    document.querySelectorAll(".nav-menu a").forEach(function(link) {

        link.addEventListener("click", function() {

            document.getElementById("navMenu")
                .classList.remove("active");

        });

    });


    /* BACK TO TOP */
    const backToTop = document.getElementById("backToTop");

    window.addEventListener("scroll", function() {

        if (window.scrollY > 400) {

            backToTop.style.display = "block";

        } else {

            backToTop.style.display = "none";

        }

    });


    function topFunction() {

        window.scrollTo({
            top: 0,
            behavior: "smooth"
        });

    }

</script>

</body>
</html>
