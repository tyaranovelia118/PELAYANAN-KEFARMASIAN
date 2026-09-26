<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Pelayanan Kefarmasian</title>

    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(135deg, #e8fff7, #f5fffc, #e6f7ff);
            color: #263b35;
            line-height: 1.7;
        }

        /* HEADER */
        header {
            background: linear-gradient(135deg, #087f73, #16a085);
            color: white;
            padding: 25px 18px 30px;
            text-align: center;
            border-radius: 0 0 30px 30px;
            box-shadow: 0 5px 18px rgba(0,0,0,0.12);
        }

        header .icon {
            font-size: 45px;
            margin-bottom: 5px;
        }

        header h1 {
            font-size: 27px;
            margin-bottom: 5px;
        }

        header p {
            font-size: 14px;
            opacity: 0.95;
        }

        /* NAVIGASI */
        nav {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(255,255,255,0.96);
            backdrop-filter: blur(8px);
            padding: 10px 8px;
            box-shadow: 0 3px 12px rgba(0,0,0,0.08);
            overflow-x: auto;
            white-space: nowrap;
        }

        nav a {
            display: inline-block;
            color: #087f73;
            text-decoration: none;
            font-size: 12px;
            font-weight: bold;
            margin: 0 7px;
            padding: 7px 5px;
        }

        nav a:hover {
            color: #d68910;
        }

        /* CONTAINER */
        .container {
            width: 92%;
            max-width: 650px;
            margin: auto;
        }

        /* SECTION */
        section {
            padding: 25px 0;
            scroll-margin-top: 55px;
        }

        .section-title {
            text-align: center;
            color: #087f73;
            font-size: 22px;
            margin-bottom: 18px;
        }

        /* CARD */
        .card {
            background: rgba(255,255,255,0.95);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 15px;
            box-shadow: 0 5px 18px rgba(0,0,0,0.08);
            border: 1px solid rgba(22,160,133,0.12);
        }

        .card h3 {
            color: #087f73;
            font-size: 18px;
            margin-bottom: 10px;
        }

        .card p {
            font-size: 14px;
            text-align: justify;
        }

        /* HERO */
        .hero {
            padding: 30px 0 15px;
        }

        .hero-card {
            background: linear-gradient(135deg, #ffffff, #eafff8);
            border-radius: 25px;
            padding: 25px 20px;
            text-align: center;
            box-shadow: 0 8px 25px rgba(0,0,0,0.09);
        }

        .hero-card h2 {
            color: #087f73;
            font-size: 24px;
            margin-bottom: 10px;
        }

        .hero-card p {
            font-size: 14px;
            margin-bottom: 18px;
        }

        /* BUTTON */
        .button {
            display: block;
            width: 100%;
            text-align: center;
            text-decoration: none;
            background: linear-gradient(135deg, #087f73, #16a085);
            color: white;
            padding: 13px 15px;
            border-radius: 13px;
            font-size: 14px;
            font-weight: bold;
            margin-top: 12px;
            box-shadow: 0 5px 12px rgba(8,127,115,0.25);
            transition: 0.3s;
        }

        .button:hover {
            transform: translateY(-2px);
            opacity: 0.9;
        }

        .button-wa {
            background: linear-gradient(135deg, #20b878, #0da66f);
        }

        /* INFO BOX */
        .info-box {
            background: #fff8e7;
            border-left: 5px solid #f0a500;
            padding: 15px;
            border-radius: 12px;
            margin-top: 15px;
            font-size: 13px;
        }

        .info-box strong {
            color: #a66b00;
        }

        /* ALUR */
        .flow {
            display: flex;
            flex-direction: column;
            gap: 12px;
        }

        .flow-item {
            background: #f4fffc;
            border-radius: 16px;
            padding: 15px;
            display: flex;
            align-items: flex-start;
            gap: 12px;
            border: 1px solid #d6f1e9;
        }

        .number {
            min-width: 35px;
            height: 35px;
            background: #087f73;
            color: white;
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            font-weight: bold;
        }

        .flow-item h4 {
            color: #087f73;
            margin-bottom: 3px;
            font-size: 15px;
        }

        .flow-item p {
            font-size: 13px;
        }

        /* ICON GRID */
        .service-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 12px;
        }

        .service {
            background: white;
            border-radius: 17px;
            padding: 17px 10px;
            text-align: center;
            box-shadow: 0 4px 14px rgba(0,0,0,0.07);
        }

        .service .emoji {
            font-size: 30px;
            margin-bottom: 5px;
        }

        .service h4 {
            color: #087f73;
            font-size: 14px;
        }

        .service p {
            font-size: 11px;
            margin-top: 4px;
        }

        /* CONTACT */
        .contact-item {
            display: flex;
            gap: 12px;
            align-items: flex-start;
            padding: 12px 0;
            border-bottom: 1px solid #e5eeee;
        }

        .contact-item:last-child {
            border-bottom: none;
        }

        .contact-icon {
            font-size: 23px;
        }

        .contact-item strong {
            color: #087f73;
            font-size: 13px;
        }

        .contact-item p,
        .contact-item a {
            font-size: 13px;
            color: #333;
            text-decoration: none;
        }

        /* FOOTER */
        footer {
            background: linear-gradient(135deg, #087f73, #075e54);
            color: white;
            text-align: center;
            padding: 25px 15px;
            margin-top: 25px;
            border-radius: 30px 30px 0 0;
        }

        footer p {
            font-size: 12px;
        }

        /* MOBILE */
        @media (max-width: 480px) {

            header h1 {
                font-size: 24px;
            }

            .section-title {
                font-size: 20px;
            }

            .hero-card h2 {
                font-size: 21px;
            }

            .container {
                width: 93%;
            }

            nav a {
                font-size: 11px;
                margin: 0 5px;
            }
        }
    </style>
</head>

<body>

<!-- HEADER -->
<header>
    <div class="icon">💊</div>
    <h1>Pelayanan Kefarmasian</h1>
    <p>Informasi dan Pelayanan Kefarmasian untuk Masyarakat</p>
</header>


<!-- NAVIGASI -->
<nav>
    <a href="#beranda">Beranda</a>
    <a href="#pengertian">Pengertian</a>
    <a href="#pendaftaran">Pendaftaran</a>
    <a href="#resep">Pelayanan Resep</a>
    <a href="#konsultasi">Konsultasi</a>
    <a href="#kontak">Kontak</a>
</nav>


<div class="container">

    <!-- BERANDA -->
    <section id="beranda" class="hero">

        <div class="hero-card">

            <div style="font-size:45px;">🩺💊</div>

            <h2>Selamat Datang</h2>

            <p>
                Selamat datang di website Pelayanan Kefarmasian.
                Website ini menyediakan informasi mengenai pelayanan
                kefarmasian, pendaftaran pasien, pelayanan resep,
                serta konsultasi bersama apoteker.
            </p>

            <a href="#pendaftaran" class="button">
                📋 DAFTAR PELAYANAN
            </a>

        </div>

    </section>


    <!-- PENGERTIAN -->
    <section id="pengertian">

        <h2 class="section-title">
            📚 Pengertian Pelayanan Kefarmasian
        </h2>

        <div class="card">

            <h3>💊 Apa itu Pelayanan Kefarmasian?</h3>

            <p>
                Pelayanan kefarmasian merupakan pelayanan yang diberikan
                oleh tenaga kefarmasian kepada pasien atau masyarakat
                berkaitan dengan penggunaan obat dan pelayanan kesehatan.
                Pelayanan ini tidak hanya berfokus pada penyediaan obat,
                tetapi juga mencakup pemberian informasi obat, konseling,
                pelayanan resep, pemantauan penggunaan obat, serta upaya
                untuk memastikan obat digunakan secara tepat, aman,
                dan efektif.
            </p>

            <br>

            <p>
                Melalui pelayanan kefarmasian, pasien dapat memperoleh
                informasi yang jelas mengenai nama obat, manfaat obat,
                aturan penggunaan, dosis, waktu penggunaan, efek samping,
                serta hal-hal yang perlu diperhatikan selama menggunakan
                obat.
            </p>

        </div>


        <div class="service-grid">

            <div class="service">
                <div class="emoji">💊</div>
                <h4>Pelayanan Resep</h4>
                <p>Pelayanan obat berdasarkan resep dokter.</p>
            </div>

            <div class="service">
                <div class="emoji">🩺</div>
                <h4>Konsultasi</h4>
                <p>Konsultasi mengenai penggunaan obat.</p>
            </div>

            <div class="service">
                <div class="emoji">📖</div>
                <h4>Informasi Obat</h4>
                <p>Informasi mengenai penggunaan obat yang tepat.</p>
            </div>

            <div class="service">
                <div class="emoji">🌿</div>
                <h4>Swamedikasi</h4>
                <p>Panduan penggunaan obat secara mandiri.</p>
            </div>

        </div>

    </section>


    <!-- PENDAFTARAN -->
    <section id="pendaftaran">

        <h2 class="section-title">
            📝 Pendaftaran Pelayanan
        </h2>

        <div class="card">

            <h3>📋 Formulir Pendaftaran Pasien</h3>

            <p>
                Sebelum mendapatkan pelayanan, pasien dapat melakukan
                pendaftaran melalui formulir online. Silakan mengisi
                data dengan benar agar petugas dapat menghubungi pasien
                untuk memberikan informasi mengenai antrean pelayanan.
            </p>

            <br>

            <p>
                Formulir pendaftaran berisi:
            </p>

            <ul style="font-size:14px; padding-left:22px; margin-top:8px;">
                <li>Nama pasien</li>
                <li>Nomor BPJS (jika ada)</li>
                <li>Keluhan pasien</li>
                <li>Nomor WhatsApp yang dapat dihubungi</li>
            </ul>

            <!-- GANTI LINK DI BAWAH -->
            <a
                href="https://forms.gle/jG8p9wozy5nmoMrS8"
                target="_blank"
                class="button">
                📋 BUKA FORMULIR PENDAFTARAN
            </a>

            <div class="info-box">

                <strong>📱 Informasi Antrean</strong>

                <br><br>

                Nomor antrean akan segera dikirimkan melalui
                WhatsApp ke nomor yang telah dicantumkan pada
                formulir pendaftaran.

                <br><br>

                <strong>
                    *Urutan antrean akan diambil berdasarkan urutan
                    pasien yang mengirimkan formulir terlebih dahulu.
                </strong>

            </div>

        </div>


        <!-- ALUR PENDAFTARAN -->
        <div class="card">

            <h3>🔄 Alur Pendaftaran</h3>

            <div class="flow">

                <div class="flow-item">
                    <div class="number">1</div>
                    <div>
                        <h4>Buka Formulir</h4>
                        <p>
                            Pasien membuka formulir pendaftaran
                            melalui tombol pendaftaran.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">2</div>
                    <div>
                        <h4>Isi Data Pasien</h4>
                        <p>
                            Isi nama pasien, nomor BPJS jika ada,
                            keluhan, dan nomor WhatsApp.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">3</div>
                    <div>
                        <h4>Kirim Formulir</h4>
                        <p>
                            Pastikan seluruh data sudah benar,
                            kemudian kirim formulir.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">4</div>
                    <div>
                        <h4>Menunggu Nomor Antrean</h4>
                        <p>
                            Nomor antrean akan dikirimkan melalui
                            WhatsApp yang telah didaftarkan.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">5</div>
                    <div>
                        <h4>Mendapatkan Pelayanan</h4>
                        <p>
                            Pasien datang dan mendapatkan pelayanan
                            sesuai nomor antrean.
                        </p>
                    </div>
                </div>

            </div>

        </div>

    </section>


    <!-- PELAYANAN RESEP -->
    <section id="resep">

        <h2 class="section-title">
            💊 Pelayanan Resep
        </h2>

        <div class="card">

            <h3>📖 Pengertian</h3>

            <p>
                Pelayanan resep merupakan rangkaian kegiatan pelayanan
                kefarmasian yang dilakukan terhadap resep pasien mulai
                dari penerimaan resep, pemeriksaan kelengkapan resep,
                penyiapan obat, pemberian etiket, pemeriksaan akhir,
                hingga penyerahan obat disertai informasi mengenai
                penggunaan obat.
            </p>

        </div>


        <div class="card">

            <h3>🔄 Alur Pelayanan Resep</h3>

            <div class="flow">

                <div class="flow-item">
                    <div class="number">1</div>
                    <div>
                        <h4>Penerimaan Resep</h4>
                        <p>
                            Resep diterima oleh petugas kefarmasian
                            dari pasien.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">2</div>
                    <div>
                        <h4>Pemeriksaan Resep</h4>
                        <p>
                            Dilakukan pemeriksaan administrasi,
                            farmasetik, dan klinis resep.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">3</div>
                    <div>
                        <h4>Penyiapan Obat</h4>
                        <p>
                            Obat disiapkan sesuai dengan resep,
                            jumlah, bentuk sediaan, dan dosis.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">4</div>
                    <div>
                        <h4>Pemberian Etiket</h4>
                        <p>
                            Obat diberi etiket yang berisi informasi
                            aturan dan cara penggunaan obat.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">5</div>
                    <div>
                        <h4>Pemeriksaan Akhir</h4>
                        <p>
                            Dilakukan pemeriksaan kembali untuk
                            memastikan kesesuaian obat dengan resep.
                        </p>
                    </div>
                </div>


                <div class="flow-item">
                    <div class="number">6</div>
                    <div>
                        <h4>Penyerahan dan KIE</h4>
                        <p>
                            Obat diserahkan kepada pasien disertai
                            informasi dan edukasi mengenai penggunaan obat.
                        </p>
                    </div>
                </div>

            </div>

        </div>

    </section>


    <!-- KONSULTASI -->
    <section id="konsultasi">

        <h2 class="section-title">
            🩺 Konsultasi Kefarmasian
        </h2>

        <div class="card">

            <h3>👩‍⚕️ Konsultasi Pasien dengan Apoteker</h3>

            <p>
                Konsultasi kefarmasian merupakan kegiatan komunikasi
                antara pasien dengan apoteker untuk membahas masalah
                yang berkaitan dengan penggunaan obat dan kesehatan.
                Pasien dapat menyampaikan keluhan, obat yang sedang
                digunakan, riwayat penggunaan obat, maupun pertanyaan
                mengenai obat.
            </p>

            <br>

            <p>
                Apoteker akan memberikan informasi yang sesuai mengenai
                penggunaan obat, aturan pakai, waktu penggunaan,
                efek samping yang mungkin terjadi, interaksi obat,
                serta hal-hal yang perlu diperhatikan selama terapi.
            </p>

            <a
                href="https://wa.me/6285717420989"
                target="_blank"
                class="button button-wa">
                💬 KONSULTASI MELALUI WHATSAPP
            </a>

        </div>


        <div class="card">

            <h3>💬 Hal yang Dapat Dikonsultasikan</h3>

            <ul style="font-size:14px; padding-left:22px;">
                <li>Cara penggunaan obat</li>
                <li>Aturan dan waktu minum obat</li>
                <li>Efek samping obat</li>
                <li>Interaksi obat</li>
                <li>Penggunaan obat pada kondisi tertentu</li>
                <li>Penggunaan obat bebas untuk keluhan ringan</li>
                <li>Pertanyaan mengenai obat yang sedang digunakan</li>
            </ul>

        </div>

    </section>


    <!-- KONTAK -->
    <section id="kontak">

        <h2 class="section-title">
            📞 Kontak yang Dapat Dihubungi
        </h2>

        <div class="card">

            <div class="contact-item">

                <div class="contact-icon">📍</div>

                <div>
                    <strong>Alamat</strong>
                    <p>
                        Jl. Pangandaran No. 77,
                        Kelurahan Antirogo,
                        Kecamatan Sumbersari,
                        Kabupaten Jember
                    </p>
                </div>

            </div>


            <div class="contact-item">

                <div class="contact-icon">📱</div>

                <div>
                    <strong>WhatsApp</strong>
                    <p>
                        <a href="https://wa.me/6285717420989"
                           target="_blank">
                            085717420989
                        </a>
                    </p>
                </div>

            </div>


            <div class="contact-item">

                <div class="contact-icon">📧</div>

                <div>
                    <strong>Email</strong>
                    <p>
                        <a href="mailto:tyaranovelia118@gmail.com">
                            tyaranovelia118@gmail.com
                        </a>
                    </p>
                </div>

            </div>


            <a
                href="https://wa.me/6285717420989"
                target="_blank"
                class="button button-wa">
                📱 HUBUNGI MELALUI WHATSAPP
            </a>

        </div>

    </section>

</div>


<!-- FOOTER -->
<footer>

    <div style="font-size:30px;">💊</div>

    <p>
        <strong>PELAYANAN KEFARMASIAN</strong>
    </p>

    <p>
        Memberikan informasi dan pelayanan kefarmasian
        untuk mendukung penggunaan obat yang tepat dan aman.
    </p>

    <br>

    <p>
        © 2026 Pelayanan Kefarmasian
    </p>

</footer>

</body>
</html>
