<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>PELAYANAN KEFARMASIAN</title>
  <meta name="description" content="Website informasi dan pendaftaran pelayanan kefarmasian. Mudah mendaftar, nyaman mendapatkan pelayanan.">

  <style>
    :root {
      --sage: #A8BFAE;
      --sage-dark: #789781;
      --sage-light: #EFF5F0;
      --white: #FFFFFF;
      --pink: #E8B7C3;
      --pink-dark: #D38FA0;
      --text: #35443A;
      --text-light: #657269;
      --border: #DCE7DE;
      --shadow: 0 10px 30px rgba(82, 111, 91, 0.12);
      --radius: 20px;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: "Segoe UI", Arial, sans-serif;
      background: var(--white);
      color: var(--text);
      line-height: 1.7;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button,
    a {
      -webkit-tap-highlight-color: transparent;
    }

    .container {
      width: 90%;
      max-width: 1180px;
      margin: auto;
    }

    /* ================= NAVBAR ================= */

    header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(255,255,255,0.96);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid rgba(168,191,174,0.3);
    }

    nav {
      height: 75px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 20px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 800;
      color: var(--sage-dark);
      font-size: 18px;
      white-space: nowrap;
    }

    .logo-icon {
      width: 40px;
      height: 40px;
      border-radius: 12px;
      background: var(--sage-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 21px;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 20px;
      list-style: none;
    }

    .nav-links a {
      font-size: 13px;
      font-weight: 600;
      color: var(--text);
      transition: .3s;
    }

    .nav-links a:hover {
      color: var(--sage-dark);
    }

    .nav-cta {
      background: var(--sage-dark) !important;
      color: white !important;
      padding: 10px 17px;
      border-radius: 25px;
    }

    .nav-cta:hover {
      background: var(--pink-dark) !important;
    }

    .hamburger {
      display: none;
      border: none;
      background: var(--sage-light);
      width: 43px;
      height: 43px;
      border-radius: 12px;
      font-size: 22px;
      cursor: pointer;
      color: var(--text);
    }

    /* ================= HERO ================= */

    .hero {
      min-height: 100vh;
      padding-top: 120px;
      display: flex;
      align-items: center;
      background:
        radial-gradient(circle at 90% 20%, rgba(232,183,195,.25), transparent 25%),
        radial-gradient(circle at 10% 90%, rgba(168,191,174,.30), transparent 30%),
        var(--sage-light);
      position: relative;
    }

    .hero-content {
      display: grid;
      grid-template-columns: 1.1fr .9fr;
      align-items: center;
      gap: 60px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: white;
      color: var(--sage-dark);
      padding: 8px 15px;
      border-radius: 30px;
      font-size: 13px;
      font-weight: 700;
      margin-bottom: 20px;
      box-shadow: 0 5px 20px rgba(0,0,0,.05);
    }

    .hero h1 {
      font-size: clamp(38px, 6vw, 65px);
      line-height: 1.08;
      margin-bottom: 20px;
      color: var(--text);
      letter-spacing: -1.5px;
    }

    .hero h1 span {
      color: var(--sage-dark);
    }

    .hero-tagline {
      font-size: 21px;
      font-weight: 700;
      color: var(--pink-dark);
      margin-bottom: 15px;
    }

    .hero-description {
      color: var(--text-light);
      max-width: 650px;
      margin-bottom: 30px;
      font-size: 16px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 13px;
    }

    .btn {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
      padding: 13px 22px;
      border-radius: 13px;
      font-weight: 700;
      border: 2px solid transparent;
      transition: .3s;
      cursor: pointer;
    }

    .btn-primary {
      background: var(--sage-dark);
      color: white;
    }

    .btn-primary:hover {
      transform: translateY(-3px);
      background: #64866d;
      box-shadow: var(--shadow);
    }

    .btn-secondary {
      background: white;
      border-color: var(--sage);
      color: var(--sage-dark);
    }

    .btn-secondary:hover {
      background: var(--pink);
      color: white;
      border-color: var(--pink);
    }

    .hero-visual {
      display: flex;
      justify-content: center;
      position: relative;
    }

    .health-card {
      width: min(380px, 90%);
      min-height: 390px;
      background: white;
      border-radius: 35px;
      box-shadow: var(--shadow);
      padding: 35px;
      position: relative;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
    }

    .medical-symbol {
      width: 150px;
      height: 150px;
      border-radius: 45px;
      background: var(--sage-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 75px;
      margin-bottom: 25px;
      transform: rotate(-5deg);
    }

    .health-card h3 {
      font-size: 24px;
      margin-bottom: 8px;
    }

    .health-card p {
      text-align: center;
      color: var(--text-light);
      font-size: 14px;
    }

    .floating {
      position: absolute;
      padding: 10px 15px;
      background: white;
      border-radius: 15px;
      box-shadow: var(--shadow);
      font-size: 13px;
      font-weight: 700;
    }

    .floating.one {
      top: 20px;
      right: 0;
      color: var(--pink-dark);
    }

    .floating.two {
      bottom: 30px;
      left: 0;
      color: var(--sage-dark);
    }

    /* ================= GENERAL SECTION ================= */

    section {
      padding: 90px 0;
    }

    .section-header {
      text-align: center;
      max-width: 750px;
      margin: 0 auto 50px;
    }

    .section-label {
      color: var(--pink-dark);
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 1.5px;
      font-size: 12px;
      margin-bottom: 8px;
    }

    .section-title {
      font-size: clamp(28px, 4vw, 42px);
      line-height: 1.2;
      margin-bottom: 13px;
    }

    .section-description {
      color: var(--text-light);
      font-size: 15px;
    }

    /* ================= PENGERTIAN ================= */

    .definition {
      background: white;
    }

    .definition-box {
      background: var(--sage-light);
      padding: 35px;
      border-radius: var(--radius);
      border-left: 5px solid var(--sage-dark);
      margin-bottom: 35px;
    }

    .definition-box p {
      font-size: 17px;
    }

    .three-cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .info-card {
      padding: 28px;
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      box-shadow: 0 5px 20px rgba(80,110,90,.05);
      transition: .3s;
    }

    .info-card:hover {
      transform: translateY(-7px);
      box-shadow: var(--shadow);
    }

    .card-icon {
      width: 55px;
      height: 55px;
      border-radius: 16px;
      background: var(--sage-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 26px;
      margin-bottom: 18px;
    }

    .info-card:nth-child(2) .card-icon {
      background: #fff0f3;
    }

    .info-card h3 {
      margin-bottom: 8px;
      font-size: 19px;
    }

    .info-card p {
      color: var(--text-light);
      font-size: 14px;
    }

    /* ================= SERVICES ================= */

    .services {
      background: var(--sage-light);
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .service-card {
      background: white;
      padding: 27px;
      border-radius: var(--radius);
      transition: .3s;
      border: 1px solid transparent;
    }

    .service-card:hover {
      transform: translateY(-5px);
      border-color: var(--sage);
      box-shadow: var(--shadow);
    }

    .service-icon {
      font-size: 32px;
      margin-bottom: 14px;
    }

    .service-card h3 {
      font-size: 18px;
      margin-bottom: 7px;
    }

    .service-card p {
      color: var(--text-light);
      font-size: 14px;
    }

    /* ================= REGISTRATION ================= */

    .registration {
      background: white;
    }

    .registration-wrapper {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 35px;
      align-items: stretch;
    }

    .registration-box {
      background: var(--sage-light);
      border-radius: 28px;
      padding: 40px;
    }

    .registration-box h3 {
      font-size: 26px;
      margin-bottom: 12px;
    }

    .registration-box p {
      color: var(--text-light);
      margin-bottom: 25px;
    }

    .form-list {
      list-style: none;
      margin-bottom: 25px;
    }

    .form-list li {
      padding: 10px 0;
      border-bottom: 1px solid rgba(120,151,129,.2);
      font-size: 14px;
    }

    .form-list li::before {
      content: "✓";
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 23px;
      height: 23px;
      background: white;
      color: var(--sage-dark);
      border-radius: 50%;
      margin-right: 10px;
      font-weight: bold;
    }

    .important-note {
      background: white;
      border: 2px solid var(--pink);
      border-radius: 18px;
      padding: 23px;
      height: 100%;
    }

    .important-note h3 {
      color: var(--pink-dark);
      margin-bottom: 15px;
    }

    .important-note p {
      color: var(--text-light);
      font-size: 14px;
      margin-bottom: 12px;
    }

    .note-item {
      display: flex;
      gap: 10px;
      margin-bottom: 12px;
    }

    .note-number {
      min-width: 28px;
      height: 28px;
      border-radius: 50%;
      background: #fff0f3;
      color: var(--pink-dark);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
      font-size: 12px;
    }

    /* ================= QUEUE ================= */

    .queue {
      background: #fafcfb;
    }

    .queue-box {
      background: white;
      border-radius: 25px;
      padding: 35px;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }

    .queue-steps {
      display: grid;
      grid-template-columns: repeat(5, 1fr);
      gap: 10px;
    }

    .queue-step {
      text-align: center;
      position: relative;
    }

    .queue-icon {
      width: 60px;
      height: 60px;
      margin: 0 auto 12px;
      border-radius: 50%;
      background: var(--sage-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 24px;
    }

    .queue-step:nth-child(4) .queue-icon {
      background: #fff0f3;
    }

    .queue-step strong {
      display: block;
      font-size: 14px;
      margin-bottom: 5px;
    }

    .queue-step span {
      color: var(--text-light);
      font-size: 12px;
    }

    /* ================= FLOW ================= */

    .flow {
      background: white;
    }

    .timeline {
      display: grid;
      grid-template-columns: repeat(6, 1fr);
      gap: 10px;
      position: relative;
    }

    .timeline-item {
      text-align: center;
      position: relative;
    }

    .timeline-number {
      width: 55px;
      height: 55px;
      margin: 0 auto 15px;
      border-radius: 16px;
      background: var(--sage-dark);
      color: white;
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: 800;
    }

    .timeline-item:nth-child(even) .timeline-number {
      background: var(--pink-dark);
    }

    .timeline-item h4 {
      font-size: 14px;
      margin-bottom: 5px;
    }

    .timeline-item p {
      font-size: 12px;
      color: var(--text-light);
    }

    /* ================= RESEP ================= */

    .prescription {
      background: var(--sage-light);
    }

    .prescription-flow {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .prescription-step {
      background: white;
      padding: 25px 20px;
      border-radius: 20px;
      position: relative;
      transition: .3s;
    }

    .prescription-step:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow);
    }

    .prescription-step .step-icon {
      width: 50px;
      height: 50px;
      background: var(--sage-light);
      border-radius: 14px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 23px;
      margin-bottom: 14px;
    }

    .prescription-step:nth-child(2) .step-icon,
    .prescription-step:nth-child(5) .step-icon {
      background: #fff0f3;
    }

    .prescription-step h3 {
      font-size: 16px;
      margin-bottom: 7px;
    }

    .prescription-step p {
      color: var(--text-light);
      font-size: 13px;
    }

    /* ================= CONSULTATION ================= */

    .consultation {
      background: white;
    }

    .consultation-wrapper {
      display: grid;
      grid-template-columns: .9fr 1.1fr;
      gap: 45px;
      align-items: center;
    }

    .consultation-text h3 {
      font-size: 28px;
      margin-bottom: 15px;
    }

    .consultation-text p {
      color: var(--text-light);
      margin-bottom: 20px;
    }

    .topics {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 8px;
      list-style: none;
      margin-bottom: 25px;
    }

    .topics li {
      font-size: 13px;
      background: var(--sage-light);
      padding: 9px 12px;
      border-radius: 10px;
    }

    .chat-box {
      background: var(--sage-light);
      border-radius: 28px;
      padding: 28px;
    }

    .chat-title {
      font-weight: 800;
      margin-bottom: 20px;
    }

    .message {
      max-width: 82%;
      padding: 13px 16px;
      border-radius: 18px;
      margin-bottom: 15px;
      font-size: 14px;
    }

    .patient {
      background: white;
      border-bottom-left-radius: 5px;
    }

    .pharmacist {
      background: var(--sage-dark);
      color: white;
      margin-left: auto;
      border-bottom-right-radius: 5px;
    }

    .message small {
      display: block;
      opacity: .7;
      font-size: 10px;
      margin-bottom: 3px;
    }

    /* ================= SWAMEDIKASI ================= */

    .self-medication {
      background: #fafcfb;
    }

    .self-box {
      max-width: 900px;
      margin: auto;
      background: white;
      border-radius: 25px;
      padding: 35px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
      text-align: center;
    }

    .self-icon {
      font-size: 50px;
      margin-bottom: 15px;
    }

    .self-box p {
      color: var(--text-light);
      font-size: 15px;
    }

    .warning {
      display: inline-block;
      margin-top: 18px;
      background: #fff0f3;
      color: #8d5261;
      border-radius: 12px;
      padding: 12px 17px;
      font-size: 13px;
      font-weight: 600;
    }

    /* ================= FAQ ================= */

    .faq {
      background: white;
    }

    .faq-container {
      max-width: 850px;
      margin: auto;
    }

    details {
      border: 1px solid var(--border);
      border-radius: 15px;
      margin-bottom: 12px;
      padding: 18px 20px;
      background: white;
    }

    summary {
      cursor: pointer;
      font-weight: 700;
      list-style: none;
      position: relative;
      padding-right: 30px;
    }

    summary::after {
      content: "+";
      position: absolute;
      right: 0;
      font-size: 22px;
      color: var(--sage-dark);
    }

    details[open] summary::after {
      content: "−";
    }

    details p {
      color: var(--text-light);
      font-size: 14px;
      margin-top: 12px;
      padding-top: 12px;
      border-top: 1px solid var(--border);
    }

    /* ================= CONTACT ================= */

    .contact {
      background: var(--sage-light);
    }

    .contact-wrapper {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
    }

    .contact-card {
      background: white;
      border-radius: 25px;
      padding: 35px;
      box-shadow: var(--shadow);
    }

    .contact-item {
      display: flex;
      align-items: flex-start;
      gap: 15px;
      margin-bottom: 22px;
    }

    .contact-icon {
      min-width: 48px;
      height: 48px;
      border-radius: 14px;
      background: var(--sage-light);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 21px;
    }

    .contact-item:nth-child(2) .contact-icon {
      background: #fff0f3;
    }

    .contact-item h4 {
      font-size: 14px;
      margin-bottom: 3px;
    }

    .contact-item p,
    .contact-item a {
      font-size: 14px;
      color: var(--text-light);
    }

    .contact-item a:hover {
      color: var(--pink-dark);
    }

    .contact-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 10px;
    }

    /* ================= FOOTER ================= */

    footer {
      background: var(--text);
      color: white;
      padding: 50px 0 25px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1.3fr 1fr 1fr;
      gap: 40px;
      padding-bottom: 35px;
      border-bottom: 1px solid rgba(255,255,255,.15);
    }

    .footer-brand h3 {
      color: var(--sage);
      margin-bottom: 10px;
    }

    .footer-brand p {
      color: #c8d2cb;
      font-size: 13px;
      max-width: 350px;
    }

    footer h4 {
      margin-bottom: 13px;
    }

    .footer-links {
      list-style: none;
    }

    .footer-links li {
      margin-bottom: 7px;
    }

    .footer-links a {
      color: #c8d2cb;
      font-size: 13px;
    }

    .footer-links a:hover {
      color: var(--pink);
    }

    .footer-contact {
      color: #c8d2cb;
      font-size: 13px;
    }

    .copyright {
      text-align: center;
      padding-top: 25px;
      color: #aebbb2;
      font-size: 12px;
    }

    /* ================= BACK TO TOP ================= */

    #backTop {
      position: fixed;
      right: 22px;
      bottom: 22px;
      width: 45px;
      height: 45px;
      border: none;
      border-radius: 50%;
      background: var(--sage-dark);
      color: white;
      cursor: pointer;
      font-size: 20px;
      display: none;
      z-index: 999;
      box-shadow: var(--shadow);
    }

    #backTop:hover {
      background: var(--pink-dark);
    }

    /* ================= TOAST ================= */

    .toast {
      position: fixed;
      bottom: 25px;
      left: 50%;
      transform: translate(-50%, 100px);
      background: var(--text);
      color: white;
      padding: 13px 20px;
      border-radius: 13px;
      font-size: 13px;
      z-index: 2000;
      opacity: 0;
      transition: .4s;
    }

    .toast.show {
      transform: translate(-50%, 0);
      opacity: 1;
    }

    /* ================= ANIMATION ================= */

    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: .7s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* ================= RESPONSIVE ================= */

    @media (max-width: 1000px) {
      .nav-links {
        gap: 12px;
      }

      .nav-links a {
        font-size: 12px;
      }

      .hero-content {
        gap: 30px;
      }

      .timeline {
        grid-template-columns: repeat(3, 1fr);
        gap: 30px 10px;
      }

      .prescription-flow {
        grid-template-columns: repeat(2, 1fr);
      }

      .queue-steps {
        grid-template-columns: repeat(3, 1fr);
        gap: 25px 10px;
      }
    }

    @media (max-width: 800px) {
      header {
        height: 70px;
      }

      nav {
        height: 70px;
      }

      .hamburger {
        display: block;
      }

      .nav-links {
        position: absolute;
        top: 70px;
        left: 0;
        width: 100%;
        background: white;
        flex-direction: column;
        align-items: stretch;
        gap: 0;
        padding: 10px 5%;
        box-shadow: 0 10px 20px rgba(0,0,0,.08);
        display: none;
      }

      .nav-links.active {
        display: flex;
      }

      .nav-links li {
        border-bottom: 1px solid var(--border);
      }

      .nav-links a {
        display: block;
        padding: 13px 5px;
        font-size: 14px;
      }

      .nav-cta {
        text-align: center;
        margin: 8px 0;
      }

      .hero {
        padding-top: 105px;
      }

      .hero-content {
        grid-template-columns: 1fr;
        text-align: center;
      }

      .hero-description {
        margin-left: auto;
        margin-right: auto;
      }

      .hero-buttons {
        justify-content: center;
      }

      .hero-visual {
        margin-top: 20px;
      }

      .three-cards,
      .service-grid {
        grid-template-columns: 1fr 1fr;
      }

      .registration-wrapper,
      .consultation-wrapper,
      .contact-wrapper {
        grid-template-columns: 1fr;
      }

      .footer-grid {
        grid-template-columns: 1fr 1fr;
      }
    }

    @media (max-width: 560px) {
      .container {
        width: 92%;
      }

      section {
        padding: 65px 0;
      }

      .logo {
        font-size: 15px;
      }

      .logo-icon {
        width: 36px;
        height: 36px;
      }

      .hero h1 {
        font-size: 40px;
      }

      .hero-tagline {
        font-size: 17px;
      }

      .hero-description {
        font-size: 14px;
      }

      .health-card {
        min-height: 320px;
      }

      .floating.one {
        right: -5px;
      }

      .floating.two {
        left: -5px;
      }

      .three-cards,
      .service-grid,
      .prescription-flow,
      .timeline,
      .queue-steps {
        grid-template-columns: 1fr;
      }

      .registration-box,
      .important-note,
      .queue-box,
      .self-box,
      .contact-card {
        padding: 25px;
      }

      .topics {
        grid-template-columns: 1fr;
      }

      .footer-grid {
        grid-template-columns: 1fr;
        gap: 28px;
      }

      .btn {
        width: 100%;
      }

      .hero-buttons {
        width: 100%;
      }

      .hero-buttons .btn {
        width: 100%;
      }
    }
  </style>
</head>

<body>

  <!-- ================= NAVBAR ================= -->

  <header>
    <div class="container">
      <nav>

        <a href="#beranda" class="logo">
          <span class="logo-icon">💊</span>
          PELAYANAN KEFARMASIAN
        </a>

        <button class="hamburger" id="hamburger" aria-label="Menu">
          ☰
        </button>

        <ul class="nav-links" id="navLinks">
          <li><a href="#beranda">Beranda</a></li>
          <li><a href="#pengertian">Pengertian</a></li>
          <li><a href="#pendaftaran">Pendaftaran</a></li>
          <li><a href="#alur">Alur Pendaftaran</a></li>
          <li><a href="#resep">Pelayanan Resep</a></li>
          <li><a href="#konsultasi">Konsultasi</a></li>
          <li><a href="#swamedikasi">Swamedikasi</a></li>
          <li><a href="#kontak">Kontak</a></li>
          <li>
            <a
              href="MASUKKAN_LINK_GOOGLE_FORM_DI_SINI"
              target="_blank"
              rel="noopener noreferrer"
              class="nav-cta"
              onclick="showToast('Membuka formulir pendaftaran...')">
              Daftar Sekarang
            </a>
          </li>
        </ul>

      </nav>
    </div>
  </header>


  <!-- ================= HERO ================= -->

  <main>

    <section class="hero" id="beranda">
      <div class="container">

        <div class="hero-content">

          <div class="reveal">

            <div class="badge">
              💚 Informasi & Pendaftaran Pelayanan
            </div>

            <h1>
              PELAYANAN<br>
              <span>KEFARMASIAN</span>
            </h1>

            <div class="hero-tagline">
              Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
            </div>

            <p class="hero-description">
              Website pelayanan kefarmasian yang memberikan informasi
              pelayanan serta memudahkan pasien melakukan pendaftaran
              secara online.
            </p>

            <div class="hero-buttons">

              <a
                href="MASUKKAN_LINK_GOOGLE_FORM_DI_SINI"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-primary"
                onclick="showToast('Membuka formulir pendaftaran...')">
                📝 Daftar Sekarang
              </a>

              <a href="#pelayanan" class="btn btn-secondary">
                💊 Lihat Pelayanan
              </a>

            </div>

          </div>

          <div class="hero-visual reveal">

            <div class="health-card">

              <div class="floating one">
                💗 Ramah Pasien
              </div>

              <div class="medical-symbol">
                ⚕️
              </div>

              <h3>Pharmacy Care</h3>

              <p>
                Informasi obat, pelayanan kefarmasian,
                konsultasi dan pendaftaran pasien.
              </p>

              <div class="floating two">
                🌿 Mudah & Nyaman
              </div>

            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- ================= PENGERTIAN ================= -->

    <section class="definition" id="pengertian">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Tentang Pelayanan</div>

          <h2 class="section-title">
            Pengertian Pelayanan Kefarmasian
          </h2>

          <p class="section-description">
            Mengenal pelayanan kefarmasian dan perannya dalam membantu
            pasien menggunakan obat secara tepat.
          </p>
        </div>

        <div class="definition-box reveal">

          <p>
            <strong>Pelayanan kefarmasian</strong> merupakan pelayanan yang
            diberikan oleh tenaga kefarmasian kepada pasien yang berkaitan
            dengan penggunaan obat dan pelayanan kesehatan untuk membantu
            memastikan obat digunakan secara tepat, aman, dan efektif.
            Pelayanan kefarmasian berorientasi pada kebutuhan pasien,
            sehingga tidak hanya berfokus pada penyediaan obat tetapi juga
            mencakup pemberian informasi, konsultasi, konseling, serta
            pemantauan penggunaan obat.
          </p>

        </div>

        <div class="three-cards">

          <div class="info-card reveal">
            <div class="card-icon">💊</div>
            <h3>Pengelolaan Obat</h3>
            <p>
              Meliputi pengadaan, penerimaan, penyimpanan dan pengelolaan
              obat agar mutu obat tetap terjaga.
            </p>
          </div>

          <div class="info-card reveal">
            <div class="card-icon">🧑‍⚕️</div>
            <h3>Pelayanan kepada Pasien</h3>
            <p>
              Pelayanan diberikan dengan memperhatikan kebutuhan pasien
              serta ketepatan dan keamanan penggunaan obat.
            </p>
          </div>

          <div class="info-card reveal">
            <div class="card-icon">💬</div>
            <h3>Informasi & Konsultasi</h3>
            <p>
              Pasien dapat memperoleh informasi mengenai penggunaan obat,
              aturan pakai, efek samping dan hal penting lainnya.
            </p>
          </div>

        </div>

      </div>
    </section>


    <!-- ================= SERVICES ================= -->

    <section class="services" id="pelayanan">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Layanan</div>

          <h2 class="section-title">
            Pelayanan yang Tersedia
          </h2>

          <p class="section-description">
            Berbagai pelayanan kefarmasian untuk membantu pasien memperoleh
            informasi dan pelayanan yang sesuai.
          </p>
        </div>

        <div class="service-grid">

          <div class="service-card reveal">
            <div class="service-icon">📋</div>
            <h3>Pelayanan Resep</h3>
            <p>
              Pelayanan resep mulai dari penerimaan, pemeriksaan,
              penyiapan hingga penyerahan obat kepada pasien.
            </p>
          </div>

          <div class="service-card reveal">
            <div class="service-icon">🌿</div>
            <h3>Swamedikasi</h3>
            <p>
              Informasi dan bantuan dalam memilih obat untuk keluhan ringan
              dengan memperhatikan keamanan penggunaannya.
            </p>
          </div>

          <div class="service-card reveal">
            <div class="service-icon">🩺</div>
            <h3>Konsultasi Kefarmasian</h3>
            <p>
              Konsultasi bersama apoteker mengenai obat dan masalah yang
              berkaitan dengan penggunaannya.
            </p>
          </div>

          <div class="service-card reveal">
            <div class="service-icon">💬</div>
            <h3>Konseling Obat</h3>
            <p>
              Pemberian informasi dan edukasi agar pasien memahami
              penggunaan obat dengan benar.
            </p>
          </div>

          <div class="service-card reveal">
            <div class="service-icon">📚</div>
            <h3>Informasi Obat</h3>
            <p>
              Informasi mengenai nama obat, kegunaan, aturan pakai,
              efek samping, penyimpanan dan perhatian penggunaan.
            </p>
          </div>

          <div class="service-card reveal">
            <div class="service-icon">🩹</div>
            <h3>Pemeriksaan Kesehatan Sederhana</h3>
            <p>
              Pelayanan pemeriksaan kesehatan sederhana sesuai fasilitas
              yang tersedia.
            </p>
          </div>

        </div>

      </div>
    </section>


    <!-- ================= PENDAFTARAN ================= -->

    <section class="registration" id="pendaftaran">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Pendaftaran Online</div>

          <h2 class="section-title">
            Pendaftaran Pelayanan
          </h2>

          <p class="section-description">
            Silakan melakukan pendaftaran terlebih dahulu sebelum mendapatkan
            pelayanan. Isi formulir dengan data yang benar agar proses
            pelayanan dapat berjalan dengan baik.
          </p>
        </div>

        <div class="registration-wrapper">

          <div class="registration-box reveal">

            <h3>📝 Isi Formulir Pendaftaran</h3>

            <p>
              Pendaftaran dilakukan melalui Google Form. Formulir dapat
              digunakan oleh pasien untuk menyampaikan data dan kebutuhan
              pelayanan.
            </p>

            <ul class="form-list">

              <li>Nama pasien</li>

              <li>Nomor BPJS jika ada <strong>(opsional)</strong></li>

              <li>Keluhan atau kebutuhan pelayanan</li>

              <li>Nomor WhatsApp yang dapat dihubungi</li>

            </ul>

            <a
              href="https://forms.gle/jG8p9wozy5nmoMrS8"
              target="_blank"
              rel="noopener noreferrer"
              class="btn btn-primary"
              onclick="showToast('Membuka Google Form...')">
              📝 Isi Formulir Pendaftaran
            </a>

          </div>


          <div class="important-note reveal">

            <h3>📌 Informasi Penting Pendaftaran</h3>

            <p>
              Perhatikan informasi berikut setelah mengisi formulir
              pendaftaran:
            </p>

            <div class="note-item">
              <div class="note-number">1</div>
              <p>
                Setelah formulir dikirim, <strong>nomor antrean akan segera
                dikirimkan melalui WhatsApp</strong> ke nomor yang telah
                dimasukkan pada formulir.
              </p>
            </div>

            <div class="note-item">
              <div class="note-number">2</div>
              <p>
                Pastikan nomor WhatsApp yang dicantumkan <strong>aktif dan
                dapat dihubungi</strong>.
              </p>
            </div>

            <div class="note-item">
              <div class="note-number">3</div>
              <p>
                Urutan antrean ditentukan berdasarkan <strong>urutan waktu
                pengiriman formulir</strong>. Pasien yang mengirim formulir
                lebih dahulu akan memperoleh urutan antrean lebih dahulu.
              </p>
            </div>

            <div class="note-item">
              <div class="note-number">4</div>
              <p>
                Setelah mendapatkan nomor antrean, pasien dapat datang sesuai
                dengan antrean yang telah diberikan.
              </p>
            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- ================= INFORMASI ANTREAN ================= -->

    <section class="queue">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Antrean</div>

          <h2 class="section-title">
            Informasi Antrean
          </h2>

          <p class="section-description">
            Berikut tahapan yang dilakukan setelah pasien mengisi formulir
            pendaftaran.
          </p>
        </div>

        <div class="queue-box reveal">

          <div class="queue-steps">

            <div class="queue-step">
              <div class="queue-icon">📝</div>
              <strong>Isi Google Form</strong>
              <span>Pasien mengisi data pendaftaran.</span>
            </div>

            <div class="queue-step">
              <div class="queue-icon">📥</div>
              <strong>Data Diterima</strong>
              <span>Formulir masuk dan diproses.</span>
            </div>

            <div class="queue-step">
              <div class="queue-icon">🔢</div>
              <strong>Antrean Diproses</strong>
              <span>Nomor antrean ditentukan berdasarkan urutan pengiriman.</span>
            </div>

            <div class="queue-step">
              <div class="queue-icon">📱</div>
              <strong>WhatsApp</strong>
              <span>Nomor antrean dikirim melalui WhatsApp.</span>
            </div>

            <div class="queue-step">
              <div class="queue-icon">🏥</div>
              <strong>Datang ke Pelayanan</strong>
              <span>Pasien datang sesuai nomor antrean.</span>
            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- ================= ALUR PENDAFTARAN ================= -->

    <section class="flow" id="alur">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Langkah Pendaftaran</div>

          <h2 class="section-title">
            Alur Pendaftaran Pelayanan
          </h2>

          <p class="section-description">
            Ikuti langkah berikut untuk melakukan pendaftaran secara online.
          </p>
        </div>

        <div class="timeline">

          <div class="timeline-item reveal">
            <div class="timeline-number">01</div>
            <h4>Buka Website</h4>
            <p>Akses website pelayanan kefarmasian.</p>
          </div>

          <div class="timeline-item reveal">
            <div class="timeline-number">02</div>
            <h4>Pilih Pendaftaran</h4>
            <p>Klik tombol pendaftaran pelayanan.</p>
          </div>

          <div class="timeline-item reveal">
            <div class="timeline-number">03</div>
            <h4>Isi Google Form</h4>
            <p>Isi data pasien dengan benar.</p>
          </div>

          <div class="timeline-item reveal">
            <div class="timeline-number">04</div>
            <h4>Kirim Formulir</h4>
            <p>Periksa data kemudian kirim formulir.</p>
          </div>

          <div class="timeline-item reveal">
            <div class="timeline-number">05</div>
            <h4>Dapat Nomor Antrean</h4>
            <p>Nomor antrean dikirim melalui WhatsApp.</p>
          </div>

          <div class="timeline-item reveal">
            <div class="timeline-number">06</div>
            <h4>Datang ke Pelayanan</h4>
            <p>Datang sesuai urutan antrean.</p>
          </div>

        </div>

        <div style="text-align:center; margin-top:45px;" class="reveal">

          <a
            href="MASUKKAN_LINK_GOOGLE_FORM_DI_SINI"
            target="_blank"
            rel="noopener noreferrer"
            class="btn btn-primary"
            onclick="showToast('Membuka Google Form...')">
            📝 Daftar Sekarang
          </a>

        </div>

      </div>
    </section>


    <!-- ================= PELAYANAN RESEP ================= -->

    <section class="prescription" id="resep">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Pelayanan Resep</div>

          <h2 class="section-title">
            Alur Pelayanan Resep
          </h2>

          <p class="section-description">
            Pelayanan resep dilakukan secara sistematis untuk membantu
            memastikan obat diterima pasien dengan tepat dan aman.
          </p>
        </div>

        <div class="prescription-flow">

          <div class="prescription-step reveal">
            <div class="step-icon">📋</div>
            <h3>1. Penerimaan Resep</h3>
            <p>
              Pasien menyerahkan resep kepada tenaga kefarmasian untuk
              dilakukan proses pelayanan.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">🔍</div>
            <h3>2. Pemeriksaan Resep</h3>
            <p>
              Resep diperiksa dari aspek kelengkapan dan kesesuaian
              sebelum obat disiapkan.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">💊</div>
            <h3>3. Penyiapan Obat</h3>
            <p>
              Obat disiapkan sesuai resep serta dilakukan pelabelan
              dan penyiapan yang diperlukan.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">🔎</div>
            <h3>4. Pemeriksaan Kembali</h3>
            <p>
              Dilakukan pemeriksaan kembali terhadap obat dan etiket
              sebelum diserahkan kepada pasien.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">🤲</div>
            <h3>5. Penyerahan Obat</h3>
            <p>
              Obat diserahkan kepada pasien dengan memastikan pasien
              menerima obat yang sesuai.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">💬</div>
            <h3>6. Pemberian KIE</h3>
            <p>
              Pasien diberikan informasi mengenai nama obat, penggunaan,
              dosis, waktu penggunaan, penyimpanan dan perhatian lainnya.
            </p>
          </div>

          <div class="prescription-step reveal">
            <div class="step-icon">✅</div>
            <h3>7. Pelayanan Selesai</h3>
            <p>
              Pasien dapat menggunakan obat sesuai informasi yang telah
              diberikan.
            </p>
          </div>

        </div>

      </div>
    </section>


    <!-- ================= KONSULTASI ================= -->

    <section class="consultation" id="konsultasi">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Konsultasi</div>

          <h2 class="section-title">
            Konsultasi Kefarmasian
          </h2>

          <p class="section-description">
            Pasien dapat berkonsultasi dengan apoteker mengenai penggunaan
            obat dan masalah yang berkaitan dengan terapi obat.
          </p>
        </div>

        <div class="consultation-wrapper">

          <div class="consultation-text reveal">

            <h3>💬 Konsultasi Bersama Apoteker</h3>

            <p>
              Konsultasi kefarmasian memberikan kesempatan kepada pasien
              untuk menyampaikan pertanyaan atau masalah terkait obat yang
              sedang digunakan.
            </p>

            <ul class="topics">

              <li>✓ Cara penggunaan obat</li>
              <li>✓ Aturan pakai</li>
              <li>✓ Waktu penggunaan</li>
              <li>✓ Efek samping</li>
              <li>✓ Interaksi obat</li>
              <li>✓ Penyimpanan obat</li>
              <li>✓ Penggunaan beberapa obat</li>
              <li>✓ Masalah terkait obat</li>

            </ul>

            <a
              href="https://wa.me/6285717420989?text=Halo,%20saya%20ingin%20berkonsultasi%20mengenai%20obat."
              target="_blank"
              rel="noopener noreferrer"
              class="btn btn-primary"
              onclick="showToast('Membuka WhatsApp...')">
              💬 Konsultasi dengan Apoteker
            </a>

          </div>


          <div class="chat-box reveal">

            <div class="chat-title">
              Contoh Konsultasi
            </div>

            <div class="message patient">
              <small>Pasien</small>
              Saya ingin berkonsultasi mengenai obat yang sedang saya gunakan.
            </div>

            <div class="message pharmacist">
              <small>Apoteker</small>
              Silakan sampaikan nama obat, aturan penggunaan, serta keluhan
              atau pertanyaan yang ingin dikonsultasikan.
            </div>

            <div class="message patient">
              <small>Pasien</small>
              Saya ingin mengetahui cara penggunaan dan waktu minum obat
              tersebut.
            </div>

            <div class="message pharmacist">
              <small>Apoteker</small>
              Informasi penggunaan obat akan disampaikan sesuai dengan
              kebutuhan dan kondisi pasien.
            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- ================= SWAMEDIKASI ================= -->

    <section class="self-medication" id="swamedikasi">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Swamedikasi</div>

          <h2 class="section-title">
            Pelayanan Swamedikasi
          </h2>

          <p class="section-description">
            Penggunaan obat secara mandiri untuk menangani keluhan ringan
            dengan memperhatikan ketepatan dan keamanan penggunaan obat.
          </p>
        </div>

        <div class="self-box reveal">

          <div class="self-icon">🌿</div>

          <p>
            Swamedikasi dapat dilakukan untuk beberapa keluhan ringan,
            namun pemilihan obat tetap perlu memperhatikan kondisi pasien,
            aturan penggunaan dan informasi pada obat. Tenaga kefarmasian
            dapat membantu memberikan informasi yang sesuai agar obat
            digunakan secara aman dan tepat.
          </p>

          <div class="warning">
            ⚠️ Jika keluhan semakin berat, tidak membaik, atau muncul
            gejala yang mengkhawatirkan, segera konsultasikan kepada
            tenaga kesehatan.
          </div>

        </div>

      </div>
    </section>


    <!-- ================= FAQ ================= -->

    <section class="faq">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">FAQ</div>

          <h2 class="section-title">
            Pertanyaan yang Sering Diajukan
          </h2>

          <p class="section-description">
            Informasi singkat mengenai pendaftaran dan pelayanan.
          </p>
        </div>

        <div class="faq-container">

          <details class="reveal">
            <summary>Bagaimana cara melakukan pendaftaran?</summary>
            <p>
              Klik tombol "Daftar Sekarang" atau "Isi Formulir Pendaftaran",
              kemudian isi Google Form dengan data yang diminta dan kirim
              formulir tersebut.
            </p>
          </details>

          <details class="reveal">
            <summary>Apakah semua pasien dapat melakukan pendaftaran?</summary>
            <p>
              Ya. Pendaftaran dapat dilakukan oleh pasien dengan mengisi
              formulir sesuai data yang diperlukan.
            </p>
          </details>

          <details class="reveal">
            <summary>Apakah nomor BPJS wajib diisi?</summary>
            <p>
              Tidak. Nomor BPJS bersifat opsional dan dapat dikosongkan
              apabila pasien tidak memiliki atau tidak menggunakannya.
            </p>
          </details>

          <details class="reveal">
            <summary>Bagaimana cara mendapatkan nomor antrean?</summary>
            <p>
              Setelah formulir pendaftaran dikirim, nomor antrean akan
              segera diproses dan dikirim melalui WhatsApp ke nomor yang
              dicantumkan pada formulir.
            </p>
          </details>

          <details class="reveal">
            <summary>Bagaimana urutan antrean ditentukan?</summary>
            <p>
              Urutan antrean ditentukan berdasarkan urutan waktu pengiriman
              formulir. Pengirim terdahulu memperoleh urutan antrean lebih
              dahulu.
            </p>
          </details>

          <details class="reveal">
            <summary>Apa yang dilakukan setelah mendapatkan nomor antrean?</summary>
            <p>
              Pasien dapat datang ke tempat pelayanan sesuai dengan nomor
              antrean yang telah dikirimkan melalui WhatsApp.
            </p>
          </details>

        </div>

      </div>
    </section>


    <!-- ================= CONTACT ================= -->

    <section class="contact" id="kontak">
      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Hubungi Kami</div>

          <h2 class="section-title">
            Kontak Pelayanan
          </h2>

          <p class="section-description">
            Silakan hubungi kontak berikut untuk mendapatkan informasi
            lebih lanjut mengenai pelayanan kefarmasian.
          </p>
        </div>

        <div class="contact-wrapper">

          <div class="contact-card reveal">

            <div class="contact-item">

              <div class="contact-icon">📍</div>

              <div>
                <h4>Alamat</h4>
                <p>
                  Jl. Pangandaran No. 77, Kelurahan Antirogo,
                  Kecamatan Sumbersari, Kabupaten Jember
                </p>
              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">📱</div>

              <div>
                <h4>WhatsApp</h4>
                <a
                  href="https://wa.me/6285717420989"
                  target="_blank"
                  rel="noopener noreferrer">
                  085717420989
                </a>
              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">✉️</div>

              <div>
                <h4>Email</h4>
                <a href="mailto:tyaranovelia118@gmail.com">
                  tyaranovelia118@gmail.com
                </a>
              </div>

            </div>


            <div class="contact-actions">

              <a
                href="https://wa.me/6285717420989"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-primary">
                📱 WhatsApp
              </a>

              <a
                href="mailto:tyaranovelia118@gmail.com"
                class="btn btn-secondary">
                ✉️ Email
              </a>

            </div>

          </div>


          <div class="contact-card reveal">

            <h3 style="font-size:25px; margin-bottom:15px;">
              🏥 Pelayanan Kefarmasian
            </h3>

            <p style="color:var(--text-light); margin-bottom:20px;">
              Website ini dibuat untuk memberikan informasi mengenai
              pelayanan kefarmasian sekaligus memudahkan pasien dalam
              melakukan pendaftaran pelayanan.
            </p>

            <div style="
              background:var(--sage-light);
              padding:20px;
              border-radius:17px;
              margin-bottom:15px;">
              <strong>Jam Pelayanan</strong>
              <p style="color:var(--text-light); font-size:13px; margin-top:5px;">
                Silakan menghubungi kontak pelayanan untuk mendapatkan
                informasi mengenai jadwal pelayanan.
              </p>
            </div>

            <div style="
              background:#fff0f3;
              padding:20px;
              border-radius:17px;">
              <strong>📌 Perhatian</strong>
              <p style="color:var(--text-light); font-size:13px; margin-top:5px;">
                Pastikan nomor WhatsApp yang digunakan saat pendaftaran
                aktif agar nomor antrean dapat diterima.
              </p>
            </div>

          </div>

        </div>

      </div>
    </section>

  </main>


  <!-- ================= FOOTER ================= -->

  <footer>

    <div class="container">

      <div class="footer-grid">

        <div class="footer-brand">

          <h3>💊 PELAYANAN KEFARMASIAN</h3>

          <p>
            Mudah Mendaftar, Nyaman Mendapatkan Pelayanan.
            Website informasi dan pendaftaran pelayanan kefarmasian
            untuk membantu pasien mendapatkan pelayanan secara lebih
            mudah dan nyaman.
          </p>

        </div>


        <div>

          <h4>Navigasi</h4>

          <ul class="footer-links">

            <li><a href="#beranda">Beranda</a></li>
            <li><a href="#pengertian">Pengertian</a></li>
            <li><a href="#pendaftaran">Pendaftaran</a></li>
            <li><a href="#alur">Alur Pendaftaran</a></li>
            <li><a href="#resep">Pelayanan Resep</a></li>
            <li><a href="#konsultasi">Konsultasi</a></li>

          </ul>

        </div>


        <div>

          <h4>Kontak</h4>

          <div class="footer-contact">

            <p>📍 Jl. Pangandaran No. 77, Kelurahan Antirogo, Kecamatan Sumbersari, Kabupaten Jember</p>

            <br>

            <p>📱 085717420989</p>

            <p>✉️ tyaranovelia118@gmail.com</p>

          </div>

        </div>

      </div>


      <div class="copyright">
        © <span id="year"></span> PELAYANAN KEFARMASIAN. All Rights Reserved.
      </div>

    </div>

  </footer>


  <!-- BACK TO TOP -->

  <button id="backTop" title="Kembali ke atas">
    ↑
  </button>


  <!-- TOAST -->

  <div class="toast" id="toast">
    Membuka halaman...
  </div>


  <!-- ================= JAVASCRIPT ================= -->

  <script>

    /* ================= MOBILE MENU ================= */

    const hamburger = document.getElementById("hamburger");
    const navLinks = document.getElementById("navLinks");

    hamburger.addEventListener("click", function() {
      navLinks.classList.toggle("active");

      if (navLinks.classList.contains("active")) {
        hamburger.innerHTML = "✕";
      } else {
        hamburger.innerHTML = "☰";
      }
    });


    /* Close menu after clicking navigation */

    document.querySelectorAll(".nav-links a").forEach(function(link) {

      link.addEventListener("click", function() {

        navLinks.classList.remove("active");
        hamburger.innerHTML = "☰";

      });

    });


    /* ================= SCROLL REVEAL ================= */

    function revealElements() {

      const reveals = document.querySelectorAll(".reveal");

      reveals.forEach(function(element) {

        const windowHeight = window.innerHeight;
        const elementTop = element.getBoundingClientRect().top;

        if (elementTop < windowHeight - 80) {
          element.classList.add("active");
        }

      });

    }

    window.addEventListener("scroll", revealElements);
    window.addEventListener("load", revealElements);


    /* ================= BACK TO TOP ================= */

    const backTop = document.getElementById("backTop");

    window.addEventListener("scroll", function() {

      if (window.scrollY > 500) {
        backTop.style.display = "block";
      } else {
        backTop.style.display = "none";
      }

    });

    backTop.addEventListener("click", function() {

      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });

    });


    /* ================= TOAST NOTIFICATION ================= */

    function showToast(message) {

      const toast = document.getElementById("toast");

      toast.textContent = message;
      toast.classList.add("show");

      setTimeout(function() {
        toast.classList.remove("show");
      }, 2500);

    }


    /* ================= CURRENT YEAR ================= */

    document.getElementById("year").textContent =
      new Date().getFullYear();


    /* ================= SMOOTH ANCHOR ================= */

    document.querySelectorAll('a[href^="#"]').forEach(function(anchor) {

      anchor.addEventListener("click", function(e) {

        const target = document.querySelector(this.getAttribute("href"));

        if (target) {

          e.preventDefault();

          target.scrollIntoView({
            behavior: "smooth",
            block: "start"
          });

        }

      });

    });

  </script>

</body>
</html>
