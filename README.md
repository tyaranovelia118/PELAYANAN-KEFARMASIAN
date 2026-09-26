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
            font-family: Arial, Helvetica, sans-serif;
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
            background-color: white;
            display: flex;
            justify-content: center;
            flex-wrap: wrap;
            gap: 8px;
            padding: 15px;
            position: sticky;
            top: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.12);
        }

        nav a {
            text-decoration: none;
            color: #087f5b;
            font-weight: bold;
            padding: 10px 16px;
            border-radius: 25px;
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
            background-color: #e5f7f0;
        }

        .hero h2 {
            font-size: 35px;
            color: #087f5b;
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
            padding: 13px 28px;
            background-color: #087f5b;
            color: white;
            text-decoration: none;
            border-radius: 30px;
            font-weight: bold;
            transition: 0.3s;
        }

        .button:hover {
            background-color: #055c42;
            transform: translateY(-2px);
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
            grid-template-columns: repeat(auto-fit, minmax(270px, 1fr));
            gap: 25px;
        }

        .card {
            background-color: white;
            padding: 28px;
            border-radius: 16px;
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
            padding: 22px;
            border-left: 6px solid #20c997;
            border-radius: 10px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
        }

        .step h3 {
            color: #087f5b;
            margin-bottom: 6px;
        }

        /* PENDAFTARAN */
        .registration {
            background-color: #e5f7f0;
        }

        .registration-box {
            max-width: 850px;
            margin: auto;
            background-color: white;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
            text-align: center;
        }

        .registration-box h3 {
            color: #087f5b;
            font-size: 24px;
            margin-bottom: 15px;
        }

        .registration-box p {
            margin-bottom: 12px;
        }

        .important {
            background-color: #fff8e1;
            border-left: 5px solid #f0ad4e;
            padding: 18px;
            margin-top: 20px;
            text-align: left;
            border-radius: 8px;
        }

        .important strong {
            color: #9a6700;
        }

        /* KONSULTASI */
        .consultation {
            background-color: #eef9f5;
        }

        /* KONTAK */
        .contact {
            background-color: #e5f7f0;
        }

        .contact-box {
            max-width: 800px;
            margin: auto;
            background-color: white;
            padding: 35px;
            border-radius: 18px;
            box-shadow: 0 4px 15px rgba(0,0,0,0.08);
        }

        .contact-item {
            margin-bottom: 20px;
        }

        .contact-item h3 {
            color: #087f5b;
            margin-bottom: 5px;
        }

        .contact-item a {
            color: #087f5b;
            text-decoration: none;
            font-weight: bold;
        }

        .contact-item a:hover {
            text-decoration: underline;
        }

        /* FOOTER */
        footer {
            background-color: #055c42;
            color: white;
            text-align: center;
            padding: 25px;
        }

        /* RESPONSIVE */
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


<!-- ================= HEADER ================= -->

<header>

    <h1>PELAYANAN KEFARMASIAN</h1>

    <p>
        Informasi, Pendaftaran, Pelayanan Resep, dan Konsultasi Kefarmasian
    </p>

</header>



<!-- ================= NAVIGASI ================= -->

<nav>

    <a href="#pengertian">💊 Pengertian</a>

    <a href="#pendaftaran">📝 Pendaftaran</a>

    <a href="#resep">💊 Pelayanan Resep</a>

    <a href="#konsultasi">🩺 Konsultasi</a>

    <a href="#kontak">📞 Kontak</a>

</nav>



<!-- ================= HERO ================= -->

<div class="hero">

    <h2>
        Selamat Datang di Website Pelayanan Kefarmasian
    </h2>

    <p>
        Website ini menyediakan informasi mengenai pelayanan kefarmasian,
        pendaftaran pasien, pelayanan resep, konsultasi dengan apoteker,
        serta informasi kontak yang dapat dihubungi.
    </p>

    <a href="#pendaftaran" class="button">
        Daftar Pelayanan
    </a>

</div>



<!-- ================= PENGERTIAN ================= -->

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
                    nama obat, manfaat, dosis, aturan pakai,
                    waktu penggunaan, efek samping, interaksi obat,
                    dan cara penyimpanan obat.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- ================= PENDAFTARAN ================= -->

