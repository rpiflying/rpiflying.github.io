---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="assets/RFC_icon.png">
</head>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;800&display=swap');

  :root {
    --rpi-red: #D6001C;
  }

  /* 1. Global Styles & New Background */
  header.site-header, .site-title, #header { display: none !important; }

  body { 
    margin: 0; padding: 0;
    font-family: 'Inter', sans-serif;
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    scroll-behavior: smooth;
  }

  /* 2. Navigation Bar with Logo */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 80px;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(15px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    box-sizing: border-box;
  }

  .nav-logo-img { height: 50px; transition: transform 0.3s; }
  .nav-logo-img:hover { transform: scale(1.05); }

  .nav-links { display: flex; gap: 25px; align-items: center; }
  .nav-item { 
    text-decoration: none; color: #333; font-weight: 600; font-size: 0.9rem; 
    transition: 0.3s; padding: 8px 12px; border-radius: 6px;
  }
  .nav-item:hover { color: var(--rpi-red); background: rgba(214, 0, 28, 0.05); }

  .nav-btn-special { 
    background: var(--rpi-red); color: white !important; 
    padding: 10px 20px; box-shadow: 0 4px 15px rgba(214, 0, 28, 0.2); 
  }

  /* 3. Hero Section with Animated GIF */
  .hero-section {
    height: 90vh; display: flex; align-items: center; justify-content: center;
    flex-direction: column; text-align: center; color: white;
  }

  .animated-logo { width: 180px; margin-bottom: 20px; filter: drop-shadow(0 0 20px rgba(255,255,255,0.2)); }

  .hero-title { font-size: 5.5rem; font-weight: 800; line-height: 0.85; letter-spacing: -4px; margin: 0; }

  /* 4. White Content Content Area */
  .main-wrapper {
    background: white; position: relative; z-index: 10;
    border-radius: 50px 50px 0 0; padding: 100px 8%;
    box-shadow: 0 -30px 60px rgba(0,0,0,0.2);
  }

  /* 5. Partnership Section */
  .partner-box {
    background: #f9f9f9; border-radius: 20px; padding: 40px;
    display: flex; align-items: center; justify-content: space-between;
    margin-bottom: 80px; border: 1px solid #eee;
  }
  .partner-logo { height: 80px; opacity: 0.8; transition: 0.3s; }
  .partner-logo:hover { opacity: 1; transform: scale(1.05); }

  /* Grid & Cards */
  .event-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 25px; margin: 40px 0;
  }
  .event-img { 
    width: 100%; height: 350px; object-fit: cover; border-radius: 20px; 
    transition: 0.5s; filter: grayscale(30%);
  }
  .event-img:hover { filter: grayscale(0%); transform: scale(1.02); }

  .discord-fab {
    position: fixed; bottom: 30px; right: 30px; background: #5865F2;
    color: white !important; width: 65px; height: 65px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 9999;
    transition: 0.3s;
  }
</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="#events" class="nav-item">Events</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item nav-btn-special">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" style="width: 40px; border-radius: 50%;">
</a>

<header class="hero-section">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC">
  <h1 class="hero-title">YOUR JOURNEY<br>STARTS HERE</h1>
  <p style="font-size: 1.5rem; text-transform: uppercase; letter-spacing: 4px; margin-top: 20px; opacity: 0.9;">Advancing Aviation at Rensselaer</p>
</header>

<div class="main-wrapper">
  
  <div class="partner-box">
    <div>
      <h4 style="margin: 0; color: #888; text-transform: uppercase; letter-spacing: 1px;">Training Partner</h4>
      <p style="font-size: 1.2rem; font-weight: 700;">Partnering with local flight schools to get you in the air.</p>
    </div>
    <img src="assets/hewison_transparent.png" class="partner-logo" alt="Hewison Aviation">
  </div>

  <div style="text-align: center; margin-bottom: 80px;">
    <h2 style="font-size: 3rem; font-weight: 800;">Join the community.</h2>
    <p style="font-size: 1.2rem; color: #666; max-width: 600px; margin: 20px auto;">
      From ground school to fly-ins, the RPI Flying Club provides the wings for your ambition.
    </p>
  </div>

  <h2 id="events" style="font-weight: 800; font-size: 2rem;">Latest Events</h2>
  <div class="event-grid">
    <img src="assets/event1.jpg" class="event-img" alt="RFC Event 1">
    <img src="assets/event2.jpg" class="event-img" alt="RFC Event 2">
    <img src="assets/event3.jpg" class="event-img" alt="RFC Event 3">
  </div>

  <h2 style="text-align: center; font-size: 2.5rem; font-weight: 800; margin-top: 100px;">Our Leadership</h2>
  <div class="event-grid" style="grid-template-columns: repeat(auto-fit, minmax(180px, 1fr)); text-align: center;">
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Andreas</strong><br><small>President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Jordan</strong><br><small>Vice President</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Shane</strong><br><small>Treasurer</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Stella</strong><br><small>Secretary</small></div>
    <div><strong style="color: var(--rpi-red); font-size: 1.3rem;">Matthew</strong><br><small>Safety Officer</small></div>
  </div>

  <div style="margin-top: 80px; text-align: center;">
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-transparent-Logo.png" style="height: 60px; opacity: 0.5;" alt="Runway Bar Logo">
  </div>

  <footer style="margin-top: 100px; text-align: center; border-top: 1px solid #eee; padding-top: 50px; color: #bbb;">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p>© 2026 RPI Flying Club</p>
  </footer>
</div>
