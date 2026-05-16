<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GOSWAMI Jewellery – Elegant, Best Prices</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Josefin+Sans:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --gold: #c9a84c;
    --gold-light: #e8c97e;
    --gold-dark: #8a6a1f;
    --cream: #faf6ef;
    --dark: #1a1208;
    --mid: #3b2d10;
    --text: #2a1f08;
    --white: #fff;
    --radius: 2px;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'Josefin Sans', sans-serif;
    background: var(--cream);
    color: var(--text);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; width: 100%; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 18px 5vw;
    background: rgba(26,18,8,0.82);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(201,168,76,0.25);
  }
  .nav-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.7rem; font-weight: 600; letter-spacing: 0.12em;
    color: var(--gold); text-decoration: none;
  }
  .nav-logo span { font-style: italic; font-weight: 300; }
  .nav-links { display: flex; gap: 28px; list-style: none; }
  .nav-links a {
    color: #e8dcc8; font-size: 0.72rem; letter-spacing: 0.18em;
    text-transform: uppercase; text-decoration: none;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold-light); }

  /* ── HERO ── */
  #hero {
    position: relative; height: 100vh; min-height: 560px;
    display: flex; align-items: center; justify-content: center;
    overflow: hidden;
  }
  .hero-bg {
    position: absolute; inset: 0;
    background: url('https://images.unsplash.com/photo-1515562141207-7a88fb7ce338?w=1600&q=80') center/cover no-repeat;
    filter: brightness(0.42);
    transform: scale(1.04);
    animation: heroZoom 12s ease-in-out infinite alternate;
  }
  @keyframes heroZoom {
    from { transform: scale(1.04); }
    to   { transform: scale(1.10); }
  }
  .hero-overlay {
    position: absolute; inset: 0;
    background: linear-gradient(160deg, rgba(26,18,8,0.55) 0%, rgba(201,168,76,0.08) 100%);
  }
  .hero-content {
    position: relative; text-align: center; padding: 0 24px;
    animation: fadeUp 1.1s ease both;
  }
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(36px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero-eyebrow {
    font-size: 0.68rem; letter-spacing: 0.35em; color: var(--gold);
    text-transform: uppercase; margin-bottom: 18px;
  }
  .hero-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(3rem, 9vw, 7.5rem);
    font-weight: 300; line-height: 1.05; color: var(--white);
    margin-bottom: 14px;
  }
  .hero-title em { font-style: italic; color: var(--gold-light); }
  .hero-tagline {
    font-size: 0.78rem; letter-spacing: 0.25em; color: #d4c4a0;
    text-transform: uppercase; margin-bottom: 42px;
  }
  .btn-hero {
    display: inline-block; padding: 15px 42px;
    border: 1px solid var(--gold); color: var(--gold);
    font-family: 'Josefin Sans', sans-serif;
    font-size: 0.72rem; letter-spacing: 0.22em; text-transform: uppercase;
    text-decoration: none; cursor: pointer; background: transparent;
    transition: background 0.3s, color 0.3s;
  }
  .btn-hero:hover { background: var(--gold); color: var(--dark); }

  /* ── DIVIDER ── */
  .divider {
    text-align: center; padding: 52px 0 20px;
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.8rem, 4vw, 2.8rem);
    font-weight: 300; color: var(--mid);
    letter-spacing: 0.06em;
  }
  .divider span { color: var(--gold); font-style: italic; }
  .divider-line {
    width: 60px; height: 1px; background: var(--gold);
    margin: 10px auto 48px;
  }

  /* ── CAROUSEL ── */
  #products { padding: 0 0 80px; }

  .carousel-track-wrap {
    overflow: hidden; position: relative;
  }
  .carousel-track {
    display: flex; gap: 24px; padding: 10px 5vw 20px;
    transition: transform 0.55s cubic-bezier(0.25,0.46,0.45,0.94);
    will-change: transform;
  }

  .product-card {
    flex: 0 0 260px; background: var(--white);
    border: 1px solid rgba(201,168,76,0.18);
    box-shadow: 0 4px 24px rgba(26,18,8,0.07);
    transition: transform 0.3s, box-shadow 0.3s;
    cursor: pointer;
    display: flex; flex-direction: column;
  }
  .product-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 14px 36px rgba(26,18,8,0.14);
  }
  .card-img-wrap {
    width: 100%; aspect-ratio: 1/1; overflow: hidden;
    background: #f5efe4;
  }
  .card-img-wrap img {
    width: 100%; height: 100%; object-fit: cover;
    transition: transform 0.55s ease;
  }
  .product-card:hover .card-img-wrap img { transform: scale(1.06); }

  .card-body { padding: 18px 16px 20px; flex: 1; display: flex; flex-direction: column; }
  .card-name {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.1rem; font-weight: 600; color: var(--dark);
    margin-bottom: 4px; line-height: 1.3;
  }
  .card-sub {
    font-size: 0.65rem; letter-spacing: 0.18em; text-transform: uppercase;
    color: var(--gold-dark); margin-bottom: 10px;
  }
  .card-price {
    font-size: 1.05rem; color: var(--gold-dark); font-weight: 600;
    margin-bottom: 14px;
  }
  .btn-addcart {
    margin-top: auto;
    display: inline-block; padding: 10px 0; text-align: center;
    border: 1px solid var(--gold); color: var(--gold-dark);
    font-size: 0.68rem; letter-spacing: 0.16em; text-transform: uppercase;
    background: transparent; cursor: pointer; width: 100%;
    transition: background 0.25s, color 0.25s;
  }
  .btn-addcart:hover { background: var(--gold); color: var(--white); }

  /* carousel nav */
  .carousel-nav {
    display: flex; justify-content: center; gap: 14px; margin-top: 28px;
  }
  .carousel-btn {
    width: 42px; height: 42px; border: 1px solid var(--gold);
    background: transparent; color: var(--gold); font-size: 1.1rem;
    cursor: pointer; display: flex; align-items: center; justify-content: center;
    transition: background 0.2s, color 0.2s;
  }
  .carousel-btn:hover { background: var(--gold); color: var(--dark); }

  /* ── CART BADGE ── */
  .cart-bar {
    position: fixed; bottom: 90px; right: 22px; z-index: 99;
    background: var(--dark); color: var(--gold);
    border: 1px solid var(--gold);
    padding: 10px 16px; font-size: 0.7rem; letter-spacing: 0.14em;
    text-transform: uppercase; cursor: pointer;
    box-shadow: 0 4px 18px rgba(0,0,0,0.3);
    display: flex; align-items: center; gap: 8px;
    transition: background 0.2s;
  }
  .cart-bar:hover { background: var(--gold); color: var(--dark); }
  .cart-count {
    background: #c0392b; color: #fff;
    border-radius: 50%; width: 20px; height: 20px;
    display: flex; align-items: center; justify-content: center;
    font-size: 0.65rem; font-weight: 700;
  }

  /* ── ORDER FORM MODAL ── */
  .modal-overlay {
    position: fixed; inset: 0; z-index: 200;
    background: rgba(10,6,0,0.78);
    display: flex; align-items: center; justify-content: center;
    padding: 20px;
    opacity: 0; pointer-events: none;
    transition: opacity 0.3s;
  }
  .modal-overlay.open { opacity: 1; pointer-events: all; }

  .modal {
    background: var(--cream); width: 100%; max-width: 560px;
    max-height: 88vh; overflow-y: auto;
    border: 1px solid rgba(201,168,76,0.35);
    padding: 40px 36px;
    transform: translateY(30px);
    transition: transform 0.35s;
    position: relative;
  }
  .modal-overlay.open .modal { transform: translateY(0); }

  .modal-close {
    position: absolute; top: 16px; right: 20px;
    background: none; border: none; font-size: 1.4rem;
    color: var(--gold-dark); cursor: pointer;
  }
  .modal-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.9rem; font-weight: 400; color: var(--dark);
    margin-bottom: 6px;
  }
  .modal-sub { font-size: 0.68rem; letter-spacing: 0.2em; color: var(--gold); text-transform: uppercase; margin-bottom: 28px; }

  .cart-items-list { margin-bottom: 22px; }
  .cart-item-row {
    display: flex; justify-content: space-between; align-items: center;
    padding: 8px 0; border-bottom: 1px solid rgba(201,168,76,0.18);
    font-size: 0.82rem; color: var(--mid);
  }
  .cart-item-row .remove-btn {
    background: none; border: none; color: #c0392b; cursor: pointer;
    font-size: 0.75rem; letter-spacing: 0.1em; text-transform: uppercase;
  }
  .empty-cart { font-size: 0.8rem; color: #888; font-style: italic; margin-bottom: 18px; }

  .form-group { margin-bottom: 18px; }
  .form-group label {
    display: block; font-size: 0.65rem; letter-spacing: 0.2em;
    text-transform: uppercase; color: var(--gold-dark); margin-bottom: 6px;
  }
  .form-group input, .form-group textarea {
    width: 100%; padding: 12px 14px;
    border: 1px solid rgba(201,168,76,0.35); background: var(--white);
    font-family: 'Josefin Sans', sans-serif; font-size: 0.85rem;
    color: var(--dark); outline: none;
    transition: border-color 0.2s;
  }
  .form-group input:focus, .form-group textarea:focus {
    border-color: var(--gold);
  }
  .form-group textarea { resize: vertical; min-height: 80px; }

  .btn-submit {
    width: 100%; padding: 15px;
    background: var(--gold); border: none;
    font-family: 'Josefin Sans', sans-serif;
    font-size: 0.75rem; letter-spacing: 0.22em; text-transform: uppercase;
    color: var(--dark); font-weight: 600; cursor: pointer;
    transition: background 0.25s;
  }
  .btn-submit:hover { background: var(--gold-dark); color: var(--white); }

  .success-msg {
    display: none; text-align: center; padding: 22px 0;
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.3rem; color: var(--gold-dark);
  }

  /* ── ABOUT STRIP ── */
  #about {
    background: var(--dark);
    padding: 72px 5vw;
    display: flex; gap: 48px; align-items: center;
    flex-wrap: wrap;
  }
  .about-text { flex: 1; min-width: 240px; }
  .about-eyebrow {
    font-size: 0.65rem; letter-spacing: 0.28em; color: var(--gold);
    text-transform: uppercase; margin-bottom: 14px;
  }
  .about-title {
    font-family: 'Cormorant Garamond', serif;
    font-size: clamp(1.8rem, 3.5vw, 2.8rem);
    font-weight: 300; color: var(--white); line-height: 1.2;
    margin-bottom: 18px;
  }
  .about-body { font-size: 0.82rem; line-height: 1.85; color: #c4b89a; }
  .about-stats { display: flex; gap: 36px; flex-wrap: wrap; }
  .stat { text-align: center; }
  .stat-num {
    font-family: 'Cormorant Garamond', serif;
    font-size: 2.6rem; font-weight: 300; color: var(--gold);
  }
  .stat-label { font-size: 0.62rem; letter-spacing: 0.2em; color: #a09070; text-transform: uppercase; }

  /* ── FOOTER ── */
  footer {
    background: #0e0b04; padding: 40px 5vw 28px;
    text-align: center;
  }
  .footer-logo {
    font-family: 'Cormorant Garamond', serif;
    font-size: 1.6rem; font-weight: 300; color: var(--gold);
    margin-bottom: 14px; letter-spacing: 0.1em;
  }
  .footer-links { display: flex; gap: 24px; justify-content: center; margin-bottom: 18px; }
  .footer-links a {
    font-size: 0.65rem; letter-spacing: 0.16em; color: #806848;
    text-transform: uppercase; text-decoration: none;
    transition: color 0.2s;
  }
  .footer-links a:hover { color: var(--gold); }
  .footer-copy { font-size: 0.62rem; color: #4a3a1a; letter-spacing: 0.1em; }

  /* ── WHATSAPP FLOAT ── */
  .wa-float {
    position: fixed; bottom: 22px; right: 22px; z-index: 99;
    width: 56px; height: 56px; border-radius: 50%;
    background: #25d366;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 4px 20px rgba(37,211,102,0.38);
    text-decoration: none;
    animation: waPulse 2.8s ease-in-out infinite;
  }
  .wa-float svg { width: 28px; height: 28px; fill: #fff; }
  @keyframes waPulse {
    0%,100% { box-shadow: 0 4px 20px rgba(37,211,102,0.38); }
    50%      { box-shadow: 0 4px 30px rgba(37,211,102,0.65); }
  }

  /* ── RESPONSIVE ── */
  @media (max-width: 600px) {
    .nav-links { display: none; }
    .product-card { flex: 0 0 220px; }
    .modal { padding: 28px 20px; }
    #about { flex-direction: column; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <a class="nav-logo" href="#"><span>The</span> Jewellery</a>
  <ul class="nav-links">
    <li><a href="#products">Collection</a></li>
    <li><a href="#about">About</a></li>
    <li><a href="#" onclick="openModal()">Order</a></li>
  </ul>
</nav>

<!-- HERO -->
<section id="hero">
  <div class="hero-bg"></div>
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <p class="hero-eyebrow">Handcrafted Since Forever</p>
    <h1 class="hero-title">The<br><em>Jewellery</em></h1>
    <p class="hero-tagline">Elegant &nbsp;·&nbsp; Best Prices &nbsp;·&nbsp; Pure Gold</p>
    <a class="btn-hero" href="#products">Shop Now</a>
  </div>
</section>

<!-- PRODUCTS -->
<section id="products">
  <div class="divider">Our <span>Collection</span></div>
  <div class="divider-line"></div>

  <div class="carousel-track-wrap">
    <div class="carousel-track" id="carouselTrack">

      <!-- Card 1 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/xSBSRGzP/GOL-22-KT-SET-LSE22-ANT-0103-1758690602559.png" alt="22KT Gold Set" loading="lazy">
        </div>
        <div class="card-body">
          <div class="card-sub">22KT Gold</div>
          <div class="card-name">Royal Antique Gold Set</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Royal Antique Gold Set')">Add to Cart</button>
        </div>
      </div>

      <!-- Card 2 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/Df85FKXR/HO-SET10714-1770618691443.png" alt="Bridal Set" loading="lazy">
        </div>
        <div class="card-body">
          <div class="card-sub">Bridal Collection</div>
          <div class="card-name">Heritage Bridal Set</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Heritage Bridal Set')">Add to Cart</button>
        </div>
      </div>

      <!-- Card 3 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/xSBSRGzP/GOL-22-KT-SET-LSE22-ANT-0103-1758690602559.png" alt="Gold Necklace" loading="lazy" style="object-position: top;">
        </div>
        <div class="card-body">
          <div class="card-sub">Gold Necklace</div>
          <div class="card-name">Lakshmi Temple Necklace</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Lakshmi Temple Necklace')">Add to Cart</button>
        </div>
      </div>

      <!-- Card 4 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/Df85FKXR/HO-SET10714-1770618691443.png" alt="Earrings" loading="lazy" style="object-position: bottom;">
        </div>
        <div class="card-body">
          <div class="card-sub">Statement Earrings</div>
          <div class="card-name">Chandelier Drop Earrings</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Chandelier Drop Earrings')">Add to Cart</button>
        </div>
      </div>

      <!-- Card 5 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/xSBSRGzP/GOL-22-KT-SET-LSE22-ANT-0103-1758690602559.png" alt="Bangles" loading="lazy">
        </div>
        <div class="card-body">
          <div class="card-sub">Gold Bangles</div>
          <div class="card-name">Antique Kangan Set</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Antique Kangan Set')">Add to Cart</button>
        </div>
      </div>

      <!-- Card 6 -->
      <div class="product-card">
        <div class="card-img-wrap">
          <img src="https://i.ibb.co/Df85FKXR/HO-SET10714-1770618691443.png" alt="Choker" loading="lazy">
        </div>
        <div class="card-body">
          <div class="card-sub">Choker Necklace</div>
          <div class="card-name">Pearl & Gold Choker</div>
          <div class="card-price">₹ On Request</div>
          <button class="btn-addcart" onclick="addToCart('Pearl & Gold Choker')">Add to Cart</button>
        </div>
      </div>

    </div><!-- /track -->
  </div>

  <div class="carousel-nav">
    <button class="carousel-btn" id="prevBtn" onclick="slideCarousel(-1)">&#8592;</button>
    <button class="carousel-btn" id="nextBtn" onclick="slideCarousel(1)">&#8594;</button>
  </div>
</section>

<!-- ABOUT -->
<section id="about">
  <div class="about-text">
    <p class="about-eyebrow">Our Story</p>
    <h2 class="about-title">Crafting Elegance<br>for Every Occasion</h2>
    <p class="about-body">
      At The Jewellery, every piece is a labour of love — handcrafted by master artisans using the finest 22KT gold and precious stones. We believe that fine jewellery should be accessible without compromise on quality. Whether it's a bridal trousseau, a festive gift, or an everyday statement, our collection speaks the language of elegance at the best prices.
    </p>
  </div>
  <div class="about-stats">
    <div class="stat">
      <div class="stat-num">500+</div>
      <div class="stat-label">Designs</div>
    </div>
    <div class="stat">
      <div class="stat-num">22KT</div>
      <div class="stat-label">Pure Gold</div>
    </div>
    <div class="stat">
      <div class="stat-num">10K+</div>
      <div class="stat-label">Happy Customers</div>
    </div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-logo">The Jewellery</div>
  <div class="footer-links">
    <a href="#hero">Home</a>
    <a href="#products">Shop</a>
    <a href="mailto:dealersahil.0@gmail.com">Contact</a>
    <a href="https://wa.me/8082012783" target="_blank">WhatsApp</a>
  </div>
  <p class="footer-copy">&copy; 2026 The Jewellery · dealersahil.0@gmail.com · All rights reserved</p>
</footer>

<!-- CART BAR -->
<div class="cart-bar" onclick="openModal()">
  🛒 View Cart <span class="cart-count" id="cartCount">0</span>
</div>

<!-- WHATSAPP FLOAT -->
<a class="wa-float" href="https://wa.me/8082012783" target="_blank" aria-label="Chat on WhatsApp">
  <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.741.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.89-5.335 11.893-11.893a11.821 11.821 0 00-3.48-8.413z"/>
  </svg>
</a>

<!-- ORDER MODAL -->
<div class="modal-overlay" id="modalOverlay" onclick="handleOverlayClick(event)">
  <div class="modal">
    <button class="modal-close" onclick="closeModal()">✕</button>
    <div class="modal-title">Place Your Order</div>
    <p class="modal-sub">Elegant · Best Prices · Delivered with Care</p>

    <!-- Cart Items -->
    <div class="cart-items-list" id="cartItemsList"></div>

    <!-- Form -->
    <div id="orderForm">
      <div class="form-group">
        <label>Your Full Name *</label>
        <input type="text" id="custName" placeholder="e.g. Priya Sharma" required>
      </div>
      <div class="form-group">
        <label>Phone Number *</label>
        <input type="tel" id="custPhone" placeholder="e.g. 9876543210" required>
      </div>
      <div class="form-group">
        <label>Email Address</label>
        <input type="email" id="custEmail" placeholder="optional">
      </div>
      <div class="form-group">
        <label>Delivery Address *</label>
        <textarea id="custAddress" placeholder="Enter your full address..." required></textarea>
      </div>
      <div class="form-group">
        <label>Special Requests / Notes</label>
        <textarea id="custNotes" placeholder="Any customization, size, or message..."></textarea>
      </div>
      <button class="btn-submit" onclick="submitOrder()">Send Order via Email</button>
    </div>
    <div class="success-msg" id="successMsg">
      ✦ Thank you! Your order has been received.<br>We'll contact you shortly.
    </div>
  </div>
</div>

<script>
  // ── CART STATE ──
  let cart = [];

  function addToCart(name) {
    cart.push(name);
    document.getElementById('cartCount').textContent = cart.length;
    showToast(name + ' added to cart');
  }

  function removeFromCart(idx) {
    cart.splice(idx, 1);
    document.getElementById('cartCount').textContent = cart.length;
    renderCartItems();
  }

  function renderCartItems() {
    const list = document.getElementById('cartItemsList');
    if (cart.length === 0) {
      list.innerHTML = '<p class="empty-cart">Your cart is empty. Browse our collection above.</p>';
      return;
    }
    list.innerHTML = cart.map((item, i) => `
      <div class="cart-item-row">
        <span>✦ ${item}</span>
        <button class="remove-btn" onclick="removeFromCart(${i})">Remove</button>
      </div>
    `).join('');
  }

  // ── MODAL ──
  function openModal() {
    renderCartItems();
    document.getElementById('successMsg').style.display = 'none';
    document.getElementById('orderForm').style.display = 'block';
    document.getElementById('modalOverlay').classList.add('open');
    document.body.style.overflow = 'hidden';
  }

  function closeModal() {
    document.getElementById('modalOverlay').classList.remove('open');
    document.body.style.overflow = '';
  }

  function handleOverlayClick(e) {
    if (e.target === document.getElementById('modalOverlay')) closeModal();
  }

  // ── SUBMIT ORDER ──
  function submitOrder() {
    const name    = document.getElementById('custName').value.trim();
    const phone   = document.getElementById('custPhone').value.trim();
    const email   = document.getElementById('custEmail').value.trim();
    const address = document.getElementById('custAddress').value.trim();
    const notes   = document.getElementById('custNotes').value.trim();

    if (!name)    { alert('Please enter your name.'); return; }
    if (!phone)   { alert('Please enter your phone number.'); return; }
    if (!address) { alert('Please enter your delivery address.'); return; }

    const itemList = cart.length > 0 ? cart.join(', ') : 'No items selected';

    const subject = encodeURIComponent('New Order from ' + name + ' – The Jewellery');
    const body = encodeURIComponent(
      'Customer Name: ' + name + '\n' +
      'Phone Number: ' + phone + '\n' +
      (email ? 'Email: ' + email + '\n' : '') +
      'Delivery Address: ' + address + '\n' +
      'Items Ordered: ' + itemList + '\n' +
      (notes ? 'Special Requests: ' + notes : '')
    );

    window.location.href = 'mailto:dealersahil.0@gmail.com?subject=' + subject + '&body=' + body;

    document.getElementById('orderForm').style.display = 'none';
    document.getElementById('successMsg').style.display = 'block';
    cart = [];
    document.getElementById('cartCount').textContent = 0;
  }

  // ── CAROUSEL ──
  let currentSlide = 0;
  const track = document.getElementById('carouselTrack');

  function getCardWidth() {
    const card = track.querySelector('.product-card');
    return card ? card.offsetWidth + 24 : 284;
  }

  function slideCarousel(dir) {
    const cards = track.querySelectorAll('.product-card');
    const visible = Math.floor(track.parentElement.offsetWidth / getCardWidth());
    const max = cards.length - visible;
    currentSlide = Math.max(0, Math.min(currentSlide + dir, max));
    track.style.transform = `translateX(-${currentSlide * getCardWidth()}px)`;
  }

  // Auto-slide
  setInterval(() => slideCarousel(1), 3800);
  // Reset when at end
  setInterval(() => {
    const cards = track.querySelectorAll('.product-card');
    const visible = Math.floor(track.parentElement.offsetWidth / getCardWidth());
    if (currentSlide >= cards.length - visible) currentSlide = 0, track.style.transform = 'translateX(0)';
  }, 3850);

  // ── TOAST ──
  function showToast(msg) {
    const t = document.createElement('div');
    t.textContent = msg;
    Object.assign(t.style, {
      position:'fixed', bottom:'160px', left:'50%', transform:'translateX(-50%)',
      background:'#1a1208', color:'#c9a84c', padding:'10px 22px',
      fontSize:'0.72rem', letterSpacing:'0.1em', zIndex:'300',
      border:'1px solid rgba(201,168,76,0.4)', pointerEvents:'none',
      opacity:'1', transition:'opacity 0.4s'
    });
    document.body.appendChild(t);
    setTimeout(() => { t.style.opacity = '0'; setTimeout(() => t.remove(), 400); }, 2000);
  }
</script>
</body>
</html>
