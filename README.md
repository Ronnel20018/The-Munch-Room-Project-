<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Munch Room | Sips & Stems</title>
    <link href='https://unpkg.com/boxicons@2.1.4/css/boxicons.min.css' rel='stylesheet'>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <header id="home">
        <div class="logo-area">
            <img src="logo-munch.png" alt="Munch Room Logo" class="mushroom-icon">
        </div>
        <nav>
            <ul class="nav-links">
                <li><a href="#home">Home</a></li>
                <li><a href="#menu">Menu</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#feedback">Feedback</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </header>

    <div class="main-wrapper container">
        <aside class="sidebar">
            <h3>Categories</h3>
            <ul>
                <li><a href="#"><i class='bx bxs-coffee-togo'></i> Milk Desserts</a></li>
                <li><a href="#"><i class='bx bxs-leaf'></i> Fresh Flowers</a></li>
                <li><a href="#"><i class='bx bxs-package'></i> Special Bundles</a></li>
                <li><a href="#"><i class='bx bxs-gift'></i> Gift Sets</a></li>
            </ul>
        </aside>

        <main class="body-area" id="menu">
            <div class="welcome-section">
                <h2>Our Sweet Collections</h2>
                <p>Handcrafted milk desserts paired with fresh blooms.</p>
            </div>

            <div class="product-grid">
                <div class="product-card">
                    <div class="product-img-container">
                        <img src="Product 1.jpg" alt="Midnight Bloom Combo">
                    </div>
                    <div class="card-info">
                        <div class="text-content">
                            <h4>Midnight Bloom Combo</h4>
                            <p>Oreo Dessert + Fresh Flowers + Picture Frame</p>
                        </div>
                        <div class="card-footer">
                            <span class="price">₱250.00</span>
                            <button class="buy-btn">Order Now</button>
                        </div>
                    </div>
                </div>

                <div class="product-card">
                    <div class="product-img-container">
                        <img src="Product2.jpg" alt="Mango Blossom Bundle">
                    </div>
                    <div class="card-info">
                        <div class="text-content">
                            <h4>Mango Blossom Bundle</h4>
                            <p>Mango Fruit Dessert + Seasonal Flowers</p>
                        </div>
                        <div class="card-footer">
                            <span class="price">₱150.00</span>
                            <button class="buy-btn">Order Now</button>
                        </div>
                    </div>
                </div>
            </div>
        </main>
    </div>

    <footer id="contact">


    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');

/*-- CSS Ginagmay --*/

:root {
    --dark-bg: #1a1a1a;
    --card-bg: #262626;
    --accent: #d4a373; /* Latte color */
    --text-light: #f4f4f4;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
}

body {
    background-color: var(--dark-bg);
    color: var(--text-light);
}

.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}

/* --- Header & Interactive Logo --- */
header {
    text-align: center;
    padding: 40px 0;
    border-bottom: 1px solid #333;
}

.mushroom-icon {
    height: 95px;
    width: 95px;
    border-radius: 50%;
    border: 3px solid var(--accent);
    padding: 10px;
    background: rgba(255, 255, 255, 0.05);
    cursor: pointer;
    transition: all 0.3s ease;
    animation: breathing 4s ease-in-out infinite;
    box-shadow: 0 0 10px rgba(212, 163, 115, 0.2);
}

.mushroom-icon:hover {
    box-shadow: 0 0 25px var(--accent);
    transform: scale(1.05);
}

.mushroom-icon:active {
    animation: click-shake 0.2s ease-in-out;
    border-color: #fff;
}

/* --- Glowing Navigation --- */
.nav-links {
    display: flex;
    justify-content: center;
    list-style: none;
    gap: 30px;
    margin-top: 25px;
}

.nav-links a {
    text-decoration: none;
    color: var(--text-light);
    font-size: 14px;
    text-transform: uppercase;
    transition: all 0.4s ease;
}

.nav-links a:hover {
    color: var(--accent);
    text-shadow: 0 0 10px var(--accent), 0 0 20px var(--accent);
    letter-spacing: 2px;
}

