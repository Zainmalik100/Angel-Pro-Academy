<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
  <title>Angel Pro Academy | Excellence in Learning</title>
  <!-- Google Fonts & simple reset -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,300;14..32,400;14..32,600;14..32,700&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      font-family: 'Inter', sans-serif;
      background-color: #fefcf5;
      color: #1e1e2a;
      line-height: 1.5;
      scroll-behavior: smooth;
    }

    .container {
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 24px;
    }

    /* header / nav */
    header {
      background: #ffffff;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.03), 0 2px 6px rgba(0, 0, 0, 0.05);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .navbar {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      align-items: center;
      padding: 18px 0;
      gap: 20px;
    }

    .logo h1 {
      font-size: 1.8rem;
      font-weight: 700;
      letter-spacing: -0.3px;
      background: linear-gradient(135deg, #c2410c, #f97316);
      background-clip: text;
      -webkit-background-clip: text;
      color: transparent;
    }

    .logo p {
      font-size: 0.75rem;
      color: #f97316;
      letter-spacing: 0.5px;
      font-weight: 500;
    }

    .nav-links {
      display: flex;
      gap: 32px;
      flex-wrap: wrap;
    }

    .nav-links a {
      text-decoration: none;
      font-weight: 600;
      color: #2d2f3e;
      transition: 0.2s;
      font-size: 1rem;
    }

    .nav-links a:hover, .nav-links a.active {
      color: #f97316;
      border-bottom: 2px solid #f97316;
      padding-bottom: 4px;
    }

    /* buttons */
    .btn-primary {
      background: #f97316;
      color: white;
      border: none;
      padding: 12px 28px;
      font-weight: 600;
      border-radius: 40px;
      cursor: pointer;
      transition: 0.2s;
      font-size: 0.9rem;
      display: inline-block;
      text-decoration: none;
    }

    .btn-primary:hover {
      background: #e2620c;
      transform: translateY(-2px);
      box-shadow: 0 8px 18px rgba(249,115,22,0.2);
    }

    .btn-outline {
      background: transparent;
      border: 1.5px solid #f97316;
      color: #f97316;
      padding: 8px 20px;
      border-radius: 40px;
      font-weight: 600;
      transition: 0.2s;
      cursor: pointer;
      text-decoration: none;
      display: inline-block;
    }

    .btn-outline:hover {
      background: #f97316;
      color: white;
    }

    /* hero section */
    .hero {
      padding: 60px 0 60px;
      background: linear-gradient(120deg, #fffaf2, #fff4e6);
    }

    .hero-grid {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      gap: 40px;
      justify-content: space-between;
    }

    .hero-content {
      flex: 1.2;
    }

    .hero-content h2 {
      font-size: 3rem;
      font-weight: 800;
      line-height: 1.2;
      color: #222;
    }

    .hero-highlight {
      color: #f97316;
    }

    .hero-content p {
      font-size: 1.1rem;
      margin: 24px 0;
      color: #4b5563;
    }

    .hero-stats {
      display: flex;
      gap: 32px;
      margin-top: 28px;
    }

    .stat span {
      font-size: 1.8rem;
      font-weight: 800;
      color: #f97316;
    }

    .hero-image {
      flex: 0.9;
      background: #ffedd5;
      border-radius: 40px;
      padding: 30px 20px;
      text-align: center;
      box-shadow: 0 20px 30px -12px rgba(0,0,0,0.08);
    }

    .hero-image i {
      font-size: 7rem;
      color: #f97316;
      margin-bottom: 16px;
    }

    /* section general */
    section {
      padding: 70px 0;
    }

    .section-title {
      font-size: 2.2rem;
      font-weight: 700;
      margin-bottom: 40px;
      text-align: center;
      position: relative;
    }

    .section-title:after {
      content: '';
      display: block;
      width: 70px;
      height: 4px;
      background: #f97316;
      margin: 12px auto 0;
      border-radius: 4px;
    }

    /* courses cards */
    .cards-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      justify-content: center;
    }

    .card {
      background: white;
      border-radius: 28px;
      padding: 32px 24px;
      width: 280px;
      text-align: center;
      box-shadow: 0 12px 28px rgba(0,0,0,0.04);
      transition: all 0.25s ease;
      border: 1px solid #ffeedd;
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 24px 36px rgba(0,0,0,0.08);
    }

    .card i {
      font-size: 2.8rem;
      color: #f97316;
      margin-bottom: 18px;
    }

    .card h3 {
      font-size: 1.5rem;
      margin-bottom: 12px;
    }

    .card p {
      color: #4b5563;
    }

    /* contact & info */
    .contact-info {
      background: #ffffff;
      border-radius: 40px;
      box-shadow: 0 10px 25px -5px rgba(0,0,0,0.05);
      padding: 40px;
      display: flex;
      flex-wrap: wrap;
      gap: 40px;
      justify-content: space-between;
    }

    .info-block {
      flex: 1;
      min-width: 220px;
    }

    .info-block i {
      font-size: 2rem;
      color: #f97316;
      margin-bottom: 16px;
    }

    .info-block h4 {
      font-size: 1.3rem;
      margin-bottom: 12px;
    }

    .info-block p, .info-block a {
      color: #2d3e50;
      text-decoration: none;
      font-weight: 500;
    }

    .info-block a:hover {
      color: #f97316;
    }

    /* map placeholder */
    .map-placeholder {
      background: #e9e6dd;
      border-radius: 28px;
      height: 200px;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-top: 24px;
      background-image: url('https://placehold.co/800x200/ffedd5/f97316?text=📍+Angel+Pro+Academy+Location');
      background-size: cover;
      background-position: center;
      color: #7b5e3c;
      font-weight: 500;
    }

    /* legal pages content */
    .legal-content {
      background: white;
      border-radius: 32px;
      padding: 40px;
      box-shadow: 0 8px 20px rgba(0,0,0,0.02);
    }

    .legal-content h3 {
      margin: 28px 0 12px 0;
      color: #c2410c;
    }

    .legal-content p {
      margin-bottom: 16px;
      color: #2c3e4e;
    }

    footer {
      background: #1e1e2a;
      color: #cdcddd;
      padding: 40px 0 24px;
      margin-top: 20px;
    }

    .footer-flex {
      display: flex;
      flex-wrap: wrap;
      justify-content: space-between;
      gap: 30px;
      align-items: center;
    }

    .footer-links a {
      color: #fcd9b6;
      text-decoration: none;
      margin: 0 12px;
      font-weight: 500;
    }

    .footer-links a:hover {
      color: #f97316;
    }

    .copyright {
      text-align: center;
      padding-top: 32px;
      margin-top: 20px;
      border-top: 1px solid #2d2f42;
      font-size: 0.85rem;
    }

    .hidden-page {
      display: none;
    }

    .active-page {
      display: block;
    }

    .page-transition {
      animation: fade 0.3s ease;
    }

    @keyframes fade {
      from { opacity: 0; transform: translateY(6px);}
      to { opacity: 1; transform: translateY(0);}
    }

    @media (max-width: 780px) {
      .navbar {
        flex-direction: column;
      }
      .hero-content h2 {
        font-size: 2.2rem;
      }
      .contact-info {
        flex-direction: column;
      }
    }
  </style>
</head>
<body>

<header>
  <div class="container">
    <div class="navbar">
      <div class="logo">
        <h1>Angel Pro Academy</h1>
        <p>🌟 Empowering Dreams, Building Excellence</p>
      </div>
      <div class="nav-links">
        <a href="#" data-page="home" class="nav-link active">Home</a>
        <a href="#" data-page="contact" class="nav-link">Contact</a>
        <a href="#" data-page="privacy" class="nav-link">Privacy Policy</a>
        <a href="#" data-page="terms" class="nav-link">Terms & Conditions</a>
      </div>
    </div>
  </div>
</header>

<main>
  <!-- HOME PAGE -->
  <div id="home-page" class="active-page page-transition">
    <div class="hero">
      <div class="container">
        <div class="hero-grid">
          <div class="hero-content">
            <h2>Shape Your Future with <span class="hero-highlight">Angel Pro Academy</span></h2>
            <p>Top-notch coaching, career guidance, and skill development programs. Join us to unlock your true potential with expert mentors and modern learning environment.</p>
            <a href="#" data-page="contact" class="btn-primary nav-link" style="background:#f97316;">📞 Get in Touch</a>
            <div class="hero-stats">
              <div class="stat"><span>500+</span><br>Students Trained</div>
              <div class="stat"><span>12+</span><br>Expert Faculty</div>
              <div class="stat"><span>98%</span><br>Satisfaction</div>
            </div>
          </div>
          <div class="hero-image">
            <i class="fas fa-chalkboard-user"></i>
            <i class="fas fa-star-of-life" style="font-size:2rem; display:block; margin-top:6px;"></i>
            <p style="margin-top:12px;">Learn • Grow • Succeed</p>
          </div>
        </div>
      </div>
    </div>

    <section>
      <div class="container">
        <h2 class="section-title">Our Premium Courses</h2>
        <div class="cards-grid">
          <div class="card"><i class="fas fa-code"></i><h3>Web Dev</h3><p>Full-stack, frontend, backend — build real projects.</p></div>
          <div class="card"><i class="fas fa-chart-line"></i><h3>Digital Marketing</h3><p>SEO, social media, analytics & branding.</p></div>
          <div class="card"><i class="fas fa-database"></i><h3>Data Science</h3><p>Python, ML, Tableau, real-world case studies.</p></div>
          <div class="card"><i class="fas fa-language"></i><h3>Spoken English</h3><p>Personality development, communication mastery.</p></div>
        </div>
      </div>
    </section>

    <section style="background: #fff9f0;">
      <div class="container">
        <h2 class="section-title">Why Angel Pro Academy?</h2>
        <div class="cards-grid">
          <div class="card"><i class="fas fa-user-graduate"></i><h3>Expert Mentors</h3><p>Industry professionals with years of teaching experience.</p></div>
          <div class="card"><i class="fas fa-hand-peace"></i><h3>Small Batches</h3><p>Personal attention, doubt-solving sessions.</p></div>
          <div class="card"><i class="fas fa-laptop-code"></i><h3>Practical Approach</h3><p>Live projects and internships support.</p></div>
        </div>
      </div>
    </section>

    <!-- quick contact preview on home -->
    <div class="container" style="margin-bottom: 40px;">
      <div class="contact-info" style="background:#fff4e8;">
        <div class="info-block"><i class="fas fa-phone-alt"></i><h4>Call / WhatsApp</h4><p><strong>+91 8369797314</strong></p></div>
        <div class="info-block"><i class="fas fa-envelope"></i><h4>Email Us</h4><p><a href="mailto:Maheshlake@gmail.com">Maheshlake@gmail.com</a></p></div>
        <div class="info-block"><i class="fas fa-map-marker-alt"></i><h4>Visit Us</h4><p>Basavaling Complex 1st floor, near Domino's Pizza, Shivanagar Hyderabad Nanded road, Bidar</p></div>
      </div>
      <div class="map-placeholder">
        <span><i class="fas fa-map-pin"></i> 📍 Angel Pro Academy – Basavaling Complex, Shivanagar, Bidar</span>
      </div>
    </div>
  </div>

  <!-- CONTACT PAGE -->
  <div id="contact-page" class="hidden-page page-transition">
    <div class="container" style="padding-top: 50px; padding-bottom: 70px;">
      <h2 class="section-title">Contact Angel Pro Academy</h2>
      <div class="contact-info" style="background: white; box-shadow: 0 12px 28px rgba(0,0,0,0.05);">
        <div class="info-block"><i class="fas fa-phone-alt"></i><h4>Mobile Number</h4><p><strong>8369797314</strong><br>(+91) for calls & WhatsApp</p></div>
        <div class="info-block"><i class="fas fa-envelope-open-text"></i><h4>Official Email</h4><p><a href="mailto:Maheshlake@gmail.com">Maheshlake@gmail.com</a><br>Response within 24h</p></div>
        <div class="info-block"><i class="fas fa-location-dot"></i><h4>Complete Address</h4><p>Angel Pro Academy, Basavaling Complex 1st floor, Near Domino's Pizza, Shivanagar Hyderabad Nanded road, Bidar - 585401</p></div>
      </div>

      <div style="margin-top: 48px; background: #fff9ef; border-radius: 32px; padding: 32px;">
        <h3 style="margin-bottom: 16px; color:#c2410c;"><i class="fas fa-clock"></i> Academy Hours</h3>
        <p><strong>Mon - Sat:</strong> 9:00 AM – 7:00 PM  |  <strong>Sunday:</strong> Closed (special workshops on request)</p>
        <p>📍 Landmark: Above Dominos / Basavaling Complex, Shivanagar. Easily accessible from Hyderabad Nanded road.</p>
        <div class="map-placeholder" style="margin-top: 20px; background: #e6dfd1; justify-content: center; align-items: center; display: flex;">
          <i class="fas fa-map-marker-alt fa-2x" style="margin-right: 12px;"></i> <strong>Near Domino's Pizza, Shivanagar, Bidar</strong>
        </div>
      </div>

      <div style="margin-top: 40px; text-align: center;">
        <a href="#" data-page="home" class="btn-primary nav-link"><i class="fas fa-arrow-left"></i> Back to Home</a>
      </div>
    </div>
  </div>

  <!-- PRIVACY POLICY PAGE -->
  <div id="privacy-page" class="hidden-page page-transition">
    <div class="container" style="padding-top: 50px; padding-bottom: 70px;">
      <h2 class="section-title">Privacy Policy</h2>
      <div class="legal-content">
        <p><strong>Last updated:</strong> 2025 | Angel Pro Academy</p>
        <p>Angel Pro Academy (“we”, “our”, “us”) respects your privacy. This policy describes how we collect, use, and protect your personal information when you visit our website or contact us.</p>
        <h3>1. Information We Collect</h3>
        <p>We may collect personal details such as your name, email address (Maheshlake@gmail.com), phone number (8369797314), and any information you voluntarily provide via contact forms, email, or phone.</p>
        <h3>2. How We Use Your Information</h3>
        <p>We use the information to respond to inquiries, provide course updates, improve our services, and communicate important academy announcements. Your data is never sold to third parties.</p>
        <h3>3. Data Security</h3>
        <p>We adopt appropriate security measures to protect your personal data against unauthorized access, alteration, or destruction.</p>
        <h3>4. Third-Party Links</h3>
        <p>Our website may contain links to external sites. We are not responsible for their privacy practices.</p>
        <h3>5. Contact Us</h3>
        <p>For any privacy-related questions, contact us at <strong>Maheshlake@gmail.com</strong> or call <strong>8369797314</strong>.</p>
        <p><i>By using this site, you agree to this Privacy Policy.</i></p>
      </div>
      <div style="margin-top: 32px; text-align: center;">
        <a href="#" data-page="home" class="btn-outline nav-link">← Return Home</a>
      </div>
    </div>
  </div>

  <!-- TERMS AND CONDITIONS PAGE -->
  <div id="terms-page" class="hidden-page page-transition">
    <div class="container" style="padding-top: 50px; padding-bottom: 70px;">
      <h2 class="section-title">Terms & Conditions</h2>
      <div class="legal-content">
        <p><strong>Effective Date:</strong> 2025 | Angel Pro Academy</p>
        <p>Welcome to Angel Pro Academy. By accessing our website, contacting us, or enrolling in courses, you agree to these Terms & Conditions.</p>
        <h3>1. Use of Website</h3>
        <p>All content provided on this site is for informational purposes. We reserve the right to modify or discontinue any part of our services without notice.</p>
        <h3>2. Intellectual Property</h3>
        <p>All course material, logos, and content displayed are the property of Angel Pro Academy. You may not reproduce or distribute without written permission.</p>
        <h3>3. Fee & Refund Policy</h3>
        <p>Course fees are communicated at the time of enrollment. Refunds, if applicable, are governed by individual course policies. Please reach out to <strong>8369797314</strong> for clarification.</p>
        <h3>4. Limitation of Liability</h3>
        <p>Angel Pro Academy is not liable for any indirect damages arising from the use of our services or failure to access the website.</p>
        <h3>5. Governing Law</h3>
        <p>These terms are governed by the laws of India, and any disputes will be subject to the jurisdiction of courts in Bidar, Karnataka.</p>
        <h3>6. Contact Information</h3>
        <p>For any questions regarding terms, contact us at <strong>Maheshlake@gmail.com</strong> or visit our address: Basavaling Complex 1st floor, near Domino's Pizza, Shivanagar, Hyderabad Nanded road, Bidar.</p>
      </div>
      <div style="margin-top: 32px; text-align: center;">
        <a href="#" data-page="home" class="btn-outline nav-link">← Back to Home</a>
      </div>
    </div>
  </div>
</main>

<footer>
  <div class="container">
    <div class="footer-flex">
      <div>
        <h3 style="color:#f97316;">Angel Pro Academy</h3>
        <p style="margin-top: 8px;">Empowering careers with skills & mentorship</p>
      </div>
      <div class="footer-links">
        <a href="#" data-page="home" class="nav-link">Home</a>
        <a href="#" data-page="contact" class="nav-link">Contact</a>
        <a href="#" data-page="privacy" class="nav-link">Privacy</a>
        <a href="#" data-page="terms" class="nav-link">Terms</a>
      </div>
    </div>
    <div class="copyright">
      © 2025 Angel Pro Academy. All rights reserved. | Designed with 💙 for excellence | Copyright by Angel Pro Academy
    </div>
  </div>
</footer>

<script>
  // simple SPA style navigation between pages
  const pages = {
    home: document.getElementById('home-page'),
    contact: document.getElementById('contact-page'),
    privacy: document.getElementById('privacy-page'),
    terms: document.getElementById('terms-page')
  };

  function showPage(pageId) {
    // hide all pages
    Object.values(pages).forEach(page => {
      if(page) page.classList.add('hidden-page');
      if(page) page.classList.remove('active-page');
    });
    const activePage = pages[pageId];
    if(activePage) {
      activePage.classList.remove('hidden-page');
      activePage.classList.add('active-page');
      activePage.classList.add('page-transition');
    }
    // update nav active styling
    document.querySelectorAll('.nav-link').forEach(link => {
      link.classList.remove('active');
      if(link.getAttribute('data-page') === pageId) {
        link.classList.add('active');
      }
    });
    // scroll to top
    window.scrollTo({ top: 0, behavior: 'smooth' });
  }

  // attach click events to all nav-links including those inside footer / buttons
  document.querySelectorAll('.nav-link').forEach(link => {
    link.addEventListener('click', (e) => {
      e.preventDefault();
      const page = link.getAttribute('data-page');
      if(page && pages[page]) {
        showPage(page);
      } else if(page === 'home') {
        showPage('home');
      } else if(page === 'contact') {
        showPage('contact');
      } else if(page === 'privacy') {
        showPage('privacy');
      } else if(page === 'terms') {
        showPage('terms');
      }
    });
  });

  // initial active home already visible, but ensure address consistency
  // additional: if any direct hash navigation (optional) ignore.

  // verify contact details display on all pages if needed
  console.log("Angel Pro Academy site loaded | contact: 8369797314, email: Maheshlake@gmail.com, address: Basavaling Complex, Shivanagar, Bidar");
</script>
</body>
</html>
