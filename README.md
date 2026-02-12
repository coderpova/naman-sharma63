<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Profile Gallery</title>
    <link rel="stylesheet" href="project1.css">
<nav class="navbar">
</head>
<body>
        <div class="logo">Swift<span>Shop</span></div>
        <ul class="nav-links">
            <li><a href="#">Home</a></li>
            <li><a href="#">Shop</a></li>
            <li><a href="#">Deals</a></li>
            <li><a href="#">Contact</a></li>
        </ul>
        <div class="nav-icons">
            <i class="fas fa-search"></i>
            <i class="fas fa-shopping-cart"></i>
            <i class="fas fa-user"></i>
        </div>
    </nav>

    <header class="hero">
        <div class="hero-content">
            <h1>Upgrade Your Setup</h1>
            <p>Exclusive deals on premium peripherals and hardware.</p>
            <a href="#shop" class="btn">Shop Now</a>
        </div>
    </header>

    <section class="products" id="shop">
        <h2 class="section-title">Featured Products</h2>
        <div class="product-grid">
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1527443224154-c4a3942d3acf?q=80&w=500" alt="Monitor">
                <h3>UltraWide Monitor</h3>
                <p class="price">$499.00</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQD1e2FGI_Z5K085TLKbnuIcHkMHGxyvNjbXQ&s" alt="Keyboard">
                <h3>Mechanical Keyboard</h3>
                <p class="price">$129.00</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1527443154391-507e9dc6c5cc?q=80&w=500" alt="Mouse">
                <h3>Wireless Gaming Mouse</h3>
                <p class="price">$79.00</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
            <div class="product-card">
                <img src="https://images.unsplash.com/photo-1505740420928-5e560c06d30e?q=80&w=500" alt="Headphones">
                <h3>Noise Cancelling Studio</h3>
                <p class="price">$249.00</p>
                <button class="add-to-cart">Add to Cart</button>
            </div>
        </div>
    </section>

    <footer>
        <p>&copy; 2026 SwiftShop. All rights reserved.</p>
    </footer>

css

/* General Reset */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

body {
    background-color: #f4f4f4;
    color: #333;
}

/* Navbar */
.navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 10%;
    background: #fff;
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
    position: sticky;
    top: 0;
    z-index: 1000;
}

.logo {
    font-size: 24px;
    font-weight: bold;
    letter-spacing: 1px;
}

.logo span {
    color: #ff4757;
}

.nav-links {
    list-style: none;
    display: flex;
}

.nav-links li {
    margin: 0 20px;
}

.nav-links a {
    text-decoration: none;
    color: #333;
    font-weight: 500;
    transition: 0.3s;
}

.nav-links a:hover {
    color: #ff4757;
}

.nav-icons i {
    margin-left: 15px;
    cursor: pointer;
    font-size: 18px;
}

/* Hero Section */
.hero {
    height: 60vh;
    background: linear-gradient(rgba(0,0,0,0.5), rgba(0,0,0,0.5)), 
                url('https://images.unsplash.com/photo-1498050108023-c5249f4df085?q=80&w=1200');
    background-size: cover;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;
    text-align: center;
    color: white;
}

.hero-content h1 {
    font-size: 3rem;
    margin-bottom: 10px;
}

.btn {
    display: inline-block;
    background: #ff4757;
    color: white;
    padding: 12px 30px;
    text-decoration: none;
    border-radius: 5px;
    margin-top: 20px;
    transition: 0.3s;
}

.btn:hover {
    background: #e84118;
}

/* Products Section */
.products {
    padding: 50px 10%;
}

.section-title {
    text-align: center;
    margin-bottom: 40px;
    font-size: 2rem;
}

.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 30px;
}

.product-card {
    background: white;
    padding: 20px;
    border-radius: 10px;
    text-align: center;
    transition: transform 0.3s;
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
}

.product-card:hover {
    transform: translateY(-10px);
}

.product-card img {
    max-width: 100%;
    height: 200px;
    object-fit: cover;
    border-radius: 5px;
}

.product-card h3 {
    margin: 15px 0 10px;
}

.price {
    color: #ff4757;
    font-weight: bold;
    font-size: 1.2rem;
    margin-bottom: 15px;
}

.add-to-cart {
    background: #333;
    color: white;
    border: none;
    padding: 10px 20px;
    cursor: pointer;
    border-radius: 5px;
    width: 100%;
}

.add-to-cart:hover {
    background: #555;
}

/* Footer */
footer {
    background: #222;
    color: white;
    text-align: center;
    padding: 20px;
    margin-top: 50px;
}
