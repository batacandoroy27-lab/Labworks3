
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Laboratory Work 3 - Mini Responsive Website</title>
  <style>
    /* Reset & Base Styles */
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    body {
      background-color: #0f172a;
      color: #f8fafc;
      line-height: 1.6;
    }

    /* Requirement 5: Visible Keyboard Focus */
    a:focus-visible, 
    button:focus-visible {
      outline: 3px solid #38bdf8;
      outline-offset: 3px;
    }

    /* Header & Navigation (Requirement 1: Flexbox) */
    header {
      background-color: #1e293b;
      padding: 1rem 2rem;
      border-bottom: 1px solid #334155;
    }

    nav {
      max-width: 1100px;
      margin: 0 auto;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-size: 1.3rem;
      font-weight: bold;
      color: #38bdf8;
    }

    .nav-links {
      display: flex; /* Flexbox */
      list-style: none;
      gap: 1.5rem;
    }

    .nav-links a {
      color: #cbd5e1;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.2s ease;
    }

    /* Requirement 2 - Pseudo-class 1: :hover */
    .nav-links a:hover {
      color: #38bdf8;
    }

    /* Requirement 3 - Pseudo-element 1: ::before */
    .nav-links a::before {
      content: "• ";
      color: #38bdf8;
    }

    /* Hero Section */
    .hero {
      text-align: center;
      padding: 4rem 1.5rem;
      max-width: 800px;
      margin: 0 auto;
    }

    .hero h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
      position: relative;
      display: inline-block;
    }

    /* Requirement 3 - Pseudo-element 2: ::after */
    .hero h1::after {
      content: "";
      display: block;
      width: 60px;
      height: 4px;
      background-color: #38bdf8;
      margin: 8px auto 0;
      border-radius: 2px;
    }

    .hero p {
      color: #94a3b8;
      font-size: 1.1rem;
      margin-top: 1rem;
      margin-bottom: 1.5rem;
    }

    .cta-btn {
      display: inline-block;
      background-color: #0284c7;
      color: #ffffff;
      padding: 0.75rem 1.5rem;
      border-radius: 6px;
      text-decoration: none;
      font-weight: bold;
      transition: background-color 0.2s ease;
    }

    .cta-btn:hover {
      background-color: #0369a1;
    }

    /* Features Section (Requirement 1: Flexbox) */
    .features-section {
      max-width: 1100px;
      margin: 0 auto 4rem;
      padding: 0 1.5rem;
    }

    .features-grid {
      display: flex; /* Flexbox */
      gap: 1.5rem;
      justify-content: space-between;
    }

    .feature-card {
      background-color: #1e293b;
      padding: 2rem;
      border-radius: 8px;
      border: 1px solid #334155;
      flex: 1;
      transition: transform 0.2s ease;
    }

    .feature-card:hover {
      transform: translateY(-5px);
    }

    /* Requirement 2 - Pseudo-class 2: :first-child */
    .feature-card:first-child {
      border-top: 4px solid #38bdf8;
    }

    .feature-card h3 {
      color: #f1f5f9;
      margin-bottom: 0.75rem;
    }

    .feature-card p {
      color: #94a3b8;
      font-size: 0.95rem;
    }

    /* Footer */
    footer {
      background-color: #1e293b;
      text-align: center;
      padding: 2rem 1rem;
      border-top: 1px solid #334155;
      color: #64748b;
      font-size: 0.9rem;
    }

    /* Requirement 4: Media Query for responsive layout */
    @media (max-width: 768px) {
      nav {
        flex-direction: column;
        gap: 1rem;
      }

      .nav-links {
        flex-direction: column;
        text-align: center;
        gap: 0.75rem;
      }

      .features-grid {
        flex-direction: column; /* Switches 3 cards from row to column */
      }
    }
  </style>
</head>
<body>

  <!-- Header + Navigation -->
  <header>
    <nav>
      <div class="logo">DevLab</div>
      <ul class="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#features">Features</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>

  <!-- Hero Section -->
  <main>
    <section class="hero" id="home">
      <h1>Modern Web Solutions</h1>
      <p>Building responsive, accessible, and fast web experiences for every screen size.</p>
      <a href="#features" class="cta-btn">Get Started</a>
    </section>

    <!-- 3 Feature Cards -->
    <section class="features-section" id="features">
      <div class="features-grid">
        <div class="feature-card">
          <h3>⚡ Fast Performance</h3>
          <p>Optimized structure and lightweight styles to make your site load in milliseconds.</p>
        </div>
        <div class="feature-card">
          <h3>📱 Fully Responsive</h3>
          <p>Fluid flexbox layouts tailored seamlessly for mobile, tablet, and desktop views.</p>
        </div>
        <div class="feature-card">
          <h3>♿ Accessible First</h3>
          <p>Designed with keyboard navigation and high-contrast visuals right out of the box.</p>
        </div>
      </div>
    </section>
  </main>

  <!-- Footer -->
  <footer id="contact">
    <p>&copy; 2026 DevLab. All rights reserved.</p>
  </footer>

</body>
</html>
