<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Level Database | Open New Member</title>

  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: Arial, sans-serif;
      background: #f7fbff;
      color: #172033;
      line-height: 1.6;
    }

    .container {
      width: 92%;
      max-width: 1050px;
      margin: auto;
    }

    header {
      background: rgba(255,255,255,0.96);
      padding: 18px 0;
      position: sticky;
      top: 0;
      z-index: 10;
      box-shadow: 0 2px 15px rgba(0,0,0,0.06);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 22px;
      font-weight: 800;
      color: #367fc4;
    }

    .nav a {
      text-decoration: none;
      color: #367fc4;
      font-weight: 600;
      font-size: 14px;
    }

    .hero {
      padding: 65px 0 50px;
      background: linear-gradient(135deg, #ffffff, #eaf6ff);
      text-align: center;
    }

    .badge {
      display: inline-block;
      background: #dff1ff;
      color: #3177b5;
      padding: 8px 16px;
      border-radius: 50px;
      font-size: 13px;
      font-weight: bold;
      margin-bottom: 18px;
    }

    h1 {
      font-size: 42px;
      line-height: 1.15;
      margin-bottom: 18px;
    }

    .hero h1 span {
      color: #3886cf;
    }

    .hero p {
      max-width: 680px;
      margin: auto;
      color: #596579;
      font-size: 17px;
    }

    .cta {
      display: inline-block;
      margin-top: 28px;
      background: #3b91dc;
      color: white;
      text-decoration: none;
      padding: 15px 28px;
      border-radius: 50px;
      font-weight: bold;
      box-shadow: 0 8px 20px rgba(59,145,220,.25);
    }

    .stats {
      margin-top: 35px;
      display: flex;
      justify-content: center;
      gap: 15px;
      flex-wrap: wrap;
    }

    .stat {
      background: white;
      padding: 18px 25px;
      border-radius: 16px;
      box-shadow: 0 5px 20px rgba(0,0,0,.06);
      min-width: 145px;
    }

    .stat strong {
      display: block;
      color: #347fc5;
      font-size: 22px;
    }

    .stat small {
      color: #687386;
    }

    section {
      padding: 65px 0;
    }

    .section-title {
      text-align: center;
      margin-bottom: 35px;
    }

    .section-title h2 {
      font-size: 30px;
      margin-bottom: 8px;
    }

    .section-title p {
      color: #687386;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 18px;
    }

    .card {
      background: white;
      border-radius: 20px;
      padding: 25px;
      box-shadow: 0 5px 22px rgba(31,75,110,.08);
      border: 1px solid #e5f1fa;
    }

    .icon {
      width: 48px;
      height: 48px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 14px;
      background: #e4f4ff;
      font-size: 23px;
      margin-bottom: 15px;
    }

    .card h3 {
      margin-bottom: 8px;
      font-size: 18px;
    }

    .card p {
      color: #687386;
      font-size: 14px;
    }

    .about {
      background: #eaf6ff;
    }

    .about-box {
      max-width: 800px;
      margin: auto;
      background: white;
      padding: 30px;
      border-radius: 22px;
      box-shadow: 0 5px 20px rgba(31,75,110,.06);
    }

    .about-box p {
      color: #596579;
      margin-bottom: 14px;
    }

    .price-box {
      max-width: 420px;
      margin: auto;
      background: white;
      border: 2px solid #bfe3fb;
      border-radius: 25px;
      padding: 35px 25px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(31,75,110,.09);
    }

    .price-box .label {
      color: #397fb9;
      font-weight: bold;
    }

    .price {
      font-size: 42px;
      font-weight: 800;
      color: #2e83cc;
      margin: 10px 0;
    }

    .price-box ul {
      list-style: none;
      text-align: left;
      margin: 20px 0;
    }

    .price-box li {
      padding: 8px 0;
      border-bottom: 1px solid #edf3f7;
    }

    .testimonials {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .testimonial {
      background: white;
      padding: 25px;
      border-radius: 20px;
      box-shadow: 0 5px 22px rgba(31,75,110,.08);
    }

    .testimonial .stars {
      color: #f2b84b;
      margin-bottom: 10px;
    }

    .testimonial p {
      color: #4d596b;
      font-size: 15px;
    }

    .testimonial strong {
      display: block;
      margin-top: 15px;
      color: #2f80c5;
    }

    .notice {
      background: #fff;
      border-left: 4px solid #5b9ed4;
      padding: 15px;
      margin-top: 25px;
      border-radius: 10px;
      color: #657184;
      font-size: 13px;
    }

    .join {
      text-align: center;
      background: linear-gradient(135deg, #dff2ff, #f8fcff);
    }

    .join h2 {
      font-size: 32px;
      margin-bottom: 12px;
    }

    .join p {
      color: #5d6878;
      max-width: 600px;
      margin: auto;
    }

    footer {
      background: #17334b;
      color: white;
      padding: 30px 0;
      text-align: center;
    }

    footer p {
      font-size: 13px;
      opacity: .8;
    }

    .wa {
      position: fixed;
      right: 18px;
      bottom: 18px;
      width: 58px;
      height: 58px;
      background: #25d366;
      color: white;
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 27px;
      text-decoration: none;
      box-shadow: 0 5px 18px rgba(0,0,0,.2);
      z-index: 99;
    }

    @media (max-width: 700px) {
      h1 {
        font-size: 32px;
      }

      .hero {
        padding: 50px 0 40px;
      }

      section {
        padding: 45px 0;
      }

      .cards,
      .testimonials {
        grid-template-columns: 1fr;
      }

      .nav a {
        display: none;
      }

      .stat {
        min-width: 130px;
      }
    }
  </style>
</head>

<body>

<header>
  <div class="container nav">
    <div class="logo">LEVEL DATABASE</div>
    <a href="#fasilitas">Fasilitas</a>
    <a href="#testimoni">Testimoni</a>
    <a href="#daftar">Daftar</a>
  </div>
</header>

<section class="hero">
  <div class="container">

    <div class="badge">OPEN NEW MEMBER ✨</div>

    <h1>
      Mulai Kembangkan Potensi dari
      <span>HP Kamu</span>
    </h1>

    <p>
      Level Database hadir untuk membantu kamu mendapatkan akses
      ke berbagai materi, komunitas, bimbingan, dan bahan yang
      bisa digunakan untuk mengembangkan aktivitas digital.
    </p>

    <a class="cta" href="#daftar">
      🚀 JOIN SEKARANG
    </a>

    <div class="stats">
      <div class="stat">
        <strong>100.000+</strong>
        <small>Member</small>
      </div>

      <div class="stat">
        <strong>Lengkap</strong>
        <small>Materi & Fasilitas</small>
      </div>

      <div class="stat">
        <strong>Support</strong>
        <small>Komunitas Member</small>
      </div>
    </div>

  </div>
</section>

<section id="fasilitas">
  <div class="container">

    <div class="section-title">
      <h2>Fasilitas Level Database</h2>
      <p>Dapatkan akses ke berbagai fasilitas yang tersedia untuk member.</p>
    </div>

    <div class="cards">

      <div class="card">
        <div class="icon">📚</div>
        <h3>Materi & Panduan</h3>
        <p>
          Akses materi dan panduan yang dapat membantu kamu
          belajar dan mengembangkan kemampuan digital.
        </p>
      </div>

      <div class="card">
        <div class="icon">👥</div>
        <h3>Komunitas Member</h3>
        <p>
          Bergabung dengan komunitas dan berinteraksi dengan
          member lainnya.
        </p>
      </div>

      <div class="card">
        <div class="icon">💬</div>
        <h3>Bimbingan & Support</h3>
        <p>
          Mendapatkan arahan dan support selama kamu mengikuti
          program yang tersedia.
        </p>
      </div>

      <div class="card">
        <div class="icon">📱</div>
        <h3>Bahan Promosi</h3>
        <p>
          Tersedia bahan yang dapat membantu kebutuhan promosi
          dan aktivitas media sosial.
        </p>
      </div>

      <div class="card">
        <div class="icon">💡</div>
        <h3>Tips & Trik</h3>
        <p>
          Berbagai tips dan informasi untuk membantu kamu
          mengeksplorasi peluang di dunia digital.
        </p>
      </div>

      <div class="card">
        <div class="icon">⚡</div>
        <h3>Akses Praktis</h3>
        <p>
          Dirancang agar mudah digunakan melalui HP dan dapat
          diakses kapan saja.
        </p>
      </div>

    </div>
  </div>
</section>

<section class="about">
  <div class="container">

    <div class="section-title">
      <h2>Tentang Level Database</h2>
    </div>

    <div class="about-box">

      <p>
        Level Database merupakan wadah yang menyediakan berbagai
        materi, bahan promosi, informasi, komunitas, serta support
        untuk member.
      </p>

      <p>
        Kamu bisa mempelajari berbagai hal yang tersedia sesuai
        kebutuhan dan mengembangkan kemampuanmu secara bertahap.
      </p>

      <p>
        Cocok untuk kamu yang ingin mulai belajar dunia digital
        hanya dengan menggunakan HP.
      </p>

      <div class="notice">
        ℹ️ Hasil setiap orang dapat berbeda-beda dan bergantung
        pada usaha, strategi, waktu, serta aktivitas masing-masing.
      </div>

    </div>
  </div>
</section>

<section>
  <div class="container">

    <div class="section-title">
      <h2>Paket Open New Member</h2>
      <p>Mulai dengan akses yang tersedia untuk member.</p>
    </div>

    <div class="price-box">

      <div class="label">PAKET BASIC</div>

      <div class="price">Rp55.000</div>

      <p>Akses member Level Database</p>

      <ul>
        <li>✅ Materi & panduan</li>
        <li>✅ Komunitas member</li>
        <li>✅ Support & bimbingan</li>
        <li>✅ Bahan promosi</li>
        <li>✅ Tips & trik</li>
        <li>✅ Akses melalui HP</li>
      </ul>

      <a class="cta" href="#daftar">
        DAFTAR SEKARANG
      </a>

    </div>
  </div>
</section>

<section id="testimoni">
  <div class="container">

    <div class="section-title">
      <h2>Testimoni Member 💙</h2>
      <p>Beberapa cerita yang dibagikan oleh member.</p>
    </div>

    <div class="testimonials">

      <div class="testimonial">
        <div class="stars">★★★★★</div>
        <p>
          “Alhamdulillah dari mengikuti bisnis freelance ini
          aku bisa kebeli HP lagi. Senang banget dan terima kasih
          atas bimbingan dan supportnya selama ini.”
        </p>
        <strong>— Testimoni Member</strong>
      </div>

      <div class="testimonial">
        <div class="stars">★★★★★</div>
        <p>
          “Awalnya belum serius, tapi setelah mulai fokus dan
          belajar lebih banyak, aku mulai merasakan perkembangan.
          Tetap semangat dan jangan menyerah.”
        </p>
        <strong>— Testimoni Member</strong>
      </div>

      <div class="testimonial">
        <div class="stars">★★★★★</div>
        <p>
          “Banyak ilmu yang bisa didapat. Yang penting terus
          belajar, explore dan jalankan sesuai kemampuan masing-masing.”
        </p>
        <strong>— Testimoni Member</strong>
      </div>

      <div class="testimonial">
        <div class="stars">★★★★★</div>
        <p>
          “Terima kasih untuk bimbingan dan supportnya.
          Semoga teman-teman yang sedang berproses juga tetap
          semangat.”
        </p>
        <strong>— Testimoni Member</strong>
      </div>

    </div>

  </div>
</section>

<section class="join" id="daftar">
  <div class="container">

    <h2>Siap Jadi Member?</h2>

    <p>
      Kalau kamu ingin mengetahui informasi lengkap dan cara
      bergabung, langsung hubungi kami melalui WhatsApp.
    </p>

    <a
      class="cta"
      href="https://wa.me/6288989149209?text=Halo%20kak,%20saya%20tertarik%20join%20Level%20Database.%20Boleh%20minta%20informasi%20lengkapnya%3F"
      target="_blank">
      💬 CHAT WHATSAPP
    </a>

  </div>
</section>

<footer>
  <div class="container">
    <h3>LEVEL DATABASE</h3>
    <p>Open New Member • Informasi & Pendaftaran</p>
    <p>WhatsApp: 088989149209</p>
    <br>
    <p>© 2026 Level Database. All rights reserved.</p>
  </div>
</footer>

<a
  class="wa"
  href="https://wa.me/6288989149209?text=Halo%20kak,%20saya%20tertarik%20join%20Level%20Database."
  target="_blank">
  ☎
</a>

</body>
</html>