/* --- Main Layout --- */
.main-wrapper {
    display: flex;
    gap: 30px;
    margin-top: 40px;
}

.sidebar {
    flex: 1;
    background: var(--card-bg);
    padding: 25px;
    border-radius: 15px;
    height: fit-content;
}

.sidebar ul li { list-style: none; margin-bottom: 15px; }
.sidebar a { text-decoration: none; color: #fff; display: flex; align-items: center; gap: 10px; }

.body-area {
    flex: 3;
    background: var(--card-bg);
    padding: 30px;
    border-radius: 15px;
}

/* --- Tupong Product Grid & Cards --- */
.product-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 25px;
    margin-top: 30px;
}

.product-card {
    background: #333;
    border-radius: 15px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    height: 100%; /* Gipugos ang cards nga mag-tupong */
    transition: 0.3s;
}

.product-img-container {
    width: 100%;
    height: 320px; /* Parehas nga height sa picture */
    overflow: hidden;
}

.product-card img {
    width: 100%;
    height: 100%;
    object-fit: cover; /* Dili ma-stretch */
}

.card-info {
    padding: 20px;
    flex-grow: 1; /* Mupatuyhad sa card content */
    display: flex;
    flex-direction: column;
    justify-content: space-between; /* Push footer down */
}

.card-info h4 { color: var(--accent); margin-bottom: 5px; }
.card-info p { font-size: 0.9rem; color: #bbb; }

.price { display: block; margin-top: 15px; font-weight: 600; font-size: 1.1rem; }

.buy-btn {
    width: 100%;
    padding: 12px;
    background: var(--accent);
    border: none;
    border-radius: 8px;
    font-weight: 600;
    cursor: pointer;
    margin-top: 10px;
    transition: 0.3s;
}

.buy-btn:hover { background: #fff; }

/* --- Animations --- */
@keyframes breathing {
    0%, 100% { transform: scale(1); }
    50% { transform: scale(1.03); }
}

@keyframes click-shake {
    0%, 100% { transform: rotate(0deg); }
    25% { transform: rotate(5deg); }
    75% { transform: rotate(-5deg); }
}

footer { text-align: center; padding: 40px; opacity: 0.5; }

/* --- NEW GLASS SLIDE EFFECT --- */

.sidebar ul li {
    list-style: none;
    margin-bottom: 12px;
}

.sidebar ul li a { 
    text-decoration: none; 
    color: var(--text-light); 
    display: flex; 
    align-items: center; 
    gap: 15px; 
    padding: 12px 15px;
    border-radius: 10px;
    position: relative;
    overflow: hidden; /* Para sa light sweep effect */
    transition: all 0.4s cubic-bezier(0.25, 0.8, 0.25, 1);
}

/* Hover State: Glassmorphism + Slide */
.sidebar ul li a:hover { 
    background: rgba(212, 163, 115, 0.15); /* Warm Glass Glow */
    color: var(--accent);
    padding-left: 25px; /* Ang slide effect */
    transform: translateX(5px); /* Mo-move ang tibuok container */
    backdrop-filter: blur(5px); /* Murag bildo tan-awon */
}

/* Indicator Line sa kilid */
.sidebar ul li a::before {
    content: '';
    position: absolute;
    left: 0;
    top: 50%;
    transform: translateY(-50%);
    width: 4px;
    height: 0; /* Hidden sa sugod */
    background: var(--accent);
    border-radius: 0 5px 5px 0;
    transition: height 0.3s ease;
}

.sidebar ul li a:hover::before {
    height: 70%; /* Mogawas ang line inig hover */
}

/* Icon Animation */
.sidebar ul li a i {
    font-size: 20px;
    transition: all 0.4s ease;
}

.sidebar ul li a:hover i {
    color: #fff;
    transform: scale(1.3) rotate(-10deg);
    filter: drop-shadow(0 0 5px var(--accent));
}
        <p>&copy; 2026 The Munch Room | Dipolog City, Philippines</p>
    </footer>
