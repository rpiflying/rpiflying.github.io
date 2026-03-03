---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;700;800&display=swap');

  :root {
    --rpi-red: #D6001C;
    --sidebar-width: 250px;
  }

  /* 1. Reset the Jekyll Container constraints */
  body, html {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    font-family: 'Inter', sans-serif;
  }

  /* This targets the default Jekyll wrapper to allow full-width children */
  .wrapper, .main-content, .container {
    max-width: none !important;
    padding: 0 !important;
    margin: 0 !important;
  }

  /* 2. The Full-Width Hero Section */
  .hero-section {
    position: relative;
    width: 100vw; /* Forces 100% of viewport width */
    height: 70vh;
    left: 50%;
    right: 50%;
    margin-left: -50vw;
    margin-right: -50vw;
    display: flex;
    align-items: center;
    justify-content: center;
    background-image: url('assets/BANNER.png');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    overflow: hidden;
  }

  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: rgba(0, 0, 0, 0.4); /* Darkens banner for text pop */
    backdrop-filter: blur(4px); /* The blur you requested */
    z-index: 1;
  }

  .hero-text {
    position: relative;
    text-align: center;
    color: white;
    z-index: 2;
    padding: 20px;
    animation: fadeInUp 1s ease-out;
  }

  @keyframes fadeInUp {
    from { opacity: 0; transform: translateY(30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  /* 3. Navigation Sidebar (Desktop) */
  .custom-sidebar {
    width: var(--sidebar-width);
    height: 100vh;
    background: rgba(255, 255, 255, 0.98);
    border-right: 1px solid #eee;
    position: fixed;
    top: 0; left: 0;
    padding: 40px 20px;
    z-index: 1000;
  }

  .sidebar-link {
    display: block;
    text-decoration: none;
    color: #444;
    font-weight: 600;
    padding: 12px 15px;
    margin-bottom: 8px;
    border-radius: 8px;
    transition: all 0.3s ease;
  }

  .sidebar-link:hover {
    background: var(--rpi-red);
    color: white !important;
    transform: translateX(8px);
  }

  /* 4. Content Area */
  .page-body {
    margin-left: var(--sidebar-width);
    background: white;
    min-height: 100vh;
    position: relative;
  }

  .section-container {
    max-width: 1000px;
    margin: 0 auto;
    padding: 80px 40px;
  }

  /* Buttons & Cards */
  .btn-join { 
    background-color: var(--rpi-red); 
    color: white !important; 
    padding: 16px 45px; 
    text-decoration: none; 
    border-radius: 50px; 
    font-weight: 800; 
    display: inline-block;
    transition: 0.3s;
    box-shadow: 0 10px 20px rgba(214, 0, 28, 0.3);
    text-transform: uppercase;
    letter-spacing: 1px;
  }

  .btn-join:hover { transform: scale(1.05); box-shadow: 0 15px 30px rgba(214, 0, 28, 0.4); }

  .benefit-card { 
    border: 1px solid #f0f0f0; 
    padding: 35px; 
    border-radius: 20px; 
    background: #fff; 
    transition: 0.4s ease;
    box-shadow: 0 4px 6px rgba(0,0,0,0.02);
  }

  .benefit-card:hover { transform: translateY(-12px); box-shadow: 0 20px 40px rgba(0,0,0,0.08); }

  /* Mobile Adjustments */
  @media (max-width: 900px) {
    .custom-sidebar { width: 100%; height: auto; position: relative; display: flex; flex-wrap: wrap; justify-content: center; padding: 20px; }
    .page-body { margin-left: 0; }
    .hero-section { width: 100%; left: 0; margin: 0; }
  }
</style>

<nav class="custom-sidebar">
  <div style="font-weight: 800; color: #D6001C; margin-bottom: 30px; font-size: 1.4em;">RPI FLYING CLUB</div>
  <a href="/" class="sidebar-link">Home</a>
  <a href="/join" class="sidebar-link">Join Now</a>
  <a href="#benefits" class="sidebar-link">Benefits</a>
  <a href="#leadership" class="sidebar-link">Leadership</a>
  <a href="mailto:rpiflying@gmail.com" class="sidebar-link">Contact</a>
</nav>

<div class="page-body">
  <header class="hero-section">
    <div class="hero-overlay"></div>
    <div class="hero-text">
      <h1 style="font-size: 4em; font-weight: 800; margin: 0; letter-spacing: -2px;">Your Journey Starts Here</h1>
      <p style="font-size: 1.5em; font-weight: 300; opacity: 0.9; margin-top: 10px;">Advancing Aviation at Rensselaer</p>
    </div>
  </header>

  <div class="section-container">
  <div style="text-align: center; margin-bottom: 100px;">
    <h2 style="font-size: 2.2em; color: #111;">Pilot? Planespotter? Aviation enthusiast?</h2>
    <p style="color: #666; font-size: 1.2em; max-width: 650px; margin: 25px auto; line-height: 1.8;">
      We are the club for you. We provide the resources, community, and connections to help you take to the skies and jumpstart your aviation journey.
    </p>
    <br>
    <a href="/join" class="btn-join">Get On The Flight List</a>
  </div>

  <div id="benefits" style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 40px;">
    <div class="benefit-card">
      <h3 style="color: var(--rpi-red); font-size: 1.5em;">Membership</h3>
      <p style="font-size: 1.1em;"><strong>$30 / Semester</strong> or <strong>$50 / Year</strong></p>
      <ul style="padding-left: 20px; color: #555; line-height: 2;">
        <li>All club meetings, trips, & events</li>
        <li>Discounted paid trip fees</li>
        <li>Free food & drinks at Social Nights</li>
        <li>Exclusive club merchandise & stickers</li>
      </ul>
    </div>
    <div class="benefit-card">
      <h3 style="color: var(--rpi-red); font-size: 1.5em;">Industry Network</h3>
      <p>Access alumni connections from companies like:</p>
      <div style="font-weight: 800; color: #222; margin-top: 20px; display: grid; grid-template-columns: 1fr 1fr; gap: 15px; font-size: 0.8em; letter-spacing: 1px;">
        <span>BOEING</span>
        <span>DELTA</span>
        <span>LOCKHEED MARTIN</span>
        <span>PRATT & WHITNEY</span>
      </div>
    </div>
  </div>

  <h2 id="leadership" style="margin-top: 100px; text-align: center; font-weight: 800; font-size: 2em;">Our Leadership</h2>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(150px, 1fr)); gap: 30px; margin-top: 50px; text-align: center;">
    <div><strong style="color: var(--rpi-red); font-size: 1.2em;">Andreas</strong><br><small style="text-transform: uppercase; color: #888;">President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.2em;">Jordan</strong><br><small style="text-transform: uppercase; color: #888;">Vice President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.2em;">Shane</strong><br><small style="text-transform: uppercase; color: #888;">Treasurer</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.2em;">Stella</strong><br><small style="text-transform: uppercase; color: #888;">Secretary</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.2em;">Matthew</strong><br><small style="text-transform: uppercase; color: #888;">Safety Officer</small></div>
  </div>

  <footer style="margin-top: 120px; text-align: center; border-top: 1px solid #eee; padding-top: 50px; color: #bbb; font-size: 0.9em;">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p style="margin-top: 10px;">© 2026 RPI Flying Club. All rights reserved.</p>
  </footer>
  </div>
</div>
