
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="theme-color" content="#789781" />
  <meta
    name="description"
    content="Website Pelayanan Kefarmasian Klinik Poltekes Jember untuk informasi pelayanan dan pendaftaran pasien."
  />

  <title>Pelayanan Kefarmasian Klinik Poltekes Jember</title>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap"
    rel="stylesheet"
  />

  <!-- Font Awesome -->
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
  />

  <style>
    /* =========================================================
       PENGATURAN WARNA UTAMA
       ========================================================= */
    :root {
      --sage: #a8bfae;
      --sage-dark: #789781;
      --sage-light: #eff5f0;
      --sage-deep: #5f8068;

      --white: #ffffff;
      --pink: #e8b7c3;
      --pink-dark: #d38fa0;

      --text: #35443a;
      --text-soft: #68766d;
      --border: #dce7de;

      --shadow: 0 12px 35px rgba(71, 100, 78, 0.10);
      --shadow-hover: 0 18px 45px rgba(71, 100, 78, 0.16);

      --radius: 22px;
      --radius-small: 14px;

      --container: 1180px;
    }

    /* =========================================================
       RESET
       ========================================================= */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      scroll-padding-top: 85px;
    }

    body {
      font-family: "DM Sans", sans-serif;
      background: var(--white);
      color: var(--text);
      line-height: 1.7;
      overflow-x: hidden;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button,
    a {
      -webkit-tap-highlight-color: transparent;
    }

    button {
      font-family: inherit;
    }

    .container {
      width: min(100% - 32px, var(--container));
      margin-inline: auto;
    }

    section {
      padding: 75px 0;
    }

    /* =========================================================
       UTILITY
       ========================================================= */
    .section-label {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 7px 13px;
      background: var(--sage-light);
      color: var(--sage-dark);
      border-radius: 50px;
      font-size: 0.82rem;
      font-weight: 700;
      margin-bottom: 14px;
    }

    .section-title {
      font-family: "Playfair Display", serif;
      font-size: clamp(1.8rem, 5vw, 2.8rem);
      line-height: 1.2;
      margin-bottom: 16px;
      color: var(--text);
    }

    .section-description {
      max-width: 720px;
      color: var(--text-soft);
      font-size: 0.98rem;
    }

    .section-heading {
      margin-bottom: 38px;
    }

    .text-center {
      text-align: center;
    }

    .text-center .section-description {
      margin-inline: auto;
    }

    /* =========================================================
       BUTTON
       ========================================================= */
    .btn {
      min-height: 50px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      padding: 13px 20px;
      border-radius: 13px;
      border: 2px solid transparent;
      font-weight: 700;
      font-size: 0.93rem;
      cursor: pointer;
      transition: 0.3s ease;
      text-align: center;
    }

    .btn-primary {
      background: var(--sage-dark);
      color: white;
      box-shadow: 0 8px 20px rgba(120, 151, 129, 0.25);
    }

    .btn-primary:hover {
      background: var(--sage-deep);
      transform: translateY(-2px);
      box-shadow: 0 13px 27px rgba(120, 151, 129, 0.30);
    }

    .btn-secondary {
      background: white;
      color: var(--sage-dark);
      border-color: var(--sage);
    }

    .btn-secondary:hover {
      background: var(--sage-light);
      transform: translateY(-2px);
    }

    .btn-pink {
      background: var(--pink);
      color: var(--text);
    }

    .btn-pink:hover {
      background: var(--pink-dark);
      color: white;
      transform: translateY(-2px);
    }

    .btn-full {
      width: 100%;
    }

    /* =========================================================
       NAVBAR
       ========================================================= */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(255, 255, 255, 0.94);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(168, 191, 174, 0.35);
    }

    .nav-inner {
      min-height: 72px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 10px;
      min-width: 0;
    }

    .brand-icon {
      width: 42px;
      height: 42px;
      flex: 0 0 42px;
      display: grid;
      place-items: center;
      border-radius: 13px;
      background: var(--sage);
      color: white;
      font-size: 1.15rem;
    }

    .brand-text {
      line-height: 1.15;
    }

    .brand-name {
      font-weight: 800;
      font-size: 0.86rem;
      letter-spacing: 0.2px;
    }

    .brand-subtitle {
      color: var(--text-soft);
      font-size: 0.65rem;
    }

    .nav-menu {
      position: fixed;
      top: 72px;
      left: 0;
      width: 100%;
      background: white;
      padding: 18px 16px 24px;
      border-bottom: 1px solid var(--border);
      box-shadow: var(--shadow);
      transform: translateY(-130%);
      opacity: 0;
      pointer-events: none;
      transition: 0.3s ease;
    }

    .nav-menu.active {
      transform: translateY(0);
      opacity: 1;
      pointer-events: auto;
    }

    .nav-links {
      list-style: none;
      display: flex;
      flex-direction: column;
      gap: 5px;
    }

    .nav-link {
      display: block;
      padding: 11px 12px;
      border-radius: 10px;
      font-size: 0.9rem;
      font-weight: 600;
      color: var(--text);
      transition: 0.25s;
    }

    .nav-link:hover {
      background: var(--sage-light);
      color: var(--sage-dark);
    }

    .nav-register {
      width: 100%;
      margin-top: 13px;
    }

    .menu-toggle {
      width: 44px;
      height: 44px;
      border: 0;
      border-radius: 12px;
      background: var(--sage-light);
      color: var(--sage-dark);
      font-size: 1.1rem;
      cursor: pointer;
    }

    /* =========================================================
       HERO
       ========================================================= */
    .hero {
      min-height: 100svh;
      padding-top: 120px;
      padding-bottom: 65px;
      background:
        radial-gradient(circle at 85% 15%, rgba(232, 183, 195, 0.24), transparent 23%),
        linear-gradient(145deg, var(--sage-light), white 65%);
      display: flex;
      align-items: center;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 48px;
      align-items: center;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 8px 13px;
      background: white;
      color: var(--sage-dark);
      border: 1px solid var(--border);
      border-radius: 50px;
      font-size: 0.78rem;
      font-weight: 700;
      box-shadow: 0 5px 18px rgba(70, 90, 75, 0.06);
      margin-bottom: 18px;
    }

    .hero-title {
      font-family: "Playfair Display", serif;
      font-size: clamp(2.15rem, 9vw, 4.6rem);
      line-height: 1.08;
      letter-spacing: -1px;
      margin-bottom: 17px;
    }

    .hero-title span {
      color: var(--sage-dark);
    }

    .hero-tagline {
      font-size: clamp(1.1rem, 4vw, 1.45rem);
      font-weight: 700;
      margin-bottom: 13px;
    }

    .hero-description {
      color: var(--text-soft);
      max-width: 630px;
      font-size: 1rem;
      margin-bottom: 26px;
    }

    .hero-actions {
      display: flex;
      flex-direction: column;
      gap: 11px;
    }

    .hero-actions .btn {
      width: 100%;
    }

    /* Pharmacy illustration */
    .hero-visual {
      position: relative;
      min-height: 370px;
      display: grid;
      place-items: center;
    }

    .illustration {
      position: relative;
      width: min(100%, 430px);
      height: 350px;
    }

    .ill-circle {
      position: absolute;
      inset: 25px 15px 10px;
      border-radius: 50%;
      background: var(--sage);
      opacity: 0.34;
    }

    .ill-circle-small {
      position: absolute;
      width: 75px;
      height: 75px;
      top: 0;
      right: 10px;
      background: var(--pink);
      opacity: 0.65;
      border-radius: 50%;
    }

    .pharmacist {
      position: absolute;
      width: 125px;
      height: 170px;
      left: 23%;
      bottom: 28px;
      z-index: 2;
    }

    .person-head {
      position: absolute;
      width: 66px;
      height: 66px;
      left: 30px;
      top: 0;
      border-radius: 50%;
      background: #f4d5c8;
      border: 5px solid white;
      box-shadow: var(--shadow);
    }

    .person-hair {
      position: absolute;
      width: 67px;
      height: 30px;
      left: 30px;
      top: -3px;
      border-radius: 45px 45px 10px 10px;
      background: var(--text);
      z-index: 2;
    }

    .person-body {
      position: absolute;
      width: 125px;
      height: 108px;
      bottom: 0;
      border-radius: 45px 45px 15px 15px;
      background: white;
      border: 4px solid var(--sage-dark);
      box-shadow: var(--shadow);
    }

    .person-shirt {
      position: absolute;
      width: 70px;
      height: 85px;
      bottom: 0;
      left: 28px;
      background: var(--sage-light);
      border-radius: 20px 20px 0 0;
    }

    .cross {
      position: absolute;
      left: 50%;
      top: 27px;
      transform: translateX(-50%);
      color: var(--pink-dark);
      font-size: 1.6rem;
      z-index: 3;
    }

    .medicine-box {
      position: absolute;
      right: 10%;
      bottom: 55px;
      width: 120px;
      height: 90px;
      background: white;
      border: 3px solid var(--sage-dark);
      border-radius: 16px;
      transform: rotate(7deg);
      z-index: 3;
      box-shadow: var(--shadow);
    }

    .medicine-box::before {
      content: "";
      position: absolute;
      width: 100%;
      height: 22px;
      top: 20px;
      background: var(--sage);
    }

    .medicine-box::after {
      content: "+";
      position: absolute;
      right: 17px;
      top: 24px;
      font-size: 1.6rem;
      font-weight: 800;
      color: white;
    }

    .patient {
      position: absolute;
      right: 14%;
      bottom: 23px;
      width: 100px;
      height: 145px;
      z-index: 4;
    }

    .patient .person-head {
      width: 52px;
      height: 52px;
      left: 25px;
      border-width: 4px;
    }

    .patient .person-hair {
      width: 54px;
      height: 27px;
      left: 24px;
    }

    .patient .person-body {
      width: 100px;
      height: 88px;
      border: 0;
      background: var(--pink);
      border-radius: 40px 40px 12px 12px;
    }

    .tablet {
      position: absolute;
      top: 55px;
      left: 7%;
      width: 62px;
      height: 42px;
      background: white;
      border-radius: 12px;
      transform: rotate(-12deg);
      box-shadow: var(--shadow);
      border: 2px solid var(--sage);
      z-index: 5;
    }

    .tablet::after {
      content: "Rx";
      position: absolute;
      left: 50%;
      top: 50%;
      transform: translate(-50%, -50%);
      color: var(--sage-dark);
      font-weight: 800;
    }

    .floating-plus {
      position: absolute;
      color: var(--pink-dark);
      font-size: 1.5rem;
      animation: float 3s ease-in-out infinite;
    }

    .plus-one {
      top: 65px;
      right: 23%;
    }

    .plus-two {
      bottom: 90px;
      left: 4%;
      animation-delay: 0.8s;
    }

    @keyframes float {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-8px);
      }
    }

    /* =========================================================
       INFO CARDS
       ========================================================= */
    .cards-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 17px;
    }

    .card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 24px;
      box-shadow: var(--shadow);
      transition: 0.3s ease;
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-hover);
    }

    .icon-box {
      width: 50px;
      height: 50px;
      display: grid;
      place-items: center;
      background: var(--sage-light);
      color: var(--sage-dark);
      border-radius: 15px;
      font-size: 1.15rem;
      margin-bottom: 17px;
    }

    .icon-box.pink {
      background: #faedf0;
      color: var(--pink-dark);
    }

    .card h3 {
      font-size: 1.08rem;
      margin-bottom: 8px;
    }

    .card p {
      color: var(--text-soft);
      font-size: 0.91rem;
    }

    /* =========================================================
       PENGERTIAN
       ========================================================= */
    .definition-section {
      background: white;
    }

    /* =========================================================
       REGISTRATION
       ========================================================= */
    .registration-section {
      background: var(--sage-light);
      position: relative;
      overflow: hidden;
    }

    .registration-wrapper {
      display: grid;
      grid-template-columns: 1fr;
      gap: 25px;
    }

    .registration-card {
      background: white;
      border-radius: 28px;
      padding: 28px;
      box-shadow: var(--shadow);
      border: 1px solid var(--border);
    }

    .registration-card.highlight {
      background: var(--sage-dark);
      color: white;
    }

    .registration-card.highlight p {
      color: rgba(255,255,255,0.85);
    }

    .registration-card.highlight .icon-box {
      background: rgba(255,255,255,0.15);
      color: white;
    }

    .registration-card.highlight .btn {
      background: white;
      color: var(--sage-dark);
    }

    .registration-card.highlight .btn:hover {
      background: var(--pink);
      color: var(--text);
    }

    .big-register-btn {
      width: 100%;
      min-height: 60px;
      font-size: 1rem;
      margin-top: 20px;
    }

    .no-login {
      display: flex;
      gap: 10px;
      align-items: flex-start;
      margin-top: 16px;
      font-size: 0.82rem;
      color: var(--text-soft);
    }

    .no-login i {
      color: var(--sage-dark);
      margin-top: 4px;
    }

    /* =========================================================
       FORM INFO
       ========================================================= */
    .form-items {
      display: grid;
      grid-template-columns: 1fr;
      gap: 12px;
      margin-top: 20px;
    }

    .form-item {
      display: flex;
      gap: 13px;
      align-items: flex-start;
      padding: 15px;
      background: var(--sage-light);
      border-radius: 14px;
    }

    .form-item-icon {
      width: 34px;
      height: 34px;
      flex: 0 0 34px;
      display: grid;
      place-items: center;
      background: white;
      color: var(--sage-dark);
      border-radius: 10px;
      font-size: 0.82rem;
    }

    .form-item strong {
      display: block;
      margin-bottom: 2px;
      font-size: 0.9rem;
    }

    .form-item span {
      display: block;
      color: var(--text-soft);
      font-size: 0.78rem;
    }

    .required {
      color: var(--pink-dark);
      font-size: 0.72rem;
      font-weight: 700;
    }

    /* Important badge */
    .important-box {
      margin-top: 20px;
      padding: 19px;
      background: #fff8fa;
      border: 1px solid #f1d5dc;
      border-left: 5px solid var(--pink-dark);
      border-radius: 15px;
    }

    .important-box strong {
      display: block;
      color: var(--pink-dark);
      margin-bottom: 5px;
    }

    .important-box p {
      color: var(--text);
      font-size: 0.87rem;
    }

    /* =========================================================
       QUEUE
       ========================================================= */
    .queue-section {
      background: white;
    }

    .queue-list {
      max-width: 800px;
      margin: 0 auto;
      position: relative;
    }

    .queue-list::before {
      content: "";
      position: absolute;
      left: 22px;
      top: 25px;
      bottom: 25px;
      width: 2px;
      background: var(--sage);
    }

    .queue-step {
      position: relative;
      display: flex;
      gap: 17px;
      align-items: flex-start;
      padding: 10px 0 20px;
    }

    .queue-number {
      width: 46px;
      height: 46px;
      flex: 0 0 46px;
      display: grid;
      place-items: center;
      background: var(--sage-dark);
      color: white;
      border: 4px solid white;
      border-radius: 50%;
      z-index: 2;
      font-weight: 800;
      box-shadow: 0 0 0 2px var(--sage);
    }

    .queue-content {
      background: var(--sage-light);
      border-radius: 15px;
      padding: 13px 16px;
      flex: 1;
    }

    .queue-content h3 {
      font-size: 0.94rem;
      margin-bottom: 2px;
    }

    .queue-content p {
      color: var(--text-soft);
      font-size: 0.79rem;
    }

    .queue-note {
      margin-top: 20px;
      padding: 15px 18px;
      border-radius: 15px;
      background: #fff8fa;
      border: 1px solid #f0d7dd;
      color: var(--text);
      font-size: 0.86rem;
      text-align: center;
    }

    /* =========================================================
       TIMELINE
       ========================================================= */
    .timeline-section {
      background: var(--sage-light);
    }

    .timeline {
      position: relative;
      display: grid;
      grid-template-columns: 1fr;
      gap: 17px;
    }

    .timeline-card {
      position: relative;
      background: white;
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 21px;
      box-shadow: 0 8px 25px rgba(71, 100, 78, 0.06);
    }

    .timeline-number {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      width: 39px;
      height: 39px;
      border-radius: 12px;
      background: var(--sage);
      color: white;
      font-weight: 800;
      font-size: 0.8rem;
      margin-bottom: 14px;
    }

    .timeline-card h3 {
      font-size: 1rem;
      margin-bottom: 5px;
    }

    .timeline-card p {
      color: var(--text-soft);
      font-size: 0.83rem;
    }

    /* =========================================================
       RESEP
       ========================================================= */
    .prescription-section {
      background: white;
    }

    .prescription-flow {
      display: grid;
      grid-template-columns: 1fr;
      gap: 13px;
      max-width: 850px;
      margin: 0 auto;
    }

    .prescription-step {
      display: flex;
      gap: 15px;
      align-items: flex-start;
      padding: 18px;
      background: var(--sage-light);
      border: 1px solid var(--border);
      border-radius: 17px;
      transition: 0.3s;
    }

    .prescription-step:hover {
      transform: translateX(4px);
      background: white;
      box-shadow: var(--shadow);
    }

    .prescription-icon {
      width: 46px;
      height: 46px;
      flex: 0 0 46px;
      display: grid;
      place-items: center;
      border-radius: 13px;
      background: white;
      color: var(--sage-dark);
      box-shadow: 0 5px 15px rgba(71, 100, 78, 0.08);
    }

    .prescription-step h3 {
      font-size: 0.95rem;
      margin-bottom: 3px;
    }

    .prescription-step p {
      font-size: 0.8rem;
      color: var(--text-soft);
    }

    .kie-list {
      margin-top: 8px;
      padding-left: 17px;
      color: var(--text-soft);
      font-size: 0.79rem;
    }

    /* =========================================================
       CONSULTATION
       ========================================================= */
    .consultation-section {
      background: var(--sage-light);
    }

    .consult-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 25px;
      align-items: start;
    }

    .chat-box {
      background: white;
      padding: 23px;
      border-radius: 23px;
      box-shadow: var(--shadow);
    }

    .chat {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
    }

    .chat:last-child {
      margin-bottom: 0;
    }

    .chat-avatar {
      width: 39px;
      height: 39px;
      flex: 0 0 39px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--sage);
      color: white;
      font-size: 0.8rem;
    }

    .chat.pharmacist .chat-avatar {
      background: var(--pink);
      color: var(--text);
    }

    .chat-bubble {
      max-width: 88%;
      padding: 12px 15px;
      border-radius: 16px;
      background: var(--sage-light);
      font-size: 0.83rem;
    }

    .chat.pharmacist .chat-bubble {
      background: #fff0f3;
    }

    .chat-name {
      display: block;
      font-size: 0.73rem;
      font-weight: 800;
      margin-bottom: 3px;
    }

    .consult-list {
      list-style: none;
      display: grid;
      grid-template-columns: 1fr;
      gap: 9px;
      margin: 20px 0;
    }

    .consult-list li {
      display: flex;
      gap: 9px;
      align-items: flex-start;
      color: var(--text-soft);
      font-size: 0.84rem;
    }

    .consult-list i {
      color: var(--sage-dark);
      margin-top: 5px;
    }

    /* Pharmacist cards */
    .pharmacist-list {
      display: grid;
      grid-template-columns: 1fr;
      gap: 13px;
      margin-top: 25px;
    }

    .pharmacist-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 17px;
      padding: 17px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 12px;
      box-shadow: 0 7px 22px rgba(71, 100, 78, 0.06);
    }

    .pharmacist-info {
      min-width: 0;
    }

    .pharmacist-info h3 {
      font-size: 0.83rem;
      line-height: 1.35;
      margin-bottom: 3px;
    }

    .pharmacist-info p {
      color: var(--text-soft);
      font-size: 0.74rem;
    }

    .wa-small {
      width: 42px;
      height: 42px;
      flex: 0 0 42px;
      display: grid;
      place-items: center;
      border-radius: 12px;
      background: var(--sage-dark);
      color: white;
      transition: 0.25s;
    }

    .wa-small:hover {
      background: var(--pink-dark);
      transform: scale(1.05);
    }

    /* =========================================================
       SERVICES
       ========================================================= */
    .services-section {
      background: white;
    }

    .service-card {
      position: relative;
      overflow: hidden;
    }

    .service-card::after {
      content: "";
      position: absolute;
      width: 80px;
      height: 80px;
      right: -30px;
      top: -30px;
      background: var(--sage-light);
      border-radius: 50%;
      z-index: 0;
    }

    .service-card > * {
      position: relative;
      z-index: 1;
    }

    /* =========================================================
       CONTACT
       ========================================================= */
    .contact-section {
      background: var(--sage-light);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 22px;
    }

    .contact-card {
      background: white;
      border-radius: 23px;
      padding: 25px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    .contact-item {
      display: flex;
      gap: 14px;
      padding: 14px 0;
      border-bottom: 1px solid var(--border);
    }

    .contact-item:last-child {
      border-bottom: 0;
    }

    .contact-icon {
      width: 43px;
      height: 43px;
      flex: 0 0 43px;
      display: grid;
      place-items: center;
      background: var(--sage-light);
      color: var(--sage-dark);
      border-radius: 12px;
    }

    .contact-item h3 {
      font-size: 0.83rem;
      margin-bottom: 2px;
    }

    .contact-item p,
    .contact-item a {
      color: var(--text-soft);
      font-size: 0.79rem;
      overflow-wrap: anywhere;
    }

    .contact-buttons {
      display: grid;
      grid-template-columns: 1fr;
      gap: 10px;
      margin-top: 20px;
    }

    .map-card {
      min-height: 350px;
      padding: 0;
      overflow: hidden;
      position: relative;
    }

    .map-card iframe {
      width: 100%;
      height: 100%;
      min-height: 350px;
      border: 0;
    }

    .map-link {
      position: absolute;
      bottom: 15px;
      left: 15px;
      right: 15px;
    }

    /* =========================================================
       FAQ
       ========================================================= */
    .faq-section {
      background: white;
    }

    .faq-list {
      max-width: 850px;
      margin: 0 auto;
      display: grid;
      gap: 11px;
    }

    .faq-item {
      border: 1px solid var(--border);
      border-radius: 15px;
      overflow: hidden;
      background: white;
    }

    .faq-question {
      width: 100%;
      border: 0;
      background: white;
      color: var(--text);
      padding: 17px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 15px;
      text-align: left;
      font-weight: 700;
      font-size: 0.87rem;
      cursor: pointer;
    }

    .faq-question i {
      color: var(--sage-dark);
      transition: 0.3s;
    }

    .faq-item.active .faq-question i {
      transform: rotate(180deg);
    }

    .faq-answer {
      max-height: 0;
      overflow: hidden;
      transition: max-height 0.35s ease;
    }

    .faq-answer-inner {
      padding: 0 17px 17px;
      color: var(--text-soft);
      font-size: 0.82rem;
    }

    /* =========================================================
       FOOTER
       ========================================================= */
    footer {
      background: var(--text);
      color: white;
      padding: 48px 0 22px;
    }

    .footer-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 30px;
    }

    .footer-brand {
      display: flex;
      align-items: center;
      gap: 10px;
      margin-bottom: 14px;
    }

    .footer-brand .brand-icon {
      background: var(--sage);
    }

    .footer-brand-name {
      font-weight: 800;
      font-size: 0.9rem;
    }

    .footer p {
      color: rgba(255,255,255,0.68);
      font-size: 0.8rem;
    }

    .footer h3 {
      font-size: 0.9rem;
      margin-bottom: 12px;
    }

    .footer-links {
      list-style: none;
      display: grid;
      gap: 7px;
    }

    .footer-links a {
      color: rgba(255,255,255,0.68);
      font-size: 0.8rem;
      transition: 0.2s;
    }

    .footer-links a:hover {
      color: white;
    }

    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,0.12);
      margin-top: 32px;
      padding-top: 18px;
      text-align: center;
      color: rgba(255,255,255,0.55);
      font-size: 0.72rem;
    }

    /* =========================================================
       TOAST
       ========================================================= */
    .toast {
      position: fixed;
      left: 50%;
      bottom: 20px;
      transform: translate(-50%, 120px);
      width: calc(100% - 30px);
      max-width: 450px;
      background: var(--text);
      color: white;
      padding: 13px 17px;
      border-radius: 14px;
      box-shadow: 0 12px 35px rgba(0,0,0,0.18);
      z-index: 2000;
      display: flex;
      align-items: center;
      gap: 10px;
      font-size: 0.82rem;
      transition: 0.35s ease;
    }

    .toast.show {
      transform: translate(-50%, 0);
    }

    .toast i {
      color: var(--pink);
    }

    /* =========================================================
       BACK TO TOP
       ========================================================= */
    .back-top {
      position: fixed;
      right: 16px;
      bottom: 17px;
      width: 45px;
      height: 45px;
      display: grid;
      place-items: center;
      border: 0;
      border-radius: 14px;
      background: var(--sage-dark);
      color: white;
      cursor: pointer;
      box-shadow: var(--shadow);
      opacity: 0;
      visibility: hidden;
      transform: translateY(15px);
      transition: 0.3s;
      z-index: 1500;
    }

    .back-top.show {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }

    /* =========================================================
       REVEAL ANIMATION
       ========================================================= */
    .reveal {
      opacity: 0;
      transform: translateY(22px);
      transition: opacity 0.65s ease, transform 0.65s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================================================
       TABLET
       ========================================================= */
    @media (min-width: 600px) {
      .container {
        width: min(100% - 44px, var(--container));
      }

      .hero-actions {
        flex-direction: row;
      }

      .hero-actions .btn {
        width: auto;
      }

      .cards-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .form-items {
        grid-template-columns: repeat(2, 1fr);
      }

      .pharmacist-list {
        grid-template-columns: repeat(2, 1fr);
      }

      .contact-buttons {
        grid-template-columns: repeat(2, 1fr);
      }

      .timeline {
        grid-template-columns: repeat(2, 1fr);
      }

      .footer-grid {
        grid-template-columns: 1.4fr 1fr;
      }
    }

    /* =========================================================
       DESKTOP
       ========================================================= */
    @media (min-width: 981px) {
      section {
        padding: 100px 0;
      }

      .menu-toggle {
        display: none;
      }

      .nav-menu {
        position: static;
        width: auto;
        padding: 0;
        border: 0;
        box-shadow: none;
        background: transparent;
        transform: none;
        opacity: 1;
        pointer-events: auto;
        display: flex;
        align-items: center;
        gap: 13px;
      }

      .nav-links {
        flex-direction: row;
        align-items: center;
        gap: 2px;
      }

      .nav-link {
        font-size: 0.75rem;
        padding: 8px 8px;
      }

      .nav-register {
        width: auto;
        margin-top: 0;
        min-height: 42px;
        padding: 10px 15px;
        font-size: 0.78rem;
      }

      .hero {
        padding-top: 120px;
      }

      .hero-grid {
        grid-template-columns: 1.08fr 0.92fr;
        gap: 45px;
      }

      .hero-actions .btn {
        min-width: 180px;
      }

      .registration-wrapper {
        grid-template-columns: 1fr 1.15fr;
      }

      .timeline {
        grid-template-columns: repeat(6, 1fr);
        gap: 10px;
      }

      .timeline::before {
        content: "";
        position: absolute;
        left: 8%;
        right: 8%;
        top: 37px;
        height: 2px;
        background: var(--sage);
        z-index: 0;
      }

      .timeline-card {
        z-index: 1;
      }

      .prescription-flow {
        gap: 0;
      }

      .prescription-step {
        position: relative;
        border-radius: 0;
        border-left: 0;
        border-right: 0;
        margin-bottom: 1px;
      }

      .prescription-step:first-child {
        border-radius: 17px 17px 0 0;
      }

      .prescription-step:last-child {
        border-radius: 0 0 17px 17px;
      }

      .consult-grid {
        grid-template-columns: 0.9fr 1.1fr;
      }

      .contact-grid {
        grid-template-columns: 1fr 1fr;
      }

      .footer-grid {
        grid-template-columns: 1.5fr 1fr 1fr;
      }
    }

    @media (min-width: 1150px) {
      .nav-link {
        font-size: 0.78rem;
        padding: 8px 9px;
      }
    }

    /* =========================================================
       REDUCED MOTION
       ========================================================= */
    @media (prefers-reduced-motion: reduce) {
      html {
        scroll-behavior: auto;
      }

      *,
      *::before,
      *::after {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
      }
    }
  </style>
</head>

<body>

  <!-- =======================================================
       NAVBAR
       ======================================================== -->
  <header class="navbar">
    <div class="container nav-inner">

      <a href="#beranda" class="brand">
        <div class="brand-icon">
          <i class="fa-solid fa-prescription-bottle-medical"></i>
        </div>

        <div class="brand-text">
          <div class="brand-name">PELAYANAN KEFARMASIAN</div>
          <div class="brand-subtitle">Klinik Poltekes Jember</div>
        </div>
      </a>

      <button
        class="menu-toggle"
        id="menuToggle"
        aria-label="Buka menu"
        aria-expanded="false"
        aria-controls="navMenu"
      >
        <i class="fa-solid fa-bars"></i>
      </button>

      <nav class="nav-menu" id="navMenu">
        <ul class="nav-links">

          <li>
            <a href="#beranda" class="nav-link">
              🏠 Beranda
            </a>
          </li>

          <li>
            <a href="#pengertian" class="nav-link">
              📖 Pengertian
            </a>
          </li>

          <!-- Pendaftaran langsung ke Google Form -->
          <li>
            <a
              href="#"
              class="nav-link registration-link"
              data-registration-link
              target="_blank"
              rel="noopener noreferrer"
            >
              📝 Pendaftaran
            </a>
          </li>

          <li>
            <a href="#alur-pendaftaran" class="nav-link">
              🔄 Alur Pendaftaran
            </a>
          </li>

          <li>
            <a href="#pelayanan-resep" class="nav-link">
              💊 Pelayanan Resep
            </a>
          </li>

          <li>
            <a href="#konsultasi" class="nav-link">
              💬 Konsultasi
            </a>
          </li>

          <li>
            <a href="#kontak" class="nav-link">
              📞 Kontak
            </a>
          </li>
        </ul>

        <a
          href="#"
          class="btn btn-primary nav-register registration-link"
          data-registration-link
          target="_blank"
          rel="noopener noreferrer"
        >
          📝 Daftar Sekarang
        </a>
      </nav>
    </div>
  </header>


  <main>

    <!-- =====================================================
         HERO / BERANDA
         ====================================================== -->
    <section class="hero" id="beranda">
      <div class="container hero-grid">

        <div class="hero-content reveal">

          <div class="hero-badge">
            <i class="fa-solid fa-circle-check"></i>
            Portal Pelayanan Kefarmasian
          </div>

          <h1 class="hero-title">
            PELAYANAN KEFARMASIAN
            <span>KLINIK POLTEKES JEMBER</span>
          </h1>

          <h2 class="hero-tagline">
            Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
          </h2>

          <p class="hero-description">
            Website pelayanan kefarmasian yang memberikan informasi
            pelayanan serta memudahkan pasien melakukan pendaftaran secara
            online.
          </p>

          <div class="hero-actions">

            <a
              href="#"
              class="btn btn-primary registration-link"
              data-registration-link
              target="_blank"
              rel="noopener noreferrer"
            >
              <i class="fa-regular fa-clipboard"></i>
              DAFTAR SEKARANG
            </a>

            <a href="#informasi-pelayanan" class="btn btn-secondary">
              <i class="fa-solid fa-pills"></i>
              LIHAT PELAYANAN
            </a>

          </div>
        </div>


        <!-- Ilustrasi -->
        <div class="hero-visual reveal">

          <div class="illustration">

            <div class="ill-circle"></div>
            <div class="ill-circle-small"></div>

            <div class="tablet"></div>

            <div class="pharmacist">
              <div class="person-hair"></div>
              <div class="person-head"></div>

              <div class="person-body">
                <div class="person-shirt"></div>
                <div class="cross">
                  <i class="fa-solid fa-plus"></i>
                </div>
              </div>
            </div>

            <div class="medicine-box"></div>

            <div class="patient">
              <div class="person-hair"></div>
              <div class="person-head"></div>
              <div class="person-body"></div>
            </div>

            <div class="floating-plus plus-one">
              <i class="fa-solid fa-plus"></i>
            </div>

            <div class="floating-plus plus-two">
              <i class="fa-solid fa-heart-pulse"></i>
            </div>

          </div>
        </div>

      </div>
    </section>


    <!-- =====================================================
         PENGERTIAN
         ====================================================== -->
    <section class="definition-section" id="pengertian">
      <div class="container">

        <div class="section-heading reveal">
          <span class="section-label">
            <i class="fa-solid fa-book-open"></i>
            Pengertian
          </span>

          <h2 class="section-title">
            Apa Itu Pelayanan Kefarmasian?
          </h2>

          <p class="section-description">
            Pelayanan kefarmasian merupakan pelayanan yang diberikan
            oleh tenaga kefarmasian kepada pasien yang berkaitan dengan
            penggunaan obat dan pelayanan kesehatan untuk membantu memastikan
            obat digunakan secara tepat, aman, dan efektif.
          </p>

          <p class="section-description" style="margin-top: 10px;">
            Pelayanan kefarmasian tidak hanya berfokus pada obat, tetapi
            juga memperhatikan kebutuhan dan kondisi pasien.
          </p>
        </div>


        <div class="cards-grid">

          <article class="card reveal">
            <div class="icon-box">
              <i class="fa-solid fa-box-open"></i>
            </div>

            <h3>Pengelolaan Obat</h3>

            <p>
              Pengelolaan obat dilakukan untuk memastikan ketersediaan,
              penyimpanan, dan penggunaan obat secara tepat.
            </p>
          </article>


          <article class="card reveal">
            <div class="icon-box pink">
              <i class="fa-solid fa-user-doctor"></i>
            </div>

            <h3>Pelayanan kepada Pasien</h3>

            <p>
              Pelayanan diberikan dengan memperhatikan kebutuhan pasien
              dan memberikan informasi yang sesuai.
            </p>
          </article>


          <article class="card reveal">
            <div class="icon-box">
              <i class="fa-solid fa-comments"></i>
            </div>

            <h3>Informasi dan Konsultasi</h3>

            <p>
              Pasien dapat memperoleh informasi mengenai penggunaan obat
              dan berkonsultasi dengan apoteker.
            </p>
          </article>

        </div>
      </div>
    </section>


    <!-- =====================================================
         PENDAFTARAN
         ====================================================== -->
    <section class="registration-section" id="pendaftaran">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-regular fa-clipboard"></i>
            Pendaftaran Pasien
          </span>

          <h2 class="section-title">
            Pendaftaran Pelayanan
          </h2>

          <p class="section-description">
            Silakan melakukan pendaftaran terlebih dahulu sebelum
            mendapatkan pelayanan. Isi formulir dengan data yang benar agar
            proses pelayanan dapat berjalan dengan baik.
          </p>
        </div>


        <div class="registration-wrapper">

          <div class="registration-card highlight reveal">

            <div class="icon-box">
              <i class="fa-solid fa-pen-to-square"></i>
            </div>

            <h3 style="font-size:1.4rem; margin-bottom:10px;">
              Daftar Secara Online
            </h3>

            <p>
              Klik tombol di bawah untuk mengisi formulir pendaftaran
              pelayanan kefarmasian.
            </p>

            <a
              href="#"
              class="btn big-register-btn registration-link"
              data-registration-link
              target="_blank"
              rel="noopener noreferrer"
            >
              📝 ISI FORMULIR PENDAFTARAN
            </a>

            <div class="no-login">
              <i class="fa-solid fa-lock-open"></i>
              <span>
                Tidak memerlukan login. Formulir dapat diakses oleh semua
                pasien yang membutuhkan pelayanan.
              </span>
            </div>

          </div>


          <div class="registration-card reveal">

            <div class="icon-box">
              <i class="fa-solid fa-file-lines"></i>
            </div>

            <h3 style="font-size:1.25rem; margin-bottom:7px;">
              Isi Google Form
            </h3>

            <p style="color:var(--text-soft); font-size:.87rem;">
              Siapkan data berikut sebelum mengisi formulir.
            </p>


            <div class="form-items">

              <div class="form-item">
                <div class="form-item-icon">
                  <i class="fa-solid fa-user"></i>
                </div>

                <div>
                  <strong>Nama Pasien</strong>
                  <span>
                    Wajib diisi.
                    <small class="required">WAJIB</small>
                  </span>
                </div>
              </div>


              <div class="form-item">
                <div class="form-item-icon">
                  <i class="fa-solid fa-id-card"></i>
                </div>

                <div>
                  <strong>Nomor BPJS</strong>
                  <span>
                    Diisi jika pasien memiliki BPJS.
                    <small class="required">OPSIONAL</small>
                  </span>
                </div>
              </div>


              <div class="form-item">
                <div class="form-item-icon">
                  <i class="fa-solid fa-notes-medical"></i>
                </div>

                <div>
                  <strong>Keluhan</strong>
                  <span>
                    Tuliskan keluhan atau kebutuhan pelayanan.
                  </span>
                </div>
              </div>


              <div class="form-item">
                <div class="form-item-icon">
                  <i class="fa-brands fa-whatsapp"></i>
                </div>

                <div>
                  <strong>Nomor WhatsApp</strong>
                  <span>
                    Digunakan untuk menghubungi pasien.
                    <small class="required">WAJIB</small>
                  </span>
                </div>
              </div>

            </div>


            <div class="important-box">

              <strong>
                ⚠️ PENTING
              </strong>

              <p>
                Setelah mengisi formulir, nomor antrean akan segera
                dikirimkan melalui WhatsApp ke nomor yang telah dicantumkan
                pada formulir.
              </p>

              <p style="margin-top:8px;">
                Nomor antrean diberikan berdasarkan urutan pengiriman
                formulir. Pasien yang mengirimkan formulir terlebih dahulu
                akan mendapatkan urutan antrean terlebih dahulu.
              </p>

            </div>

          </div>

        </div>
      </div>
    </section>


    <!-- =====================================================
         INFORMASI ANTREAN
         ====================================================== -->
    <section class="queue-section" id="antrean">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-ticket"></i>
            Nomor Antrean
          </span>

          <h2 class="section-title">
            Informasi Antrean
          </h2>

          <p class="section-description">
            Setelah formulir diterima, proses nomor antrean dilakukan
            sesuai urutan waktu pengiriman formulir.
          </p>
        </div>


        <div class="queue-list">

          <div class="queue-step reveal">
            <div class="queue-number">1</div>

            <div class="queue-content">
              <h3>Isi Google Form</h3>
              <p>Pasien mengisi formulir pendaftaran secara lengkap.</p>
            </div>
          </div>


          <div class="queue-step reveal">
            <div class="queue-number">2</div>

            <div class="queue-content">
              <h3>Data Diterima</h3>
              <p>Data pendaftaran diterima untuk diproses.</p>
            </div>
          </div>


          <div class="queue-step reveal">
            <div class="queue-number">3</div>

            <div class="queue-content">
              <h3>Nomor Antrean Diproses</h3>
              <p>Nomor antrean diproses berdasarkan waktu pengiriman.</p>
            </div>
          </div>


          <div class="queue-step reveal">
            <div class="queue-number">4</div>

            <div class="queue-content">
              <h3>Nomor Antrean Dikirim</h3>
              <p>Nomor antrean dikirim melalui WhatsApp.</p>
            </div>
          </div>


          <div class="queue-step reveal">
            <div class="queue-number">5</div>

            <div class="queue-content">
              <h3>Pasien Datang</h3>
              <p>Pasien datang sesuai nomor antrean yang diterima.</p>
            </div>
          </div>

        </div>


        <div class="queue-note reveal">
          <i class="fa-brands fa-whatsapp"></i>
          &nbsp;
          Mohon pastikan nomor WhatsApp yang dicantumkan aktif dan
          dapat menerima pesan.
          <br />
          <strong>
            Urutan antrean mengikuti waktu pengiriman formulir pendaftaran.
          </strong>
        </div>

      </div>
    </section>


    <!-- =====================================================
         ALUR PENDAFTARAN
         ====================================================== -->
    <section class="timeline-section" id="alur-pendaftaran">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-route"></i>
            Langkah Pendaftaran
          </span>

          <h2 class="section-title">
            Alur Pendaftaran Pelayanan
          </h2>

          <p class="section-description">
            Ikuti langkah sederhana berikut untuk melakukan pendaftaran
            pelayanan kefarmasian.
          </p>
        </div>


        <div class="timeline">

          <div class="timeline-card reveal">
            <div class="timeline-number">01</div>
            <h3>Buka Website</h3>
            <p>
              Pasien membuka website Pelayanan Kefarmasian.
            </p>
          </div>


          <div class="timeline-card reveal">
            <div class="timeline-number">02</div>
            <h3>Pilih Pendaftaran</h3>
            <p>
              Pasien menekan tombol “Daftar Sekarang”.
            </p>
          </div>


          <div class="timeline-card reveal">
            <div class="timeline-number">03</div>
            <h3>Isi Google Form</h3>
            <p>
              Isi nama, nomor BPJS jika ada, keluhan, dan nomor WhatsApp.
            </p>
          </div>


          <div class="timeline-card reveal">
            <div class="timeline-number">04</div>
            <h3>Kirim Formulir</h3>
            <p>
              Pastikan data sudah benar kemudian kirim formulir.
            </p>
          </div>


          <div class="timeline-card reveal">
            <div class="timeline-number">05</div>
            <h3>Dapatkan Antrean</h3>
            <p>
              Nomor antrean akan dikirimkan melalui WhatsApp.
            </p>
          </div>


          <div class="timeline-card reveal">
            <div class="timeline-number">06</div>
            <h3>Datang ke Pelayanan</h3>
            <p>
              Pasien datang dan menunggu sesuai urutan antrean.
            </p>
          </div>

        </div>
      </div>
    </section>


    <!-- =====================================================
         PELAYANAN RESEP
         ====================================================== -->
    <section class="prescription-section" id="pelayanan-resep">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-prescription-bottle-medical"></i>
            Pelayanan Resep
          </span>

          <h2 class="section-title">
            Alur Pelayanan Resep
          </h2>

          <p class="section-description">
            Pelayanan resep dilakukan melalui tahapan pemeriksaan,
            penyiapan, pemeriksaan kembali, hingga pemberian informasi obat
            kepada pasien.
          </p>
        </div>


        <div class="prescription-flow">

          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-file-prescription"></i>
            </div>

            <div>
              <h3>1. Penerimaan Resep</h3>
              <p>
                Pasien menyerahkan resep kepada petugas/apoteker.
              </p>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-magnifying-glass"></i>
            </div>

            <div>
              <h3>2. Pemeriksaan Resep</h3>
              <p>
                Resep diperiksa meliputi kelengkapan dan kesesuaian resep.
              </p>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-box-open"></i>
            </div>

            <div>
              <h3>3. Penyiapan Obat</h3>
              <p>
                Obat disiapkan sesuai dengan resep.
              </p>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-circle-check"></i>
            </div>

            <div>
              <h3>4. Pemeriksaan Kembali</h3>
              <p>
                Dilakukan pemeriksaan kembali terhadap obat yang telah
                disiapkan.
              </p>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-hand-holding-medical"></i>
            </div>

            <div>
              <h3>5. Penyerahan Obat</h3>
              <p>
                Obat diserahkan kepada pasien.
              </p>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-comments"></i>
            </div>

            <div>
              <h3>6. Pemberian KIE</h3>

              <p>
                Pasien mendapatkan informasi mengenai penggunaan obat.
              </p>

              <ul class="kie-list">
                <li>Nama/kegunaan obat</li>
                <li>Dosis</li>
                <li>Aturan pakai</li>
                <li>Waktu penggunaan</li>
                <li>Cara penyimpanan</li>
                <li>Hal yang perlu diperhatikan</li>
              </ul>
            </div>
          </div>


          <div class="prescription-step reveal">
            <div class="prescription-icon">
              <i class="fa-solid fa-flag-checkered"></i>
            </div>

            <div>
              <h3>7. Pelayanan Selesai</h3>
              <p>
                Pasien telah menerima obat dan informasi yang diperlukan.
              </p>
            </div>
          </div>

        </div>
      </div>
    </section>


    <!-- =====================================================
         KONSULTASI
         ====================================================== -->
    <section class="consultation-section" id="konsultasi">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-comments"></i>
            Konsultasi
          </span>

          <h2 class="section-title">
            Konsultasi Kefarmasian
          </h2>

          <p class="section-description">
            Konsultasi kefarmasian merupakan kesempatan bagi pasien
            untuk menyampaikan pertanyaan atau permasalahan terkait penggunaan
            obat kepada apoteker.
          </p>
        </div>


        <div class="consult-grid">

          <!-- Chat -->
          <div class="chat-box reveal">

            <div class="chat">

              <div class="chat-avatar">
                <i class="fa-solid fa-user"></i>
              </div>

              <div class="chat-bubble">
                <span class="chat-name">👤 Pasien</span>
                “Saya ingin berkonsultasi mengenai obat yang sedang saya
                gunakan.”
              </div>

            </div>


            <div class="chat pharmacist">

              <div class="chat-avatar">
                <i class="fa-solid fa-user-doctor"></i>
              </div>

              <div class="chat-bubble">
                <span class="chat-name">👩‍⚕️ Apoteker</span>
                “Silakan sampaikan nama obat, aturan penggunaan, serta
                keluhan atau pertanyaan yang ingin dikonsultasikan.”
              </div>

            </div>

          </div>


          <!-- Konsultasi info -->
          <div class="card reveal">

            <div class="icon-box">
              <i class="fa-solid fa-comments-medical"></i>
            </div>

            <h3>
              Pasien dapat berkonsultasi mengenai:
            </h3>

            <ul class="consult-list">

              <li>
                <i class="fa-solid fa-check"></i>
                Cara penggunaan obat
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Aturan pakai
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Waktu penggunaan obat
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Efek samping
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Interaksi obat
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Penyimpanan obat
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Penggunaan beberapa obat secara bersamaan
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                Permasalahan terkait penggunaan obat
              </li>

            </ul>

            <a href="#apoteker" class="btn btn-primary btn-full">
              <i class="fa-brands fa-whatsapp"></i>
              KONSULTASI DENGAN APOTEKER
            </a>

          </div>

        </div>


        <!-- Daftar apoteker -->
        <div id="apoteker" style="margin-top:38px;">

          <div class="section-heading reveal">
            <span class="section-label">
              <i class="fa-solid fa-user-doctor"></i>
              Pilihan Apoteker
            </span>

            <h2 class="section-title" style="font-size:1.65rem;">
              Hubungi Apoteker
            </h2>
          </div>


          <div class="pharmacist-list">

            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <h3>
                  apt. Aisyah Ramadhani Wijaya Putri, S.Farm
                </h3>

                <p>
                  <i class="fa-brands fa-whatsapp"></i>
                  085232058261
                </p>
              </div>

              <a
                class="wa-small"
                href="https://wa.me/6285232058261"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Hubungi Aisyah melalui WhatsApp"
              >
                <i class="fa-brands fa-whatsapp"></i>
              </a>

            </div>


            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <h3>
                  apt. Sasi Putri Mauritania, S.Farm
                </h3>

                <p>
                  <i class="fa-brands fa-whatsapp"></i>
                  085334255376
                </p>
              </div>

              <a
                class="wa-small"
                href="https://wa.me/6285334255376"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Hubungi Sasi melalui WhatsApp"
              >
                <i class="fa-brands fa-whatsapp"></i>
              </a>

            </div>


            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <h3>
                  apt. Sri Wahyuni, S.Farm
                </h3>

                <p>
                  <i class="fa-brands fa-whatsapp"></i>
                  087757376296
                </p>
              </div>

              <a
                class="wa-small"
                href="https://wa.me/6287757376296"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Hubungi Sri melalui WhatsApp"
              >
                <i class="fa-brands fa-whatsapp"></i>
              </a>

            </div>


            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <h3>
                  apt. Tyara Novelia Putri, S.Farm
                </h3>

                <p>
                  <i class="fa-brands fa-whatsapp"></i>
                  085717420989
                </p>
              </div>

              <a
                class="wa-small"
                href="https://wa.me/6285717420989"
                target="_blank"
                rel="noopener noreferrer"
                aria-label="Hubungi Tyara melalui WhatsApp"
              >
                <i class="fa-brands fa-whatsapp"></i>
              </a>

            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         INFORMASI PELAYANAN
         ====================================================== -->
    <section class="services-section" id="informasi-pelayanan">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-heart-pulse"></i>
            Informasi Pelayanan
          </span>

          <h2 class="section-title">
            Jenis Pelayanan
          </h2>

          <p class="section-description">
            Berbagai pelayanan kefarmasian yang dapat membantu pasien
            mendapatkan informasi dan pelayanan terkait penggunaan obat.
          </p>
        </div>


        <div class="cards-grid">

          <article class="card service-card reveal">
            <div class="icon-box">
              <i class="fa-solid fa-prescription-bottle-medical"></i>
            </div>

            <h3>Pelayanan Resep</h3>

            <p>
              Pelayanan obat berdasarkan resep disertai informasi
              penggunaan obat.
            </p>
          </article>


          <article class="card service-card reveal">
            <div class="icon-box pink">
              <i class="fa-solid fa-leaf"></i>
            </div>

            <h3>Swamedikasi</h3>

            <p>
              Membantu pasien memperoleh informasi dalam penggunaan obat
              untuk keluhan ringan.
            </p>
          </article>


          <article class="card service-card reveal">
            <div class="icon-box">
              <i class="fa-solid fa-comments"></i>
            </div>

            <h3>Konsultasi Kefarmasian</h3>

            <p>
              Konsultasi pasien bersama apoteker mengenai penggunaan
              obat.
            </p>
          </article>


          <article class="card service-card reveal">
            <div class="icon-box pink">
              <i class="fa-solid fa-user-nurse"></i>
            </div>

            <h3>Konseling</h3>

            <p>
              Pemberian informasi secara langsung agar pasien memahami
              penggunaan obat.
            </p>
          </article>

        </div>
      </div>
    </section>


    <!-- =====================================================
         KONTAK
         ====================================================== -->
    <section class="contact-section" id="kontak">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-phone"></i>
            Kontak
          </span>

          <h2 class="section-title">
            Hubungi Kami
          </h2>

          <p class="section-description">
            Silakan gunakan informasi berikut untuk mendapatkan
            informasi lebih lanjut mengenai pelayanan.
          </p>
        </div>


        <div class="contact-grid">

          <div class="contact-card reveal">

            <div class="contact-item">

              <div class="contact-icon">
                <i class="fa-solid fa-location-dot"></i>
              </div>

              <div>
                <h3>Alamat</h3>

                <p>
                  Jl. Pangandaran No.42, Plinggan, Antirogo,
                  Kec. Sumbersari, Kabupaten Jember, Jawa Timur 68125
                </p>
              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">
                <i class="fa-solid fa-phone"></i>
              </div>

              <div>
                <h3>WhatsApp / Telepon</h3>

                <p>
                  (0331) 325930
                </p>
              </div>

            </div>


            <div class="contact-item">

              <div class="contact-icon">
                <i class="fa-solid fa-globe"></i>
              </div>

              <div>
                <h3>Situs Resmi</h3>

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

              <a
                href="https://wa.me/62331325930"
                class="btn btn-primary"
                target="_blank"
                rel="noopener noreferrer"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Hubungi via WhatsApp
              </a>

              <a
                href="https://poltekesjember.ac.id/"
                class="btn btn-secondary"
                target="_blank"
                rel="noopener noreferrer"
              >
                <i class="fa-solid fa-globe"></i>
                Situs Resmi
              </a>

            </div>

          </div>


          <!-- Google Maps -->
          <div class="contact-card map-card reveal">

            <iframe
              src="https://www.google.com/maps?q=Jl.%20Pangandaran%20No.42,%20Plinggan,%20Antirogo,%20Kec.%20Sumbersari,%20Kabupaten%20Jember,%20Jawa%20Timur%2068125&output=embed"
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
              title="Lokasi Klinik Poltekes Jember"
            ></iframe>

            <a
              class="btn btn-primary map-link"
              href="https://www.google.com/maps/search/?api=1&query=Jl.%20Pangandaran%20No.42,%20Plinggan,%20Antirogo,%20Kec.%20Sumbersari,%20Kabupaten%20Jember,%20Jawa%20Timur%2068125"
              target="_blank"
              rel="noopener noreferrer"
            >
              <i class="fa-solid fa-map-location-dot"></i>
              Buka Google Maps
            </a>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         FAQ
         ====================================================== -->
    <section class="faq-section" id="faq">
      <div class="container">

        <div class="section-heading text-center reveal">
          <span class="section-label">
            <i class="fa-solid fa-circle-question"></i>
            FAQ
          </span>

          <h2 class="section-title">
            Pertanyaan yang Sering Ditanyakan
          </h2>

          <p class="section-description">
            Informasi singkat untuk membantu pasien memahami proses
            pendaftaran dan antrean.
          </p>
        </div>


        <div class="faq-list">

          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Bagaimana cara mendaftar pelayanan?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Pasien dapat menekan tombol “Daftar Sekarang” dan
                mengisi Google Form yang tersedia.
              </div>
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Apakah semua pasien dapat melakukan pendaftaran?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Ya, formulir dapat digunakan oleh pasien yang membutuhkan
                pelayanan sesuai dengan jenis pelayanan yang tersedia.
              </div>
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Apakah nomor BPJS wajib diisi?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Tidak. Nomor BPJS dapat dikosongkan apabila pasien
                tidak memiliki BPJS.
              </div>
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Bagaimana saya mendapatkan nomor antrean?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Nomor antrean akan segera dikirimkan melalui WhatsApp
                ke nomor yang dicantumkan pada formulir.
              </div>
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Bagaimana urutan antreannya?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Urutan antrean mengikuti urutan waktu pengiriman
                formulir. Pasien yang mengirimkan formulir terlebih dahulu
                mendapatkan urutan terlebih dahulu.
              </div>
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>
                Apa yang harus dilakukan setelah mendapatkan nomor antrean?
              </span>

              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              <div class="faq-answer-inner">
                Pasien datang ke tempat pelayanan sesuai nomor antrean
                yang telah diberikan.
              </div>
            </div>

          </div>

        </div>
      </div>
    </section>

  </main>


  <!-- =======================================================
       FOOTER
       ======================================================== -->
  <footer>

    <div class="container footer-grid">

      <div>

        <div class="footer-brand">

          <div class="brand-icon">
            <i class="fa-solid fa-prescription-bottle-medical"></i>
          </div>

          <div class="footer-brand-name">
            PELAYANAN KEFARMASIAN
          </div>

        </div>

        <p>
          Mudah Mendaftar, Nyaman Mendapatkan Pelayanan
        </p>

        <p style="margin-top:10px;">
          Website informasi dan pendaftaran pelayanan kefarmasian
          Klinik Poltekes Jember.
        </p>

      </div>


      <div>

        <h3>Navigasi</h3>

        <ul class="footer-links">

          <li>
            <a href="#beranda">Beranda</a>
          </li>

          <li>
            <a href="#pengertian">Pengertian</a>
          </li>

          <li>
            <a
              href="#"
              class="registration-link"
              data-registration-link
              target="_blank"
              rel="noopener noreferrer"
            >
              Pendaftaran
            </a>
          </li>

          <li>
            <a href="#alur-pendaftaran">
              Alur Pendaftaran
            </a>
          </li>

          <li>
            <a href="#pelayanan-resep">
              Pelayanan Resep
            </a>
          </li>

          <li>
            <a href="#konsultasi">
              Konsultasi
            </a>
          </li>

          <li>
            <a href="#kontak">
              Kontak
            </a>
          </li>

        </ul>

      </div>


      <div>

        <h3>Kontak</h3>

        <p>
          <i class="fa-solid fa-location-dot"></i>
          Jl. Pangandaran No.42, Plinggan, Antirogo,
          Kec. Sumbersari, Kabupaten Jember,
          Jawa Timur 68125
        </p>

        <p style="margin-top:10px;">
          <i class="fa-solid fa-phone"></i>
          (0331) 325930
        </p>

        <p style="margin-top:10px;">
          <i class="fa-solid fa-globe"></i>
          poltekesjember.ac.id
        </p>

      </div>

    </div>


    <div class="container footer-bottom">

      © <span id="year"></span>
      Pelayanan Kefarmasian Klinik Poltekes Jember.
      All Rights Reserved.

    </div>

  </footer>


  <!-- =======================================================
       TOAST
       ======================================================== -->
  <div class="toast" id="toast">

    <i class="fa-solid fa-circle-check"></i>

    <span>
      Formulir pendaftaran akan dibuka di tab baru.
    </span>

  </div>


  <!-- =======================================================
       BACK TO TOP
       ======================================================== -->
  <button
    class="back-top"
    id="backTop"
    aria-label="Kembali ke atas"
  >
    <i class="fa-solid fa-arrow-up"></i>
  </button>


  <!-- =======================================================
       JAVASCRIPT
       ======================================================== -->
  <script>

    /* =========================================================
       GOOGLE FORM
       GANTI URL DI BAGIAN INI JIKA SUATU SAAT FORM BERUBAH
       ========================================================= */

    const GOOGLE_FORM_URL =
      "https://forms.gle/jG8p9wozy5nmoMrS8";


    /* =========================================================
       SET SEMUA LINK PENDAFTARAN
       ========================================================= */

    const registrationLinks =
      document.querySelectorAll("[data-registration-link]");

    registrationLinks.forEach((link) => {

      link.href = GOOGLE_FORM_URL;

      link.addEventListener("click", function () {

        showToast(
          "Formulir pendaftaran akan dibuka di tab baru."
        );

      });

    });


    /* =========================================================
       MOBILE MENU
       ========================================================= */

    const menuToggle =
      document.getElementById("menuToggle");

    const navMenu =
      document.getElementById("navMenu");

    menuToggle.addEventListener("click", () => {

      const isActive =
        navMenu.classList.toggle("active");

      menuToggle.setAttribute(
        "aria-expanded",
        isActive
      );

      menuToggle.innerHTML = isActive
        ? '<i class="fa-solid fa-xmark"></i>'
        : '<i class="fa-solid fa-bars"></i>';

    });


    /* Tutup menu ketika menu diklik */

    document
      .querySelectorAll(".nav-link")
      .forEach((link) => {

        link.addEventListener("click", () => {

          navMenu.classList.remove("active");

          menuToggle.setAttribute(
            "aria-expanded",
            "false"
          );

          menuToggle.innerHTML =
            '<i class="fa-solid fa-bars"></i>';

        });

      });


    /* =========================================================
       TOAST NOTIFICATION
       ========================================================= */

    const toast =
      document.getElementById("toast");

    let toastTimer;

    function showToast(message) {

      toast.querySelector("span").textContent =
        message;

      toast.classList.add("show");

      clearTimeout(toastTimer);

      toastTimer = setTimeout(() => {

        toast.classList.remove("show");

      }, 2800);

    }


    /* =========================================================
       FAQ ACCORDION
       ========================================================= */

    const faqItems =
      document.querySelectorAll(".faq-item");

    faqItems.forEach((item) => {

      const question =
        item.querySelector(".faq-question");

      const answer =
        item.querySelector(".faq-answer");

      question.addEventListener("click", () => {

        const isOpen =
          item.classList.contains("active");

        faqItems.forEach((otherItem) => {

          otherItem.classList.remove("active");

          otherItem
            .querySelector(".faq-answer")
            .style.maxHeight = null;

        });

        if (!isOpen) {

          item.classList.add("active");

          answer.style.maxHeight =
            answer.scrollHeight + "px";

        }

      });

    });


    /* =========================================================
       REVEAL ON SCROLL
       ========================================================= */

    const revealElements =
      document.querySelectorAll(".reveal");

    const revealObserver =
      new IntersectionObserver(
        (entries, observer) => {

          entries.forEach((entry) => {

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


    revealElements.forEach((element) => {

      revealObserver.observe(element);

    });


    /* =========================================================
       BACK TO TOP
       ========================================================= */

    const backTop =
      document.getElementById("backTop");

    window.addEventListener("scroll", () => {

      if (window.scrollY > 500) {

        backTop.classList.add("show");

      } else {

        backTop.classList.remove("show");

      }

    });


    backTop.addEventListener("click", () => {

      window.scrollTo({
        top: 0,
        behavior: "smooth"
      });

    });


    /* =========================================================
       COPYRIGHT YEAR
       ========================================================= */

    document.getElementById("year").textContent =
      new Date().getFullYear();


    /* =========================================================
       CLOSE MENU WHEN CLICKING OUTSIDE
       ========================================================= */

    document.addEventListener("click", (event) => {

      const clickedInsideNav =
        navMenu.contains(event.target);

      const clickedToggle =
        menuToggle.contains(event.target);

      if (
        window.innerWidth < 981 &&
        !clickedInsideNav &&
        !clickedToggle &&
        navMenu.classList.contains("active")
      ) {

        navMenu.classList.remove("active");

        menuToggle.setAttribute(
          "aria-expanded",
          "false"
        );

        menuToggle.innerHTML =
          '<i class="fa-solid fa-bars"></i>';

      }

    });

  </script>

</body>
</html>
