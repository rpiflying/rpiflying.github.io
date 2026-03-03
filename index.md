---
layout: home
---

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap');

  :root {
    --rpi-red: #D6001C;
    --dark-blue: #011E5D;
  }

  /* 1. Hiding the default Jekyll Header */
  header.site-header, .site-title, #header { 
    display: none !important; 
  }

  body, html {
    margin: 0; padding: 0;
    overflow-x: hidden;
    font-family: 'Inter', sans-serif;
    scroll-behavior: smooth;
  }

  /* 2. Custom Top Navigation Bar */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%;
    height: 70px;
    background: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(10px);
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 5%;
    z-index: 9999;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    box-sizing: border-box;
  }

  .nav-logo {
    font-weight: 800;
    color: var(--rpi-red);
    text-decoration: none;
    font-size: 1.2rem;
    letter-spacing: -1px;
  }

  .nav-links {
    display: flex;
    gap: 20px;
  }

  .nav-item {
    text-decoration: none;
    color: #444;
    font-weight: 600;
    font-size: 0.9rem;
    transition: 0.3s;
    padding: 8px 12px;
    border-radius: 6px;
  }

  .nav-item:hover {
    color: var(--rpi-red);
    background: rgba(214, 0, 28, 0.05);
  }

  .nav-btn-special {
    background: var(--rpi-red);
    color: white !important;
    box-shadow: 0 4px 10px rgba(214, 0, 28, 0.2);
  }

  /* 3. Full-Width Hero Section */
  .hero-section {
    position: relative;
    width: 100vw;
    height: 85vh; /* Taller hero since nav is now at top */
    background-image: url('assets/BANNER.png');
    background-attachment: fixed;
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: linear-gradient(to bottom, rgba(0,0,0,0.3), rgba(0,0,0,0.6));
    backdrop-filter: blur(2px);
  }

  .hero-text {
    position: relative;
    text-align: center;
    color: white;
    z-index: 2;
    padding: 20px;
  }

  /* 4. Content Styling */
  .main-wrapper {
    background: white;
    position: relative;
    z-index: 10;
    margin-top: -5vh; /* Overlaps hero slightly */
    border-radius: 40px 40px 0 0;
    padding: 80px 5%;
  }

  .grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
    max-width: 1100px;
    margin: 40px auto;
  }

  .benefit-card {
    padding: 40px;
    border-radius: 24px;
    background: #fdfdfd;
    border: 1px solid #f0f0f0;
    transition: 0.4s;
  }

  .benefit-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 20px 40px rgba(0,0,0,0.05);
  }

  /* 5. Discord Floating Button */
  .discord-fab {
    position: fixed;
    bottom: 30px;
    right: 30px;
    background: #5865F2;
    color: white !important;
    width: 60px;
    height: 60px;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    box-shadow: 0 10px 20px rgba(88, 101, 242, 0.4);
    z-index: 9999;
    text-decoration: none;
    transition: 0.3s;
  }

  .discord-fab:hover { transform: scale(1.1) rotate(5deg); }

  @media (max-width: 768px) {
    .nav-links { display: none; } /* We can add a mobile menu later */
    .hero-text h1 { font-size: 2.5rem !important; }
  }
</style>

<nav class="top-nav">
  <a href="/" class="nav-logo">RPI FLYING CLUB</a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="#leadership" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item nav-btn-special">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <span style="font-weight: 800; font-size: 0.7rem;">DISCORD</span>
</a>

<header class="hero-section">
  <div class="hero-overlay"></div>
  <div class="hero-text">
    <h1 style="font-size: 5rem; font-weight: 800; margin: 0; letter-spacing: -3px; line-height: 0.9;">YOUR JOURNEY<br>STARTS HERE</h1>
    <p style="font-size: 1.5rem; font-weight: 300; margin-top: 20px; letter-spacing: 2px; text-transform: uppercase;">Advancing Aviation at Rensselaer</p>
  </div>
</header>

<div class="main-wrapper">
  <div style="text-align: center; max-width: 800px; margin: 0 auto 60px;">
    <h2 style="font-size: 2.5rem; font-weight: 800; color: #111;">Pilot? Planespotter?<br>Aviation enthusiast?</h2>
    <p style="font-size: 1.2rem; color: #666; line-height: 1.8; margin-top: 20px;">
      We are the club for you. From flight training resources to industry networking, we make aviation accessible to the RPI community.
    </p>
  </div>

  <div class="grid">
    <div class="benefit-card">
      <h3 style="color: var(--rpi-red); font-size: 1.8rem;">Membership</h3>
      <p style="font-size: 1.1rem; font-weight: 600;">$30 / Semester • $50 / Year</p>
      <p style="color: #666;">Includes access to all fly-ins, airport tours, social nights (with free food), and exclusive merchandise.</p>
    </div>

  <div class="benefit-card">
    <h3 style="color: var(--rpi-red); font-size: 1.8rem;">Career Path</h3>
    <p style="color: #666;">Join a network of alumni at <strong>Boeing, Delta, Lockheed Martin,</strong> and <strong>Pratt & Whitney</strong>.</p>
  </div>
  </div>

  <h2 id="leadership" style="text-align: center; font-size: 2.5rem; font-weight: 800; margin-top: 100px;">Our Leadership</h2>
  <div class="grid" style="grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); text-align: center;">
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Andreas</strong><br><small>President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Jordan</strong><br><small>Vice President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Shane</strong><br><small>Treasurer</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Stella</strong><br><small>Secretary</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Matthew</strong><br><small>Safety Officer</small></div>
  </div>

  <footer style="margin-top: 100px; text-align: center; padding-top: 40px; border-top: 1px solid #eee; color: #ccc; font-size: 0.9rem;">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p>© 2026 RPI Flying Club</p>
  </footer>
</div>
