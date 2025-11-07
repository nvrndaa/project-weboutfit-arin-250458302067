<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Myoutfit</title>
  <style>
    body {
      margin: 0;
      font-family: 'Poppins', sans-serif;
      background: url('https://i.pinimg.com/1200x/e4/bb/9b/e4bb9b25dd14dcbd93f5771a3a97c7b9.jpg') no-repeat center center fixed;
      background-size: cover;
      backdrop-filter: blur(6px);
      color: #3c2f2f;
      line-height: 1.6;
    }

    /* Overlay lembut biar teks tetap jelas */
    body::before {
      content: "";
      position: fixed;
      top: 0; left: 0; right: 0; bottom: 0;
      background-color: rgba(255, 247, 230, 0.8);
      z-index: -1;
    }

    header {
      background-color: rgba(255, 250, 240, 0.9);
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      padding: 20px 60px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: sticky;
      top: 0;
      z-index: 10;
      border-radius: 0 0 15px 15px;
      backdrop-filter: blur(8px);
    }

    header h1 {
      font-size: 1.8rem;
      color: #a47e3c;
      letter-spacing: 1px;
    }

    nav a {
      text-decoration: none;
      color: #5a4634;
      margin: 0 10px;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    nav a:hover {
      color: #c49a6c;
    }

    .hero {
      text-align: center;
      padding: 120px 20px 100px;
      background: rgba(255, 249, 242, 0.7);
      border-radius: 20px;
      max-width: 900px;
      margin: 60px auto;
      backdrop-filter: blur(8px);
    }

    .hero h2 {
      font-size: 2.8rem;
      margin-bottom: 10px;
      color: #6f4f28;
    }

    .hero p {
      font-size: 1.1rem;
      color: #7a6650;
      margin-bottom: 30px;
    }

    .btn {
      background-color: #c49a6c;
      color: white;
      padding: 12px 28px;
      border: none;
      border-radius: 30px;
      font-size: 1rem;
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .btn:hover {
      background-color: #a47e3c;
      transform: scale(1.05);
    }

    /* Produk Section */
    .produk {
      padding: 80px 60px;
      text-align: center;
    }

    .produk h2 {
      font-size: 2rem;
      margin-bottom: 40px;
      color: #6f4f28;
    }

    .produk-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 30px;
    }

    .produk-item {
      background-color: rgba(255, 250, 240, 0.9);
      border-radius: 15px;
      box-shadow: 0 3px 8px rgba(0,0,0,0.1);
      overflow: hidden;
      transition: transform 0.3s ease;
      backdrop-filter: blur(6px);
    }

    .produk-item:hover {
      transform: translateY(-8px);
    }

    .produk-item img {
      width: 100%;
      height: 280px;
      object-fit: cover;
    }

    .produk-item h3 {
      margin: 15px 0 5px;
      font-size: 1.2rem;
      color: #5a4634;
    }

    .produk-item p {
      color: #8a7a6a;
      margin-bottom: 20px;
    }

    .produk-item .btn {
      margin-bottom: 20px;
    }

    /* Tentang */
    .tentang {
      background-color: rgba(255, 247, 230, 0.9);
      padding: 80px 60px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      flex-wrap: wrap;
      border-radius: 20px;
      margin: 60px;
      backdrop-filter: blur(6px);
    }

    .tentang-text {
      flex: 1 1 400px;
      padding: 20px;
    }

    .tentang-text h2 {
      color: #6f4f28;
      font-size: 2rem;
      margin-bottom: 15px;
    }

    .tentang-text p {
      color: #7a6650;
    }

    .tentang-img {
      flex: 1 1 400px;
      text-align: center;
    }

    .tentang-img img {
      width: 80%;
      border-radius: 15px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }

    /* Kontak */
    .kontak {
      text-align: center;
      padding: 80px 60px;
      background-color: rgba(255, 249, 242, 0.8);
      border-radius: 20px;
      margin: 60px;
      backdrop-filter: blur(6px);
    }

    .kontak h2 {
      color: #6f4f28;
      margin-bottom: 20px;
    }

    .kontak a {
      text-decoration: none;
      color: white;
      background-color: #c49a6c;
      padding: 12px 30px;
      border-radius: 30px;
      transition: 0.3s ease;
    }

    .kontak a:hover {
      background-color: #a47e3c;
    }

    footer {
      background-color: rgba(255, 244, 222, 0.9);
      text-align: center;
      padding: 20px;
      color: #6f4f28;
      font-size: 0.9rem;
      backdrop-filter: blur(6px);
    }

    @media (max-width: 768px) {
      header {
        flex-direction: column;
      }
      .tentang {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>Myoutfit</h1>
    <nav>
      <a href="#home">Home</a>
      <a href="#produk">Produk</a>
      <a href="#tentang">Tentang</a>
      <a href="#kontak">Kontak</a>
    </nav>
  </header>

  <section class="hero" id="home">
    <h2>Selamat Datang di Myoutfit</h2>
    <p>Temukan koleksi fashion elegan dengan desain modern yang memancarkan pesonamu.</p>
    <button class="btn">Lihat Koleksi</button>
  </section>

  <section class="produk" id="produk">
    <h2>Koleksi Kami</h2>
    <div class="produk-grid">
      <div class="produk-item">
        <img src="https://i.pinimg.com/1200x/61/89/14/618914f925019dbb52cd56df32b171d3.jpg" alt="Produk 1">
        <h3>Gaun </h3>
        <p>Rp 250.000</p>
        <button class="btn">Tambah ke Keranjang</button>
      </div>
      <div class="produk-item">
        <img src="https://i.pinimg.com/736x/cc/ac/2e/ccac2eeab2d4f4c8b9fe3d7a36f75592.jpg" alt="Produk 2">
        <h3>Blouse Casual</h3>
        <p>Rp 180.000</p>
        <button class="btn">Tambah ke Keranjang</button>
      </div>
      <div class="produk-item">
        <img src="https://i.pinimg.com/1200x/76/b0/02/76b00215e899b418b99bcd3ea1de3c5d.jpg" alt="Produk 3">
        <h3>Setelan Santai</h3>
        <p>Rp 300.000</p>
        <button class="btn">Tambah ke Keranjang</button>
      </div>
    </div>
  </section>

  <section class="tentang" id="tentang">
    <div class="tentang-text">
      <h2>Tentang Kami</h2>
      <p>Myoutfit menghadirkan pakaian bergaya modern dengan bahan berkualitas tinggi. 
         Setiap koleksi dirancang agar kamu selalu tampil percaya diri, elegan, dan nyaman di setiap kesempatan.</p>
    </div>
    <div class="tentang-img">
      <img src="https://i.pinimg.com/1200x/bf/0a/d4/bf0ad4653e757e076f9d541a6e1c1129.jpg" alt="Tentang Kami">
    </div>
  </section>

  <section class="kontak" id="kontak">
    <h2>Hubungi Kami</h2>
    <p>Ingin memesan atau bertanya tentang produk kami?</p>
    <a href="mailto:novaboutique@email.com">Kirim Email</a>
  </section>

  <footer>
    <p>© 2025 Myoutfit. All rights reserved.</p>
  </footer>
</body>
</html>
