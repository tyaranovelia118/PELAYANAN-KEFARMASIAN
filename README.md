
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
  <meta name="theme-color" content="#789781">
  <meta name="description" content="Website Pelayanan Kefarmasian Klinik Poltekes Jember">

  <title>Pelayanan Kefarmasian Klinik Poltekes Jember</title>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">

  <style>
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
      --shadow: 0 10px 35px rgba(74, 103, 83, 0.10);
      --radius: 22px;
      --max-width: 1180px;
    }

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

    img {
      max-width: 100%;
      display: block;
    }

    .container {
      width: min(92%, var(--max-width));
      margin: auto;
    }

    /* =========================
       LOADING
    ========================== */

    #loader {
      position: fixed;
      inset: 0;
      background: var(--white);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      transition: opacity .5s ease, visibility .5s ease;
    }

    #loader.hide {
      opacity: 0;
      visibility: hidden;
    }

    .loader-circle {
      width: 48px;
      height: 48px;
      border: 4px solid var(--sage-light);
      border-top-color: var(--sage-dark);
      border-radius: 50%;
      animation: spin 1s linear infinite;
    }

    @keyframes spin {
      to {
        transform: rotate(360deg);
      }
    }

    /* =========================
       NAVBAR
    ========================== */

    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      background: rgba(255,255,255,.94);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(120,151,129,.12);
      z-index: 1000;
    }

    .nav-inner {
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
    }

    .logo {
      display: flex;
      align-items: center;
      gap: 10px;
      font-weight: 700;
      font-size: 14px;
      color: var(--sage-dark);
      max-width: 245px;
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

    .nav-links {
      display: flex;
      align-items: center;
      gap: 4px;
    }

    .nav-links a {
      padding: 9px 11px;
      font-size: 13px;
      font-weight: 600;
      border-radius: 10px;
      color: var(--text);
      transition: .3s;
    }

    .nav-links a:hover {
      background: var(--sage-light);
      color: var(--sage-dark);
    }

    .nav-register {
      background: var(--sage-dark) !important;
      color: white !important;
      padding: 10px 16px !important;
    }

    .nav-register:hover {
      background: var(--pink-dark) !important;
    }

    .menu-btn {
      display: none;
      border: none;
      background: var(--sage-light);
      color: var(--sage-dark);
      width: 44px;
      height: 44px;
      border-radius: 12px;
      font-size: 23px;
      cursor: pointer;
    }

    /* =========================
       HERO
    ========================== */

    .hero {
      padding: 145px 0 80px;
      background:
        radial-gradient(circle at 90% 10%, rgba(232,183,195,.30), transparent 22%),
        linear-gradient(135deg, var(--sage-light), #fff 65%);
      position: relative;
      overflow: hidden;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      align-items: center;
      gap: 55px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      background: white;
      color: var(--sage-dark);
      padding: 8px 13px;
      border-radius: 30px;
      font-size: 12px;
      font-weight: 700;
      box-shadow: var(--shadow);
      margin-bottom: 20px;
    }

    .badge span {
      color: var(--pink-dark);
    }

    .hero h1 {
      font-family: "Playfair Display", serif;
      font-size: clamp(38px, 5vw, 65px);
      line-height: 1.12;
      margin-bottom: 20px;
      color: var(--text);
    }

    .hero h1 span {
      color: var(--sage-dark);
    }

    .hero-subtitle {
      font-size: clamp(18px, 2vw, 23px);
      font-weight: 600;
      color: var(--sage-dark);
      margin-bottom: 15px;
    }

    .hero-description {
      color: var(--text-light);
      max-width: 600px;
      margin-bottom: 30px;
      font-size: 16px;
    }

    .hero-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
    }

    .btn {
      min-height: 50px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 8px;
      padding: 13px 22px;
      border-radius: 14px;
      font-size: 14px;
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
      border-color: var(--sage);
      color: var(--sage-dark);
    }

    .btn-secondary:hover {
      background: var(--sage-light);
      transform: translateY(-3px);
    }

    /* Hero illustration */

    .hero-visual {
      position: relative;
      min-height: 400px;
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .visual-card {
      width: min(100%, 420px);
      height: 350px;
      background: white;
      border-radius: 35px;
      box-shadow: 0 25px 60px rgba(73,103,83,.15);
      position: relative;
      display: flex;
      align-items: center;
      justify-content: center;
      overflow: hidden;
    }

    .visual-card::before {
      content: "";
      position: absolute;
      width: 270px;
      height: 270px;
      background: var(--sage-light);
      border-radius: 50%;
      top: -80px;
      right: -60px;
    }

    .visual-card::after {
      content: "";
      position: absolute;
      width: 120px;
      height: 120px;
      background: rgba(232,183,195,.35);
      border-radius: 50%;
      bottom: -30px;
      left: -30px;
    }

    .pharmacy-illustration {
      position: relative;
      z-index: 2;
      text-align: center;
    }

    .pharmacy-icon {
      width: 150px;
      height: 150px;
      border-radius: 50%;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      font-size: 80px;
      margin: auto;
      box-shadow: inset 0 0 0 12px white;
    }

    .illustration-title {
      margin-top: 18px;
      font-weight: 700;
      color: var(--sage-dark);
    }

    .floating {
      position: absolute;
      background: white;
      box-shadow: var(--shadow);
      border-radius: 14px;
      padding: 11px 14px;
      font-size: 12px;
      font-weight: 700;
      z-index: 4;
    }

    .float-one {
      top: 40px;
      left: 0;
    }

    .float-two {
      bottom: 45px;
      right: 0;
    }

    /* =========================
       SECTION
    ========================== */

    section {
      padding: 85px 0;
    }

    .section-header {
      max-width: 700px;
      margin: 0 auto 45px;
      text-align: center;
    }

    .section-label {
      color: var(--sage-dark);
      font-size: 12px;
      font-weight: 800;
      text-transform: uppercase;
      letter-spacing: 2px;
      margin-bottom: 9px;
    }

    .section-header h2 {
      font-family: "Playfair Display", serif;
      font-size: clamp(30px, 4vw, 44px);
      line-height: 1.2;
      margin-bottom: 13px;
    }

    .section-header p {
      color: var(--text-light);
    }

    /* =========================
       ABOUT
    ========================== */

    .about {
      background: white;
    }

    .about-main {
      max-width: 900px;
      margin: auto;
      text-align: center;
      color: var(--text-light);
      font-size: 16px;
    }

    .about-main strong {
      color: var(--sage-dark);
    }

    .cards-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
      margin-top: 42px;
    }

    .card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 28px;
      box-shadow: var(--shadow);
      transition: .35s;
    }

    .card:hover {
      transform: translateY(-7px);
      box-shadow: 0 18px 40px rgba(74,103,83,.15);
    }

    .card-icon {
      width: 55px;
      height: 55px;
      display: grid;
      place-items: center;
      border-radius: 16px;
      background: var(--sage-light);
      font-size: 27px;
      margin-bottom: 18px;
    }

    .card:nth-child(3) .card-icon {
      background: #faedf0;
    }

    .card h3 {
      font-size: 18px;
      margin-bottom: 9px;
    }

    .card p {
      color: var(--text-light);
      font-size: 14px;
    }

    /* =========================
       REGISTRATION
    ========================== */

    .registration {
      background: var(--sage-light);
    }

    .register-box {
      background: var(--sage-dark);
      color: white;
      border-radius: 30px;
      padding: 50px;
      display: grid;
      grid-template-columns: 1fr .8fr;
      gap: 40px;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .register-box::after {
      content: "";
      position: absolute;
      width: 250px;
      height: 250px;
      border-radius: 50%;
      background: rgba(255,255,255,.07);
      right: -80px;
      top: -100px;
    }

    .register-box h2 {
      font-family: "Playfair Display", serif;
      font-size: 38px;
      margin-bottom: 12px;
    }

    .register-box p {
      opacity: .9;
      margin-bottom: 25px;
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
      background: rgba(255,255,255,.12);
      border: 1px solid rgba(255,255,255,.2);
      padding: 25px;
      border-radius: 20px;
      position: relative;
      z-index: 2;
    }

    .form-info h3 {
      margin-bottom: 15px;
    }

    .form-info ul {
      list-style: none;
    }

    .form-info li {
      margin: 10px 0;
      font-size: 14px;
    }

    /* Important */

    .important-box {
      margin-top: 25px;
      background: #fff8fa;
      border: 1px solid var(--pink);
      color: var(--text);
      border-radius: 18px;
      padding: 20px;
    }

    .important-box strong {
      color: var(--pink-dark);
    }

    /* =========================
       QUEUE
    ========================== */

    .queue {
      background: white;
    }

    .queue-flow {
      display: flex;
      align-items: stretch;
      justify-content: center;
      gap: 0;
      margin-top: 40px;
    }

    .queue-item {
      flex: 1;
      max-width: 210px;
      text-align: center;
      position: relative;
    }

    .queue-number {
      width: 55px;
      height: 55px;
      background: var(--sage);
      color: white;
      border-radius: 50%;
      display: grid;
      place-items: center;
      margin: 0 auto 14px;
      font-weight: 800;
    }

    .queue-item:not(:last-child)::after {
      content: "→";
      position: absolute;
      right: -15px;
      top: 13px;
      color: var(--sage-dark);
      font-size: 25px;
    }

    .queue-item h4 {
      font-size: 14px;
      margin-bottom: 5px;
    }

    .queue-item p {
      color: var(--text-light);
      font-size: 12px;
    }

    .queue-note {
      max-width: 750px;
      margin: 35px auto 0;
      padding: 17px 20px;
      background: var(--sage-light);
      border-radius: 14px;
      text-align: center;
      color: var(--sage-dark);
      font-size: 14px;
      font-weight: 600;
    }

    /* =========================
       REGISTRATION STEPS
    ========================== */

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
      border-radius: 20px;
      padding: 23px 17px;
      text-align: center;
      border: 1px solid var(--border);
      position: relative;
      transition: .3s;
    }

    .step:hover {
      transform: translateY(-5px);
    }

    .step-number {
      font-size: 25px;
      font-weight: 800;
      color: var(--sage-dark);
      margin-bottom: 8px;
    }

    .step h3 {
      font-size: 14px;
      margin-bottom: 8px;
    }

    .step p {
      font-size: 12px;
      color: var(--text-light);
    }

    /* =========================
       RECIPE
    ========================== */

    .recipe {
      background: white;
    }

    .recipe-flow {
      max-width: 850px;
      margin: auto;
    }

    .recipe-step {
      display: flex;
      gap: 20px;
      align-items: flex-start;
      padding: 22px;
      background: var(--sage-light);
      border-radius: 18px;
      margin-bottom: 12px;
      transition: .3s;
    }

    .recipe-step:hover {
      transform: translateX(5px);
    }

    .recipe-icon {
      width: 52px;
      height: 52px;
      flex-shrink: 0;
      display: grid;
      place-items: center;
      background: white;
      border-radius: 15px;
      font-size: 23px;
      box-shadow: var(--shadow);
    }

    .recipe-step h3 {
      font-size: 16px;
      margin-bottom: 4px;
    }

    .recipe-step p {
      font-size: 13px;
      color: var(--text-light);
    }

    .kie-list {
      display: flex;
      flex-wrap: wrap;
      gap: 7px;
      margin-top: 9px;
    }

    .kie-list span {
      background: white;
      border-radius: 20px;
      padding: 5px 10px;
      font-size: 11px;
      color: var(--sage-dark);
    }

    /* =========================
       CONSULTATION
    ========================== */

    .consultation {
      background: var(--sage-light);
    }

    .consult-grid {
      display: grid;
      grid-template-columns: .9fr 1.1fr;
      gap: 40px;
      align-items: center;
    }

    .consult-text p {
      color: var(--text-light);
      margin-bottom: 22px;
    }

    .consult-list {
      list-style: none;
      margin-bottom: 25px;
    }

    .consult-list li {
      padding: 8px 0;
      color: var(--text-light);
      font-size: 14px;
    }

    .consult-list li::before {
      content: "✓";
      color: var(--sage-dark);
      font-weight: 800;
      margin-right: 9px;
    }

    .chat {
      background: white;
      border-radius: 25px;
      padding: 30px;
      box-shadow: var(--shadow);
    }

    .chat-message {
      display: flex;
      gap: 12px;
      margin-bottom: 18px;
    }

    .chat-message.doctor {
      flex-direction: row-reverse;
    }

    .avatar {
      width: 45px;
      height: 45px;
      border-radius: 50%;
      background: var(--sage-light);
      display: grid;
      place-items: center;
      flex-shrink: 0;
      font-size: 21px;
    }

    .doctor .avatar {
      background: #faedf0;
    }

    .bubble {
      max-width: 75%;
      padding: 14px 17px;
      background: var(--sage-light);
      border-radius: 16px 16px 16px 3px;
      font-size: 13px;
    }

    .doctor .bubble {
      background: #faedf0;
      border-radius: 16px 16px 3px 16px;
    }

    .bubble strong {
      display: block;
      margin-bottom: 4px;
      font-size: 12px;
    }

    /* =========================
       SERVICES
    ========================== */

    .services {
      background: white;
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .service-card {
      padding: 27px 20px;
      border-radius: 20px;
      background: var(--sage-light);
      transition: .3s;
      border: 1px solid transparent;
    }

    .service-card:hover {
      transform: translateY(-6px);
      border-color: var(--sage);
      background: white;
      box-shadow: var(--shadow);
    }

    .service-icon {
      font-size: 32px;
      margin-bottom: 12px;
    }

    .service-card h3 {
      font-size: 16px;
      margin-bottom: 7px;
    }

    .service-card p {
      font-size: 13px;
      color: var(--text-light);
    }

    /* =========================
       SWAMEDIKASI
    ========================== */

    .selfmed {
      background: var(--sage-light);
    }

    .selfmed-box {
      max-width: 900px;
      margin: auto;
      background: white;
      padding: 35px;
      border-radius: 25px;
      box-shadow: var(--shadow);
    }

    .selfmed-box p {
      color: var(--text-light);
      margin-bottom: 20px;
    }

    .warning {
      padding: 17px;
      background: #fff8fa;
      border-left: 4px solid var(--pink-dark);
      border-radius: 10px;
      font-size: 13px;
    }

    /* =========================
       CONTACT
    ========================== */

    .contact {
      background: white;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 30px;
    }

    .contact-card {
      background: var(--sage-light);
      padding: 32px;
      border-radius: 25px;
    }

    .contact-item {
      display: flex;
      gap: 15px;
      padding: 16px 0;
      border-bottom: 1px solid var(--border);
    }

    .contact-item:last-child {
      border-bottom: none;
    }

    .contact-icon {
      width: 44px;
      height: 44px;
      flex-shrink: 0;
      display: grid;
      place-items: center;
      border-radius: 13px;
      background: white;
      font-size: 20px;
    }

    .contact-item h4 {
      font-size: 14px;
      margin-bottom: 2px;
    }

    .contact-item p,
    .contact-item a {
      color: var(--text-light);
      font-size: 13px;
      word-break: break-word;
    }

    .map {
      width: 100%;
      min-height: 100%;
      border: 0;
      border-radius: 25px;
    }

    /* =========================
       FAQ
    ========================== */

    .faq {
      background: var(--sage-light);
    }

    .faq-container {
      max-width: 850px;
      margin: auto;
    }

    details {
      background: white;
      border-radius: 16px;
      margin-bottom: 11px;
      border: 1px solid var(--border);
      overflow: hidden;
    }

    summary {
      cursor: pointer;
      padding: 18px 20px;
      font-weight: 700;
      font-size: 14px;
      list-style: none;
      position: relative;
      padding-right: 50px;
    }

    summary::-webkit-details-marker {
      display: none;
    }

    summary::after {
      content: "+";
      position: absolute;
      right: 20px;
      font-size: 22px;
      color: var(--sage-dark);
      transition: .3s;
    }

    details[open] summary::after {
      content: "−";
    }

    details p {
      padding: 0 20px 20px;
      color: var(--text-light);
      font-size: 13px;
    }

    /* =========================
       FOOTER
    ========================== */

    footer {
      background: #304138;
      color: white;
      padding: 55px 0 25px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1.2fr 1fr 1fr;
      gap: 40px;
      margin-bottom: 40px;
    }

    footer h3 {
      margin-bottom: 12px;
    }

    footer p,
    footer a {
      color: rgba(255,255,255,.72);
      font-size: 13px;
    }

    footer a:hover {
      color: var(--pink);
    }

    .footer-links {
      display: grid;
      gap: 7px;
    }

    .copyright {
      padding-top: 22px;
      border-top: 1px solid rgba(255,255,255,.12);
      text-align: center;
      font-size: 12px;
      color: rgba(255,255,255,.55);
    }

    /* =========================
       BACK TO TOP
    ========================== */

    #backTop {
      position: fixed;
      right: 20px;
      bottom: 20px;
      width: 45px;
      height: 45px;
      border: none;
      border-radius: 50%;
      background: var(--sage-dark);
      color: white;
      font-size: 20px;
      cursor: pointer;
      opacity: 0;
      visibility: hidden;
      transition: .3s;
      z-index: 900;
      box-shadow: var(--shadow);
    }

    #backTop.show {
      opacity: 1;
      visibility: visible;
    }

    /* =========================
       TOAST
    ========================== */

    #toast {
      position: fixed;
      left: 50%;
      bottom: 25px;
      transform: translate(-50%, 100px);
      background: #304138;
      color: white;
      padding: 13px 20px;
      border-radius: 12px;
      font-size: 13px;
      z-index: 3000;
      opacity: 0;
      transition: .35s;
      text-align: center;
      max-width: 90%;
    }

    #toast.show {
      transform: translate(-50%, 0);
      opacity: 1;
    }

    /* =========================
       SCROLL ANIMATION
    ========================== */

    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: .7s ease;
    }

    .reveal.active {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================
       TABLET
    ========================== */

    @media (max-width: 1000px) {
      .nav-links a {
        padding: 8px 7px;
        font-size: 12px;
      }

      .timeline {
        grid-template-columns: repeat(3, 1fr);
      }

      .service-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .hero-grid {
        gap: 30px;
      }
    }

    /* =========================
       MOBILE
    ========================== */

    @media (max-width: 760px) {

      body {
        font-size: 14px;
      }

      .container {
        width: min(92%, 600px);
      }

      section {
        padding: 65px 0;
      }

      /* Navbar */

      .nav-inner {
        min-height: 64px;
      }

      .logo {
        font-size: 12px;
        max-width: 220px;
      }

      .logo-icon {
        width: 36px;
        height: 36px;
        font-size: 18px;
      }

      .menu-btn {
        display: grid;
        place-items: center;
      }

      .nav-links {
        position: absolute;
        top: 64px;
        left: 0;
        width: 100%;
        background: white;
        padding: 12px 4%;
        display: none;
        flex-direction: column;
        align-items: stretch;
        box-shadow: 0 15px 30px rgba(0,0,0,.08);
        border-top: 1px solid var(--border);
      }

      .nav-links.open {
        display: flex;
      }

      .nav-links a {
        padding: 13px 14px;
        font-size: 14px;
      }

      .nav-register {
        text-align: center;
        margin-top: 5px;
      }

      /* Hero */

      .hero {
        padding: 105px 0 55px;
      }

      .hero-grid {
        grid-template-columns: 1fr;
        gap: 35px;
      }

      .hero h1 {
        font-size: 39px;
      }

      .hero-subtitle {
        font-size: 18px;
      }

      .hero-description {
        font-size: 14px;
      }

      .hero-buttons {
        flex-direction: column;
      }

      .hero-buttons .btn {
        width: 100%;
      }

      .hero-visual {
        min-height: 310px;
      }

      .visual-card {
        height: 285px;
      }

      .pharmacy-icon {
        width: 120px;
        height: 120px;
        font-size: 62px;
      }

      .float-one {
        left: 0;
        top: 20px;
      }

      .float-two {
        right: 0;
        bottom: 20px;
      }

      /* Header */

      .section-header {
        margin-bottom: 32px;
      }

      .section-header h2 {
        font-size: 30px;
      }

      .section-header p {
        font-size: 14px;
      }

      /* Cards */

      .cards-grid {
        grid-template-columns: 1fr;
        gap: 15px;
      }

      .card {
        padding: 23px;
      }

      /* Registration */

      .register-box {
        grid-template-columns: 1fr;
        padding: 30px 22px;
        border-radius: 24px;
        gap: 25px;
      }

      .register-box h2 {
        font-size: 30px;
      }

      .register-button {
        width: 100%;
      }

      /* Queue */

      .queue-flow {
        display: flex;
        flex-direction: column;
        gap: 0;
        align-items: stretch;
      }

      .queue-item {
        max-width: none;
        display: grid;
        grid-template-columns: 55px 1fr;
        column-gap: 15px;
        text-align: left;
        min-height: 80px;
      }

      .queue-number {
        margin: 0;
        grid-row: span 2;
      }

      .queue-item:not(:last-child)::after {
        content: "↓";
        right: auto;
        left: 18px;
        top: 55px;
        font-size: 20px;
      }

      .queue-item h4 {
        align-self: end;
      }

      .queue-item p {
        align-self: start;
      }

      .queue-note {
        font-size: 13px;
        text-align: left;
      }

      /* Timeline */

      .timeline {
        grid-template-columns: 1fr;
        gap: 12px;
      }

      .step {
        display: grid;
        grid-template-columns: 55px 1fr;
        column-gap: 14px;
        text-align: left;
        align-items: center;
      }

      .step-number {
        grid-row: span 2;
        margin: 0;
        font-size: 22px;
      }

      .step h3 {
        margin: 0;
      }

      /* Recipe */

      .recipe-step {
        padding: 18px;
        gap: 14px;
      }

      .recipe-icon {
        width: 45px;
        height: 45px;
        font-size: 20px;
      }

      .recipe-step h3 {
        font-size: 14px;
      }

      .recipe-step p {
        font-size: 12px;
      }

      /* Consultation */

      .consult-grid {
        grid-template-columns: 1fr;
        gap: 25px;
      }

      .chat {
        padding: 20px;
      }

      .bubble {
        max-width: 80%;
        font-size: 12px;
      }

      /* Services */

      .service-grid {
        grid-template-columns: 1fr;
      }

      /* Selfmed */

      .selfmed-box {
        padding: 23px;
      }

      /* Contact */

      .contact-grid {
        grid-template-columns: 1fr;
      }

      .map {
        min-height: 300px;
      }

      /* Footer */

      .footer-grid {
        grid-template-columns: 1fr;
        gap: 28px;
      }

      footer {
        padding: 45px 0 22px;
      }

      /* Buttons */

      .btn {
        min-height: 52px;
        font-size: 13px;
      }

      #backTop {
        right: 15px;
        bottom: 15px;
      }
    }

    /* Small phones */

    @media (max-width: 380px) {
      .hero h1 {
        font-size: 34px;
      }

      .logo {
        font-size: 11px;
      }

      .hero {
        padding-top: 95px;
      }

      .register-box h2 {
        font-size: 27px;
      }

      .card {
        padding: 20px;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       LOADING
  ========================== -->

  <div id="loader">
    <div class="loader-circle"></div>
  </div>


  <!-- =========================
       NAVBAR
  ========================== -->

  <header class="navbar">
    <div class="container nav-inner">

      <a href="#beranda" class="logo">
        <div class="logo-icon">💊</div>
        <span>PELAYANAN KEFARMASIAN<br>KLINIK POLTEKES JEMBER</span>
      </a>

      <button class="menu-btn" id="menuBtn" aria-label="Buka menu">
        ☰
      </button>

      <nav class="nav-links" id="navLinks">
        <a href="#beranda">🏠 Beranda</a>
        <a href="#pengertian">📖 Pengertian</a>
        <a href="#pendaftaran">📝 Pendaftaran</a>
        <a href="#alur">🔄 Alur</a>
        <a href="#resep">💊 Resep</a>
        <a href="#konsultasi">💬 Konsultasi</a>
        <a href="#swamedikasi">🌿 Swamedikasi</a>
        <a href="#kontak">📞 Kontak</a>

        <a
          href="https://forms.gle/jG8p9wozy5nmoMrS8"
          target="_blank"
          rel="noopener noreferrer"
          class="nav-register"
          onclick="showToast('Membuka formulir pendaftaran...')"
        >
          Daftar Sekarang
        </a>
      </nav>

    </div>
  </header>


  <main>

    <!-- =========================
         HERO
    ========================== -->

    <section class="hero" id="beranda">

      <div class="container hero-grid">

        <div class="hero-content reveal">

          <div class="badge">
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
            pelayanan serta memudahkan pasien melakukan pendaftaran secara online.
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

            <a href="#pelayanan" class="btn btn-secondary">
              💊 Lihat Pelayanan
            </a>

          </div>

        </div>


        <div class="hero-visual reveal">

          <div class="floating float-one">
            🩺 Pelayanan Pasien
          </div>

          <div class="visual-card">

            <div class="pharmacy-illustration">

              <div class="pharmacy-icon">
                👩‍⚕️
              </div>

              <div class="illustration-title">
                Pelayanan Kefarmasian
              </div>

              <small>
                Informasi • Konsultasi • Pelayanan
              </small>

            </div>

          </div>

          <div class="floating float-two">
            💊 Obat & KIE
          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         PENGERTIAN
    ========================== -->

    <section class="about" id="pengertian">

      <div class="container">

        <div class="section-header reveal">
          <div class="section-label">Tentang Pelayanan</div>

          <h2>
            Apa Itu Pelayanan Kefarmasian?
          </h2>

          <p>
            Pelayanan yang berorientasi pada kebutuhan pasien
            dan penggunaan obat yang tepat.
          </p>
        </div>

        <div class="about-main reveal">

          <p>
            Pelayanan kefarmasian merupakan pelayanan yang diberikan
            oleh tenaga kefarmasian kepada pasien yang berkaitan dengan
            penggunaan obat dan pelayanan kesehatan untuk membantu memastikan
            obat digunakan secara <strong>tepat, aman, dan efektif.</strong>
          </p>

          <br>

          <p>
            Pelayanan kefarmasian tidak hanya berfokus pada obat,
            tetapi juga memperhatikan kebutuhan dan kondisi pasien.
            Pasien dapat memperoleh informasi, konsultasi, serta
            pelayanan yang berkaitan dengan penggunaan obat.
          </p>

        </div>


        <div class="cards-grid">

          <div class="card reveal">

            <div class="card-icon">💊</div>

            <h3>Pengelolaan Obat</h3>

            <p>
              Pengelolaan obat dilakukan untuk memastikan ketersediaan,
              penyimpanan, dan penggunaan obat secara tepat.
            </p>

          </div>


          <div class="card reveal">

            <div class="card-icon">🩺</div>

            <h3>Pelayanan kepada Pasien</h3>

            <p>
              Pelayanan diberikan dengan memperhatikan kebutuhan pasien
              dan memberikan informasi yang sesuai.
            </p>

          </div>


          <div class="card reveal">

            <div class="card-icon">💬</div>

            <h3>Informasi dan Konsultasi</h3>

            <p>
              Pasien dapat memperoleh informasi mengenai penggunaan obat
              dan berkonsultasi dengan apoteker.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         PENDAFTARAN
    ========================== -->

    <section class="registration" id="pendaftaran">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Pendaftaran Pasien</div>

          <h2>Pendaftaran Pelayanan</h2>

          <p>
            Daftar terlebih dahulu sebelum mendapatkan pelayanan.
          </p>

        </div>


        <div class="register-box reveal">

          <div>

            <h2>
              Mulai Pendaftaran Anda
            </h2>

            <p>
              Silakan melakukan pendaftaran terlebih dahulu sebelum
              mendapatkan pelayanan. Isi formulir dengan data yang benar
              agar proses pelayanan dapat berjalan dengan baik.
            </p>

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

            <h3>📋 Data yang Dibutuhkan</h3>

            <ul>
              <li>✓ Nama Pasien — <strong>Wajib</strong></li>

              <li>
                ✓ Nomor BPJS — <strong>Opsional</strong>
                <br>
                <small>Diisi jika pasien memiliki BPJS.</small>
              </li>

              <li>✓ Keluhan atau kebutuhan pelayanan</li>

              <li>✓ Nomor WhatsApp — <strong>Wajib</strong></li>
            </ul>

          </div>

        </div>


        <div class="important-box reveal">

          <strong>⚠️ PENTING</strong>

          <p>
            Setelah mengisi formulir, nomor antrean akan segera
            dikirimkan melalui WhatsApp ke nomor yang telah dicantumkan
            pada formulir.
          </p>

          <br>

          <p>
            <strong>
              Nomor antrean diberikan berdasarkan urutan pengiriman formulir.
            </strong>
            Pasien yang mengirimkan formulir terlebih dahulu akan mendapatkan
            urutan antrean terlebih dahulu.
          </p>

        </div>

      </div>

    </section>


    <!-- =========================
         INFORMASI ANTREAN
    ========================== -->

    <section class="queue" id="antrean">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Informasi Antrean</div>

          <h2>Bagaimana Mendapatkan Nomor Antrean?</h2>

          <p>
            Ikuti proses berikut setelah mengisi formulir pendaftaran.
          </p>

        </div>


        <div class="queue-flow reveal">

          <div class="queue-item">

            <div class="queue-number">01</div>

            <h4>Isi Google Form</h4>

            <p>Lengkapi data pendaftaran.</p>

          </div>


          <div class="queue-item">

            <div class="queue-number">02</div>

            <h4>Data Diterima</h4>

            <p>Data pendaftaran diterima.</p>

          </div>


          <div class="queue-item">

            <div class="queue-number">03</div>

            <h4>Antrean Diproses</h4>

            <p>Nomor antrean diproses.</p>

          </div>


          <div class="queue-item">

            <div class="queue-number">04</div>

            <h4>WhatsApp</h4>

            <p>Nomor antrean dikirim.</p>

          </div>


          <div class="queue-item">

            <div class="queue-number">05</div>

            <h4>Datang</h4>

            <p>Datang sesuai antrean.</p>

          </div>

        </div>


        <div class="queue-note reveal">

          📱 Mohon pastikan nomor WhatsApp yang dicantumkan aktif
          dan dapat menerima pesan.

          <br><br>

          Urutan antrean mengikuti waktu pengiriman formulir pendaftaran.

        </div>

      </div>

    </section>


    <!-- =========================
         ALUR PENDAFTARAN
    ========================== -->

    <section class="steps" id="alur">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Panduan Pendaftaran</div>

          <h2>Alur Pendaftaran Pelayanan</h2>

          <p>
            Ikuti enam langkah sederhana berikut.
          </p>

        </div>


        <div class="timeline">

          <div class="step reveal">
            <div class="step-number">01</div>
            <h3>Buka Website</h3>
            <p>Pasien membuka website Pelayanan Kefarmasian.</p>
          </div>


          <div class="step reveal">
            <div class="step-number">02</div>
            <h3>Pilih Pendaftaran</h3>
            <p>Pasien menekan tombol Daftar Sekarang.</p>
          </div>


          <div class="step reveal">
            <div class="step-number">03</div>
            <h3>Isi Google Form</h3>
            <p>Isi nama, BPJS jika ada, keluhan dan WhatsApp.</p>
          </div>


          <div class="step reveal">
            <div class="step-number">04</div>
            <h3>Kirim Formulir</h3>
            <p>Pastikan seluruh data sudah benar.</p>
          </div>


          <div class="step reveal">
            <div class="step-number">05</div>
            <h3>Dapat Nomor Antrean</h3>
            <p>Nomor antrean dikirim melalui WhatsApp.</p>
          </div>


          <div class="step reveal">
            <div class="step-number">06</div>
            <h3>Datang ke Pelayanan</h3>
            <p>Datang dan menunggu sesuai antrean.</p>
          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         PELAYANAN RESEP
    ========================== -->

    <section class="recipe" id="resep">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Pelayanan Resep</div>

          <h2>Alur Pelayanan Resep</h2>

          <p>
            Pelayanan resep dilakukan melalui beberapa tahapan
            untuk membantu memastikan obat diberikan dengan tepat.
          </p>

        </div>


        <div class="recipe-flow">

          <div class="recipe-step reveal">

            <div class="recipe-icon">📄</div>

            <div>

              <h3>1. Penerimaan Resep</h3>

              <p>
                Pasien menyerahkan resep kepada petugas/apoteker.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">🔎</div>

            <div>

              <h3>2. Pemeriksaan Resep</h3>

              <p>
                Resep diperiksa meliputi kelengkapan dan kesesuaian resep.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">💊</div>

            <div>

              <h3>3. Penyiapan Obat</h3>

              <p>
                Obat disiapkan sesuai resep.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">✓</div>

            <div>

              <h3>4. Pemeriksaan Kembali</h3>

              <p>
                Dilakukan pemeriksaan kembali terhadap obat
                yang telah disiapkan.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">🤝</div>

            <div>

              <h3>5. Penyerahan Obat</h3>

              <p>
                Obat diserahkan kepada pasien.
              </p>

            </div>

          </div>


          <div class="recipe-step reveal">

            <div class="recipe-icon">💬</div>

            <div>

              <h3>6. Pemberian KIE</h3>

              <p>
                Pasien mendapatkan informasi mengenai penggunaan obat.
              </p>

              <div class="kie-list">

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

            <div class="recipe-icon">🌿</div>

            <div>

              <h3>7. Pelayanan Selesai</h3>

              <p>
                Pasien telah memperoleh obat dan informasi yang diperlukan.
              </p>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         KONSULTASI
    ========================== -->

    <section class="consultation" id="konsultasi">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Konsultasi Kefarmasian</div>

          <h2>Konsultasi dengan Apoteker</h2>

          <p>
            Sampaikan pertanyaan atau permasalahan Anda mengenai
            penggunaan obat.
          </p>

        </div>


        <div class="consult-grid">

          <div class="consult-text reveal">

            <p>
              Konsultasi kefarmasian merupakan kesempatan bagi pasien
              untuk menyampaikan pertanyaan atau permasalahan terkait
              penggunaan obat kepada apoteker.
            </p>

            <ul class="consult-list">

              <li>Cara penggunaan obat</li>
              <li>Aturan pakai</li>
              <li>Waktu penggunaan obat</li>
              <li>Efek samping</li>
              <li>Interaksi obat</li>
              <li>Penyimpanan obat</li>
              <li>Penggunaan beberapa obat secara bersamaan</li>
              <li>Permasalahan terkait penggunaan obat</li>

            </ul>

            <!--
              NOMOR WHATSAPP KONSULTASI
              Silakan ganti nomor di bawah apabila sudah memiliki
              nomor WhatsApp khusus apoteker.
            -->

            <a
              href="https://wa.me/62331325930"
              target="_blank"
              rel="noopener noreferrer"
              class="btn btn-primary"
            >
              💬 Konsultasi dengan Apoteker
            </a>

          </div>


          <div class="chat reveal">

            <div class="chat-message">

              <div class="avatar">👤</div>

              <div class="bubble">

                <strong>Pasien</strong>

                “Saya ingin berkonsultasi mengenai obat
                yang sedang saya gunakan.”

              </div>

            </div>


            <div class="chat-message doctor">

              <div class="avatar">👩‍⚕️</div>

              <div class="bubble">

                <strong>Apoteker</strong>

                “Silakan sampaikan nama obat, aturan penggunaan,
                serta keluhan atau pertanyaan yang ingin dikonsultasikan.”

              </div>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         INFORMASI PELAYANAN
    ========================== -->

    <section class="services" id="pelayanan">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Layanan</div>

          <h2>Informasi Pelayanan</h2>

          <p>
            Berbagai pelayanan yang dapat diperoleh pasien.
          </p>

        </div>


        <div class="service-grid">

          <div class="service-card reveal">

            <div class="service-icon">💊</div>

            <h3>Pelayanan Resep</h3>

            <p>
              Pelayanan obat berdasarkan resep disertai informasi
              penggunaan obat.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">🌿</div>

            <h3>Swamedikasi</h3>

            <p>
              Membantu pasien memperoleh informasi dalam penggunaan
              obat untuk keluhan ringan.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">💬</div>

            <h3>Konsultasi Kefarmasian</h3>

            <p>
              Konsultasi pasien bersama apoteker mengenai penggunaan obat.
            </p>

          </div>


          <div class="service-card reveal">

            <div class="service-icon">🩺</div>

            <h3>Konseling</h3>

            <p>
              Pemberian informasi secara langsung agar pasien memahami
              penggunaan obat.
            </p>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         SWAMEDIKASI
    ========================== -->

    <section class="selfmed" id="swamedikasi">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Swamedikasi</div>

          <h2>Pelayanan Swamedikasi</h2>

          <p>
            Informasi dan bantuan dalam penggunaan obat untuk
            keluhan ringan.
          </p>

        </div>


        <div class="selfmed-box reveal">

          <p>
            Swamedikasi merupakan upaya penggunaan obat oleh masyarakat
            untuk mengatasi keluhan atau gangguan kesehatan ringan.
            Dalam pelayanan kefarmasian, pasien dapat memperoleh informasi
            mengenai pilihan obat, aturan penggunaan, serta hal-hal yang
            perlu diperhatikan.
          </p>

          <p>
            Konsultasikan kondisi Anda kepada tenaga kefarmasian apabila
            memiliki pertanyaan mengenai obat yang akan digunakan,
            terutama apabila menggunakan beberapa obat secara bersamaan.
          </p>

          <div class="warning">

            ⚠️ <strong>Perhatian:</strong>
            Apabila keluhan tidak membaik, semakin berat, atau muncul
            kondisi yang mengkhawatirkan, pasien disarankan memperoleh
            pemeriksaan dan pelayanan kesehatan lebih lanjut.

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         KONTAK
    ========================== -->

    <section class="contact" id="kontak">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">Kontak</div>

          <h2>Hubungi Kami</h2>

          <p>
            Informasi lokasi dan kontak pelayanan kefarmasian.
          </p>

        </div>


        <div class="contact-grid">

          <div class="contact-card reveal">

            <div class="contact-item">

              <div class="contact-icon">📍</div>

              <div>

                <h4>Alamat</h4>

                <p>
                  Jl. Pangandaran No.42, Plinggan, Antirogo,
                  Kec. Sumbersari, Kabupaten Jember,
                  Jawa Timur 68125
                </p>

              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">📱</div>

              <div>

                <h4>WhatsApp / Telepon</h4>

                <a href="tel:+62331325930">
                  (0331) 325930
                </a>

              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">🌐</div>

              <div>

                <h4>Website Poltekes Jember</h4>

                <a
                  href="https://poltekesjember.ac.id/"
                  target="_blank"
                  rel="noopener noreferrer"
                >
                  poltekesjember.ac.id
                </a>

              </div>

            </div>


            <div style="margin-top:20px; display:flex; gap:10px; flex-wrap:wrap;">

              <a
                href="https://wa.me/62331325930"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-primary"
              >
                💬 Hubungi via WhatsApp
              </a>

              <a
                href="mailto:"
                class="btn btn-secondary"
              >
                ✉️ Kirim Email
              </a>

            </div>

          </div>


          <div class="reveal">

            <iframe
              class="map"
              src="https://www.google.com/maps?q=Poltekkes%20Kemenkes%20Malang%20Kampus%20Jember&output=embed"
              loading="lazy"
              allowfullscreen=""
              referrerpolicy="no-referrer-when-downgrade">
            </iframe>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         FAQ
    ========================== -->

    <section class="faq" id="faq">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">FAQ</div>

          <h2>Pertanyaan yang Sering Ditanyakan</h2>

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
              Nomor antrean akan segera dikirimkan melalui WhatsApp
              ke nomor yang dicantumkan pada formulir.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Bagaimana urutan antreannya?
            </summary>

            <p>
              Urutan antrean mengikuti urutan waktu pengiriman formulir.
              Pasien yang mengirimkan formulir terlebih dahulu mendapatkan
              urutan terlebih dahulu.
            </p>

          </details>


          <details class="reveal">

            <summary>
              Apa yang harus dilakukan setelah mendapatkan nomor antrean?
            </summary>

            <p>
              Pasien datang ke tempat pelayanan sesuai nomor antrean
              yang telah diberikan.
            </p>

          </details>

        </div>

      </div>

    </section>

  </main>


  <!-- =========================
       FOOTER
  ========================== -->

  <footer>

    <div class="container">

      <div class="footer-grid">

        <div>

          <h3>💊 PELAYANAN KEFARMASIAN</h3>

          <p>
            Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
          </p>

          <br>

          <p>
            Website informasi dan pendaftaran pelayanan kefarmasian
            Klinik Poltekes Jember.
          </p>

        </div>


        <div>

          <h3>Navigasi</h3>

          <div class="footer-links">

            <a href="#beranda">Beranda</a>
            <a href="#pengertian">Pengertian</a>
            <a href="#pendaftaran">Pendaftaran</a>
            <a href="#alur">Alur Pendaftaran</a>
            <a href="#resep">Pelayanan Resep</a>
            <a href="#konsultasi">Konsultasi</a>

          </div>

        </div>


        <div>

          <h3>Hubungi Kami</h3>

          <p>
            📍 Jl. Pangandaran No.42, Plinggan, Antirogo,
            Kec. Sumbersari, Kabupaten Jember,
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


  <!-- BACK TO TOP -->

  <button id="backTop" aria-label="Kembali ke atas">
    ↑
  </button>


  <!-- TOAST -->

  <div id="toast"></div>


  <!-- =========================
       JAVASCRIPT
  ========================== -->

  <script>

    /* =========================================
       GOOGLE FORM
       
       Jika ingin mengganti Google Form,
       cukup ubah URL di seluruh atribut href
       yang menggunakan URL berikut:

       https://forms.gle/jG8p9wozy5nmoMrS8
    ========================================== */


    /* Loader */

    window.addEventListener("load", function() {

      setTimeout(function() {

        document.getElementById("loader")
          .classList.add("hide");

      }, 500);

    });


    /* Mobile Menu */

    const menuBtn = document.getElementById("menuBtn");
    const navLinks = document.getElementById("navLinks");

    menuBtn.addEventListener("click", function() {

      navLinks.classList.toggle("open");

      if (navLinks.classList.contains("open")) {

        menuBtn.innerHTML = "✕";

      } else {

        menuBtn.innerHTML = "☰";

      }

    });


    /* Tutup menu ketika link diklik */

    document.querySelectorAll(".nav-links a").forEach(function(link) {

      link.addEventListener("click", function() {

        navLinks.classList.remove("open");
        menuBtn.innerHTML = "☰";

      });

    });


    /* Toast Notification */

    function showToast(message) {

      const toast = document.getElementById("toast");

      toast.textContent = message;
      toast.classList.add("show");

      setTimeout(function() {

        toast.classList.remove("show");

      }, 2500);

    }


    /* Back To Top */

    const backTop = document.getElementById("backTop");

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


    /* Scroll Reveal */

    const observer = new IntersectionObserver(

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


    document.querySelectorAll(".reveal").forEach(function(element) {

      observer.observe(element);

    });


    /* Current Year */

    document.getElementById("year").textContent =
      new Date().getFullYear();


    /* Smooth Anchor */

    document.querySelectorAll('a[href^="#"]').forEach(function(anchor) {

      anchor.addEventListener("click", function(event) {

        const target = document.querySelector(
          this.getAttribute("href")
        );

        if (target) {

          event.preventDefault();

          target.scrollIntoView({
            behavior: "smooth"
          });

        }

      });

    });

  </script>

</body>
</html>
