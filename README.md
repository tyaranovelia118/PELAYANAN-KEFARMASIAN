<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Pelayanan Kefarmasian</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: Arial, sans-serif;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            background: #f5faf8;
            color: #333;
            line-height: 1.7;
        }

        /* HEADER */
        header {
            background: linear-gradient(135deg, #087f5b, #20c997);
            color: white;
            text-align: center;
            padding: 55px 20px;
        }

        header h1 {
            font-size: 40px;
            margin-bottom: 10px;
        }

        header p {
            font-size: 18px;
        }

        /* NAVIGASI */
        nav {
            background: white;
            padding: 14px;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }

        nav a {
            text-decoration: none;
            color: #087f5b;
            font-weight: bold;
            padding: 10px 16px;
            border-radius: 25px;
        }

        nav a:hover {
            background: #087f5b;
            color: white;
        }

        /* HERO */
        .hero {
            text-align: center;
            padding: 75px 20px;
            background: #e5f7f0;
        }

        .hero h2 {
            color: #087f5b;
            font-size: 34px;
            margin-bottom: 15px;
        }

        .hero p {
            max-width: 850px;
            margin: auto;
            font-size: 18px;
        }

        .button {
            display: inline-block;
            margin-top: 25px;
            padding: 14px 28px;
            background: #087f5b;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
        }

        .button:hover {
            background: #055c42;
        }

        /* SECTION */
        section {
            padding: 65px 8%;
        }

        .container {
            max-width: 1100px;
            margin: auto;
        }

        section h2 {
            text-align: center;
            color: #087f5b;
            font-size: 30px;
            margin-bottom: 35px;
        }

        /* CARD */
        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }

        .card {
            background: white;
            padding: 28px;
            border-radius: 16px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .card h3 {
            color: #087f5b;
            margin-bottom: 12px;
        }

        /* PENDAFTARAN */
        .registration {
            background: #e5f7f0;
        }

        .registration-box {
            background: white;
            max-width: 900px;
            margin: auto;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            text-align: center;
        }

        .registration-box h3 {
            color: #087f5b;
            font-size: 25px;
            margin-bottom: 15px;
        }

        .form-data {
            text-align: left;
            margin: 25px auto;
            max-width: 650px;
        }

        .form-data li {
            margin: 10px 0;
        }

        .notice {
            background: #fff7df;
            border-left: 5px solid #e0a800;
            padding: 18px;
            margin-top: 25px;
            text-align: left;
            border-radius: 8px;
        }

        .notice strong {
            color: #856404;
        }

        /* ALUR */
        .alur {
            max-width: 850px;
            margin: auto;
        }

        .step {
            background: white;
            padding: 22px;
            margin-bottom: 18px;
            border-left: 6px solid #20c997;
            border-radius: 10px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
        }

        .step h3 {
            color: #087f5b;
            margin-bottom: 6px;
        }

        /* KONSULTASI */
        .consultation {
            background: #eef9f5;
        }

        /* KONTAK */
        .contact {
            background: #e5f7f0;
        }

        .contact-box {
            max-width: 800px;
            margin: auto;
            background: white;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .contact-item {
            margin-bottom: 22px;
        }

        .contact-item h3 {
            color: #087f5b;
            margin-bottom: 5px;
        }

        .contact-item a {
            color: #087f5b;
            font-weight: bold;
            text-decoration: none;
        }

        /* FOOTER */
        footer {
            background: #055c42;
            color: white;
            text-align: center;
            padding: 25px;
        }

        @media (max-width: 650px) {

            header h1 {
                font-size: 29px;
            }

            .hero h2 {
                font-size: 27px;
            }

            nav {
                flex-direction: column;
                align-items: center;
            }

            nav a {
                width: 100%;
                text-align: center;
            }

            section {
                padding: 45px 20px;
            }
        }
    </style>
</head>

<body>

<!-- HEADER -->
<header>

    <h1>PELAYANAN KEFARMASIAN</h1>

    <p>
        Informasi, Pendaftaran, Pelayanan Resep, dan Konsultasi Kefarmasian
    </p>

</header>


<!-- NAVIGASI -->
<nav>

    <a href="#pengertian">💊 Pengertian</a>

    <a href="#pendaftaran">📝 Pendaftaran</a>

    <a href="#resep">💊 Pelayanan Resep</a>

    <a href="#konsultasi">🩺 Konsultasi</a>

    <a href="#kontak">📞 Kontak</a>

</nav>


<!-- HERO -->
<div class="hero">

    <h2>
        Selamat Datang di Website Pelayanan Kefarmasian
    </h2>

    <p>
        Website ini menyediakan informasi mengenai pelayanan kefarmasian,
        pendaftaran pasien secara online, pelayanan resep, konsultasi
        dengan apoteker, serta informasi kontak yang dapat dihubungi.
    </p>

    <a href="#pendaftaran" class="button">
        📝 Daftar Pelayanan
    </a>

</div>


<!-- PENGERTIAN -->
<section id="pengertian">

    <div class="container">

        <h2>
            💊 Pengertian Pelayanan Kefarmasian
        </h2>

        <div class="cards">

            <div class="card">

                <h3>
                    Apa Itu Pelayanan Kefarmasian?
                </h3>

                <p>
                    Pelayanan kefarmasian merupakan pelayanan yang
                    diberikan oleh tenaga kefarmasian kepada pasien
                    yang berkaitan dengan penggunaan obat dan
                    sediaan farmasi.
                </p>

                <p>
                    Pelayanan kefarmasian tidak hanya berfokus
                    pada penyediaan obat, tetapi juga mencakup
                    pemberian informasi obat, komunikasi, edukasi,
                    konseling, serta pemantauan penggunaan obat.
                </p>

            </div>


            <div class="card">

                <h3>
                    Tujuan Pelayanan
                </h3>

                <p>
                    Pelayanan kefarmasian bertujuan membantu pasien
                    mendapatkan obat yang sesuai serta memahami
                    cara penggunaan obat secara tepat, aman,
                    dan efektif.
                </p>

            </div>


            <div class="card">

                <h3>
                    Manfaat bagi Pasien
                </h3>

                <p>
                    Pasien dapat memperoleh informasi mengenai
                    nama obat, manfaat obat, dosis, aturan pakai,
                    waktu penggunaan, efek samping, interaksi obat,
                    dan cara penyimpanan obat.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- PENDAFTARAN -->
<section id="pendaftaran" class="registration">

    <div class="container">

        <h2>
            📝 Pendaftaran Pelayanan
        </h2>

        <div class="registration-box">

            <h3>
                Daftar Pelayanan Pasien Secara Online
            </h3>

            <p>
                Pasien dapat melakukan pendaftaran dengan
                mengisi formulir Google Form melalui tombol
                di bawah ini.
            </p>

            <div class="form-data">

                <p>
                    <strong>Data yang perlu diisi:</strong>
                </p>

                <ul>

                    <li>
                        👤 Nama pasien
                    </li>

                    <li>
                        🪪 Nomor BPJS (jika ada)
                    </li>

                    <li>
                        🩺 Keluhan pasien
                    </li>

                    <li>
                        📱 Nomor WhatsApp yang dapat dihubungi
                    </li>

                </ul>

            </div>


            <!--
            (https://forms.gle/ehZyvSKFYmZqqdLK8)
            -->

            <a
                href="MASUKKAN-LINK-GOOGLE-FORM-KAMU-DI-SINI"
                target="_blank"
                class="button">

                📋 BUKA FORMULIR PENDAFTARAN

            </a>


            <div class="notice">

                <strong>
                    ⚠️ Informasi Nomor Antrean
                </strong>

                <p>
                    Setelah pasien mengirimkan formulir,
                    nomor antrean akan segera dikirimkan
                    melalui WhatsApp ke nomor yang telah
                    dicantumkan pada formulir.
                </p>

                <p>
                    <strong>
                        Urutan antrean akan diambil berdasarkan
                        urutan pasien yang mengirimkan formulir
                        terlebih dahulu.
                    </strong>
                </p>

                <p>
                    Pastikan nomor WhatsApp yang dicantumkan
                    aktif dan dapat menerima pesan.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- ALUR PENDAFTARAN -->
<section>

    <div class="container">

        <h2>
            📋 Alur Pendaftaran Pelayanan
        </h2>

        <div class="alur">

            <div class="step">

                <h3>
                    1. Buka Formulir Pendaftaran
                </h3>

                <p>
                    Pasien menekan tombol "Buka Formulir
                    Pendaftaran" pada website.
                </p>

            </div>


            <div class="step">

                <h3>
                    2. Isi Data Pasien
                </h3>

                <p>
                    Pasien mengisi nama pasien, nomor BPJS
                    jika ada, keluhan, dan nomor WhatsApp
                    yang aktif.
                </p>

            </div>


            <div class="step">

                <h3>
                    3. Kirim Formulir
                </h3>

                <p>
                    Setelah memastikan data sudah benar,
                    pasien menekan tombol kirim pada Google Form.
                </p>

            </div>


            <div class="step">

                <h3>
                    4. Menunggu Nomor Antrean
                </h3>

                <p>
                    Data pendaftaran diterima oleh petugas
                    dan antrean disusun berdasarkan urutan
                    pengiriman formulir.
                </p>

            </div>


            <div class="step">

                <h3>
                    5. Nomor Antrean Dikirim melalui WhatsApp
                </h3>

                <p>
                    Nomor antrean akan segera dikirimkan
                    melalui WhatsApp ke nomor yang telah
                    diberikan oleh pasien.
                </p>

            </div>


            <div class="step">

                <h3>
                    6. Pasien Mendapatkan Pelayanan
                </h3>

                <p>
                    Pasien datang dan mendapatkan pelayanan
                    sesuai dengan kebutuhan.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- PELAYANAN RESEP -->
<section id="resep">

    <div class="container">

        <h2>
            💊 Pelayanan Resep
        </h2>

        <div class="cards">

            <div class="card">

                <h3>
                    Pengertian Pelayanan Resep
                </h3>

                <p>
                    Pelayanan resep merupakan rangkaian kegiatan
                    pelayanan kefarmasian berdasarkan resep yang
                    diterima dari pasien.
                </p>

                <p>
                    Pelayanan dilakukan mulai dari penerimaan
                    resep, pemeriksaan resep, penyiapan obat,
                    pemberian etiket, pemeriksaan akhir,
                    hingga penyerahan obat kepada pasien.
                </p>

            </div>


            <div class="card">

                <h3>
                    Tujuan Pelayanan Resep
                </h3>

                <p>
                    Pelayanan resep bertujuan memastikan pasien
                    memperoleh obat sesuai resep serta mendapatkan
                    informasi yang benar mengenai penggunaan obat.
                </p>

            </div>

        </div>


        <h2 style="margin-top:55px;">
            📋 Alur Pelayanan Resep
        </h2>


        <div class="alur">

            <div class="step">

                <h3>
                    1. Penerimaan Resep
                </h3>

                <p>
                    Resep diterima oleh petugas dan dilakukan
                    pemeriksaan awal terhadap kelengkapan
                    dan kejelasan resep.
                </p>

            </div>


            <div class="step">

                <h3>
                    2. Pemeriksaan Resep
                </h3>

                <p>
                    Dilakukan pemeriksaan administratif,
                    farmasetik, dan klinis sesuai dengan
                    ketentuan pelayanan kefarmasian.
                </p>

            </div>


            <div class="step">

                <h3>
                    3. Penyiapan Obat
                </h3>

                <p>
                    Obat disiapkan sesuai dengan resep,
                    termasuk mengambil, menghitung,
                    dan mengemas obat.
                </p>

            </div>


            <div class="step">

                <h3>
                    4. Pemberian Etiket
                </h3>

                <p>
                    Obat diberi etiket yang memuat informasi
                    mengenai pasien dan aturan penggunaan obat.
                </p>

            </div>


            <div class="step">

                <h3>
                    5. Pemeriksaan Akhir
                </h3>

                <p>
                    Dilakukan pemeriksaan kembali untuk
                    memastikan obat telah sesuai dengan resep.
                </p>

            </div>


            <div class="step">

                <h3>
                    6. Penyerahan Obat dan KIE
                </h3>

                <p>
                    Obat diserahkan kepada pasien disertai
                    Komunikasi, Informasi, dan Edukasi (KIE)
                    mengenai cara penggunaan, aturan pakai,
                    waktu penggunaan, penyimpanan, serta
                    informasi penting lainnya.
                </p>

            </div>

        </div>

    </div>

</section>


<!-- KONSULTASI -->
<section id="konsultasi" class="consultation">

    <div class="container">

        <h2>
            🩺 Konsultasi Kefarmasian
        </h2>

        <div class="cards">

            <div class="card">

                <h3>
                    Konsultasi Pasien dengan Apoteker
                </h3>

                <p>
                    Konsultasi kefarmasian merupakan pelayanan
                    yang memungkinkan pasien berkonsultasi
                    dengan apoteker mengenai penggunaan obat
                    dan masalah yang berkaitan dengan terapi obat.
                </p>

            </div>


            <div class="card">

                <h3>
                    Hal yang Dapat Dikonsultasikan
                </h3>

                <p>
                    Pasien dapat menanyakan cara penggunaan obat,
                    aturan pakai, waktu penggunaan, efek samping,
                    interaksi obat, penyimpanan obat, serta
                    pertanyaan lain mengenai penggunaan obat.
                </p>

            </div>


            <div class="card">

                <h3>
                    Proses Konsultasi
                </h3>

                <p>
                    Pasien menyampaikan pertanyaan atau keluhan
                    kepada apoteker. Apoteker kemudian melakukan
                    penggalian informasi dan memberikan informasi
                    serta edukasi sesuai kebutuhan pasien.
                </p>

            </div>

        </div>


        <div style="text-align:center;">

            <a
                href="https://wa.me/6285717420989"
                target="_blank"
                class="button">

                💬 Hubungi Apoteker melalui WhatsApp

            </a>

        </div>

    </div>

</section>


<!-- KONTAK -->
<section id="kontak" class="contact">

    <div class="container">

        <h2>
            📞 Kontak yang Dapat Dihubungi
        </h2>

        <div class="contact-box">

            <div class="contact-item">

                <h3>
                    📍 Alamat
                </h3>

                <p>
                    Jl. Pangandaran No. 77,
                    Kelurahan Antirogo,
                    Kecamatan Sumbersari,
                    Kabupaten Jember
                </p>

            </div>


            <div class="contact-item">

                <h3>
                    📱 WhatsApp
                </h3>

                <p>

                    <a
                        href="https://wa.me/6285717420989"
                        target="_blank">

                        0857-1742-0989

                    </a>

                </p>

                <p>
                    Klik nomor WhatsApp untuk menghubungi
                    pelayanan kefarmasian.
                </p>

            </div>


            <div class="contact-item">

                <h3>
                    📧 Email
                </h3>

                <p>

                    <a
                        href="mailto:tyaranovelia118@gmail.com">

                        tyaranovelia118@gmail.com

                    </a>

                </p>

            </div>

        </div>

    </div>

</section>


<!-- FOOTER -->
<footer>

    <p>
        © 2026 Pelayanan Kefarmasian
    </p>

    <p>
        Informasi dan Edukasi Pelayanan Kefarmasian
    </p>

</footer>


</body>
</html>
