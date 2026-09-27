
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <meta name="description" content="Pelayanan Kefarmasian Klinik Poltekes Jember - Informasi pelayanan dan pendaftaran pasien secara online." />
  <meta name="theme-color" content="#A8BFAE" />

  <title>Pelayanan Kefarmasian Klinik Poltekes Jember</title>

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700&display=swap" rel="stylesheet">

  <!-- Font Awesome -->
  <link
    rel="stylesheet"
    href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css"
  />

  <style>
    /* =========================================================
       1. VARIABLES
    ========================================================= */
    :root {
      --sage: #A8BFAE;
      --sage-dark: #789781;
      --sage-light: #EFF5F0;
      --white: #FFFFFF;
      --pink: #E8B7C3;
      --pink-dark: #D38FA0;
      --text: #35443A;
      --text-light: #68766D;
      --border: #DCE7DE;
      --bg: #F8FBF9;
      --shadow: 0 12px 35px rgba(53, 68, 58, 0.09);
      --shadow-hover: 0 18px 42px rgba(53, 68, 58, 0.14);
      --radius: 22px;
      --radius-small: 14px;
      --transition: all 0.3s ease;
      --max-width: 1180px;
    }

    /* =========================================================
       2. RESET
    ========================================================= */
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
      background: var(--bg);
      color: var(--text);
      line-height: 1.7;
      overflow-x: hidden;
    }

    img {
      max-width: 100%;
      display: block;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    button,
    a {
      -webkit-tap-highlight-color: transparent;
    }

    button {
      font-family: inherit;
    }

    ul {
      list-style: none;
    }

    .container {
      width: min(100% - 32px, var(--max-width));
      margin: auto;
    }

    /* =========================================================
       3. TYPOGRAPHY
    ========================================================= */
    h1,
    h2,
    h3 {
      line-height: 1.25;
    }

    h1,
    h2 {
      font-family: "Playfair Display", serif;
    }

    .section {
      padding: 75px 0;
    }

    .section-header {
      max-width: 700px;
      margin: 0 auto 42px;
      text-align: center;
    }

    .section-label {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: var(--sage-light);
      color: var(--sage-dark);
      border: 1px solid var(--border);
      padding: 7px 14px;
      border-radius: 50px;
      font-size: 0.8rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 14px;
    }

    .section-title {
      font-size: clamp(2rem, 5vw, 3rem);
      margin-bottom: 14px;
    }

    .section-description {
      color: var(--text-light);
      font-size: 1rem;
    }

    /* =========================================================
       4. BUTTONS
    ========================================================= */
    .btn {
      min-height: 50px;
      padding: 13px 20px;
      border-radius: 13px;
      border: none;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 9px;
      font-weight: 700;
      cursor: pointer;
      transition: var(--transition);
      text-align: center;
    }

    .btn-primary {
      background: var(--sage-dark);
      color: white;
      box-shadow: 0 8px 20px rgba(120, 151, 129, 0.25);
    }

    .btn-primary:hover {
      background: var(--text);
      transform: translateY(-2px);
      box-shadow: 0 12px 25px rgba(53, 68, 58, 0.2);
    }

    .btn-secondary {
      background: white;
      color: var(--sage-dark);
      border: 1px solid var(--border);
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
      transform: translateY(-2px);
    }

    .btn-large {
      min-height: 58px;
      padding: 15px 25px;
      font-size: 1rem;
    }

    /* =========================================================
       5. NAVBAR
    ========================================================= */
    .navbar {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      background: rgba(255, 255, 255, 0.94);
      backdrop-filter: blur(15px);
      border-bottom: 1px solid rgba(220, 231, 222, 0.8);
    }

    .nav-container {
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
      border-radius: 13px;
      background: var(--sage);
      color: white;
      display: grid;
      place-items: center;
      font-size: 1.15rem;
    }

    .brand-text {
      font-weight: 800;
      line-height: 1.1;
      font-size: 0.82rem;
      max-width: 180px;
    }

    .brand-text span {
      display: block;
      color: var(--sage-dark);
    }

    .nav-menu {
      display: none;
      position: absolute;
      top: 72px;
      left: 0;
      right: 0;
      background: white;
      padding: 18px 16px 22px;
      border-bottom: 1px solid var(--border);
      box-shadow: var(--shadow);
    }

    .nav-menu.active {
      display: block;
    }

    .nav-menu ul {
      display: flex;
      flex-direction: column;
      gap: 5px;
    }

    .nav-link {
      display: flex;
      align-items: center;
      gap: 9px;
      padding: 12px;
      border-radius: 10px;
      color: var(--text-light);
      font-size: 0.9rem;
      font-weight: 600;
      transition: var(--transition);
    }

    .nav-link:hover {
      background: var(--sage-light);
      color: var(--sage-dark);
    }

    .nav-register {
      display: none;
    }

    .menu-toggle {
      width: 45px;
      height: 45px;
      border: 1px solid var(--border);
      background: white;
      color: var(--text);
      border-radius: 12px;
      font-size: 1.1rem;
      cursor: pointer;
    }

    /* =========================================================
       6. HERO
    ========================================================= */
    .hero {
      padding: 135px 0 70px;
      background:
        radial-gradient(circle at 10% 20%, rgba(168,191,174,.22), transparent 30%),
        radial-gradient(circle at 90% 80%, rgba(232,183,195,.15), transparent 25%),
        var(--sage-light);
      position: relative;
      overflow: hidden;
    }

    .hero-grid {
      display: grid;
      gap: 45px;
      align-items: center;
    }

    .hero-content {
      position: relative;
      z-index: 2;
    }

    .hero-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: white;
      color: var(--sage-dark);
      padding: 8px 14px;
      border-radius: 50px;
      border: 1px solid var(--border);
      font-size: 0.78rem;
      font-weight: 700;
      margin-bottom: 20px;
      box-shadow: 0 5px 18px rgba(53,68,58,.05);
    }

    .hero-title {
      font-size: clamp(2.25rem, 9vw, 4.6rem);
      letter-spacing: -0.04em;
      margin-bottom: 17px;
    }

    .hero-title span {
      color: var(--sage-dark);
    }

    .hero-tagline {
      font-size: clamp(1.05rem, 3vw, 1.35rem);
      font-weight: 700;
      margin-bottom: 13px;
    }

    .hero-description {
      color: var(--text-light);
      max-width: 650px;
      margin-bottom: 25px;
    }

    .hero-buttons {
      display: flex;
      flex-direction: column;
      gap: 11px;
    }

    .hero-visual {
      min-height: 330px;
      display: grid;
      place-items: center;
      position: relative;
    }

    .illustration {
      width: min(100%, 410px);
      height: 330px;
      background: white;
      border-radius: 35px;
      box-shadow: var(--shadow);
      position: relative;
      overflow: hidden;
    }

    .illustration::before,
    .illustration::after {
      content: "";
      position: absolute;
      border-radius: 50%;
      background: var(--sage-light);
    }

    .illustration::before {
      width: 190px;
      height: 190px;
      top: -70px;
      right: -45px;
    }

    .illustration::after {
      width: 150px;
      height: 150px;
      bottom: -70px;
      left: -45px;
      background: #f8e9ed;
    }

    .person {
      position: absolute;
      z-index: 2;
      bottom: 25px;
    }

    .pharmacist {
      left: 18%;
    }

    .patient {
      right: 17%;
    }

    .head {
      width: 58px;
      height: 58px;
      border-radius: 50%;
      background: #e8c5ae;
      margin: auto;
      position: relative;
    }

    .head::before {
      content: "";
      position: absolute;
      width: 62px;
      height: 28px;
      background: var(--text);
      border-radius: 50% 50% 20% 20%;
      top: -4px;
      left: -2px;
    }

    .body {
      width: 92px;
      height: 125px;
      margin-top: 6px;
      border-radius: 30px 30px 15px 15px;
      background: var(--sage);
      position: relative;
    }

    .pharmacist .body {
      background: white;
      border: 2px solid var(--sage);
    }

    .body::after {
      content: "+";
      position: absolute;
      top: 23px;
      left: 38px;
      font-size: 25px;
      font-weight: 800;
      color: var(--pink-dark);
    }

    .medicine-box {
      position: absolute;
      z-index: 4;
      width: 78px;
      height: 52px;
      background: white;
      border: 3px solid var(--sage-dark);
      border-radius: 10px;
      left: 43%;
      top: 45%;
      transform: rotate(-7deg);
      box-shadow: 0 7px 15px rgba(53,68,58,.12);
    }

    .medicine-box::after {
      content: "RX";
      position: absolute;
      inset: 0;
      display: grid;
      place-items: center;
      font-weight: 800;
      color: var(--pink-dark);
    }

    .floating-pill {
      position: absolute;
      z-index: 3;
      width: 36px;
      height: 18px;
      border-radius: 50px;
      background: var(--pink);
      transform: rotate(-25deg);
    }

    .pill-one {
      top: 25%;
      left: 20%;
    }

    .pill-two {
      bottom: 23%;
      right: 13%;
      background: var(--sage-dark);
    }

    /* =========================================================
       7. CARDS
    ========================================================= */
    .cards {
      display: grid;
      grid-template-columns: 1fr;
      gap: 18px;
    }

    .card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 25px;
      box-shadow: var(--shadow);
      transition: var(--transition);
    }

    .card:hover {
      transform: translateY(-5px);
      box-shadow: var(--shadow-hover);
    }

    .card-icon {
      width: 53px;
      height: 53px;
      display: grid;
      place-items: center;
      border-radius: 15px;
      background: var(--sage-light);
      color: var(--sage-dark);
      font-size: 1.25rem;
      margin-bottom: 18px;
    }

    .card-icon.pink {
      background: #FAEEF1;
      color: var(--pink-dark);
    }

    .card h3 {
      font-size: 1.08rem;
      margin-bottom: 8px;
    }

    .card p {
      color: var(--text-light);
      font-size: 0.92rem;
    }

    /* =========================================================
       8. PENGERTIAN
    ========================================================= */
    .about-section {
      background: white;
    }

    .about-main {
      background: var(--sage-light);
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 28px;
      margin-bottom: 20px;
    }

    .about-main p {
      color: var(--text-light);
      font-size: 1rem;
    }

    /* =========================================================
       9. REGISTRATION
    ========================================================= */
    .registration-section {
      background: var(--sage-light);
    }

    .registration-box {
      background: white;
      border-radius: 30px;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
      padding: 30px 22px;
      text-align: center;
      position: relative;
      overflow: hidden;
    }

    .registration-box::before {
      content: "";
      position: absolute;
      width: 180px;
      height: 180px;
      border-radius: 50%;
      background: rgba(168,191,174,.18);
      top: -90px;
      right: -70px;
    }

    .registration-icon {
      width: 72px;
      height: 72px;
      margin: 0 auto 18px;
      display: grid;
      place-items: center;
      border-radius: 22px;
      background: var(--sage);
      color: white;
      font-size: 1.6rem;
      position: relative;
    }

    .registration-box h2 {
      font-size: clamp(1.8rem, 6vw, 2.7rem);
      margin-bottom: 13px;
    }

    .registration-box > p {
      color: var(--text-light);
      max-width: 700px;
      margin: 0 auto 22px;
    }

    /* =========================================================
       10. FORM INFORMATION
    ========================================================= */
    .form-info {
      margin-top: 35px;
      display: grid;
      gap: 18px;
    }

    .data-list {
      display: grid;
      gap: 12px;
    }

    .data-item {
      display: flex;
      gap: 13px;
      align-items: flex-start;
      padding: 14px;
      background: var(--sage-light);
      border-radius: 14px;
    }

    .data-item i {
      color: var(--sage-dark);
      margin-top: 4px;
    }

    .data-item strong {
      display: block;
      margin-bottom: 2px;
    }

    .data-item span {
      color: var(--text-light);
      font-size: 0.86rem;
    }

    .important-note {
      background: #fff8fa;
      border: 1px solid #f0ccd5;
      border-radius: var(--radius);
      padding: 20px;
    }

    .important-note strong {
      display: block;
      color: #9f5267;
      margin-bottom: 6px;
    }

    .important-note p {
      color: var(--text-light);
      font-size: 0.9rem;
    }

    /* =========================================================
       11. QUEUE
    ========================================================= */
    .queue-section {
      background: white;
    }

    .queue-steps {
      max-width: 800px;
      margin: auto;
      position: relative;
    }

    .queue-step {
      display: flex;
      gap: 16px;
      position: relative;
      padding-bottom: 22px;
    }

    .queue-step:last-child {
      padding-bottom: 0;
    }

    .queue-step:not(:last-child)::before {
      content: "";
      position: absolute;
      left: 20px;
      top: 42px;
      width: 2px;
      height: calc(100% - 18px);
      background: var(--border);
    }

    .step-number {
      width: 42px;
      height: 42px;
      flex: 0 0 42px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--sage);
      color: white;
      font-weight: 800;
      position: relative;
      z-index: 2;
    }

    .queue-step-content {
      padding: 5px 0;
    }

    .queue-step-content h3 {
      font-size: 1rem;
      margin-bottom: 3px;
    }

    .queue-step-content p {
      color: var(--text-light);
      font-size: 0.88rem;
    }

    .queue-note {
      margin-top: 28px;
      padding: 18px;
      border-radius: 15px;
      background: var(--sage-light);
      border: 1px solid var(--border);
      color: var(--text-light);
      font-size: 0.88rem;
      text-align: center;
    }

    /* =========================================================
       12. TIMELINE
    ========================================================= */
    .timeline {
      display: grid;
      gap: 18px;
      position: relative;
    }

    .timeline-item {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 22px;
      box-shadow: var(--shadow);
      transition: var(--transition);
      position: relative;
    }

    .timeline-item:hover {
      transform: translateY(-4px);
    }

    .timeline-number {
      display: inline-flex;
      padding: 6px 10px;
      background: var(--sage-light);
      color: var(--sage-dark);
      border-radius: 8px;
      font-size: 0.78rem;
      font-weight: 800;
      margin-bottom: 12px;
    }

    .timeline-item h3 {
      font-size: 1rem;
      margin-bottom: 7px;
    }

    .timeline-item p {
      color: var(--text-light);
      font-size: 0.88rem;
    }

    /* =========================================================
       13. RECIPE SERVICE
    ========================================================= */
    .prescription-section {
      background: var(--sage-light);
    }

    .prescription-intro {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 25px;
      margin-bottom: 30px;
      color: var(--text-light);
    }

    .recipe-flow {
      display: grid;
      gap: 14px;
    }

    .recipe-step {
      display: flex;
      gap: 14px;
      align-items: flex-start;
      background: white;
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 18px;
      box-shadow: 0 7px 20px rgba(53,68,58,.05);
    }

    .recipe-icon {
      width: 45px;
      height: 45px;
      flex: 0 0 45px;
      border-radius: 13px;
      display: grid;
      place-items: center;
      background: var(--sage-light);
      color: var(--sage-dark);
    }

    .recipe-step:nth-child(6) .recipe-icon {
      background: #faeef1;
      color: var(--pink-dark);
    }

    .recipe-content h3 {
      font-size: 0.98rem;
      margin-bottom: 4px;
    }

    .recipe-content p {
      color: var(--text-light);
      font-size: 0.86rem;
    }

    .kie-list {
      display: flex;
      flex-wrap: wrap;
      gap: 6px;
      margin-top: 9px;
    }

    .kie-list span {
      background: var(--sage-light);
      color: var(--sage-dark);
      padding: 5px 9px;
      border-radius: 50px;
      font-size: 0.72rem;
      font-weight: 600;
    }

    /* =========================================================
       14. CONSULTATION
    ========================================================= */
    .chat-container {
      max-width: 720px;
      margin: 0 auto 35px;
      background: white;
      border: 1px solid var(--border);
      border-radius: 25px;
      padding: 20px;
      box-shadow: var(--shadow);
    }

    .chat-message {
      display: flex;
      gap: 10px;
      margin-bottom: 16px;
    }

    .chat-message:last-child {
      margin-bottom: 0;
    }

    .chat-avatar {
      width: 38px;
      height: 38px;
      flex: 0 0 38px;
      display: grid;
      place-items: center;
      border-radius: 50%;
      background: var(--sage);
      color: white;
      font-size: 0.9rem;
    }

    .chat-message.pharmacist .chat-avatar {
      background: var(--pink);
      color: var(--text);
    }

    .chat-bubble {
      background: var(--sage-light);
      padding: 12px 15px;
      border-radius: 5px 17px 17px 17px;
      max-width: 85%;
      font-size: 0.87rem;
    }

    .chat-message.pharmacist .chat-bubble {
      background: #fff1f4;
      border-radius: 17px 5px 17px 17px;
    }

    .chat-name {
      display: block;
      font-size: 0.72rem;
      font-weight: 800;
      color: var(--sage-dark);
      margin-bottom: 3px;
    }

    .consult-grid {
      display: grid;
      gap: 25px;
    }

    .consult-list {
      display: grid;
      gap: 10px;
    }

    .consult-list li {
      display: flex;
      gap: 10px;
      align-items: flex-start;
      color: var(--text-light);
      font-size: 0.9rem;
    }

    .consult-list i {
      color: var(--sage-dark);
      margin-top: 5px;
    }

    .pharmacist-grid {
      display: grid;
      gap: 14px;
      margin-top: 28px;
    }

    .pharmacist-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: 18px;
      padding: 18px;
      display: flex;
      flex-direction: column;
      gap: 12px;
      box-shadow: 0 7px 20px rgba(53,68,58,.05);
    }

    .pharmacist-info {
      display: flex;
      gap: 12px;
      align-items: center;
    }

    .pharmacist-avatar {
      width: 45px;
      height: 45px;
      flex: 0 0 45px;
      border-radius: 50%;
      background: var(--sage-light);
      color: var(--sage-dark);
      display: grid;
      place-items: center;
    }

    .pharmacist-info h3 {
      font-size: 0.9rem;
    }

    .pharmacist-info p {
      font-size: 0.77rem;
      color: var(--text-light);
    }

    .wa-small {
      width: 100%;
      min-height: 42px;
      font-size: 0.82rem;
    }

    /* =========================================================
       15. SERVICES
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
      width: 90px;
      height: 90px;
      border-radius: 50%;
      background: var(--sage-light);
      right: -35px;
      bottom: -40px;
      z-index: 0;
    }

    .service-card > * {
      position: relative;
      z-index: 1;
    }

    /* =========================================================
       16. CONTACT
    ========================================================= */
    .contact-section {
      background: var(--sage-light);
    }

    .contact-grid {
      display: grid;
      gap: 25px;
    }

    .contact-card {
      background: white;
      border: 1px solid var(--border);
      border-radius: var(--radius);
      padding: 25px;
      box-shadow: var(--shadow);
    }

    .contact-item {
      display: flex;
      gap: 14px;
      padding: 15px 0;
      border-bottom: 1px solid var(--border);
    }

    .contact-item:last-child {
      border-bottom: none;
    }

    .contact-icon {
      width: 43px;
      height: 43px;
      flex: 0 0 43px;
      border-radius: 12px;
      background: var(--sage-light);
      color: var(--sage-dark);
      display: grid;
      place-items: center;
    }

    .contact-item h3 {
      font-size: 0.9rem;
      margin-bottom: 2px;
    }

    .contact-item p,
    .contact-item a {
      color: var(--text-light);
      font-size: 0.85rem;
      word-break: break-word;
    }

    .contact-buttons {
      display: grid;
      gap: 10px;
      margin-top: 18px;
    }

    .map-wrapper {
      min-height: 380px;
      border-radius: var(--radius);
      overflow: hidden;
      border: 1px solid var(--border);
      box-shadow: var(--shadow);
      background: var(--sage);
    }

    .map-wrapper iframe {
      width: 100%;
      height: 100%;
      min-height: 380px;
      border: 0;
    }

    /* =========================================================
       17. FAQ
    ========================================================= */
    .faq-list {
      max-width: 850px;
      margin: auto;
      display: grid;
      gap: 11px;
    }

    .faq-item {
      background: white;
      border: 1px solid var(--border);
      border-radius: 15px;
      overflow: hidden;
    }

    .faq-question {
      width: 100%;
      padding: 18px;
      background: white;
      border: none;
      color: var(--text);
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 15px;
      text-align: left;
      font-weight: 700;
      cursor: pointer;
      font-size: 0.9rem;
    }

    .faq-question i {
      color: var(--sage-dark);
      transition: var(--transition);
    }

    .faq-answer {
      display: none;
      padding: 0 18px 18px;
      color: var(--text-light);
      font-size: 0.86rem;
    }

    .faq-item.active .faq-answer {
      display: block;
    }

    .faq-item.active .faq-question i {
      transform: rotate(180deg);
    }

    /* =========================================================
       18. FOOTER
    ========================================================= */
    footer {
      background: var(--text);
      color: white;
      padding: 55px 0 25px;
    }

    .footer-grid {
      display: grid;
      gap: 35px;
    }

    .footer-brand h2 {
      font-size: 1.55rem;
      margin-bottom: 8px;
    }

    .footer-brand p {
      color: #c7d1ca;
      font-size: 0.85rem;
      max-width: 420px;
    }

    .footer-title {
      font-size: 0.95rem;
      margin-bottom: 13px;
      color: white;
    }

    .footer-links {
      display: grid;
      gap: 7px;
    }

    .footer-links a {
      color: #c7d1ca;
      font-size: 0.83rem;
      transition: var(--transition);
    }

    .footer-links a:hover {
      color: var(--pink);
    }

    .footer-contact {
      color: #c7d1ca;
      font-size: 0.82rem;
      display: grid;
      gap: 8px;
    }

    .footer-bottom {
      border-top: 1px solid rgba(255,255,255,.12);
      margin-top: 35px;
      padding-top: 20px;
      text-align: center;
      color: #aebbb1;
      font-size: 0.75rem;
    }

    /* =========================================================
       19. TOAST
    ========================================================= */
    .toast {
      position: fixed;
      left: 16px;
      right: 16px;
      bottom: 20px;
      z-index: 2000;
      background: var(--text);
      color: white;
      padding: 14px 17px;
      border-radius: 14px;
      box-shadow: var(--shadow-hover);
      transform: translateY(130px);
      opacity: 0;
      pointer-events: none;
      transition: var(--transition);
      font-size: 0.85rem;
      text-align: center;
    }

    .toast.show {
      transform: translateY(0);
      opacity: 1;
    }

    /* =========================================================
       20. BACK TO TOP
    ========================================================= */
    .back-top {
      position: fixed;
      right: 17px;
      bottom: 18px;
      width: 46px;
      height: 46px;
      border: none;
      border-radius: 50%;
      background: var(--sage-dark);
      color: white;
      display: grid;
      place-items: center;
      cursor: pointer;
      z-index: 900;
      box-shadow: 0 8px 22px rgba(53,68,58,.2);
      opacity: 0;
      visibility: hidden;
      transform: translateY(10px);
      transition: var(--transition);
    }

    .back-top.show {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }

    /* =========================================================
       21. SCROLL REVEAL
    ========================================================= */
    .reveal {
      opacity: 0;
      transform: translateY(25px);
      transition: opacity .7s ease, transform .7s ease;
    }

    .reveal.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* =========================================================
       22. TABLET
    ========================================================= */
    @media (min-width: 600px) {
      .container {
        width: min(100% - 45px, var(--max-width));
      }

      .hero-buttons {
        flex-direction: row;
        flex-wrap: wrap;
      }

      .cards {
        grid-template-columns: repeat(2, 1fr);
      }

      .form-info {
        grid-template-columns: 1fr 1fr;
      }

      .pharmacist-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .contact-buttons {
        grid-template-columns: 1fr 1fr;
      }

      .footer-grid {
        grid-template-columns: 1.3fr 1fr 1fr;
      }

      .toast {
        left: auto;
        right: 25px;
        max-width: 360px;
        text-align: left;
      }
    }

    /* =========================================================
       23. DESKTOP
    ========================================================= */
    @media (min-width: 900px) {
      .section {
        padding: 100px 0;
      }

      .menu-toggle {
        display: none;
      }

      .nav-menu {
        display: block !important;
        position: static;
        padding: 0;
        background: transparent;
        border: none;
        box-shadow: none;
      }

      .nav-menu ul {
        flex-direction: row;
        align-items: center;
        gap: 2px;
      }

      .nav-link {
        padding: 9px 8px;
        font-size: 0.76rem;
      }

      .nav-register {
        display: inline-flex;
        min-height: 43px;
        padding: 10px 15px;
        background: var(--sage-dark);
        color: white;
        border-radius: 11px;
        font-size: 0.76rem;
        font-weight: 700;
        transition: var(--transition);
      }

      .nav-register:hover {
        background: var(--text);
        transform: translateY(-2px);
      }

      .hero {
        padding: 160px 0 100px;
      }

      .hero-grid {
        grid-template-columns: 1.05fr .95fr;
        gap: 70px;
      }

      .hero-buttons {
        flex-wrap: nowrap;
      }

      .cards {
        grid-template-columns: repeat(3, 1fr);
      }

      .form-info {
        grid-template-columns: 1fr 1fr;
        align-items: stretch;
      }

      .timeline {
        grid-template-columns: repeat(3, 1fr);
      }

      .timeline-item {
        min-height: 205px;
      }

      .timeline-item:nth-child(n+4) {
        margin-top: 5px;
      }

      .consult-grid {
        grid-template-columns: .9fr 1.1fr;
        align-items: start;
      }

      .pharmacist-grid {
        grid-template-columns: repeat(2, 1fr);
      }

      .contact-grid {
        grid-template-columns: .9fr 1.1fr;
      }
    }

    @media (min-width: 1100px) {
      .nav-link {
        padding: 9px 10px;
        font-size: 0.78rem;
      }

      .brand-text {
        max-width: 220px;
      }

      .timeline {
        grid-template-columns: repeat(6, 1fr);
      }

      .timeline-item {
        min-height: 240px;
      }

      .timeline-item:not(:last-child)::after {
        content: "";
        position: absolute;
        top: 31px;
        right: -18px;
        width: 18px;
        height: 2px;
        background: var(--border);
      }

      .timeline-item:nth-child(n+4) {
        margin-top: 0;
      }
    }

    /* =========================================================
       24. REDUCED MOTION
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
    <div class="container nav-container">

      <a href="#beranda" class="brand">
        <div class="brand-icon">
          <i class="fa-solid fa-pills"></i>
        </div>
        <div class="brand-text">
          PELAYANAN KEFARMASIAN
          <span>KLINIK POLTEKES JEMBER</span>
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
        <ul>
          <li>
            <a href="#beranda" class="nav-link">
              <i class="fa-solid fa-house"></i> Beranda
            </a>
          </li>

          <li>
            <a href="#pengertian" class="nav-link">
              <i class="fa-solid fa-book-open"></i> Pengertian
            </a>
          </li>

          <!-- Pendaftaran langsung Google Form -->
          <li>
            <a
              href="https://forms.gle/jG8p9wozy5nmoMrS8"
              target="_blank"
              rel="noopener noreferrer"
              class="nav-link registration-link"
              data-registration-link
            >
              <i class="fa-solid fa-clipboard-list"></i> Pendaftaran
            </a>
          </li>

          <li>
            <a href="#alur-pendaftaran" class="nav-link">
              <i class="fa-solid fa-route"></i> Alur Pendaftaran
            </a>
          </li>

          <li>
            <a href="#pelayanan-resep" class="nav-link">
              <i class="fa-solid fa-prescription-bottle-medical"></i> Pelayanan Resep
            </a>
          </li>

          <li>
            <a href="#konsultasi" class="nav-link">
              <i class="fa-solid fa-comments"></i> Konsultasi
            </a>
          </li>

          <li>
            <a href="#kontak" class="nav-link">
              <i class="fa-solid fa-phone"></i> Kontak
            </a>
          </li>
        </ul>
      </nav>

      <a
        href="https://forms.gle/jG8p9wozy5nmoMrS8"
        target="_blank"
        rel="noopener noreferrer"
        class="nav-register registration-link"
        data-registration-link
      >
        <i class="fa-solid fa-pen-to-square"></i>
        Daftar Sekarang
      </a>

    </div>
  </header>


  <main>

    <!-- =====================================================
         HERO
    ====================================================== -->
    <section class="hero" id="beranda">
      <div class="container hero-grid">

        <div class="hero-content reveal">

          <div class="hero-badge">
            <i class="fa-solid fa-heart-pulse"></i>
            Pelayanan Kefarmasian
          </div>

          <h1 class="hero-title">
            PELAYANAN KEFARMASIAN
            <span>KLINIK POLTEKES JEMBER</span>
          </h1>

          <p class="hero-tagline">
            “Mudah Mendaftar, Nyaman Mendapatkan Pelayanan”
          </p>

          <p class="hero-description">
            Website pelayanan kefarmasian yang memberikan informasi
            pelayanan serta memudahkan pasien melakukan pendaftaran secara online.
          </p>

          <div class="hero-buttons">

            <a
              href="https://forms.gle/jG8p9wozy5nmoMrS8"
              target="_blank"
              rel="noopener noreferrer"
              class="btn btn-primary btn-large registration-link"
              data-registration-link
            >
              <i class="fa-solid fa-clipboard-list"></i>
              DAFTAR SEKARANG
            </a>

            <a href="#informasi-pelayanan" class="btn btn-secondary btn-large">
              <i class="fa-solid fa-pills"></i>
              LIHAT PELAYANAN
            </a>

          </div>
        </div>


        <!-- Ilustrasi -->
        <div class="hero-visual reveal">

          <div class="illustration">

            <div class="floating-pill pill-one"></div>
            <div class="floating-pill pill-two"></div>

            <div class="person pharmacist">
              <div class="head"></div>
              <div class="body"></div>
            </div>

            <div class="person patient">
              <div class="head"></div>
              <div class="body"></div>
            </div>

            <div class="medicine-box"></div>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         PENGERTIAN
    ====================================================== -->
    <section class="section about-section" id="pengertian">
      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-book-open"></i>
            Pengertian
          </div>

          <h2 class="section-title">
            Apa Itu Pelayanan Kefarmasian?
          </h2>

          <p class="section-description">
            Memahami pelayanan kefarmasian sebelum mendapatkan pelayanan.
          </p>

        </div>


        <div class="about-main reveal">

          <p>
            Pelayanan kefarmasian merupakan pelayanan yang diberikan
            oleh tenaga kefarmasian kepada pasien yang berkaitan dengan
            penggunaan obat dan pelayanan kesehatan untuk membantu memastikan
            obat digunakan secara tepat, aman, dan efektif.
          </p>

          <br>

          <p>
            Pelayanan kefarmasian tidak hanya berfokus pada obat,
            tetapi juga memperhatikan kebutuhan dan kondisi pasien sehingga
            pasien memperoleh informasi yang sesuai dalam menggunakan obat.
          </p>

        </div>


        <div class="cards">

          <article class="card reveal">
            <div class="card-icon">
              <i class="fa-solid fa-boxes-stacked"></i>
            </div>

            <h3>Pengelolaan Obat</h3>

            <p>
              Pengelolaan obat dilakukan untuk memastikan ketersediaan,
              penyimpanan, dan penggunaan obat secara tepat.
            </p>
          </article>


          <article class="card reveal">
            <div class="card-icon">
              <i class="fa-solid fa-user-doctor"></i>
            </div>

            <h3>Pelayanan kepada Pasien</h3>

            <p>
              Pelayanan diberikan dengan memperhatikan kebutuhan pasien
              dan memberikan informasi yang sesuai.
            </p>
          </article>


          <article class="card reveal">
            <div class="card-icon pink">
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
    <section class="section registration-section" id="pendaftaran">
      <div class="container">

        <div class="registration-box reveal">

          <div class="registration-icon">
            <i class="fa-solid fa-clipboard-list"></i>
          </div>

          <h2>Pendaftaran Pelayanan</h2>

          <p>
            Silakan melakukan pendaftaran terlebih dahulu sebelum mendapatkan
            pelayanan. Isi formulir dengan data yang benar agar proses pelayanan
            dapat berjalan dengan baik.
          </p>

          <a
            href="https://forms.gle/jG8p9wozy5nmoMrS8"
            target="_blank"
            rel="noopener noreferrer"
            class="btn btn-primary btn-large registration-link"
            data-registration-link
          >
            <i class="fa-solid fa-pen-to-square"></i>
            ISI FORMULIR PENDAFTARAN
          </a>

          <p style="margin-top:15px; font-size:.78rem;">
            <i class="fa-solid fa-shield-halved"></i>
            Tidak memerlukan login. Formulir dapat digunakan oleh semua pasien.
          </p>

        </div>


        <!-- Isi Google Form -->
        <div class="form-info">

          <div class="card reveal">

            <div class="card-icon">
              <i class="fa-solid fa-file-lines"></i>
            </div>

            <h3 style="margin-bottom:18px;">
              Isi Google Form
            </h3>

            <div class="data-list">

              <div class="data-item">
                <i class="fa-solid fa-user"></i>
                <div>
                  <strong>Nama Pasien</strong>
                  <span>Wajib diisi.</span>
                </div>
              </div>

              <div class="data-item">
                <i class="fa-solid fa-id-card"></i>
                <div>
                  <strong>Nomor BPJS</strong>
                  <span>Opsional. Diisi jika pasien memiliki BPJS.</span>
                </div>
              </div>

              <div class="data-item">
                <i class="fa-solid fa-notes-medical"></i>
                <div>
                  <strong>Keluhan</strong>
                  <span>
                    Tuliskan keluhan atau kebutuhan pelayanan.
                  </span>
                </div>
              </div>

              <div class="data-item">
                <i class="fa-brands fa-whatsapp"></i>
                <div>
                  <strong>Nomor WhatsApp</strong>
                  <span>
                    Wajib diisi untuk menghubungi pasien dan mengirimkan
                    nomor antrean.
                  </span>
                </div>
              </div>

            </div>

          </div>


          <div class="important-note reveal">

            <strong>
              <i class="fa-solid fa-triangle-exclamation"></i>
              PENTING
            </strong>

            <p>
              Setelah mengisi formulir, nomor antrean akan segera dikirimkan
              melalui WhatsApp ke nomor yang telah dicantumkan pada formulir.
            </p>

            <br>

            <p>
              <strong>Nomor antrean diberikan berdasarkan urutan pengiriman
              formulir.</strong>
              Pasien yang mengirimkan formulir terlebih dahulu akan mendapatkan
              urutan antrean terlebih dahulu.
            </p>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         INFORMASI ANTREAN
    ====================================================== -->
    <section class="section queue-section" id="antrean">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-ticket"></i>
            Informasi Antrean
          </div>

          <h2 class="section-title">
            Informasi Antrean
          </h2>

          <p class="section-description">
            Ikuti tahapan berikut setelah mengirimkan formulir pendaftaran.
          </p>

        </div>


        <div class="queue-steps">

          <div class="queue-step reveal">
            <div class="step-number">1</div>
            <div class="queue-step-content">
              <h3>Isi Google Form</h3>
              <p>Pasien mengisi formulir pendaftaran.</p>
            </div>
          </div>

          <div class="queue-step reveal">
            <div class="step-number">2</div>
            <div class="queue-step-content">
              <h3>Data diterima</h3>
              <p>Data pendaftaran diterima melalui formulir.</p>
            </div>
          </div>

          <div class="queue-step reveal">
            <div class="step-number">3</div>
            <div class="queue-step-content">
              <h3>Nomor antrean diproses</h3>
              <p>Urutan antrean mengikuti waktu pengiriman formulir.</p>
            </div>
          </div>

          <div class="queue-step reveal">
            <div class="step-number">4</div>
            <div class="queue-step-content">
              <h3>Nomor antrean dikirim melalui WhatsApp</h3>
              <p>Pasien menerima informasi antrean melalui WhatsApp.</p>
            </div>
          </div>

          <div class="queue-step reveal">
            <div class="step-number">5</div>
            <div class="queue-step-content">
              <h3>Pasien datang sesuai antrean</h3>
              <p>Pasien datang dan menunggu sesuai nomor antrean.</p>
            </div>
          </div>

        </div>


        <div class="queue-note reveal">
          <i class="fa-brands fa-whatsapp"></i>
          Mohon pastikan nomor WhatsApp yang dicantumkan aktif dan
          dapat menerima pesan.
          <br><br>
          Urutan antrean mengikuti waktu pengiriman formulir pendaftaran.
        </div>

      </div>
    </section>


    <!-- =====================================================
         ALUR PENDAFTARAN
    ====================================================== -->
    <section class="section" id="alur-pendaftaran">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-route"></i>
            Alur Pendaftaran
          </div>

          <h2 class="section-title">
            Alur Pendaftaran Pelayanan
          </h2>

          <p class="section-description">
            Enam langkah sederhana untuk mendapatkan pelayanan.
          </p>

        </div>


        <div class="timeline">

          <div class="timeline-item reveal">
            <span class="timeline-number">01</span>
            <h3>Buka Website</h3>
            <p>
              Pasien membuka website Pelayanan Kefarmasian.
            </p>
          </div>

          <div class="timeline-item reveal">
            <span class="timeline-number">02</span>
            <h3>Pilih Pendaftaran</h3>
            <p>
              Pasien menekan tombol “Daftar Sekarang”.
            </p>
          </div>

          <div class="timeline-item reveal">
            <span class="timeline-number">03</span>
            <h3>Isi Google Form</h3>
            <p>
              Pasien mengisi nama, nomor BPJS jika ada,
              keluhan, dan nomor WhatsApp.
            </p>
          </div>

          <div class="timeline-item reveal">
            <span class="timeline-number">04</span>
            <h3>Kirim Formulir</h3>
            <p>
              Pasien memastikan data sudah benar kemudian
              mengirimkan formulir.
            </p>
          </div>

          <div class="timeline-item reveal">
            <span class="timeline-number">05</span>
            <h3>Mendapatkan Nomor Antrean</h3>
            <p>
              Nomor antrean akan segera dikirimkan melalui WhatsApp.
            </p>
          </div>

          <div class="timeline-item reveal">
            <span class="timeline-number">06</span>
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
    <section class="section prescription-section" id="pelayanan-resep">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-prescription-bottle-medical"></i>
            Pelayanan Resep
          </div>

          <h2 class="section-title">
            Pelayanan Resep
          </h2>

          <p class="section-description">
            Proses pelayanan resep dilakukan secara bertahap untuk
            mendukung penggunaan obat yang tepat dan aman.
          </p>

        </div>


        <div class="prescription-intro reveal">
          Pasien menyerahkan resep kepada petugas atau apoteker.
          Resep kemudian diperiksa, obat disiapkan, diperiksa kembali,
          dan diserahkan kepada pasien disertai informasi mengenai
          penggunaan obat.
        </div>


        <div class="recipe-flow">

          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-file-prescription"></i>
            </div>

            <div class="recipe-content">
              <h3>1. Penerimaan Resep</h3>
              <p>
                Pasien menyerahkan resep kepada petugas/apoteker.
              </p>
            </div>
          </div>


          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-magnifying-glass"></i>
            </div>

            <div class="recipe-content">
              <h3>2. Pemeriksaan Resep</h3>
              <p>
                Resep diperiksa meliputi kelengkapan dan kesesuaian resep.
              </p>
            </div>
          </div>


          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-pills"></i>
            </div>

            <div class="recipe-content">
              <h3>3. Penyiapan Obat</h3>
              <p>
                Obat disiapkan sesuai resep.
              </p>
            </div>
          </div>


          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-clipboard-check"></i>
            </div>

            <div class="recipe-content">
              <h3>4. Pemeriksaan Kembali</h3>
              <p>
                Dilakukan pemeriksaan kembali terhadap obat yang telah
                disiapkan.
              </p>
            </div>
          </div>


          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-hand-holding-medical"></i>
            </div>

            <div class="recipe-content">
              <h3>5. Penyerahan Obat</h3>
              <p>
                Obat diserahkan kepada pasien.
              </p>
            </div>
          </div>


          <div class="recipe-step reveal">
            <div class="recipe-icon">
              <i class="fa-solid fa-comments"></i>
            </div>

            <div class="recipe-content">

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
            <div class="recipe-icon">
              <i class="fa-solid fa-circle-check"></i>
            </div>

            <div class="recipe-content">
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
    <section class="section" id="konsultasi">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-comments"></i>
            Konsultasi
          </div>

          <h2 class="section-title">
            Konsultasi Kefarmasian
          </h2>

          <p class="section-description">
            Kesempatan bagi pasien untuk menyampaikan pertanyaan
            atau permasalahan terkait penggunaan obat kepada apoteker.
          </p>

        </div>


        <div class="consult-grid">

          <!-- Chat -->
          <div class="chat-container reveal">

            <div class="chat-message">

              <div class="chat-avatar">
                <i class="fa-solid fa-user"></i>
              </div>

              <div class="chat-bubble">
                <span class="chat-name">Pasien</span>
                “Saya ingin berkonsultasi mengenai obat yang sedang
                saya gunakan.”
              </div>

            </div>


            <div class="chat-message pharmacist">

              <div class="chat-avatar">
                <i class="fa-solid fa-user-doctor"></i>
              </div>

              <div class="chat-bubble">
                <span class="chat-name">Apoteker</span>
                “Silakan sampaikan nama obat, aturan penggunaan,
                serta keluhan atau pertanyaan yang ingin dikonsultasikan.”
              </div>

            </div>

          </div>


          <!-- Konsultasi info -->
          <div class="card reveal">

            <div class="card-icon pink">
              <i class="fa-solid fa-user-doctor"></i>
            </div>

            <h3 style="margin-bottom:15px;">
              Pasien dapat berkonsultasi mengenai:
            </h3>

            <ul class="consult-list">

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Cara penggunaan obat</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Aturan pakai</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Waktu penggunaan obat</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Efek samping</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Interaksi obat</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Penyimpanan obat</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Penggunaan beberapa obat secara bersamaan</span>
              </li>

              <li>
                <i class="fa-solid fa-check"></i>
                <span>Permasalahan terkait penggunaan obat</span>
              </li>

            </ul>

            <a href="#apoteker" class="btn btn-primary" style="margin-top:22px;">
              <i class="fa-brands fa-whatsapp"></i>
              KONSULTASI DENGAN APOTEKER
            </a>

          </div>

        </div>


        <!-- Daftar apoteker -->
        <div id="apoteker" style="margin-top:35px;">

          <div class="section-header" style="margin-bottom:25px;">
            <h3 style="font-size:1.4rem;">
              Pilih Apoteker untuk Konsultasi
            </h3>
          </div>

          <div class="pharmacist-grid">

            <!-- Aisyah -->
            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <div class="pharmacist-avatar">
                  <i class="fa-solid fa-user-doctor"></i>
                </div>

                <div>
                  <h3>
                    apt. Aisyah Ramadhani Wijaya Putri, S.Farm
                  </h3>
                  <p>CP: 085232058261</p>
                </div>
              </div>

              <a
                href="https://wa.me/6285232058261"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-pink wa-small"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Konsultasi via WhatsApp
              </a>

            </div>


            <!-- Sasi -->
            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <div class="pharmacist-avatar">
                  <i class="fa-solid fa-user-doctor"></i>
                </div>

                <div>
                  <h3>
                    apt. Sasi Putri Mauritania, S.Farm
                  </h3>
                  <p>CP: 085334255376</p>
                </div>
              </div>

              <a
                href="https://wa.me/6285334255376"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-pink wa-small"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Konsultasi via WhatsApp
              </a>

            </div>


            <!-- Sri -->
            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <div class="pharmacist-avatar">
                  <i class="fa-solid fa-user-doctor"></i>
                </div>

                <div>
                  <h3>
                    apt. Sri Wahyuni, S.Farm
                  </h3>
                  <p>CP: 087757376296</p>
                </div>
              </div>

              <a
                href="https://wa.me/6287757376296"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-pink wa-small"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Konsultasi via WhatsApp
              </a>

            </div>


            <!-- Tyara -->
            <div class="pharmacist-card reveal">

              <div class="pharmacist-info">
                <div class="pharmacist-avatar">
                  <i class="fa-solid fa-user-doctor"></i>
                </div>

                <div>
                  <h3>
                    apt. Tyara Novelia Putri, S.Farm
                  </h3>
                  <p>CP: 085717420989</p>
                </div>
              </div>

              <a
                href="https://wa.me/6285717420989"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-pink wa-small"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Konsultasi via WhatsApp
              </a>

            </div>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         INFORMASI PELAYANAN
    ====================================================== -->
    <section class="section services-section" id="informasi-pelayanan">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-layer-group"></i>
            Informasi Pelayanan
          </div>

          <h2 class="section-title">
            Informasi Pelayanan
          </h2>

          <p class="section-description">
            Berbagai layanan kefarmasian yang dapat diperoleh pasien.
          </p>

        </div>


        <div class="cards">

          <article class="card service-card reveal">

            <div class="card-icon">
              <i class="fa-solid fa-prescription-bottle-medical"></i>
            </div>

            <h3>Pelayanan Resep</h3>

            <p>
              Pelayanan obat berdasarkan resep disertai informasi
              penggunaan obat.
            </p>

          </article>


          <article class="card service-card reveal">

            <div class="card-icon">
              <i class="fa-solid fa-leaf"></i>
            </div>

            <h3>Swamedikasi</h3>

            <p>
              Membantu pasien memperoleh informasi dalam penggunaan
              obat untuk keluhan ringan.
            </p>

          </article>


          <article class="card service-card reveal">

            <div class="card-icon pink">
              <i class="fa-solid fa-comments"></i>
            </div>

            <h3>Konsultasi Kefarmasian</h3>

            <p>
              Konsultasi pasien bersama apoteker mengenai penggunaan obat.
            </p>

          </article>


          <article class="card service-card reveal">

            <div class="card-icon">
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
    <section class="section contact-section" id="kontak">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-phone"></i>
            Kontak
          </div>

          <h2 class="section-title">
            Hubungi Kami
          </h2>

          <p class="section-description">
            Informasi lokasi dan kontak pelayanan kefarmasian.
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
                  Kec. Sumbersari, Kabupaten Jember,
                  Jawa Timur 68125
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
                  poltekesjember.ac.id
                </a>
              </div>

            </div>


            <div class="contact-buttons">

              <!-- Sesuai nomor yang diberikan -->
              <a
                href="https://wa.me/62331325930"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-primary"
              >
                <i class="fa-brands fa-whatsapp"></i>
                Hubungi via WhatsApp
              </a>

              <!-- Karena URL yang diberikan adalah website, bukan email -->
              <a
                href="https://poltekesjember.ac.id/"
                target="_blank"
                rel="noopener noreferrer"
                class="btn btn-secondary"
              >
                <i class="fa-solid fa-envelope"></i>
                Kirim Email
              </a>

            </div>

            <p style="font-size:.72rem;color:var(--text-light);margin-top:12px;">
              * Tombol “Kirim Email” saat ini diarahkan ke situs resmi karena
              alamat email belum dicantumkan.
            </p>

          </div>


          <!-- Google Maps -->
          <div class="map-wrapper reveal">

            <iframe
              title="Lokasi Klinik Poltekes Jember"
              src="https://www.google.com/maps?q=Jl.%20Pangandaran%20No.42,%20Plinggan,%20Antirogo,%20Kec.%20Sumbersari,%20Kabupaten%20Jember,%20Jawa%20Timur%2068125&output=embed"
              loading="lazy"
              allowfullscreen
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>

          </div>

        </div>

      </div>
    </section>


    <!-- =====================================================
         FAQ
    ====================================================== -->
    <section class="section" id="faq">

      <div class="container">

        <div class="section-header reveal">

          <div class="section-label">
            <i class="fa-solid fa-circle-question"></i>
            FAQ
          </div>

          <h2 class="section-title">
            Pertanyaan yang Sering Diajukan
          </h2>

          <p class="section-description">
            Informasi singkat untuk membantu pasien menggunakan website.
          </p>

        </div>


        <div class="faq-list">

          <div class="faq-item reveal">

            <button class="faq-question">
              <span>Bagaimana cara mendaftar pelayanan?</span>
              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              Pasien dapat menekan tombol “Daftar Sekarang” dan
              mengisi Google Form yang tersedia.
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>Apakah semua pasien dapat melakukan pendaftaran?</span>
              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              Ya, formulir dapat digunakan oleh pasien yang membutuhkan
              pelayanan sesuai dengan jenis pelayanan yang tersedia.
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>Apakah nomor BPJS wajib diisi?</span>
              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              Tidak. Nomor BPJS dapat dikosongkan apabila pasien tidak
              memiliki BPJS.
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>Bagaimana saya mendapatkan nomor antrean?</span>
              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              Nomor antrean akan segera dikirimkan melalui WhatsApp
              ke nomor yang dicantumkan pada formulir.
            </div>

          </div>


          <div class="faq-item reveal">

            <button class="faq-question">
              <span>Bagaimana urutan antreannya?</span>
              <i class="fa-solid fa-chevron-down"></i>
            </button>

            <div class="faq-answer">
              Urutan antrean mengikuti urutan waktu pengiriman formulir.
              Pasien yang mengirimkan formulir terlebih dahulu mendapatkan
              urutan terlebih dahulu.
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
              Pasien datang ke tempat pelayanan sesuai nomor antrean
              yang telah diberikan.
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

    <div class="container">

      <div class="footer-grid">

        <div class="footer-brand">

          <h2>PELAYANAN KEFARMASIAN</h2>

          <p>
            “Mudah Mendaftar, Nyaman Mendapatkan Pelayanan”
          </p>

        </div>


        <div>

          <h3 class="footer-title">
            Navigasi
          </h3>

          <div class="footer-links">

            <a href="#beranda">Beranda</a>
            <a href="#pengertian">Pengertian</a>
            <a href="#alur-pendaftaran">Alur Pendaftaran</a>
            <a href="#pelayanan-resep">Pelayanan Resep</a>
            <a href="#konsultasi">Konsultasi</a>
            <a href="#kontak">Kontak</a>

          </div>

        </div>


        <div>

          <h3 class="footer-title">
            Kontak
          </h3>

          <div class="footer-contact">

            <span>
              <i class="fa-solid fa-location-dot"></i>
              Jl. Pangandaran No.42, Plinggan, Antirogo,
              Kec. Sumbersari, Kabupaten Jember,
              Jawa Timur 68125
            </span>

            <span>
              <i class="fa-solid fa-phone"></i>
              (0331) 325930
            </span>

            <a
              href="https://poltekesjember.ac.id/"
              target="_blank"
              rel="noopener noreferrer"
            >
              <i class="fa-solid fa-globe"></i>
              poltekesjember.ac.id
            </a>

          </div>

        </div>

      </div>


      <div class="footer-bottom">
        © <span id="year"></span> Pelayanan Kefarmasian Klinik Poltekes Jember.
        Semua hak dilindungi.
      </div>

    </div>

  </footer>


  <!-- Toast -->
  <div class="toast" id="toast">
    <i class="fa-solid fa-arrow-up-right-from-square"></i>
    Formulir pendaftaran akan dibuka di tab baru.
  </div>


  <!-- Back to top -->
  <button
    class="back-top"
    id="backTop"
    aria-label="Kembali ke atas"
  >
    <i class="fa-solid fa-arrow-up"></i>
  </button>


  <script>
    /* =========================================================
       KONFIGURASI WEBSITE
       Jika ingin mengganti Google Form, cukup ubah URL di bawah.
    ========================================================= */

    const GOOGLE_FORM_URL =
      "https://forms.gle/jG8p9wozy5nmoMrS8";

    const OFFICIAL_SITE_URL =
      "https://poltekesjember.ac.id/";


    /* =========================================================
       SET SEMUA LINK PENDAFTARAN
    ========================================================= */

    document.querySelectorAll("[data-registration-link]").forEach(link => {
      link.href = GOOGLE_FORM_URL;
      link.target = "_blank";
      link.rel = "noopener noreferrer";

      link.addEventListener("click", function () {
        showToast();
      });
    });


    /* =========================================================
       MOBILE NAVBAR
    ========================================================= */

    const menuToggle = document.getElementById("menuToggle");
    const navMenu = document.getElementById("navMenu");

    menuToggle.addEventListener("click", () => {

      const isActive = navMenu.classList.toggle("active");

      menuToggle.setAttribute(
        "aria-expanded",
        isActive ? "true" : "false"
      );

      menuToggle.innerHTML = isActive
        ? '<i class="fa-solid fa-xmark"></i>'
        : '<i class="fa-solid fa-bars"></i>';
    });


    /* Tutup menu ketika link internal diklik */

    document.querySelectorAll(".nav-link").forEach(link => {

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
       TOAST
    ========================================================= */

    const toast = document.getElementById("toast");
    let toastTimer;

    function showToast() {

      toast.classList.add("show");

      clearTimeout(toastTimer);

      toastTimer = setTimeout(() => {
        toast.classList.remove("show");
      }, 2500);

    }


    /* =========================================================
       FAQ ACCORDION
    ========================================================= */

    document.querySelectorAll(".faq-question").forEach(question => {

      question.addEventListener("click", () => {

        const item = question.parentElement;

        document.querySelectorAll(".faq-item").forEach(otherItem => {

          if (otherItem !== item) {
            otherItem.classList.remove("active");
          }

        });

        item.classList.toggle("active");

      });

    });


    /* =========================================================
       SCROLL REVEAL
    ========================================================= */

    const revealElements =
      document.querySelectorAll(".reveal");

    const observer =
      new IntersectionObserver(
        (entries) => {

          entries.forEach(entry => {

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

    revealElements.forEach(element => {
      observer.observe(element);
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
       CURRENT YEAR
    ========================================================= */

    document.getElementById("year").textContent =
      new Date().getFullYear();


    /* =========================================================
       CLOSE MOBILE MENU WHEN CLICKING OUTSIDE
    ========================================================= */

    document.addEventListener("click", (event) => {

      const clickedInsideMenu =
        navMenu.contains(event.target);

      const clickedToggle =
        menuToggle.contains(event.target);

      if (
        window.innerWidth < 900 &&
        navMenu.classList.contains("active") &&
        !clickedInsideMenu &&
        !clickedToggle
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
