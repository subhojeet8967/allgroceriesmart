<!DOCTYPE html><html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>All Groceries Mart</title>
  <style>
    body {
      font-family: 'Poppins', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f6f6f6;
    }
    header {
      background-color: #2ecc71;
      color: white;
      text-align: center;
      padding: 20px;
      font-size: 24px;
      font-weight: bold;
    }
    nav {
      display: flex;
      justify-content: center;
      background-color: #27ae60;
    }
    nav button {
      background: none;
      border: none;
      color: white;
      padding: 14px 20px;
      cursor: pointer;
      font-size: 16px;
    }
    nav button:hover {
      background-color: #1e8449;
    }
    .container {
      padding: 20px;
      max-width: 1000px;
      margin: auto;
    }
    .banner {
      background-image: url('https://images.unsplash.com/photo-1606813902915-dce251d5b3c9?auto=format&fit=crop&w=1400&q=80');
      background-size: cover;
      background-position: center;
      color: white;
      padding: 60px 20px;
      text-align: center;
      border-radius: 12px;
      margin-bottom: 20px;
    }
    .products {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      gap: 20px;
    }
    .product {
      background: white;
      border-radius: 12px;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      overflow: hidden;
      text-align: center;
      padding-bottom: 10px;
    }
    .product img {
      width: 100%;
      height: 150px;
      object-fit: cover;
    }
    .product h3 {
      margin: 10px 0 5px 0;
    }
    footer {
      background-color: #27ae60;
      color: white;
      text-align: center;
      padding: 20px;
      margin-top: 30px;
    }
  </style>
</head>
<body>
  <header>All Groceries Mart</header>
  <nav>
    <button onclick="setLang('en')">English</button>
    <button onclick="setLang('hi')">हिन्दी</button>
    <button onclick="setLang('bn')">বাংলা</button>
  </nav>  <div class="container">
    <div class="banner">
      <h1 id="welcome">Welcome to All Groceries Mart</h1>
      <p id="tagline">Fresh and affordable groceries everyday!</p>
    </div><h2 id="productsTitle">Our Products</h2>
<div class="products">
  <div class="product">
    <img src="https://images.unsplash.com/photo-1567306226416-28f0efdc88ce?auto=format&fit=crop&w=500&q=80" alt="Fruits" />
    <h3 id="p1">Fresh Fruits</h3>
    <p>₹120 / kg</p>
  </div>
  <div class="product">
    <img src="https://images.unsplash.com/photo-1586201375761-83865001e17a?auto=format&fit=crop&w=500&q=80" alt="Rice" />
    <h3 id="p2">Rice</h3>
    <p>₹60 / kg</p>
  </div>
  <div class="product">
    <img src="https://images.unsplash.com/photo-1604908176997-1b2d6b2b3b2a?auto=format&fit=crop&w=500&q=80" alt="Oil" />
    <h3 id="p3">Cooking Oil</h3>
    <p>₹150 / Litre</p>
  </div>
  <div class="product">
    <img src="https://images.unsplash.com/photo-1565958011705-44e211b5885a?auto=format&fit=crop&w=500&q=80" alt="Vegetables" />
    <h3 id="p4">Fresh Vegetables</h3>
    <p>₹80 / kg</p>
  </div>
</div>

<h2 id="contactTitle">Contact Us</h2>
<p id="address">📍 Address: Near Central Market, Bali</p>
<p id="phone">📞 Phone: +91 9876543210</p>

  </div>  <footer>
    <p>&copy; 2025 All Groceries Mart. All rights reserved.</p>
  </footer>  <script>
    const translations = {
      en: {
        welcome: 'Welcome to All Groceries Mart',
        tagline: 'Fresh and affordable groceries everyday!',
        productsTitle: 'Our Products',
        contactTitle: 'Contact Us',
        p1: 'Fresh Fruits',
        p2: 'Rice',
        p3: 'Cooking Oil',
        p4: 'Fresh Vegetables',
      },
      hi: {
        welcome: 'ऑल ग्रोसरीज़ मार्ट में आपका स्वागत है',
        tagline: 'ताज़ा और सस्ते किराना हर दिन!',
        productsTitle: 'हमारे उत्पाद',
        contactTitle: 'संपर्क करें',
        p1: 'ताज़े फल',
        p2: 'चावल',
        p3: 'खाने का तेल',
        p4: 'ताज़ी सब्जियाँ',
      },
      bn: {
        welcome: 'অল গ্রোসারিজ মার্টে স্বাগতম',
        tagline: 'প্রতিদিন টাটকা ও সাশ্রয়ী মুদিখানা!',
        productsTitle: 'আমাদের পণ্য',
        contactTitle: 'যোগাযোগ করুন',
        p1: 'তাজা ফল',
        p2: 'চাল',
        p3: 'রান্নার তেল',
        p4: 'তাজা সবজি',
      }
    };

    function setLang(lang) {
      for (const id in translations[lang]) {
        document.getElementById(id).innerText = translations[lang][id];
      }
    }
  </script></body>
</html>
