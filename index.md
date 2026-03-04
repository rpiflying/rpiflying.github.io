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

  /* 1. NUCLEAR HEADER REMOVAL */
  header.site-header, .site-title, #header, .header-site, .nav-bar { 
    display: none !important; 
    height: 0 !important;
    opacity: 0 !important;
  }

  body { 
    margin: 0; padding: 0;
    font-family: 'Inter', sans-serif;
    background: url('assets/bannerbackground.png') no-repeat center center fixed;
    background-size: cover;
    background-color: #000;
  }

  /* 2. NAVIGATION */
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
  .nav-links { display: flex; gap: 10px; align-items: center; }
  .nav-item { 
    text-decoration: none; color: #111; font-weight: 800; font-size: 0.8rem; 
    text-transform: uppercase; letter-spacing: 1px; padding: 10px 12px; transition: 0.3s;
  }
  .nav-item:hover { color: var(--rpi-red); }

  .nav-btn-join { 
    background: var(--rpi-red); color: white !important; border-radius: 4px;
    border: 2px solid var(--rpi-red); transition: 0.3s;
  }
  .nav-btn-join:hover { background: transparent; color: var(--rpi-red) !important; }

  /* 3. HERO SECTION (LOCKED) */
  .hero-container {
    position: relative;
    width: 100%;
    height: 100vh;
    overflow: hidden;
  }

  .hero-banner-bg {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100%;
    background: url('assets/BANNER.png') no-repeat center center;
    background-size: cover;
    /* Start with light blur */
    filter: blur(4px) brightness(0.6); 
    transform: scale(1.1);
    z-index: 1;
    transition: filter 0.5s ease-out;
  }

  /* JavaScript will trigger this class to increase blur on scroll */
  .blurred-more {
    filter: blur(15px) brightness(0.4) !important;
  }

  .hero-content-layer {
    position: fixed;
    top: 0; left: 0; width: 100%; height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    z-index: 5;
    color: white;
    text-align: center;
    animation: onLoadFadeUp 1.2s cubic-bezier(0.2, 1, 0.3, 1);
  }

  .animated-logo { 
    width: 130px; 
    margin-bottom: 30px; /* Higher up from the text */
    filter: drop-shadow(0 0 20px rgba(255,255,255,0.4));
  }

  .hero-title { 
    font-size: 11.5vw; 
    font-weight: 900; /* Ultra Bold */
    font-style: italic;
    line-height: 1; 
    letter-spacing: -0.05em; 
    margin: 0;
    text-transform: uppercase;
    width: 98vw;
    white-space: nowrap;
    text-shadow: 0 15px 60px rgba(0,0,0,0.9);
  }

  .hero-subtitle {
    font-size: 2vw;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 2.8vw;
    margin-top: 25px;
    padding-left: 2.8vw;
    opacity: 0.9;
  }

  /* 4. SCROLLABLE CONTENT */
  .main-wrapper {
    background: white;
    position: relative;
    z-index: 100;
    margin-top: 100vh;
    border-radius: 60px 60px 0 0;
    padding: 100px 8%;
    box-shadow: 0 -50px 100px rgba(0,0,0,0.7);
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
    background: #5865F2; width: 70px; height: 70px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    box-shadow: 0 10px 25px rgba(88, 101, 242, 0.4); z-index: 99999;
    overflow: hidden;
  }
  .discord-fab img { width: 100%; height: 100%; object-fit: cover; }

  @keyframes onLoadFadeUp {
    0% { opacity: 0; transform: translateY(60px); }
    100% { opacity: 1; transform: translateY(0); }
  }
</style>

<nav class="top-nav">
  <a href="/"><img src="assets/RFCLOGO.png" class="nav-logo-img" alt="RFC Logo"></a>
  <div class="nav-links">
    <a href="/about" class="nav-item">About</a>
    <a href="/ground-school" class="nav-item">Ground School</a>
    <a href="/officer-team" class="nav-item">Officers</a>
    <a href="/calendar" class="nav-item">Calendar</a>
    <a href="/join" class="nav-item nav-btn-join">Join Us</a>
  </div>
</nav>

<a href="https://discord.gg/rXG86ZeBwj" class="discord-fab" target="_blank">
  <img src="assets/discord-logo-icon-editorial-free-vector.jpg" alt="Discord">
</a>

<div class="hero-banner-bg" id="heroBg"></div>
<div class="hero-content-layer">
  <img src="assets/RFC-Discord-Logo-Animated-Extended.gif" class="animated-logo" alt="RFC Logo">
  <h1 class="hero-title">YOUR JOURNEY STARTS HERE</h1>
  <p class="hero-subtitle">RPI FLYING CLUB</p>
</div>

<div class="main-wrapper">
  
  <div class="achievement-panel">
    <div style="max-width: 450px;">
      <h2 style="font-size: 2.5rem; font-weight: 900; margin: 0;">AWARD WINNING BRAND</h2>
      <p style="font-size: 1.2rem; margin-top: 15px; color: #444;">Winner of the RPI Brand Competition. Our identity reflects the speed and precision of aviation.</p>
      <span style="font-size: 0.8rem; color: #888; font-style: italic;">Logo designed by Kaden Tennent, Ex-President '23-'25</span>
    </div>
    <img src="assets/RPI-Brand-Comp_Runway-Bar_Black-BG-Logo.png" class="bar-logo" alt="Runway Bar Award">
  </div>

  <div style="text-align: center; margin: 80px 0;">
    <h2 style="font-size: 3.5rem; font-weight: 800; letter-spacing: -2px;">Advancing Aviation at RPI</h2>
    <p style="color: #666; font-size: 1.3rem; max-width: 800px; margin: 25px auto;">
      The RPI Flying Club is a student-run organization dedicated to making flight accessible to the RPI community.
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

<script>
  window.onscroll = function() {
    var bg = document.getElementById("heroBg");
    if (document.body.scrollTop > 50 || document.documentElement.scrollTop > 50) {
      bg.classList.add("blurred-more");
    } else {
      bg.classList.remove("blurred-more");
    }
  };
</script>
