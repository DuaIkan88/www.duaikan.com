# www.duaikan.com
Web
<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>UMKM Keren - Katalog Produk</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        /* --- 1. PENGATURAN WARNA & DASAR --- */
        :root {
            /* Warna Gradasi Spesial (Orange ke Pink) - Eye Catching */
            --gradient-bg: linear-gradient(135deg, #FF512F 0%, #DD2476 100%);
            --white: #ffffff;
            --text-dark: #333;
            --shopee-color: #ee4d2d;
            --tiktok-color: #000000;
            --insta-color: #E1306C;
        }

        * { margin: 0; padding: 0; box-sizing: border-box; }
        
        body {
            font-family: 'Poppins', sans-serif;
            background-color: #f8f9fa;
            color: var(--text-dark);
            overflow-x: hidden;
        }

        a { text-decoration: none; color: inherit; }

        /* --- 2. HEADER DENGAN GRADASI --- */
        header {
            background: var(--gradient-bg);
            padding: 40px 20px;
            text-align: center;
            color: white;
            border-bottom-left-radius: 50px;
            border-bottom-right-radius: 50px;
            box-shadow: 0 10px 30px rgba(221, 36, 118, 0.3);
            margin-bottom: 50px;
        }

        header h1 {
            font-size: 2.5rem;
            font-weight: 800;
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 2px;
        }

        header p { font-size: 1rem; opacity: 0.9; }

        /* --- 3. TOMBOL SOSMED SPECIAL (Pill Shape) --- */
        .social-bar {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 25px;
            flex-wrap: wrap;
        }

        .social-btn {
            background: white;
            padding: 10px 25px;
            border-radius: 30px;
            font-weight: 600;
            display: flex;
            align-items: center;
            gap: 10px;
            transition: transform 0.3s, box-shadow 0.3s;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
            color: #333;
        }

        /* Warna khusus saat tombol sosmed di-hover */
        .social-btn.shopee:hover { color: white; background: var(--shopee-color); }
        .social-btn.tiktok:hover { color: white; background: var(--tiktok-color); }
        .social-btn.insta:hover { color: white; background: var(--insta-color); }
        
        .social-btn:hover { transform: translateY(-5px); }

        /* --- 4. KATALOG PRODUK (GRID) --- */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px 50px 20px;
        }

        .section-title {
            text-align: center;
            font-size: 1.8rem;
            margin-bottom: 30px;
            color: #444;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }
        
        /* Garis bawah judul */
        .section-title::after {
            content: '';
            display: block;
            width: 50px;
            height: 4px;
            background: var(--gradient-bg);
            margin: 10px auto 0;
            border-radius: 2px;
        }

        .product-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
        }

        /* --- 5. KARTU PRODUK (GLASS STYLE) --- */
        .product-card {
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 10px 20px rgba(0,0,0,0.05);
            transition: all 0.3s ease;
            position: relative;
            border: 1px solid rgba(0,0,0,0.03);
        }

        .product-card:hover {
            transform: translateY(-10px); /* Efek naik */
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
        }

        .img-box {
            height: 350px;
            width: 100%;
            overflow: hidden;
            position: relative;
        }

        .img-box img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s;
        }

        .product-card:hover .img-box img {
            transform: scale(1.1); /* Efek zoom gambar */
        }

        .details { padding: 20px; text-align: center; }

        .details h3 {
            font-size: 1.2rem;
            margin-bottom: 5px;
            color: #222;
        }

        .price {
            display: block;
            font-size: 1.1rem;
            font-weight: 700;
            color: #DD2476; /* Warna Pink Tua */
            margin-bottom: 15px;
        }

        .btn-buy {
            display: inline-block;
            width: 100%;
            padding: 10px 0;
            background: var(--gradient-bg);
            color: white;
            border-radius: 10px;
            font-weight: 600;
            border: none;
            cursor: pointer;
            transition: opacity 0.3s;
        }

        .btn-buy:hover { opacity: 0.9; }

        /* --- 6. FOOTER --- */
        footer {
            text-align: center;
            padding: 30px;
            background: #333;
            color: white;
            margin-top: 50px;
            font-size: 0.9rem;
        }

        /* Responsive */
        @media (max-width: 600px) {
            header h1 { font-size: 1.8rem; }
            .social-btn { width: 100%; justify-content: center; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-content">
            <h1>DUA IKAN</h1>
            <p>Produk Terbaik & Berkualitas Pilihan Kami</p>

            <div class="social-bar">
                <a href="https://instagram.com/duaikan88" target="_blank" class="social-btn insta">
                    <i class="fab fa-instagram"></i> Instagram
                </a>
                <a href="https://tiktok.com/" target="_blank" class="social-btn tiktok">
                    <i class="fab fa-tiktok"></i> TikTok Shop
                </a>
                <a href="https://shopee.co.id/stephenjapardi" target="_blank" class="social-btn shopee">
                    <i class="fas fa-shopping-bag"></i> Shopee
                </a>
            </div>
        </div>
    </header>

    <main class="container">
        <h2 class="section-title">Katalog Produk</h2>
        
        <div class="product-grid">
            
            <div class="product-card">
                <div class="img-box">
                    <img src="Mie Jumbo.jpg" alt="Produk 1">
                </div>
                <div class="details">
                    <h3>Mie Jumbo</h3>
                    <span class="price">Rp 25.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Mie Jumbo')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Stik Kentang.jpg" alt="Produk 2">
                </div>
                <div class="details">
                    <h3>Stik Kentang</h3>
                    <span class="price">Rp 24.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Stik Kentang')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Banana Crunch.jpg"Produk 3">
                </div>
                <div class="details">
                    <h3>Banana Crunch</h3>
                    <span class="price">Rp 15.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Banana Crunch')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Baby Fish.jpg" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Ikan Crispy</h3>
                    <span class="price">Rp 15.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Ikan Crispy')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Basreng Pedas Besar.jpg" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Basreng Pedas 200gr</h3>
                    <span class="price">Rp 25.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Basreng Pedas 200gr')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Jengkol Pedas Kecil.png" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Jengkol Pedas Kecil</h3>
                    <span class="price">Rp 15.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Jengkol Pedas Kecil')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Bulat Besar.jpg" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Bulat Besar</h3>
                    <span class="price">Rp 24.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Bulat Besar')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Rangginang.png" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Rangginang</h3>
                    <span class="price">Rp 20.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Rangginang')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Bangkok Pedas.png" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Bangkok Pedas</h3>
                    <span class="price">Rp 23.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Bangkok Pedas')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Kuping Gajah.png" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Kuping Gajah</h3>
                    <span class="price">Rp 23.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Kuping Gajah')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Mini Top Pedas.png" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Mini Top Pedas</h3>
                    <span class="price">Rp 23.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Mini Top Pedas')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

            <div class="product-card">
                <div class="img-box">
                    <img src="Mawar Besar.jpeg" alt="Produk 4">
                </div>
                <div class="details">
                    <h3>Mawar Besar</h3>
                    <span class="price">Rp 24.000</span>
                    <button class="btn-buy" onclick="beliViaWA('Mawar Besar')">
                        <i class="fab fa-whatsapp"></i> Pesan Sekarang
                    </button>
                </div>
            </div>

        </div>
    </main>

    <footer>
        <p>&copy; 2026 Dua Ikan. All Rights Reserved.</p>
        <p>Dibuat dengan ❤️ UMKM Indonesia</p>
    </footer>

    <script>
        function beliViaWA(namaProduk) {
            // Ganti nomor ini dengan nomor WhatsApp UMKM Anda (format: 628...)
            let nomorWA = "62895603268013"; 
            
            let pesan = `Halo kak, saya mau pesan produk *${namaProduk}* yang ada di website. Apakah masih ready?`;
            
            // Encode pesan agar bisa masuk ke URL
            let linkWA = `https://wa.me/${nomorWA}?text=${encodeURIComponent(pesan)}`;
            
            // Buka WhatsApp di tab baru
            window.open(linkWA, '_blank');
        }
    </script>

</body>
</html>
