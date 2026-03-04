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
    background-color: #000; /* Dark base for the fade-in */
  }

  /* 1. Navigation (Hidden on start, fades in) */
  .top-nav {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 80px;
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(15px);
    display: flex; align-items: center; justify-content: space-between;
    padding: 0 5%; z-index: 9999;
    border-bottom: 1px solid rgba(0,0,0,0.05);
    animation: fadeIn 2s ease-in-out;
  }

  /* 2. THE CINEMATIC HERO */
  .hero-container {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
    background: #000;
  }

  .hero-banner-bg {
    position: absolute;
    top: 0; left: 0; width: 100%; height: 100%;
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    /* Stronger blur and initial darkness */
    filter: blur(10px) brightness(0.5); 
    transform: scale(1.1);
    z-index: 1;
  }

  .hero-content-layer {
    position: relative;
    height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 5;
    color: white;
    text-align: center;
    /* The Fade-Up Animation */
    animation: onLoadFadeUp 1.5s cubic-bezier(0.2, 1, 0.3, 1);
  }

  /* TEXT AT 95% WIDTH */
  .hero-title { 
    font-size: 15vw; /* Adjusted for maximum impact */
    font-weight: 900; 
    font-style: italic;
    line-height: 0.8; 
    letter-spacing: -0.05em; 
    margin: 0;
    text-transform: uppercase;
    width: 95vw; /* 95% width as requested */
    text-shadow: 0 20px 80px rgba(0,0,0,0.8);
  }

  .hero-subtitle {
    font-size: 2.2vw;
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 3vw; /* Very wide spread */
    margin-top: 20px;
    padding-left: 3vw;
    opacity: 0.8;
  }

  .animated-logo {
    width: 150px;
    margin-bottom: 10px;
    filter: drop-shadow(0 0 30px rgba(255,255,255,0.4));
  }

  /* 3. ANIMATIONS */
  @keyframes onLoadFadeUp {
    0% { opacity: 0; transform: translateY(50px); filter: blur(10px); }
    100% { opacity: 1; transform: translateY(0); filter: blur(0); }
  }

  @keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
  }

  /* 4. CONTENT SLIDE-OVER */
  .main-wrapper {
    background: white;
    position: relative;
    z-index: 10;
    border-radius: 60px 60px 0 0;
    padding: 100px 8%;
    box-shadow: 0 -40px 100px rgba(0,0,0,0.5); /* Strong shadow for depth */
  }

  .achievement-panel {
    background: #ffffff;
    padding: 60px;
    border-radius: 30px;
    display: flex;
    align-items: center;
    justify-content: space-around;
    flex-wrap: wrap;
    margin-bottom: 80px;
    border: 8px solid var(--rpi-red);
  }

  .bar-logo { height: 180px; }

  .discord-fab {
    position: fixed; bottom: 30px; right: 30px; 
    background: #5865F2;
    width: 70px; height: 70px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 9999;
    overflow: hidden;
  }
  .discord-fab img { width: 100%; height: 100%; object-fit: cover; }
</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" style="height:50px;" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/join" class="nav-item nav-btn-special">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
</a>

<div class="hero-container">
  <div class="hero-banner-bg"></div>
  <div class="hero-content-layer">
    <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC Logo">
    <h1 class="hero-title">YOUR JOURNEY<br>STARTS HERE</h1>
    <p class="hero-subtitle">RPI FLYING CLUB</p>
  </div>
</div>

<div class="main-wrapper">
  
  <div class="achievement-panel">
    <div style="max-width: 450px;">
      <h2 style="font-size: 2.5rem; font-weight: 900; margin: 0;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.2rem; margin-top: 15px; color: #444;">Winner of the RPI Brand Competition. Designed to reflect the speed and precision of aviation.</p>
      <span style="font-size: 0.8rem; color: #888; font-style: italic;">Logo designed by Kaden Tennent, Ex-President '23-'25</span>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 80px 0;">
    <h2 style="font-size: 3.5rem; font-weight: 800; letter-spacing: -2px;">Advancing Aviation at RPI</h2>
    <p style="color: #666; font-size: 1.3rem; max-width: 800px; margin: 25px auto; line-height: 1.6;">
      Whether you're training for your Private Pilot License or just love spotting, the RPI Flying Club is your home on campus.
    </p>
  </div>

  <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); gap: 20px;">
    <img src="assets/event1.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 1">
    <img src="assets/event2.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 2">
    <img src="assets/event3.jpg" style="width:100%; height:450px; object-fit:cover; border-radius:25px;" alt="Event 3">
  </div>

  <footer style="text-align: center; padding-top: 100px; margin-top: 100px; border-top: 1px solid #eee; color: #bbb;">
    <img src="assets/RFCLOGO.png" style="height: 80px; opacity: 0.8; margin-bottom: 20px;" alt="RFC Logo">
    <p>Rensselaer Union, Troy, NY | rpiflying@gmail.com</p>
    <p>© 2026 RPI Flying Club</p>
  </footer>
</div>
