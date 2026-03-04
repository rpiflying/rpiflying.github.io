---
layout: home
---

<head>
  <link rel="icon" type="image/png" href="assets/RFC_icon.png">
</head>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Inter:ital,wght@0,300;0,400;0,600;0,800;0,900;1,900&display=swap');

  :root {
    --rpi-red: #D6001C;
  }

  header.site-header, .site-title, #header { display: none !important; }

  body { 
    margin: 0; padding: 0;
    font-family: 'Inter', sans-serif;
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    scroll-behavior: smooth;
  }

  /* 1. Navigation */
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

  .nav-logo-img { height: 50px; }

  .nav-links { display: flex; gap: 20px; align-items: center; }
  .nav-item { 
    text-decoration: none; color: #333; font-weight: 600; font-size: 0.9rem; 
    transition: 0.3s; padding: 8px 12px; border-radius: 6px;
  }
  .nav-item:hover { color: var(--rpi-red); }

  .nav-btn-special { 
    background: var(--rpi-red); color: white !important; 
    padding: 10px 20px; border-radius: 4px;
  }

  /* 2. Massive Hero Banner */
  .hero-banner {
    position: relative;
    width: 100%;
    height: 100vh; /* Fills entire screen on load */
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .hero-overlay {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: linear-gradient(to bottom, rgba(0,0,0,0.1), rgba(0,0,0,0.5));
  }

  .hero-content {
    position: relative;
    z-index: 5;
    text-align: center;
    color: white;
    width: 90%;
  }

  .hero-title { 
    font-size: clamp(3rem, 10vw, 8rem); /* Fluid sizing: Big and Wide */
    font-weight: 900; 
    font-style: italic; /* Added for extra "speed" look */
    line-height: 0.8; 
    letter-spacing: -5px; 
    margin: 0;
    text-transform: uppercase;
    text-shadow: 0 15px 40px rgba(0,0,0,0.6);
  }

  .hero-subtitle {
    font-size: clamp(1rem, 3vw, 2rem);
    font-weight: 300;
    text-transform: uppercase;
    letter-spacing: 12px; /* Super wide tracking */
    margin-top: 30px;
    opacity: 0.9;
  }

  /* 3. Main Content Wrapper */
  .main-wrapper {
    background: white;
    position: relative;
    z-index: 10;
    border-radius: 60px 60px 0 0;
    padding: 100px 8%;
    margin-top: -80px;
    box-shadow: 0 -20px 60px rgba(0,0,0,0.15);
  }

  /* 4. Inverted Achievement Box (Transparent Logo) */
  .achievement-panel {
    background: #ffffff; /* White background */
    padding: 60px;
    border-radius: 30px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    margin: 60px 0;
    color: #111;
    border: 8px solid var(--rpi-red); /* Thick RPI Red border */
    box-shadow: 0 30px 60px rgba(0,0,0,0.05);
  }

  .bar-logo {
    height: 160px; /* Even bigger */
    transition: transform 0.3s;
  }
  .bar-logo:hover { transform: scale(1.05); }

  .credit-tag {
    font-size: 0.8rem;
    color: #888;
    margin-top: 10px;
    display: block;
    font-style: italic;
  }

  /* 5. Fixed Discord Button (Removing white outline) */
  .discord-fab {
    position: fixed; bottom: 30px; right: 30px; 
    background: #5865F2;
    width: 70px; height: 70px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 9999;
    transition: 0.3s;
    overflow: hidden; /* Clips the white corners of the JPG */
  }
  .discord-fab img { 
    width: 100%; height: 100%; 
    object-fit: cover; 
    mix-blend-mode: multiply; /* Helps blend JPG white background if visible */
  }
  .discord-fab:hover { transform: scale(1.1) rotate(-5deg); border: 3px solid white; }

</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/join" class="nav-item nav-btn-special">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
</a>

<header class="hero-banner">
  <div class="hero-overlay"></div>
  <div class="hero-content">
    <h1 class="hero-title">YOUR JOURNEY<br>STARTS HERE</h1>
    <p class="hero-subtitle">RPI FLYING CLUB</p>
  </div>
</header>

<div class="main-wrapper">
  
  <div class="achievement-panel">
    <div style="max-width: 450px;">
      <h2 style="font-size: 2.5rem; font-weight: 900; margin: 0; letter-spacing: -1px;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.2rem; margin-top: 15px; color: #444;">Winner of the RPI Brand Competition. Our identity reflects the speed and precision of the flight line.</p>
      <span class="credit-tag">Logo designed by Kaden Tennent, Ex-President '23-'25</span>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-transparent-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 100px 0;">
    <h2 style="font-size: 3rem; font-weight: 800; letter-spacing: -1px;">Advancing Aviation at Rensselaer</h2>
    <p style="color: #666; font-size: 1.25rem; max-width: 750px; margin: 25px auto; line-height: 1.8;">
      We are more than just a club; we are a flight crew. Whether you're chasing your PPL or just love the sound of a turboprop, you've found your hangar.
    </p>
  </div>

  <h2 id="events" style="font-weight: 800; font-size: 2rem;">Life at RFC</h2>
  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; margin-top: 30px;">
    <img src="assets/event1.jpg" style="width:100%; height:400px; object-fit:cover; border-radius:20px;" alt="Event 1">
    <img src="assets/event2.jpg" style="width:100%; height:400px; object-fit:cover; border-radius:20px;" alt="Event 2">
    <img src="assets/event3.jpg" style="width:100%; height:400px; object-fit:cover; border-radius:20px;" alt="Event 3">
  </div>

  <footer style="text-align: center; padding-top: 80px; margin-top: 100px; border-top: 1px solid #eee; color: #bbb;">
    <img src="assets/RFCLOGO.png" style="height: 40px; filter: grayscale(1); opacity: 0.3; margin-bottom: 20px;">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p>© 2026 RPI Flying Club</p>
  </footer>
</div>