<section id="pendaftaran" class="registration">

    <div class="container">

        <h2>
            📝 Pendaftaran Pelayanan
        </h2>


        <div class="registration-box">

            <h3>
                Daftar Pelayanan Secara Online
            </h3>

            <p>
                Pasien dapat melakukan pendaftaran secara online
                dengan mengisi formulir yang telah disediakan.
            </p>

            <p>
                Data yang perlu disiapkan antara lain:
            </p>


            <div class="cards">

                <div class="card">

                    <h3>👤 Nama Pasien</h3>

                    <p>
                        Masukkan nama lengkap pasien yang akan
                        mendapatkan pelayanan.
                    </p>

                </div>


                <div class="card">

                    <h3>🪪 Nomor BPJS</h3>

                    <p>
                        Masukkan nomor BPJS apabila pasien memiliki
                        kepesertaan BPJS.
                    </p>

                </div>


                <div class="card">

                    <h3>🩺 Keluhan</h3>

                    <p>
                        Tuliskan keluhan atau kebutuhan pelayanan
                        yang dirasakan pasien.
                    </p>

                </div>


                <div class="card">

                    <h3>📱 Nomor WhatsApp</h3>

                    <p>
                        Masukkan nomor WhatsApp yang aktif dan
                        dapat dihubungi.
                    </p>

                </div>

            </div>


            <!-- TOMBOL GOOGLE FORM -->

            <a
                href="MASUKKAN-LINK-GOOGLE-FORM-DI-SINI"
                target="_blank"
                class="button">

                📋 Isi Formulir Pendaftaran

            </a>


            <div class="important">

                <strong>
                    ⚠️ Informasi Nomor Antrean
                </strong>

                <p>
                    Setelah melakukan pendaftaran, nomor antrean
                    akan segera dikirimkan melalui WhatsApp pada
                    nomor yang telah dicantumkan dalam formulir.
                </p>

                <p>
                    <strong>
                        Urutan antrean akan diambil berdasarkan
                        urutan pasien yang mengirimkan formulir
                        pendaftaran terlebih dahulu.
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



<!-- ================= ALUR PENDAFTARAN ================= -->

<section>

    <div class="container">

        <h2>
            📋 Alur Pendaftaran Pelayanan
        </h2>


        <div class="alur">


            <div class="step">

                <h3>
                    1. Membuka Formulir Pendaftaran
                </h3>

                <p>
                    Pasien membuka tautan formulir pendaftaran
                    yang tersedia pada website.
                </p>

            </div>


            <div class="step">

                <h3>
                    2. Mengisi Data Pasien
                </h3>

                <p>
                    Pasien mengisi nama, nomor BPJS jika ada,
                    keluhan, dan nomor WhatsApp yang dapat
                    dihubungi.
                </p>

            </div>


            <div class="step">

                <h3>
                    3. Mengirim Formulir
                </h3>

                <p>
                    Setelah semua data diisi dengan benar,
                    pasien mengirimkan formulir pendaftaran.
                </p>

            </div>


            <div class="step">

                <h3>
                    4. Menunggu Nomor Antrean
                </h3>

                <p>
                    Petugas menerima data pendaftaran dan
                    menentukan nomor antrean berdasarkan
                    urutan pengiriman formulir.
                </p>

            </div>


            <div class="step">

                <h3>
                    5. Nomor Antrean Dikirim
                </h3>

                <p>
                    Nomor antrean akan dikirimkan melalui
                    WhatsApp ke nomor yang telah dicantumkan
                    oleh pasien.
                </p>

            </div>


            <div class="step">

                <h3>
                    6. Mendapatkan Pelayanan
                </h3>

                <p>
                    Pasien datang dan mendapatkan pelayanan
                    sesuai dengan kebutuhan.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- ================= PELAYANAN RESEP ================= -->

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
                    memperoleh obat sesuai resep dan mendapatkan
                    informasi yang benar mengenai penggunaan
                    obat.
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
                    Obat diberi etiket yang berisi informasi
                    penting mengenai pasien dan aturan
                    penggunaan obat.
                </p>

            </div>


            <div class="step">

                <h3>
                    5. Pemeriksaan Akhir
                </h3>

                <p>
                    Petugas melakukan pemeriksaan kembali
                    untuk memastikan obat telah sesuai
                    dengan resep.
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
                    waktu penggunaan, penyimpanan, dan
                    informasi penting lainnya.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- ================= KONSULTASI ================= -->

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
                    langsung dengan apoteker mengenai penggunaan
                    obat dan masalah yang berkaitan dengan
                    terapi obat.
                </p>

            </div>


            <div class="card">

                <h3>
                    Hal yang Dapat Ditanyakan
                </h3>

                <p>
                    Pasien dapat menanyakan cara penggunaan obat,
                    aturan pakai, waktu penggunaan, efek samping,
                    interaksi obat, penyimpanan obat, serta
                    hal-hal lain yang berkaitan dengan penggunaan
                    obat.
                </p>

            </div>


            <div class="card">

                <h3>
                    Proses Konsultasi
                </h3>

                <p>
                    Pasien menyampaikan pertanyaan atau keluhan
                    kepada apoteker. Apoteker melakukan penggalian
                    informasi yang diperlukan kemudian memberikan
                    informasi dan edukasi sesuai kebutuhan pasien.
                </p>

            </div>


        </div>


        <div style="text-align:center;">

            <a
                href="https://wa.me/6285717420989"
                target="_blank"
                class="button">

                💬 Konsultasi melalui WhatsApp

            </a>

        </div>

    </div>

</section>



<!-- ================= KONTAK ================= -->

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



<!-- ================= FOOTER ================= -->

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
