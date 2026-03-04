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

  header.site-header, .site-title, #header { display: none !important; }

  body { 
    margin: 0; padding: 0;
    font-family: 'Inter', sans-serif;
    /* This keeps your beige globe background fixed while you scroll */
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    scroll-behavior: smooth;
  }

  /* 1. Navigation */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 80px;
    background: rgba(255, 255, 255, 0.9);
    backdrop-filter: blur(15px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    box-sizing: border-box;
  }

  .nav-logo-img { height: 50px; }

  .nav-links { display: flex; gap: 20px; align-items: center; }
  .nav-item { 
    text-decoration: none; color: #333; font-weight: 600; font-size: 0.9rem; 
    transition: 0.3s; padding: 8px 12px; border-radius: 6px;
  }
  .nav-item:hover { color: var(--rpi-red); background: rgba(214, 0, 28, 0.05); }

  .nav-btn-special { 
    background: var(--rpi-red); color: white !important; 
    padding: 10px 20px; border-radius: 4px;
  }

  /* 2. The Hero Banner (Top Section) */
  .hero-banner {
    position: relative;
    width: 100%;
    height: 85vh;
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
    overflow: hidden;
  }

  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: linear-gradient(to bottom, rgba(0,0,0,0.2), rgba(0,0,0,0.7));
    backdrop-filter: blur(2px);
  }

  .hero-content {
    position: relative;
    z-index: 5;
    text-align: center;
    color: white;
    padding: 20px;
  }

  .hero-title { 
    font-size: 5rem; 
    font-weight: 800; 
    line-height: 0.9; 
    letter-spacing: -3px; 
    margin: 0;
    text-shadow: 0 10px 30px rgba(0,0,0,0.5);
  }

  /* 3. Main Content Wrapper */
  .main-wrapper {
    background: white;
    position: relative;
    z-index: 10;
    border-radius: 40px 40px 0 0;
    padding: 80px 8%;
    margin-top: -60px; /* Pulls content up over the banner */
    box-shadow: 0 -20px 40px rgba(0,0,0,0.1);
  }

  /* 4. Achievement Box (RPI Bar Logo) */
  .achievement-panel {
    background: #111; /* Dark background to make the black/transparent logo pop */
    padding: 40px;
    border-radius: 24px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    margin: 60px 0;
    color: white;
    border: 4px solid var(--rpi-red);
  }

  .bar-logo {
    height: 120px; /* Made it bigger */
    filter: drop-shadow(0 0 10px rgba(255,255,255,0.2));
    transition: 0.3s;
  }

  /* 5. Discord Floating Button */
  .discord-fab {
    position: fixed; bottom: 30px; right: 30px; 
    background: #5865F2;
    width: 65px; height: 65px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 9999;
    transition: 0.3s;
  }
  .discord-fab img { width: 35px; height: 35px; object-fit: contain; }
  .discord-fab:hover { transform: scale(1.1); }

  /* Event Grid */
  .event-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 25px; margin: 40px 0;
  }
  .event-img { width: 100%; height: 300px; object-fit: cover; border-radius: 15px; }
</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="#events" class="nav-item">Events</a>
    <a href="/join" class="nav-item nav-btn-special">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
</a>

<header class="hero-banner">
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" style="width: 120px; margin-bottom: 20px;" alt="RFC">
    <h1 class="hero-title">YOUR JOURNEY<br>STARTS HERE</h1>
    <p style="font-size: 1.2rem; text-transform: uppercase; letter-spacing: 5px; margin-top: 20px; opacity: 0.8;">Rensselaer Flying Club</p>
  </div>
</header>

<div class="main-wrapper">
  
  <div class="achievement-panel">
    <div style="max-width: 400px;">
      <h2 style="color: var(--rpi-red); margin: 0;">Award Winning</h2>
      <p style="font-size: 1.1rem; opacity: 0.8;">Recognized for excellence in the RPI Brand Competition.</p>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-transparent-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 80px 0;">
    <h2 style="font-size: 2.5rem; font-weight: 800;">Advancing Aviation at RPI</h2>
    <p style="color: #666; font-size: 1.1rem; max-width: 700px; margin: 20px auto;">
      The RPI Flying Club is a community of pilots, spotters, and enthusiasts. We make flight accessible through education, networking, and club events.
    </p>
  </div>

  <h2 id="events" style="font-weight: 800;">Recent Events</h2>
  <div class="event-grid">
    <img src="assets/event1.jpg" class="event-img" alt="Event 1">
    <img src="assets/event2.jpg" class="event-img" alt="Event 2">
    <img src="assets/event3.jpg" class="event-img" alt="Event 3">
  </div>

  <div style="background: rgba(214, 0, 28, 0.05); padding: 60px; border-radius: 30px; margin: 80px 0; display: flex; align-items: center; justify-content: space-around; flex-wrap: wrap;">
    <div style="max-width: 300px;">
      <h3>Local Partners</h3>
      <p>We work with flight schools like Hewison Aviation to provide members with the best training opportunities.</p>
    </div>
    <img src="assets/hewison_transparent.png" style="height: 100px;" alt="Hewison">
  </div>

  <footer style="text-align: center; padding-top: 50px; border-top: 1px solid #eee; color: #999;">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p>© 2026 RPI Flying Club</p>
  </footer>
</div>
