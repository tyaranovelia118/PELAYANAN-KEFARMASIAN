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
            background-color: #f4faf7;
            color: #333;
            line-height: 1.7;
        }

        /* HEADER */
        header {
            background: linear-gradient(135deg, #087f5b, #20c997);
            color: white;
            padding: 45px 20px;
            text-align: center;
        }

        header h1 {
            font-size: 38px;
            margin-bottom: 10px;
        }

        header p {
            font-size: 18px;
        }

        /* NAVBAR */
        nav {
            background-color: white;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 10px;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 8px rgba(0,0,0,0.12);
        }

        nav a {
            text-decoration: none;
            color: #087f5b;
            font-weight: bold;
            padding: 10px 18px;
            border-radius: 20px;
            transition: 0.3s;
        }

        nav a:hover {
            background-color: #087f5b;
            color: white;
        }

        /* HERO */
        .hero {
            text-align: center;
            padding: 75px 20px;
            background-color: #e6f7f1;
        }

        .hero h2 {
            font-size: 35px;
            color: #087f5b;
            margin-bottom: 15px;
        }

        .hero p {
            max-width: 800px;
            margin: auto;
            font-size: 18px;
        }

        .button {
            display: inline-block;
            margin-top: 25px;
            background-color: #087f5b;
            color: white;
            text-decoration: none;
            padding: 12px 25px;
            border-radius: 25px;
            font-weight: bold;
        }

        .button:hover {
            background-color: #055c42;
        }

        /* SECTION */
        section {
            padding: 65px 8%;
        }

        section h2 {
            text-align: center;
            color: #087f5b;
            font-size: 30px;
            margin-bottom: 35px;
        }

        /* CARD */
        .container {
            max-width: 1100px;
            margin: auto;
        }

        .cards {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
            gap: 25px;
        }

        .card {
            background-color: white;
            padding: 28px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .card h3 {
            color: #087f5b;
            margin-bottom: 12px;
        }

        /* ALUR */
        .alur {
            max-width: 850px;
            margin: auto;
        }

        .step {
            background-color: white;
            margin-bottom: 18px;
            padding: 20px;
            border-left: 6px solid #20c997;
            border-radius: 8px;
            box-shadow: 0 3px 10px rgba(0,0,0,0.08);
        }

        .step h3 {
            color: #087f5b;
            margin-bottom: 5px;
        }

        /* KONSULTASI */
        .konsultasi {
            background-color: #e6f7f1;
        }

        /* KONTAK */
        .kontak {
            background-color: #e6f7f1;
        }

        .contact-box {
            max-width: 750px;
            margin: auto;
            background-color: white;
            padding: 30px;
            border-radius: 15px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .contact-box p {
            margin: 15px 0;
        }

        .contact-box a {
            color: #087f5b;
            text-decoration: none;
            font-weight: bold;
        }

        /* FOOTER */
        footer {
            background-color: #055c42;
            color: white;
            text-align: center;
            padding: 25px;
        }

        /* MOBILE */
        @media (max-width: 600px) {

            header h1 {
                font-size: 28px;
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
            Informasi dan Panduan Pelayanan Kefarmasian
        </p>
    </header>


    <!-- NAVIGASI -->
    <nav>

        <a href="#pengertian">
            💊 Pengertian
        </a>

        <a href="#pendaftaran">
            📝 Pendaftaran
        </a>

        <a href="#resep">
            💊 Pelayanan Resep
        </a>

        <a href="#konsultasi">
            🩺 Konsultasi
        </a>

        <a href="#kontak">
            📞 Kontak
        </a>

    </nav>


    <!-- HERO -->
    <div class="hero">

        <h2>
            Selamat Datang di Website Pelayanan Kefarmasian
        </h2>

        <p>
            Website ini menyediakan informasi mengenai pelayanan
            kefarmasian, alur pendaftaran, pelayanan resep,
            konsultasi kefarmasian, serta informasi kontak
            yang dapat dihubungi.
        </p>

        <a href="#pengertian" class="button">
            Pelajari Selengkapnya
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
                        Pelayanan kefarmasian merupakan pelayanan
                        yang diberikan oleh tenaga kefarmasian
                        kepada pasien yang berkaitan dengan
                        penggunaan obat dan sediaan farmasi.
                    </p>

                    <p>
                        Pelayanan kefarmasian tidak hanya berfokus
                        pada penyediaan obat, tetapi juga mencakup
                        pemberian informasi obat, komunikasi,
                        edukasi, konseling, serta pemantauan
                        penggunaan obat.
                    </p>

                </div>


                <div class="card">

                    <h3>
                        Tujuan Pelayanan Kefarmasian
                    </h3>

                    <p>
                        Tujuan pelayanan kefarmasian adalah membantu
                        pasien memperoleh obat yang sesuai dan
                        menggunakan obat secara tepat, aman,
                        efektif, dan rasional.
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
                        serta cara penyimpanan obat.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- PENDAFTARAN -->
    <section id="pendaftaran">

        <div class="container">

            <h2>
                📝 Alur Pendaftaran Pelayanan
            </h2>

            <div class="alur">

                <div class="step">

                    <h3>
                        1. Mengisi Data Pendaftaran
                    </h3>

                    <p>
                        Pasien mengisi data diri yang diperlukan,
                        seperti nama, usia, nomor telepon,
                        dan informasi lain yang dibutuhkan.
                    </p>

                </div>


                <div class="step">

                    <h3>
                        2. Menyampaikan Keluhan
                    </h3>

                    <p>
                        Pasien menyampaikan keluhan, kebutuhan,
                        atau jenis pelayanan yang ingin diperoleh.
                    </p>

                </div>


                <div class="step">

                    <h3>
                        3. Verifikasi Data
                    </h3>

                    <p>
                        Petugas melakukan pemeriksaan dan
                        memastikan data pasien telah diisi
                        dengan benar.
                    </p>

                </div>


                <div class="step">

                    <h3>
                        4. Mendapatkan Pelayanan
                    </h3>

                    <p>
                        Pasien diarahkan untuk mendapatkan
                        pelayanan sesuai dengan kebutuhannya,
                        seperti pelayanan resep atau konsultasi.
                    </p>

                </div>


                <div class="step">

                    <h3>
                        5. Pelayanan Selesai
                    </h3>

                    <p>
                        Pasien menerima pelayanan dan informasi
                        yang diperlukan.
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
                        mendapatkan obat yang sesuai dengan resep
                        dan memperoleh informasi yang benar mengenai
                        cara penggunaan obat.
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
                        Petugas melakukan pemeriksaan administratif,
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
                        penyimpanan, serta hal penting lainnya.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- KONSULTASI -->
    <section id="konsultasi" class="konsultasi">

        <div class="container">

            <h2>
                🩺 Konsultasi Kefarmasian
            </h2>

            <div class="cards">

                <div class="card">

                    <h3>
                        Apa Itu Konsultasi Kefarmasian?
                    </h3>

                    <p>
                        Konsultasi kefarmasian merupakan pelayanan
                        yang membantu pasien memperoleh informasi
                        mengenai penggunaan obat dan hal-hal yang
                        berkaitan dengan terapi obat.
                    </p>

                </div>


                <div class="card">

                    <h3>
                        Hal yang Dapat Dikonsultasikan
                    </h3>

                    <p>
                        Pasien dapat berkonsultasi mengenai cara
                        penggunaan obat, aturan pakai, waktu
                        penggunaan, efek samping, interaksi obat,
                        penyimpanan obat, serta penggunaan obat
                        yang tepat dan aman.
                    </p>

                </div>


                <div class="card">

                    <h3>
                        Proses Konsultasi
                    </h3>

                    <p>
                        Pasien menyampaikan pertanyaan atau keluhan.
                        Selanjutnya tenaga kefarmasian melakukan
                        penggalian informasi dan memberikan
                        penjelasan sesuai dengan kebutuhan pasien.
                    </p>

                </div>

            </div>

        </div>

    </section>


    <!-- KONTAK -->
    <section id="kontak" class="kontak">

        <div class="container">

            <h2>
                📞 Kontak yang Dapat Dihubungi
            </h2>

            <div class="contact-box">

                <p>
                    <strong>📍 Alamat:</strong><br>
                    Masukkan alamat fasilitas pelayanan
                    kefarmasian di sini.
                </p>


                <p>
                    <strong>📱 WhatsApp:</strong><br>

                    <a href="https://wa.me/628xxxxxxxxxx"
                       target="_blank">

                        08xxxxxxxxxx

                    </a>

                </p>


                <p>
                    <strong>📧 Email:</strong><br>

                    <a href="mailto:emailanda@gmail.com">

                        emailanda@gmail.com

                    </a>

                </p>


                <p>
                    <strong>🕐 Jam Pelayanan:</strong><br>

                    Senin – Sabtu: 08.00 – 21.00 WIB

                </p>


                <p>
                    <strong>💬 Konsultasi:</strong><br>

                    Untuk informasi dan konsultasi lebih lanjut,
                    silakan menghubungi kontak yang tersedia.

                </p>

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
