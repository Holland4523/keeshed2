<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="description" content="Keeshed - Modern Clothing Brand with edgy, contemporary aesthetics and striking high-contrast design.">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Keeshed - Modern Clothing Brand</title>
  <!-- Google Fonts for blocky typography -->
  <link href="https://fonts.googleapis.com/css2?family=Anton&family=Rubik:wght@400;500;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --black: #000000;
      --white: #FFFFFF;
      --dark-gray: #333333;
      --light-gray: #EEEEEE;
      --transition: all 0.3s ease;
      --shadow: rgba(0,0,0,0.2);
    }
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }
    body, html {
      margin: 0;
      padding: 0;
      font-family: 'Rubik', sans-serif;
      background-color: var(--white);
      color: var(--black);
      line-height: 1.6;
      overflow-x: hidden;
    }
    h1, h2, h3 {
      font-family: 'Anton', sans-serif;
      text-transform: uppercase;
      letter-spacing: 1px;
    }
    .block-text {
      -webkit-text-stroke: 1px var(--black);
      color: var(--white);
      text-shadow: 2px 2px 0 var(--black);
    }
    a {
      text-decoration: none;
      color: inherit;
    }
    .container {
      max-width: 1600px;
      margin: 0 auto;
      padding: 0 20px;
    }
    /* Header Styles */
    header {
      height: 80px;
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 100;
      background-color: rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(10px);
      transition: var(--transition);
    }
    nav {
      display: flex;
      justify-content: space-between;
      align-items: center;
      height: 100%;
    }
    .logo {
      font-size: 28px;
      font-weight: bold;
      letter-spacing: 5px;
      text-transform: uppercase;
    }
    .nav-links {
      display: flex;
      gap: 40px;
    }
    .nav-links a {
      position: relative;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 1px;
      font-size: 14px;
    }
    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background-color: var(--black);
      transition: var(--transition);
    }
    .nav-links a:hover::after {
      width: 100%;
    }
    .cart-icon {
      position: relative;
      font-size: 20px;
    }
    .cart-count {
      position: absolute;
      top: -8px;
      right: -8px;
      background-color: var(--black);
      color: var(--white);
      border-radius: 50%;
      width: 18px;
      height: 18px;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 10px;
    }
    /* Hero Section */
    .hero {
      height: 100vh;
      position: relative;
      overflow: hidden;
      display: flex;
      align-items: center;
      margin-top: 80px;
    }
    .hero-bg {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      /* Background image added inline in the HTML below */
      z-index: -1;
    }
    .hero-content {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      padding-left: 10%;
    }
    .hero h1 {
      font-size: clamp(3rem, 10vw, 8rem);
      line-height: 0.9;
      margin-bottom: 20px;
    }
    .hero p {
      font-size: clamp(1rem, 2vw, 1.5rem);
      max-width: 500px;
      margin-bottom: 40px;
    }
    .cta-button {
      background-color: var(--black);
      color: var(--white);
      border: none;
      padding: 15px 40px;
      font-size: 16px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 2px;
      cursor: pointer;
      transition: var(--transition);
    }
    .cta-button:hover {
      background-color: var(--dark-gray);
      transform: translateY(-3px);
    }
    /* Featured Collections */
    .featured {
      padding: 100px 0;
    }
    .section-title {
      font-size: clamp(2rem, 5vw, 4rem);
      margin-bottom: 60px;
      text-align: center;
    }
    .collection-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 40px;
    }
    .collection-card {
      position: relative;
      overflow: hidden;
      height: 400px;
      cursor: pointer;
    }
    .collection-img {
      width: 100%;
      height: 100%;
      background-color: var(--dark-gray);
      transition: var(--transition);
    }
    .collection-title {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      padding: 20px;
      background-color: rgba(0, 0, 0, 0.7);
      color: var(--white);
      transform: translateY(100%);
      transition: var(--transition);
    }
    .collection-card:hover .collection-img {
      transform: scale(1.05);
    }
    .collection-card:hover .collection-title {
      transform: translateY(0);
    }
    /* About Section */
    .about {
      padding: 100px 0;
      background-color: var(--light-gray);
    }
    .about-content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(400px, 1fr));
      gap: 60px;
      align-items: center;
    }
    .about-img {
      width: 100%;
      height: 500px;
      background-color: var(--dark-gray);
      /* Background image added inline in the HTML below */
    }
    .about-text h2 {
      font-size: clamp(2rem, 5vw, 3rem);
      margin-bottom: 30px;
    }
    .about-text p {
      font-size: 18px;
      line-height: 1.8;
      margin-bottom: 20px;
    }
    /* Instagram Section */
    .instagram {
      padding: 100px 0;
    }
    .insta-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      gap: 20px;
    }
    .insta-item {
      height: 250px;
      background-color: var(--dark-gray);
      position: relative;
      overflow: hidden;
      /* Background images added inline in the HTML below */
    }
    .insta-overlay {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: rgba(0, 0, 0, 0.5);
      display: flex;
      align-items: center;
      justify-content: center;
      opacity: 0;
      transition: var(--transition);
    }
    .insta-icon {
      color: var(--white);
      font-size: 30px;
    }
    .insta-item:hover .insta-overlay {
      opacity: 1;
    }
    /* Newsletter */
    .newsletter {
      padding: 80px 0;
      background-color: var(--black);
      color: var(--white);
      text-align: center;
    }
    .newsletter h2 {
      font-size: clamp(1.5rem, 3vw, 2.5rem);
      margin-bottom: 20px;
    }
    .newsletter p {
      max-width: 600px;
      margin: 0 auto 30px;
      font-size: 18px;
    }
    .newsletter-form {
      display: flex;
      max-width: 500px;
      margin: 0 auto;
    }
    .newsletter-input {
      flex: 1;
      padding: 15px;
      border: none;
      font-size: 16px;
    }
    .newsletter-button {
      background-color: var(--white);
      color: var(--black);
      border: none;
      padding: 0 30px;
      font-weight: 500;
      text-transform: uppercase;
      letter-spacing: 1px;
      cursor: pointer;
    }
    /* Footer */
    footer {
      background-color: var(--light-gray);
      padding: 80px 0 40px;
    }
    .footer-content {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 40px;
      margin-bottom: 60px;
    }
    .footer-column h3 {
      margin-bottom: 20px;
      font-size: 18px;
    }
    .footer-column ul {
      list-style: none;
    }
    .footer-column ul li {
      margin-bottom: 10px;
    }
    .footer-column ul li a {
      opacity: 0.7;
      transition: var(--transition);
    }
    .footer-column ul li a:hover {
      opacity: 1;
    }
    .social-links {
      display: flex;
      gap: 20px;
    }
    .social-link {
      width: 40px;
      height: 40px;
      background-color: var(--black);
      color: var(--white);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      transition: var(--transition);
    }
    .social-link:hover {
      transform: translateY(-3px);
    }
    .copyright {
      text-align: center;
      padding-top: 40px;
      border-top: 1px solid var(--dark-gray);
      opacity: 0.7;
    }
    /* Custom cursor */
    .cursor {
      width: 20px;
      height: 20px;
      border: 2px solid var(--black);
      border-radius: 50%;
      position: fixed;
      pointer-events: none;
      z-index: 9999;
      transition: transform 0.2s ease;
      transform: translate(-50%, -50%);
      display: none;
    }
    .cursor-follower {
      width: 8px;
      height: 8px;
      background-color: var(--black);
      border-radius: 50%;
      position: fixed;
      pointer-events: none;
      z-index: 9999;
      transition: transform 0.1s ease;
      transform: translate(-50%, -50%);
      display: none;
    }
    /* Animations */
    @keyframes fadeUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }
    .fade-up {
      animation: fadeUp 0.8s ease forwards;
    }
    .delay-1 {
      animation-delay: 0.2s;
    }
    .delay-2 {
      animation-delay: 0.4s;
    }
    .delay-3 {
      animation-delay: 0.6s;
    }
    /* Responsive Styles */
    @media (max-width: 1024px) {
      .cursor, .cursor-follower {
        display: none !important;
      }
    }
    @media (max-width: 768px) {
      .nav-links {
        display: none;
      }
      .hero-content {
        padding-left: 5%;
      }
      .collection-grid, .footer-content {
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
      }
      .about-content {
        grid-template-columns: 1fr;
      }
      .newsletter-form {
        flex-direction: column;
        width: 90%;
      }
      .newsletter-input, .newsletter-button {
        width: 100%;
        margin-bottom: 10px;
      }
    }
    @media (max-width: 480px) {
      .logo {
        font-size: 20px;
      }
      .section-title {
        margin-bottom: 40px;
      }
      .collection-grid {
        grid-template-columns: 1fr;
      }
      .insta-grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }
  </style>
