
<html lang="id">
<head>
  <meta charset="UTF-8">

  <!-- WAJIB agar tampilan mengikuti ukuran HP -->
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <meta name="theme-color" content="#789781">
  <meta name="description"
        content="Pelayanan Kefarmasian Klinik Poltekes Jember - Informasi dan pendaftaran pelayanan kefarmasian.">

  <title>Pelayanan Kefarmasian Klinik Poltekes Jember</title>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap"
        rel="stylesheet">

  <style>

    /* =====================================================
       WARNA WEBSITE
    ===================================================== */

    :root {
      --sage: #A8BFAE;
      --sage-dark: #789781;
      --sage-light: #EFF5F0;

      --white: #FFFFFF;

      --pink: #E8B7C3;
      --pink-dark: #D38FA0;

      --text: #35443A;
      --text-light: #68776D;

      --border: #DDE8DF;

      --shadow:
        0 10px 30px rgba(70, 100, 80, 0.10);

      --shadow-hover:
        0 18px 40px rgba(70, 100, 80, 0.16);

      --radius: 20px;
      --max-width: 1180px;
    }


    /* =====================================================
       RESET
    ===================================================== */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 80px;
    }

    body {
      font-family: "DM Sans", sans-serif;
      color: var(--text);
      background: var(--white);
      line-height: 1.7;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button {
      font-family: inherit;
    }

    .container {
      width: 92%;
      max-width: var(--max-width);
      margin: auto;
    }


    /* =====================================================
       LOADING
    ===================================================== */

    .loader {
      position: fixed;
      inset: 0;
      background: white;
      display: flex;
      align-items: center;
      justify-content: center;
      z-index: 9999;
      transition: .5s;
    }

    .loader.hide {
      opacity: 0;
      visibility: hidden;
    }

    .loader-circle {
      width: 50px;
      height: 50px;
      border-radius: 50%;
      border: 4px solid var(--sage-light);
      border-top-color: var(--sage-dark);
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }


    /* =====================================================
       NAVBAR
    ===================================================== */

    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(255,255,255,.96);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid var(--border);
      z-index: 1000;
    }

    .nav-container {
      min-height: 70px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 13px;
      font-weight: 700;
      line-height: 1.3;
      color: var(--sage-dark);
      max-width: 280px;
    }

    .logo-icon {
      width: 40px;
      height: 40px;
      flex-shrink: 0;
      border-radius: 12px;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      font-size: 21px;
    }

    .nav-menu {
      display: flex;
      align-items: center;
      gap: 3px;
    }

    .nav-menu a {
      padding: 9px 10px;
      border-radius: 10px;
      font-size: 12px;
      font-weight: 600;
      transition: .3s;
    }

    .nav-menu a:hover {
      color: var(--sage-dark);
      background: var(--sage-light);
    }

    .nav-register {
      background: var(--sage-dark) !important;
      color: white !important;
      padding: 10px 15px !important;
    }

    .nav-register:hover {
      background: var(--pink-dark) !important;
    }

    .hamburger {
      display: none;
      width: 44px;
      height: 44px;
      border: none;
      border-radius: 12px;
      background: var(--sage-light);
      color: var(--sage-dark);
      font-size: 23px;
      cursor: pointer;
    }


    /* =====================================================
       HERO
    ===================================================== */

    .hero {
      padding: 145px 0 80px;
      background:
        radial-gradient(
          circle at 90% 10%,
          rgba(232,183,195,.30),
          transparent 23%
        ),
        linear-gradient(
          135deg,
          var(--sage-light),
          #ffffff 70%
        );
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr .9fr;
      align-items: center;
      gap: 60px;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 8px 14px;
      border-radius: 30px;
      background: white;
      color: var(--sage-dark);
      font-size: 12px;
      font-weight: 700;
      box-shadow: var(--shadow);
      margin-bottom: 18px;
    }

    .hero-badge span {
      color: var(--pink-dark);
    }

    .hero h1 {
      font-family: "Playfair Display", serif;
      font-size: clamp(38px, 5vw, 62px);
      line-height: 1.12;
      margin-bottom: 20px;
    }

    .hero h1 span {
      color: var(--sage-dark);
    }

    .hero-subtitle {
      color: var(--sage-dark);
      font-size: clamp(17px, 2vw, 22px);
      font-weight: 700;
      margin-bottom: 13px;
    }

    .hero-description {
      max-width: 620px;
      color: var(--text-light);
      font-size: 15px;
      margin-bottom: 28px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .btn {
      min-height: 50px;
      padding: 12px 21px;
      border-radius: 14px;
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
      font-size: 13px;
      font-weight: 700;
      border: 2px solid transparent;
      transition: .3s;
      cursor: pointer;
    }

    .btn-primary {
      background: var(--sage-dark);
      color: white;
      box-shadow: 0 8px 20px rgba(120,151,129,.25);
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: var(--pink-dark);
    }

    .btn-secondary {
      background: white;
      color: var(--sage-dark);
      border-color: var(--sage);
    }

    .btn-secondary:hover {
      transform: translateY(-3px);
      background: var(--sage-light);
    }


    /* =====================================================
       HERO ILLUSTRATION
    ===================================================== */

    .hero-visual {
      position: relative;
      min-height: 390px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .visual-card {
      width: 100%;
      max-width: 430px;
      height: 350px;
      background: white;
      border-radius: 35px;
      box-shadow: 0 25px 60px rgba(70,100,80,.15);
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .visual-card::before {
      content: "";
      position: absolute;
      width: 280px;
      height: 280px;
      background: var(--sage-light);
      border-radius: 50%;
      right: -70px;
      top: -90px;
    }

    .visual-card::after {
      content: "";
      position: absolute;
      width: 130px;
      height: 130px;
      background: rgba(232,183,195,.35);
      border-radius: 50%;
      bottom: -35px;
      left: -35px;
    }

    .illustration {
      position: relative;
      z-index: 2;
      text-align: center;
    }

    .doctor-icon {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      font-size: 78px;
      margin: auto;
      border: 10px solid white;
      box-shadow: var(--shadow);
    }

    .illustration h3 {
      margin-top: 18px;
      color: var(--sage-dark);
      font-size: 18px;
    }

    .illustration p {
      font-size: 12px;
      color: var(--text-light);
    }

    .floating-card {
      position: absolute;
      background: white;
      padding: 10px 14px;
      border-radius: 13px;
      box-shadow: var(--shadow);
      font-size: 12px;
      font-weight: 700;
      z-index: 5;
    }

    .floating-one {
      left: 0;
      top: 45px;
    }

    .floating-two {
      right: 0;
      bottom: 45px;
    }


    /* =====================================================
       SECTION
    ===================================================== */

    section {
      padding: 85px 0;
    }

    .section-header {
      text-align: center;
      max-width: 720px;
      margin: 0 auto 45px;
    }

    .section-label {
      color: var(--sage-dark);
      font-size: 11px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 8px;
    }

    .section-header h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(30px, 4vw, 44px);
      line-height: 1.2;
      margin-bottom: 12px;
    }

    .section-header p {
      color: var(--text-light);
      font-size: 14px;
    }


    /* =====================================================
       PENGERTIAN
    ===================================================== */

    .about-text {
      max-width: 900px;
      margin: auto;
      text-align: center;
      color: var(--text-light);
      font-size: 15px;
    }

    .about-text strong {
      color: var(--sage-dark);
    }

    .about-cards {
      margin-top: 40px;
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .card {
      padding: 28px;
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      transition: .35s;
    }

    .card:hover {
      transform: translateY(-7px);
      box-shadow: var(--shadow-hover);
    }

    .card-icon {
      width: 55px;
      height: 55px;
      display: grid;
      place-items: center;
      border-radius: 16px;
      background: var(--sage-light);
      font-size: 27px;
      margin-bottom: 16px;
    }

    .card:nth-child(3) .card-icon {
      background: #faedf0;
    }

    .card h3 {
      font-size: 18px;
      margin-bottom: 8px;
    }

    .card p {
      color: var(--text-light);
      font-size: 13px;
    }


    /* =====================================================
       PENDAFTARAN
    ===================================================== */

    .registration {
      background: var(--sage-light);
    }

    .register-wrapper {
      background: var(--sage-dark);
      color: white;
      border-radius: 30px;
      padding: 45px;
      display: grid;
      grid-template-columns: 1fr .85fr;
      gap: 40px;
      position: relative;
      overflow: hidden;
    }

    .register-wrapper::after {
      content: "";
      position: absolute;
      width: 260px;
      height: 260px;
      border-radius: 50%;
      right: -100px;
      top: -100px;
      background: rgba(255,255,255,.07);
    }

    .register-wrapper h2 {
      font-family: "Playfair Display", serif;
      font-size: 36px;
      margin-bottom: 12px;
    }

    .register-wrapper p {
      opacity: .9;
      font-size: 14px;
      margin-bottom: 22px;
    }

    .register-button {
      background: white;
      color: var(--sage-dark);
      position: relative;
      z-index: 2;
    }

    .register-button:hover {
      background: var(--pink);
      color: white;
    }

    .form-info {
      background: rgba(255,255,255,.11);
      border: 1px solid rgba(255,255,255,.2);
      padding: 24px;
      border-radius: 20px;
      position: relative;
      z-index: 2;
    }

    .form-info h3 {
      margin-bottom: 12px;
    }

    .form-info ul {
      list-style: none;
    }

    .form-info li {
      margin: 9px 0;
      font-size: 13px;
    }


    /* =====================================================
       IMPORTANT
    ===================================================== */

    .important {
      margin-top: 20px;
      background: #fff8fa;
      border: 1px solid var(--pink);
      border-radius: 18px;
      padding: 20px;
    }

    .important-title {
      color: var(--pink-dark);
      font-weight: 800;
      margin-bottom: 5px;
    }

    .important p {
      color: var(--text);
      font-size: 13px;
    }


    /* =====================================================
       ANTREAN
    ===================================================== */

    .queue-flow {
      display: flex;
      justify-content: center;
      margin-top: 40px;
    }

    .queue-item {
      width: 190px;
      text-align: center;
      position: relative;
    }

    .queue-circle {
      width: 55px;
      height: 55px;
      margin: auto auto 13px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--sage);
      color: white;
      font-weight: 800;
    }

    .queue-item:not(:last-child)::after {
      content: "→";
      position: absolute;
      top: 10px;
      right: -12px;
      color: var(--sage-dark);
      font-size: 25px;
    }

    .queue-item h4 {
      font-size: 13px;
      margin-bottom: 4px;
    }

    .queue-item p {
      color: var(--text-light);
      font-size: 11px;
    }

    .queue-note {
      max-width: 750px;
      margin: 35px auto 0;
      background: var(--sage-light);
      color: var(--sage-dark);
      border-radius: 15px;
      padding: 16px;
      text-align: center;
      font-size: 13px;
      font-weight: 600;
    }


    /* =====================================================
       ALUR PENDAFTARAN
    ===================================================== */

    .steps {
      background: var(--sage-light);
    }

    .timeline {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 12px;
    }

    .step {
      background: white;
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 22px 15px;
      text-align: center;
      transition: .3s;
    }

    .step:hover {
      transform: translateY(-5px);
    }

    .step-number {
      color: var(--sage-dark);
      font-size: 24px;
      font-weight: 800;
      margin-bottom: 5px;
    }

    .step h3 {
      font-size: 14px;
      margin-bottom: 7px;
    }

    .step p {
      color: var(--text-light);
      font-size: 11px;
    }


    /* =====================================================
       RESEP
    ===================================================== */

    .recipe-list {
      max-width: 850px;
      margin: auto;
    }

    .recipe-step {
      display: flex;
      gap: 17px;
      background: var(--sage-light);
      border-radius: 18px;
      padding: 20px;
      margin-bottom: 12px;
      transition: .3s;
    }

    .recipe-step:hover {
      transform: translateX(5px);
    }

    .recipe-icon {
      width: 50px;
      height: 50px;
      flex-shrink: 0;
      border-radius: 14px;
      background: white;
      display: grid;
      place-items: center;
      font-size: 22px;
      box-shadow: var(--shadow);
    }

    .recipe-step h3 {
      font-size: 15px;
      margin-bottom: 3px;
    }

    .recipe-step p {
      color: var(--text-light);
      font-size: 12px;
    }

    .kie-tags {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 8px;
    }

    .kie-tags span {
      background: white;
      color: var(--sage-dark);
      padding: 4px 9px;
      border-radius: 20px;
      font-size: 10px;
    }


    /* =====================================================
       KONSULTASI
    ===================================================== */

    .consultation {
      background: var(--sage-light);
    }

    .consult-grid {
      display: grid;
      grid-template-columns: .9fr 1.1fr;
      gap: 40px;
      align-items: start;
    }

    .consult-description {
      color: var(--text-light);
      font-size: 14px;
      margin-bottom: 18px;
    }

    .consult-list {
      list-style: none;
      margin-bottom: 22px;
    }

    .consult-list li {
      color: var(--text-light);
      font-size: 13px;
      padding: 5px 0;
    }

    .consult-list li::before {
      content: "✓";
      color: var(--sage-dark);
      font-weight: 800;
      margin-right: 8px;
    }


    /* CHAT */

    .chat-box {
      background: white;
      border-radius: 25px;
      padding: 25px;
      box-shadow: var(--shadow);
      margin-bottom: 25px;
    }

    .chat {
      display: flex;
      gap: 10px;
      margin-bottom: 17px;
    }

    .chat.doctor {
      flex-direction: row-reverse;
    }

    .avatar {
      width: 45px;
      height: 45px;
      flex-shrink: 0;
      border-radius: 50%;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      font-size: 21px;
    }

    .doctor .avatar {
      background: #faedf0;
    }

    .bubble {
      max-width: 75%;
      background: var(--sage-light);
      border-radius: 15px 15px 15px 3px;
      padding: 12px 15px;
      font-size: 12px;
    }

    .doctor .bubble {
      background: #faedf0;
      border-radius: 15px 15px 3px 15px;
    }

    .bubble strong {
      display: block;
      font-size: 11px;
      margin-bottom: 3px;
    }


    /* =====================================================
       DAFTAR APOTEKER
    ===================================================== */

    .pharmacist-section {
      margin-top: 30px;
    }

    .pharmacist-title {
      text-align: center;
      margin-bottom: 20px;
    }

    .pharmacist-title h3 {
      font-family: "Playfair Display", serif;
      font-size: 25px;
    }

    .pharmacist-title p {
      color: var(--text-light);
      font-size: 12px;
    }

    .pharmacist-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
    }

    .pharmacist-card {
      background: white;
      border-radius: 18px;
      padding: 20px 14px;
      text-align: center;
      border: 1px solid var(--border);
      transition: .3s;
    }

    .pharmacist-card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow);
    }

    .pharmacist-avatar {
      width: 55px;
      height: 55px;
      border-radius: 50%;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      margin: 0 auto 12px;
      font-size: 27px;
    }

    .pharmacist-card h4 {
      font-size: 13px;
      line-height: 1.4;
      margin-bottom: 5px;
    }

    .pharmacist-card p {
      color: var(--text-light);
      font-size: 11px;
      margin-bottom: 12px;
    }

    .wa-button {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 5px;
      width: 100%;
      min-height: 38px;
      border-radius: 10px;
      background: var(--sage-dark);
      color: white;
      font-size: 11px;
      font-weight: 700;
      transition: .3s;
    }

    .wa-button:hover {
      background: var(--pink-dark);
    }


    /* =====================================================
       PELAYANAN
    ===================================================== */

    .service-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .service-card {
      padding: 25px 20px;
      border-radius: 20px;
      background: var(--sage-light);
      transition: .3s;
    }

    .service-card:hover {
      background: white;
      box-shadow: var(--shadow);
      transform: translateY(-5px);
    }

    .service-icon {
      font-size: 31px;
      margin-bottom: 10px;
    }

    .service-card h3 {
      font-size: 15px;
      margin-bottom: 6px;
    }

    .service-card p {
      color: var(--text-light);
      font-size: 12px;
    }


    /* =====================================================
       SWAMEDIKASI
    ===================================================== */

    .self-medication {
      background: var(--sage-light);
    }

    .self-box {
      max-width: 900px;
      margin: auto;
      padding: 30px;
      background: white;
      border-radius: 25px;
      box-shadow: var(--shadow);
    }

    .self-box p {
      color: var(--text-light);
      font-size: 14px;
      margin-bottom: 15px;
    }

    .warning-box {
      border-left: 4px solid var(--pink-dark);
      background: #fff8fa;
      padding: 15px;
      border-radius: 10px;
      font-size: 12px;
    }


    /* =====================================================
       KONTAK
    ===================================================== */

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .contact-card {
      padding: 30px;
      background: var(--sage-light);
      border-radius: 25px;
    }

    .contact-item {
      display: flex;
      gap: 13px;
      padding: 14px 0;
      border-bottom: 1px solid var(--border);
    }

    .contact-item:last-child {
      border-bottom: none;
    }

    .contact-icon {
      width: 44px;
      height: 44px;
      flex-shrink: 0;
      background: white;
      border-radius: 13px;
      display: grid;
      place-items: center;
      font-size: 19px;
    }

    .contact-item h4 {
      font-size: 13px;
      margin-bottom: 2px;
    }

    .contact-item p,
    .contact-item a {
      color: var(--text-light);
      font-size: 12px;
      word-break: break-word;
    }

    .contact-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 9px;
      margin-top: 20px;
    }

    .map {
      width: 100%;
      height: 100%;
      min-height: 350px;
      border: none;
      border-radius: 25px;
    }


    /* =====================================================
       FAQ
    ===================================================== */

    .faq {
      background: var(--sage-light);
    }

    .faq-container {
      max-width: 850px;
      margin: auto;
    }

    details {
      background: white;
      border: 1px solid var(--border);
      border-radius: 15px;
      margin-bottom: 10px;
      overflow: hidden;
    }

    summary {
      padding: 17px 20px;
      cursor: pointer;
      font-weight: 700;
      font-size: 13px;
      list-style: none;
      position: relative;
      padding-right: 45px;
    }

    summary::-webkit-details-marker {
      display: none;
    }

    summary::after {
      content: "+";
      position: absolute;
      right: 20px;
      color: var(--sage-dark);
      font-size: 20px;
    }

    details[open] summary::after {
      content: "−";
    }

    details p {
      padding: 0 20px 18px;
      color: var(--text-light);
      font-size: 12px;
    }


    /* =====================================================
       FOOTER
    ===================================================== */

    footer {
      background: #304138;
      color: white;
      padding: 50px 0 22px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1.2fr 1fr 1fr;
      gap: 40px;
      margin-bottom: 35px;
    }

    footer h3 {
      margin-bottom: 12px;
      font-size: 16px;
    }

    footer p,
    footer a {
      color: rgba(255,255,255,.72);
      font-size: 12px;
    }

    footer a:hover {
      color: var(--pink);
    }

    .footer-links {
      display: grid;
      gap: 6px;
    }

    .copyright {
      border-top: 1px solid rgba(255,255,255,.12);
      padding-top: 20px;
      text-align: center;
      color: rgba(255,255,255,.5);
      font-size: 11px;
    }


    /* =====================================================
       BACK TO TOP
    ===================================================== */

    #backTop {
      position: fixed;
      right: 18px;
      bottom: 18px;
      width: 45px;
      height: 45px;
      border: none;
      border-radius: 50%;
      background: var(--sage-dark);
      color: white;
      font-size: 20px;
      cursor: pointer;
      box-shadow: var(--shadow);
      opacity: 0;
      visibility: hidden;
      transition: .3s;
      z-index: 900;
    }

    #backTop.show {
      opacity: 1;
      visibility: visible;
    }


    /* =====================================================
       TOAST
    ===================================================== */

    #toast {
      position: fixed;
      left: 50%;
      bottom: 25px;
      transform: translate(-50%, 100px);
      background: #304138;
      color: white;
      padding: 13px 18px;
      border-radius: 12px;
      font-size: 12px;
      opacity: 0;
      transition: .3s;
      z-index: 5000;
      max-width: 90%;
      text-align: center;
    }

    #toast.show {
      opacity: 1;
      transform: translate(-50%, 0);
    }


    /* =====================================================
       ANIMATION
    ===================================================== */

    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: .7s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }


    /* =====================================================
       TABLET
    ===================================================== */

    @media (max-width: 1050px) {

      .nav-menu a {
        padding: 8px 6px;
        font-size: 11px;
      }

      .timeline {
        grid-template-columns: repeat(3, 1fr);
      }

      .service-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .pharmacist-grid {
        grid-template-columns: repeat(2, 1fr);
      }

    }


    /* =====================================================
       MOBILE
       DESAIN UTAMA UNTUK HP
    ===================================================== */

    @media (max-width: 768px) {

      body {
        font-size: 14px;
      }

      .container {
        width: 92%;
      }

      section {
        padding: 60px 0;
      }


      /* =========================
         MOBILE NAVBAR
      ========================== */

      .nav-container {
        min-height: 64px;
      }

      .logo {
        max-width: 230px;
        font-size: 10px;
      }

      .logo-icon {
        width: 36px;
        height: 36px;
        font-size: 18px;
      }

      .hamburger {
        display: grid;
        place-items: center;
      }

      .nav-menu {
        position: absolute;
        top: 64px;
        left: 0;
        width: 100%;
        padding: 10px 4%;
        background: white;
        display: none;
        flex-direction: column;
        align-items: stretch;
        box-shadow: 0 15px 30px rgba(0,0,0,.08);
      }

      .nav-menu.open {
        display: flex;
      }

      .nav-menu a {
        padding: 13px 14px;
        font-size: 13px;
      }

      .nav-register {
        text-align: center;
        margin-top: 5px;
      }


      /* =========================
         MOBILE HERO
      ========================== */

      .hero {
        padding: 105px 0 55px;
      }

      .hero-grid {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .hero h1 {
        font-size: 37px;
      }

      .hero-subtitle {
        font-size: 17px;
      }

      .hero-description {
        font-size: 13px;
      }

      .hero-buttons {
        flex-direction: column;
      }

      .hero-buttons .btn {
        width: 100%;
      }

      .hero-visual {
        min-height: 300px;
      }

      .visual-card {
        height: 285px;
        border-radius: 28px;
      }

      .doctor-icon {
        width: 115px;
        height: 115px;
        font-size: 60px;
      }

      .floating-card {
        font-size: 10px;
        padding: 8px 10px;
      }

      .floating-one {
        left: -4px;
        top: 20px;
      }

      .floating-two {
        right: -4px;
        bottom: 20px;
      }


      /* =========================
         MOBILE SECTION
      ========================== */

      .section-header {
        margin-bottom: 32px;
      }

      .section-header h2 {
        font-size: 29px;
      }

      .section-header p {
        font-size: 13px;
      }


      /* =========================
         MOBILE CARDS
      ========================== */

      .about-cards {
        grid-template-columns: 1fr;
        gap: 14px;
      }

      .card {
        padding: 22px;
      }


      /* =========================
         MOBILE PENDAFTARAN
      ========================== */

      .register-wrapper {
        grid-template-columns: 1fr;
        padding: 28px 20px;
        border-radius: 24px;
        gap: 22px;
      }

      .register-wrapper h2 {
        font-size: 29px;
      }

      .register-button {
        width: 100%;
      }

      .form-info {
        padding: 20px;
      }


      /* =========================
         MOBILE ANTREAN
      ========================== */

      .queue-flow {
        flex-direction: column;
        align-items: stretch;
      }

      .queue-item {
        width: 100%;
        min-height: 75px;
        display: grid;
        grid-template-columns: 55px 1fr;
        column-gap: 14px;
        text-align: left;
      }

      .queue-circle {
        margin: 0;
        grid-row: span 2;
      }

      .queue-item:not(:last-child)::after {
        content: "↓";
        left: 18px;
        right: auto;
        top: 53px;
        font-size: 19px;
      }

      .queue-item h4 {
        align-self: end;
      }

      .queue-item p {
        align-self: start;
      }

      .queue-note {
        text-align: left;
        font-size: 12px;
      }


      /* =========================
         MOBILE TIMELINE
      ========================== */

      .timeline {
        grid-template-columns: 1fr;
        gap: 11px;
      }

      .step {
        display: grid;
        grid-template-columns: 55px 1fr;
        column-gap: 13px;
        text-align: left;
        align-items: center;
        padding: 18px;
      }

      .step-number {
        grid-row: span 2;
        margin: 0;
      }

      .step h3 {
        margin: 0;
      }


      /* =========================
         MOBILE RESEP
      ========================== */

      .recipe-step {
        padding: 17px;
        gap: 12px;
      }

      .recipe-icon {
        width: 44px;
        height: 44px;
        font-size: 19px;
      }

      .recipe-step h3 {
        font-size: 13px;
      }

      .recipe-step p {
        font-size: 11px;
      }


      /* =========================
         MOBILE KONSULTASI
      ========================== */

      .consult-grid {
        grid-template-columns: 1fr;
        gap: 25px;
      }

      .consult-description {
        font-size: 13px;
      }

      .chat-box {
        padding: 18px;
      }

      .bubble {
        max-width: 80%;
        font-size: 11px;
      }


      /* =========================
         MOBILE APOTEKER
      ========================== */

      .pharmacist-grid {
        grid-template-columns: 1fr;
        gap: 12px;
      }

      .pharmacist-card {
        display: grid;
        grid-template-columns: 55px 1fr auto;
        align-items: center;
        gap: 12px;
        text-align: left;
        padding: 15px;
      }

      .pharmacist-avatar {
        margin: 0;
      }

      .pharmacist-card p {
        margin: 0;
      }

      .wa-button {
        width: auto;
        padding: 0 12px;
      }


      /* =========================
         MOBILE SERVICES
      ========================== */

      .service-grid {
        grid-template-columns: 1fr;
      }


      /* =========================
         MOBILE SWAMEDIKASI
      ========================== */

      .self-box {
        padding: 22px;
      }


      /* =========================
         MOBILE CONTACT
      ========================== */

      .contact-grid {
        grid-template-columns: 1fr;
      }

      .contact-card {
        padding: 22px;
      }

      .contact-buttons {
        flex-direction: column;
      }

      .contact-buttons .btn {
        width: 100%;
      }

      .map {
        height: 300px;
        min-height: 300px;
      }


      /* =========================
         MOBILE FOOTER
      ========================== */

      .footer-grid {
        grid-template-columns: 1fr;
        gap: 28px;
      }

      footer {
        padding: 42px 0 22px;
      }


      /* =========================
         MOBILE BUTTON
      ========================== */

      .btn {
        min-height: 52px;
        width: 100%;
        font-size: 12px;
      }

    }


    /* =====================================================
       HP KECIL
    ===================================================== */

    @media (max-width: 380px) {

      .hero h1 {
        font-size: 33px;
      }

      .hero {
        padding-top: 95px;
      }

      .logo {
        font-size: 9px;
      }

      .register-wrapper h2 {
        font-size: 26px;
      }

    }

  </style>
</head>


<body>


  <!-- =====================================================
       LOADING
  ===================================================== -->

  <div class="loader" id="loader">
    <div class="loader-circle"></div>
  </div>


  <!-- =====================================================
       NAVBAR
  ===================================================== -->

  <header class="navbar">

    <div class="container nav-container">

      <a href="#beranda" class="logo">

        <div class="logo-icon">
          💊
        </div>

        <span>
          PELAYANAN KEFARMASIAN<br>
          KLINIK POLTEKES JEMBER
        </span>

      </a>


      <button
        class="hamburger"
        id="hamburger"
        aria-label="Menu"
      >
        ☰
      </button>


      <nav class="nav-menu" id="navMenu">

        <a href="#beranda">🏠 Beranda</a>

        <a href="#pengertian">📖 Pengertian</a>

        <a href="#pendaftaran">📝 Pendaftaran</a>

        <a href="#alur">🔄 Alur Pendaftaran</a>

        <a href="#resep">💊 Pelayanan Resep</a>

        <a href="#konsultasi">💬 Konsultasi</a>

        <a href="#kontak">📞 Kontak</a>

        <a
          href="https://forms.gle/jG8p9wozy5nmoMrS8"
          target="_blank"
          rel="noopener noreferrer"
          class="nav-register"
          onclick="showToast('Membuka Google Form pendaftaran...')"
        >
          📝 Daftar Sekarang
        </a>

      </nav>

    </div>

  </header>


  <main>


    <!-- =====================================================
         BERANDA
    ===================================================== -->

    <section class="hero" id="beranda">

      <div class="container hero-grid">

        <div class="reveal">

          <div class="hero-badge">
            <span>✦</span>
            Portal Pelayanan Kefarmasian
          </div>


          <h1>
            Pelayanan Kefarmasian
            <span>Klinik Poltekes Jember</span>
          </h1>


          <div class="hero-subtitle">
            Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
          </div>


          <p class="hero-description">
            Website pelayanan kefarmasian yang memberikan informasi
            pelayanan serta memudahkan pasien melakukan pendaftaran
            secara online.
          </p>


          <div class="hero-buttons">

            <a
              href="https://forms.gle/jG8p9wozy5nmoMrS8"
              target="_blank"
              rel="noopener noreferrer"
              class="btn btn-primary"
              onclick="showToast('Membuka Google Form pendaftaran...')"
            >
              📝 Daftar Sekarang
            </a>


            <a
              href="#pelayanan"
              class="btn btn-secondary"
            >
              💊 Lihat Pelayanan
            </a>

          </div>

        </div>


        <!-- ILUSTRASI -->

        <div class="hero-visual reveal">

          <div class="floating-card floating-one">
            🩺 Pelayanan Pasien
          </div>


          <div class="visual-card">

            <div class="illustration">

              <div class="doctor-icon">
                👩‍⚕️
              </div>

              <h3>
                Pelayanan Kefarmasian
              </h3>

              <p>
                Informasi • Konsultasi • Pelayanan
              </p>

            </div>

          </div>


          <div class="floating-card floating-two">
            💊 Obat & KIE
          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         PENGERTIAN
    ===================================================== -->

    <section id="pengertian">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Tentang Pelayanan
          </div>

          <h2>
            Apa Itu Pelayanan Kefarmasian?
          </h2>

          <p>
            Pelayanan yang berorientasi pada kebutuhan pasien
            dan penggunaan obat yang tepat.
          </p>

        </div>


        <div class="about-text reveal">

          <p>
            Pelayanan kefarmasian merupakan pelayanan yang diberikan
            oleh tenaga kefarmasian kepada pasien yang berkaitan dengan
            penggunaan obat dan pelayanan kesehatan untuk membantu
            memastikan obat digunakan secara
            <strong>tepat, aman, dan efektif.</strong>
          </p>

          <br>

          <p>
            Pelayanan kefarmasian tidak hanya berfokus pada obat,
            tetapi juga memperhatikan kebutuhan dan kondisi pasien.
          </p>

        </div>


        <div class="about-cards">

          <div class="card reveal">

            <div class="card-icon">
              💊
            </div>

            <h3>
              Pengelolaan Obat
            </h3>

            <p>
              Pengelolaan obat dilakukan untuk memastikan ketersediaan,
              penyimpanan, dan penggunaan obat secara tepat.
            </p>

          </div>


          <div class="card reveal">

            <div class="card-icon">
              🩺
            </div>

            <h3>
              Pelayanan kepada Pasien
            </h3>

            <p>
              Pelayanan diberikan dengan memperhatikan kebutuhan pasien
              dan memberikan informasi yang sesuai.
            </p>

          </div>


          <div class="card reveal">

            <div class="card-icon">
              💬
            </div>

            <h3>
              Informasi dan Konsultasi
            </h3>

            <p>
              Pasien dapat memperoleh informasi mengenai penggunaan obat
              dan berkonsultasi dengan apoteker.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         PENDAFTARAN
    ===================================================== -->

    <section
      class="registration"
      id="pendaftaran"
    >

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Pendaftaran Pasien
          </div>

          <h2>
            Pendaftaran Pelayanan
          </h2>

          <p>
            Silakan melakukan pendaftaran terlebih dahulu
            sebelum mendapatkan pelayanan.
          </p>

        </div>


        <div class="register-wrapper reveal">

          <div>

            <h2>
              Mulai Pendaftaran Anda
            </h2>

            <p>
              Isi formulir dengan data yang benar agar proses
              pelayanan dapat berjalan dengan baik.
            </p>


            <!-- =================================================
                 GOOGLE FORM
                 LINK UTAMA WEBSITE
            ================================================== -->

            <a
              href="https://forms.gle/jG8p9wozy5nmoMrS8"
              target="_blank"
              rel="noopener noreferrer"
              class="btn register-button"
              onclick="showToast('Membuka Google Form pendaftaran...')"
            >
              📝 Isi Formulir Pendaftaran
            </a>

          </div>


          <div class="form-info">

            <h3>
              📋 Data Pasien
            </h3>

            <ul>

              <li>
                ✓ Nama Pasien —
                <strong>Wajib diisi</strong>
              </li>

              <li>
                ✓ Nomor BPJS —
                <strong>Opsional</strong>
                <br>
                <small>
                  Diisi jika pasien memiliki BPJS.
                </small>
              </li>

              <li>
                ✓ Keluhan atau kebutuhan pelayanan
              </li>

              <li>
                ✓ Nomor WhatsApp —
                <strong>Wajib diisi</strong>
              </li>

            </ul>

          </div>

        </div>


        <div class="important reveal">

          <div class="important-title">
            ⚠️ PENTING
          </div>

          <p>
            Setelah mengisi formulir, nomor antrean akan segera
            dikirimkan melalui WhatsApp ke nomor yang telah
            dicantumkan pada formulir.
          </p>

          <br>

          <p>
            <strong>
              Nomor antrean diberikan berdasarkan urutan
              pengiriman formulir.
            </strong>
            Pasien yang mengirimkan formulir terlebih dahulu
            akan mendapatkan urutan antrean terlebih dahulu.
          </p>

        </div>

      </div>

    </section>


    <!-- =====================================================
         INFORMASI ANTREAN
    ===================================================== -->

    <section id="antrean">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Informasi Antrean
          </div>

          <h2>
            Informasi Nomor Antrean
          </h2>

          <p>
            Berikut proses setelah pasien mengirimkan formulir.
          </p>

        </div>


        <div class="queue-flow reveal">

          <div class="queue-item">

            <div class="queue-circle">
              01
            </div>

            <h4>
              Isi Google Form
            </h4>

            <p>
              Lengkapi data pendaftaran.
            </p>

          </div>


          <div class="queue-item">

            <div class="queue-circle">
              02
            </div>

            <h4>
              Data Diterima
            </h4>

            <p>
              Data pendaftaran diterima.
            </p>

          </div>


          <div class="queue-item">

            <div class="queue-circle">
              03
            </div>

            <h4>
              Antrean Diproses
            </h4>

            <p>
              Nomor antrean diproses.
            </p>

          </div>


          <div class="queue-item">

            <div class="queue-circle">
              04
            </div>

            <h4>
              WhatsApp
            </h4>

            <p>
              Nomor antrean dikirim.
            </p>

          </div>


          <div class="queue-item">

            <div class="queue-circle">
              05
            </div>

            <h4>
              Pasien Datang
            </h4>

            <p>
              Datang sesuai antrean.
            </p>

          </div>

        </div>


        <div class="queue-note reveal">

          📱 Pastikan nomor WhatsApp yang dicantumkan aktif
          dan dapat menerima pesan.

          <br><br>

          Urutan antrean mengikuti waktu pengiriman
          formulir pendaftaran.

        </div>

      </div>

    </section>


    <!-- =====================================================
         ALUR PENDAFTARAN
    ===================================================== -->

    <section
      class="steps"
      id="alur"
    >

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Panduan
          </div>

          <h2>
            Alur Pendaftaran Pelayanan
          </h2>

          <p>
            Ikuti enam langkah sederhana berikut.
          </p>

        </div>


        <div class="timeline">

          <div class="step reveal">

            <div class="step-number">
              01
            </div>

            <h3>
              Buka Website
            </h3>

            <p>
              Pasien membuka website Pelayanan Kefarmasian.
            </p>

          </div>


          <div class="step reveal">

            <div class="step-number">
              02
            </div>

            <h3>
              Pilih Pendaftaran
            </h3>

            <p>
              Pasien menekan tombol “Daftar Sekarang”.
            </p>

          </div>


          <div class="step reveal">

            <div class="step-number">
              03
            </div>

            <h3>
              Isi Google Form
            </h3>

            <p>
              Isi nama, BPJS jika ada, keluhan dan WhatsApp.
            </p>

          </div>


          <div class="step reveal">

            <div class="step-number">
              04
            </div>

            <h3>
              Kirim Formulir
            </h3>

            <p>
              Pastikan seluruh data sudah benar.
            </p>

          </div>


          <div class="step reveal">

            <div class="step-number">
              05
            </div>

            <h3>
              Nomor Antrean
            </h3>

            <p>
              Nomor antrean dikirim melalui WhatsApp.
            </p>

          </div>


          <div class="step reveal">

            <div class="step-number">
              06
            </div>

            <h3>
              Datang ke Pelayanan
            </h3>

            <p>
              Datang sesuai nomor antrean.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         PELAYANAN RESEP
    ===================================================== -->

    <section id="resep">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Pelayanan Resep
          </div>

          <h2>
            Alur Pelayanan Resep
          </h2>

          <p>
            Pelayanan resep dilakukan melalui beberapa tahapan
            untuk membantu memastikan obat diberikan dengan tepat.
          </p>

        </div>


        <div class="recipe-list">

          <div class="recipe-step reveal">

            <div class="recipe-icon">
              📄
            </div>

            <div>

              <h3>
                1. Penerimaan Resep
              </h3>

              <p>
                Pasien menyerahkan resep kepada petugas/apoteker.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              🔎
            </div>

            <div>

              <h3>
                2. Pemeriksaan Resep
              </h3>

              <p>
                Resep diperiksa meliputi kelengkapan dan
                kesesuaian resep.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              💊
            </div>

            <div>

              <h3>
                3. Penyiapan Obat
              </h3>

              <p>
                Obat disiapkan sesuai resep.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              ✓
            </div>

            <div>

              <h3>
                4. Pemeriksaan Kembali
              </h3>

              <p>
                Dilakukan pemeriksaan kembali terhadap obat
                yang telah disiapkan.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              🤝
            </div>

            <div>

              <h3>
                5. Penyerahan Obat
              </h3>

              <p>
                Obat diserahkan kepada pasien.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              💬
            </div>

            <div>

              <h3>
                6. Pemberian KIE
              </h3>

              <p>
                Pasien mendapatkan informasi mengenai penggunaan obat.
              </p>

              <div class="kie-tags">

                <span>Nama/Kegunaan</span>
                <span>Dosis</span>
                <span>Aturan Pakai</span>
                <span>Waktu Penggunaan</span>
                <span>Penyimpanan</span>
                <span>Hal yang Perlu Diperhatikan</span>

              </div>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">
              🌿
            </div>

            <div>

              <h3>
                7. Pelayanan Selesai
              </h3>

              <p>
                Pasien telah memperoleh obat dan informasi
                yang diperlukan.
              </p>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         KONSULTASI
    ===================================================== -->

    <section
      class="consultation"
      id="konsultasi"
    >

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Konsultasi Kefarmasian
          </div>

          <h2>
            Konsultasi dengan Apoteker
          </h2>

          <p>
            Sampaikan pertanyaan atau permasalahan Anda
            mengenai penggunaan obat.
          </p>

        </div>


        <div class="consult-grid">

          <div class="reveal">

            <p class="consult-description">

              Konsultasi kefarmasian merupakan kesempatan bagi pasien
              untuk menyampaikan pertanyaan atau permasalahan terkait
              penggunaan obat kepada apoteker.

            </p>


            <ul class="consult-list">

              <li>
                Cara penggunaan obat
              </li>

              <li>
                Aturan pakai
              </li>

              <li>
                Waktu penggunaan obat
              </li>

              <li>
                Efek samping
              </li>

              <li>
                Interaksi obat
              </li>

              <li>
                Penyimpanan obat
              </li>

              <li>
                Penggunaan beberapa obat secara bersamaan
              </li>

              <li>
                Permasalahan terkait penggunaan obat
              </li>

            </ul>

          </div>


          <!-- CHAT -->

          <div class="chat-box reveal">

            <div class="chat">

              <div class="avatar">
                👤
              </div>

              <div class="bubble">

                <strong>
                  Pasien
                </strong>

                “Saya ingin berkonsultasi mengenai obat
                yang sedang saya gunakan.”

              </div>

            </div>


            <div class="chat doctor">

              <div class="avatar">
                👩‍⚕️
              </div>

              <div class="bubble">

                <strong>
                  Apoteker
                </strong>

                “Silakan sampaikan nama obat, aturan penggunaan,
                serta keluhan atau pertanyaan yang ingin dikonsultasikan.”

              </div>

            </div>

          </div>

        </div>


        <!-- =================================================
             DAFTAR APOTEKER
        ================================================== -->

        <div class="pharmacist-section">

          <div class="pharmacist-title reveal">

            <h3>
              Pilih Apoteker untuk Konsultasi
            </h3>

            <p>
              Klik tombol WhatsApp untuk memulai konsultasi.
            </p>

          </div>


          <div class="pharmacist-grid">


            <!-- APOTEKER 1 -->

            <div class="pharmacist-card reveal">

              <div class="pharmacist-avatar">
                👩‍⚕️
              </div>

              <div>

                <h4>
                  apt. Aisyah Ramadhani
                  Wijaya Putri
                </h4>

                <p>
                  085232058261
                </p>

              </div>

              <a
                href="https://wa.me/6285232058261"
                target="_blank"
                rel="noopener noreferrer"
                class="wa-button"
              >
                💬 WhatsApp
              </a>

            </div>


            <!-- APOTEKER 2 -->

            <div class="pharmacist-card reveal">

              <div class="pharmacist-avatar">
                👩‍⚕️
              </div>

              <div>

                <h4>
                  apt. Sasi Putri
                  Mauritania
                </h4>

                <p>
                  085334255376
                </p>

              </div>

              <a
                href="https://wa.me/6285334255376"
                target="_blank"
                rel="noopener noreferrer"
                class="wa-button"
              >
                💬 WhatsApp
              </a>

            </div>


            <!-- APOTEKER 3 -->

            <div class="pharmacist-card reveal">

              <div class="pharmacist-avatar">
                👩‍⚕️
              </div>

              <div>

                <h4>
                  apt. Sri Wahyuni
                </h4>

                <p>
                  087757376296
                </p>

              </div>

              <a
                href="https://wa.me/6287757376296"
                target="_blank"
                rel="noopener noreferrer"
                class="wa-button"
              >
                💬 WhatsApp
              </a>

            </div>


            <!-- APOTEKER 4 -->

            <div class="pharmacist-card reveal">

              <div class="pharmacist-avatar">
                👩‍⚕️
              </div>

              <div>

                <h4>
                  apt. Tyara Novelia Putri
                </h4>

                <p>
                  085717420989
                </p>

              </div>

              <a
                href="https://wa.me/6285717420989"
                target="_blank"
                rel="noopener noreferrer"
                class="wa-button"
              >
                💬 WhatsApp
              </a>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         INFORMASI PELAYANAN
    ===================================================== -->

    <section id="pelayanan">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Layanan
          </div>

          <h2>
            Informasi Pelayanan
          </h2>

          <p>
            Berbagai pelayanan yang dapat diperoleh pasien.
          </p>

        </div>


        <div class="service-grid">


          <div class="service-card reveal">

            <div class="service-icon">
              💊
            </div>

            <h3>
              Pelayanan Resep
            </h3>

            <p>
              Pelayanan obat berdasarkan resep disertai
              informasi penggunaan obat.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">
              🌿
            </div>

            <h3>
              Swamedikasi
            </h3>

            <p>
              Membantu pasien memperoleh informasi dalam
              penggunaan obat untuk keluhan ringan.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">
              💬
            </div>

            <h3>
              Konsultasi Kefarmasian
            </h3>

            <p>
              Konsultasi pasien bersama apoteker mengenai
              penggunaan obat.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">
              🩺
            </div>

            <h3>
              Konseling
            </h3>

            <p>
              Pemberian informasi secara langsung agar pasien
              memahami penggunaan obat.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         SWAMEDIKASI
    ===================================================== -->

    <section
      class="self-medication"
      id="swamedikasi"
    >

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Swamedikasi
          </div>

          <h2>
            Pelayanan Swamedikasi
          </h2>

          <p>
            Informasi dan bantuan dalam penggunaan obat
            untuk keluhan ringan.
          </p>

        </div>


        <div class="self-box reveal">

          <p>
            Swamedikasi merupakan upaya penggunaan obat oleh
            masyarakat untuk mengatasi keluhan atau gangguan
            kesehatan ringan.
          </p>

          <p>
            Dalam pelayanan kefarmasian, pasien dapat memperoleh
            informasi mengenai pilihan obat, aturan penggunaan,
            serta hal-hal yang perlu diperhatikan.
          </p>

          <div class="warning-box">

            ⚠️ <strong>Perhatian:</strong>

            Apabila keluhan tidak membaik, semakin berat,
            atau muncul kondisi yang mengkhawatirkan, pasien
            disarankan memperoleh pemeriksaan dan pelayanan
            kesehatan lebih lanjut.

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         KONTAK
    ===================================================== -->

    <section id="kontak">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            Kontak
          </div>

          <h2>
            Hubungi Kami
          </h2>

          <p>
            Informasi lokasi dan kontak pelayanan kefarmasian.
          </p>

        </div>


        <div class="contact-grid">


          <div class="contact-card reveal">


            <!-- ALAMAT -->

            <div class="contact-item">

              <div class="contact-icon">
                📍
              </div>

              <div>

                <h4>
                  Alamat
                </h4>

                <p>
                  Jl. Pangandaran No.42,
                  Plinggan, Antirogo,
                  Kec. Sumbersari,
                  Kabupaten Jember,
                  Jawa Timur 68125
                </p>

              </div>

            </div>


            <!-- TELEPON -->

            <div class="contact-item">

              <div class="contact-icon">
                📱
              </div>

              <div>

                <h4>
                  WhatsApp / Telepon
                </h4>

                <a href="tel:+62331325930">
                  (0331) 325930
                </a>

              </div>

            </div>


            <!-- WEBSITE -->

            <div class="contact-item">

              <div class="contact-icon">
                🌐
              </div>

              <div>

                <h4>
                  Website
                </h4>

                <a
                  href="https://poltekesjember.ac.id/"
                  target="_blank"
                  rel="noopener noreferrer"
                >
                  https://poltekesjember.ac.id/
                </a>

              </div>

            </div>


            <div class="contact-buttons">

              <!--
                Nomor 0331 merupakan nomor yang diberikan.
                Jika nomor tersebut aktif WhatsApp,
                tombol ini akan membuka WhatsApp.
              -->

              <a
                href="https://wa.me/62331325930"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-primary"
              >
                💬 Hubungi via WhatsApp
              </a>


              <!--
                Tidak ada alamat email spesifik yang diberikan.
                Karena itu tombol diarahkan ke website resmi
                agar tidak membuat alamat email palsu.
              -->

              <a
                href="https://poltekesjember.ac.id/"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-secondary"
              >
                ✉️ Situs Resmi
              </a>

            </div>

          </div>


          <!-- GOOGLE MAPS -->

          <div class="reveal">

            <iframe
              class="map"
              src="https://www.google.com/maps?q=Jl.%20Pangandaran%20No.42,%20Plinggan,%20Antirogo,%20Kecamatan%20Sumbersari,%20Kabupaten%20Jember,%20Jawa%20Timur&output=embed"
              loading="lazy"
              allowfullscreen
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         FAQ
    ===================================================== -->

    <section
      class="faq"
      id="faq"
    >

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            FAQ
          </div>

          <h2>
            Pertanyaan yang Sering Ditanyakan
          </h2>

          <p>
            Informasi singkat untuk membantu proses pendaftaran.
          </p>

        </div>


        <div class="faq-container">


          <details class="reveal">

            <summary>
              Bagaimana cara mendaftar pelayanan?
            </summary>

            <p>
              Pasien dapat menekan tombol “Daftar Sekarang”
              dan mengisi Google Form yang tersedia.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Apakah semua pasien dapat melakukan pendaftaran?
            </summary>

            <p>
              Ya, formulir dapat digunakan oleh pasien yang
              membutuhkan pelayanan sesuai dengan jenis pelayanan
              yang tersedia.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Apakah nomor BPJS wajib diisi?
            </summary>

            <p>
              Tidak. Nomor BPJS dapat dikosongkan apabila
              pasien tidak memiliki BPJS.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Bagaimana saya mendapatkan nomor antrean?
            </summary>

            <p>
              Nomor antrean akan segera dikirimkan melalui
              WhatsApp ke nomor yang dicantumkan pada formulir.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Bagaimana urutan antreannya?
            </summary>

            <p>
              Urutan antrean mengikuti urutan waktu pengiriman
              formulir. Pasien yang mengirimkan formulir terlebih
              dahulu mendapatkan urutan terlebih dahulu.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Apa yang dilakukan setelah mendapatkan
              nomor antrean?
            </summary>

            <p>
              Pasien datang ke tempat pelayanan sesuai
              nomor antrean yang telah diberikan.
            </p>

          </details>

        </div>

      </div>

    </section>

  </main>


  <!-- =====================================================
       FOOTER
  ===================================================== -->

  <footer>

    <div class="container">

      <div class="footer-grid">


        <div>

          <h3>
            💊 PELAYANAN KEFARMASIAN
          </h3>

          <p>
            Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
          </p>

          <br>

          <p>
            Website informasi dan pendaftaran pelayanan
            kefarmasian Klinik Poltekes Jember.
          </p>

        </div>


        <div>

          <h3>
            Navigasi
          </h3>

          <div class="footer-links">

            <a href="#beranda">
              Beranda
            </a>

            <a href="#pengertian">
              Pengertian
            </a>

            <a href="#pendaftaran">
              Pendaftaran
            </a>

            <a href="#alur">
              Alur Pendaftaran
            </a>

            <a href="#resep">
              Pelayanan Resep
            </a>

            <a href="#konsultasi">
              Konsultasi
            </a>

            <a href="#kontak">
              Kontak
            </a>

          </div>

        </div>


        <div>

          <h3>
            Hubungi Kami
          </h3>

          <p>
            📍 Jl. Pangandaran No.42,
            Plinggan, Antirogo,
            Kec. Sumbersari,
            Kabupaten Jember,
            Jawa Timur 68125
          </p>

          <br>

          <p>
            📱 (0331) 325930
          </p>

          <br>

          <a
            href="https://poltekesjember.ac.id/"
            target="_blank"
            rel="noopener noreferrer"
          >
            🌐 poltekesjember.ac.id
          </a>

        </div>

      </div>


      <div class="copyright">

        © <span id="year"></span>
        Pelayanan Kefarmasian Klinik Poltekes Jember.
        All Rights Reserved.

      </div>

    </div>

  </footer>


  <!-- =====================================================
       BACK TO TOP
  ===================================================== -->

  <button
    id="backTop"
    aria-label="Kembali ke atas"
  >
    ↑
  </button>


  <!-- =====================================================
       TOAST
  ===================================================== -->

  <div id="toast"></div>


  <!-- =====================================================
       JAVASCRIPT
  ===================================================== -->

  <script>


    /* =====================================================
       GOOGLE FORM UTAMA

       Jika nanti ingin mengganti Google Form,
       cukup cari URL ini di kode:

       https://forms.gle/jG8p9wozy5nmoMrS8

       Semua tombol pendaftaran menggunakan URL tersebut.
    ===================================================== */


    /* =====================================================
       LOADING
    ===================================================== */

    window.addEventListener("load", function() {

      setTimeout(function() {

        document
          .getElementById("loader")
          .classList.add("hide");

      }, 500);

    });


    /* =====================================================
       HAMBURGER MENU
    ===================================================== */

    const hamburger =
      document.getElementById("hamburger");

    const navMenu =
      document.getElementById("navMenu");


    hamburger.addEventListener("click", function() {

      navMenu.classList.toggle("open");

      if (navMenu.classList.contains("open")) {

        hamburger.innerHTML = "✕";

      } else {

        hamburger.innerHTML = "☰";

      }

    });


    /* =====================================================
       TUTUP MENU MOBILE
       KETIKA LINK DIKLIK
    ===================================================== */

    document
      .querySelectorAll(".nav-menu a")
      .forEach(function(link) {

        link.addEventListener("click", function() {

          navMenu.classList.remove("open");

          hamburger.innerHTML = "☰";

        });

      });


    /* =====================================================
       TOAST
    ===================================================== */

    function showToast(message) {

      const toast =
        document.getElementById("toast");

      toast.textContent = message;

      toast.classList.add("show");


      setTimeout(function() {

        toast.classList.remove("show");

      }, 2500);

    }


    /* =====================================================
       BACK TO TOP
    ===================================================== */

    const backTop =
      document.getElementById("backTop");


    window.addEventListener("scroll", function() {

      if (window.scrollY > 500) {

        backTop.classList.add("show");

      } else {

        backTop.classList.remove("show");

      }

    });


    backTop.addEventListener("click", function() {

      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });

    });


    /* =====================================================
       SCROLL ANIMATION
    ===================================================== */

    const observer =
      new IntersectionObserver(

        function(entries) {

          entries.forEach(function(entry) {

            if (entry.isIntersecting) {

              entry.target.classList.add("active");

              observer.unobserve(entry.target);

            }

          });

        },

        {
          threshold: 0.12
        }

      );


    document
      .querySelectorAll(".reveal")
      .forEach(function(element) {

        observer.observe(element);

      });


    /* =====================================================
       TAHUN FOOTER
    ===================================================== */

    document.getElementById("year").textContent =
      new Date().getFullYear();


  </script>

</body>
</html>