</head>
<body>
  <div class="cursor"></div>
  <div class="cursor-follower"></div>

  <header>
    <div class="container">
      <nav>
        <div class="logo">KEESHED</div>
        <div class="nav-links">
          <a href="index.html">Home</a>
          <a href="about.html">About</a>
          <a href="shop.html">Shop</a>
          <a href="collections.html">Collections</a>
          <a href="contact.html">Contact</a>
        </div>
        <div class="cart-icon">
          <span>🛒</span>
          <div class="cart-count">0</div>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <!-- Hero Section -->
    <section class="hero">
      <!-- Hero background now shows your first image -->
      <div class="hero-bg" style="background: url('/mnt/data/e6c334cf-1bb3-46bf-9496-6652d32390d4.webp') center/cover no-repeat;"></div>
      <div class="container">
        <div class="hero-content">
          <h1 class="block-text fade-up">BOLD.<br>MODERN.<br>UNIQUE.</h1>
          <p class="fade-up delay-1">Discover clothing that defines the new era of street fashion with our edgy, contemporary designs.</p>
          <a href="shop.html" class="cta-button fade-up delay-2">Shop Now</a>
        </div>
      </div>
    </section>

    <!-- Featured Collections -->
    <section class="featured">
      <div class="container">
        <h2 class="section-title">Featured Collections</h2>
        <div class="collection-grid">
          <div class="collection-card">
            <div class="collection-img" style="background: url('/mnt/data/235f3a15-57a3-4a21-93fc-467029028cd4.webp') center/cover no-repeat;"></div>
            <div class="collection-title">
              <h3>SUMMER 2025</h3>
            </div>
          </div>
          <div class="collection-card">
            <div class="collection-img" style="background: url('/mnt/data/daf782de-1306-4069-9f7b-f1efbd8eb902.webp') center/cover no-repeat;"></div>
            <div class="collection-title">
              <h3>ESSENTIALS</h3>
            </div>
          </div>
          <div class="collection-card">
            <div class="collection-img" style="background: url('/mnt/data/1a98b537-140c-400d-bf27-e4b9eb157ed2.webp') center/cover no-repeat;"></div>
            <div class="collection-title">
              <h3>LIMITED EDITION</h3>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- About Section -->
    <section class="about">
      <div class="container">
        <div class="about-content">
          <!-- About image now shows your provided image -->
          <div class="about-img" style="background: url('/mnt/data/9f8dee4a-063f-495f-b8d0-0a3ab01cd8ba.webp') center/cover no-repeat;"></div>
          <div class="about-text">
            <h2>OUR STORY</h2>
            <p>Founded in 2023, KEESHED emerged from a vision to challenge conventional fashion norms. We combine striking visual design with premium quality materials to create clothing that makes a statement.</p>
            <p>Our designs embrace the unconventional, the bold, and the unapologetic. Every piece tells a story of individuality and self-expression, designed for those who dare to stand out.</p>
            <a href="about.html" class="cta-button">Learn More</a>
          </div>
        </div>
      </div>
    </section>

    <!-- Instagram Feed -->
    <section class="instagram">
      <div class="container">
        <h2 class="section-title">Follow Our Style</h2>
        <div class="insta-grid">
          <div class="insta-item" style="background: url('/mnt/data/ae33cfbc-9481-47ed-8735-595b0d05edd1.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
          <div class="insta-item" style="background: url('/mnt/data/2432409e-efc4-4f07-9385-cc6f6f4b1f86.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
          <div class="insta-item" style="background: url('/mnt/data/0e9d650e-77bf-42c5-be0c-fd9c529ea577.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
          <div class="insta-item" style="background: url('/mnt/data/ae33cfbc-9481-47ed-8735-595b0d05edd1.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
          <div class="insta-item" style="background: url('/mnt/data/2432409e-efc4-4f07-9385-cc6f6f4b1f86.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
          <div class="insta-item" style="background: url('/mnt/data/0e9d650e-77bf-42c5-be0c-fd9c529ea577.webp') center/cover no-repeat;">
            <div class="insta-overlay">
              <div class="insta-icon">📷</div>
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Newsletter -->
    <section class="newsletter">
      <div class="container">
        <h2>JOIN THE MOVEMENT</h2>
        <p>Subscribe to our newsletter for exclusive offers, new arrivals, and fashion inspiration delivered straight to your inbox.</p>
        <div class="newsletter-form">
          <input type="email" placeholder="Enter your email" class="newsletter-input">
          <button class="newsletter-button">Subscribe</button>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-content">
        <div class="footer-column">
          <h3>SHOP</h3>
          <ul>
            <li><a href="shop.html#new-arrivals">New Arrivals</a></li>
            <li><a href="shop.html#best-sellers">Best Sellers</a></li>
            <li><a href="shop.html#sales">Sales</a></li>
            <li><a href="collections.html">Collections</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>HELP</h3>
          <ul>
            <li><a href="support.html#shipping">Shipping</a></li>
            <li><a href="support.html#returns">Returns & Exchanges</a></li>
            <li><a href="support.html#sizing">Sizing Guide</a></li>
            <li><a href="contact.html">Contact Us</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>ABOUT</h3>
          <ul>
            <li><a href="about.html#our-story">Our Story</a></li>
            <li><a href="about.html#sustainability">Sustainability</a></li>
            <li><a href="about.html#careers">Careers</a></li>
          </ul>
        </div>
        <div class="footer-column">
          <h3>CONNECT</h3>
          <div class="social-links">
            <a href="#" class="social-link">IG</a>
            <a href="#" class="social-link">FB</a>
            <a href="#" class="social-link">TW</a>
            <a href="#" class="social-link">YT</a>
          </div>
        </div>
      </div>
      <div class="copyright">
        &copy; 2025 KEESHED. All Rights Reserved.
      </div>
    </div>
  </footer>

  <!-- Scripts -->
  <script>
    // Custom cursor effect and other interactions
    document.addEventListener('DOMContentLoaded', function() {
      const cursor = document.querySelector('.cursor');
      const cursorFollower = document.querySelector('.cursor-follower');
      
      if (window.innerWidth > 1024) {
        cursor.style.display = 'block';
        cursorFollower.style.display = 'block';
        
        document.addEventListener('mousemove', function(e) {
          cursor.style.left = e.clientX + 'px';
          cursor.style.top = e.clientY + 'px';
          
          setTimeout(function() {
            cursorFollower.style.left = e.clientX + 'px';
            cursorFollower.style.top = e.clientY + 'px';
          }, 50);
        });
        
        // Change cursor on hoverable elements
        const hoverables = document.querySelectorAll('a, button, .collection-card, .insta-item');
        hoverables.forEach(function(hoverable) {
          hoverable.addEventListener('mouseenter', function() {
            cursor.style.transform = 'translate(-50%, -50%) scale(1.5)';
            cursorFollower.style.opacity = '0.5';
          });
          hoverable.addEventListener('mouseleave', function() {
            cursor.style.transform = 'translate(-50%, -50%) scale(1)';
            cursorFollower.style.opacity = '1';
          });
        });
      }
      
      // Parallax effect on scroll (fixed to use a template literal)
      window.addEventListener('scroll', function() {
        const scrolled = window.scrollY;
        const heroContent = document.querySelector('.hero-content');
        heroContent.style.transform = `translateY(${scrolled * 0.3}px)`;
      });
      
      // Shopping cart functionality:
      // When a featured collection card is clicked, increment the cart count.
      const collectionCards = document.querySelectorAll('.collection-card');
      collectionCards.forEach(function(card) {
        card.addEventListener('click', function() {
          const cartCountElem = document.querySelector('.cart-count');
          let count = parseInt(cartCountElem.innerText, 10) || 0;
          count++;
          cartCountElem.innerText = count;
        });
      });
    });
  </script>
</body>
</html>
